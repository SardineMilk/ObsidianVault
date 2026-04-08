### Garden of Projects
Falling sand / Particle sim
Projects represented by plants
- Leaves are input, books videos etc
- Flowers are projects
Stratified by year, nodes only grow in their year
#### Mechanics
Start as a seed
contains leaf/flower nodes
grow plant innards/skin
- 2 wide innards, to allow nodes to pass each other
Seed releases nodes
Nodes grow where able
Grown nodes release hormone that prevents growth in an area


#### Technology
HTML/CSS for website design
JS for interactivity
WebGPU for performance critical sections

Particle behaviour is complex
A robust, easily expandable system to create rules is mandatory

A naive solution is to hardcode particle behaviour in the main loop:

```
if array[x, y] IS WATER:
	if array[x-1, y-1] == 0:
		swap([x, y], [x-1, y-1])
	if array[x, y-1] == 0:
		swap([x, y], [x, y-1])
	if array[x+1, y-1] == 0:
		swap([x, y], [x+1, y-1])
		
	if array[x-1, y] == 0:
		swap([x, y], [x-1, y])
	...
```
Obviously, this does not scale.
Due to the sequential nature of the rules, some have higher priority.
In this case, the water will bias towards `-x`
This can be fixed with the addition of chance, but that adds even more boilerplate

I decided to describe particles with a custom pseudo-language, using a structured JavaScript object.
```
WATER: {
	id: 2,
	colour: {
		r: 15,
		g: 94,
		b: 156,
		a: 150
	},
	properties: [
		"LIQUID",
		"DYNAMIC"
	],
	rules: [
		{
		pattern: {
			dx: [-1, 0, 1],
			dy: [-1, 0]
		},
		filter: {
			is: ["GAS"]
		},
		result: {
			move: {
				x: "$x",
				y: "$y"
			}
		}
		}
	],
},
```
Every particle has a named entry.
Properties have no inherent effect, but they act as tags that can be referenced by rule filters
Ever particle can have any number of rules.
The rule is applied to all cells that match the pattern.
If any of those cells match the filter, one is chosen randomly and the result is applied

The config file is compiled, with possible computation done in advance and abstractions expanded into full instructions
This compiled version is then used by the simulation every step to decide particle behaviour