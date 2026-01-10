#### Flappy Bird
Inputs:
- Start/ Restart
- Flap

Process
- Bird falls at a constant speed
- Flapping increases bird height by 1
- Pipes spawn on right side of screen, random height, move left
- If bird hits pipe, game ends
- Speed increases


Outputs:
- Bird position
- Pipes 
- Score 
	- visible at end
- Sound
	- Per flap
	- Per pipe
	- End
- Clear ending


Every speed:
- move all pillars left by one
- delete any pillars off the screen

Every speed/2:
- Add new pillar
	- random height 0-3

Changes:
- The high latency and low fps mean a real time gravity system is difficult and not fun
	- This was discovered in first user tests
- We changed the design from gravity based to a simple up/down system using the A/B buttons
	- This received much better feedback, with users better able to predict and react to the latency
- Users had trouble differentiating the bird from the pipes
	- The bird led was dimmed to half brightness

Teamed up with group 9
- Agreed to use the same score system
	- Set interval ticks
	- If successful on tick, +1 score, else +0 score
- Designed a server to display scores from multiple games
- PvP, flappy bird vs rhythm game
- Each column displays binary score
	- First to 31 score wins

API:
- Name from 0 to 5
- Each tick, send ("Name", score) on radio
