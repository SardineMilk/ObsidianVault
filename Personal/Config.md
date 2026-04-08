conditions \[\]
	pattern
		include
			grid
				{dx:\[\], dy:\[\]}
				{x:\[\],  y:\[\]}
			cells
				\[{dx, dy}, {x,  y}\]
		exclude
			grid
			cells
	filter
		all
			\["tag/id"\]
		any
			\["tag/id"\]
		none
			\["tag/id"\]

result
	select
		"first"
		"random"
	swap 
		(dx, dy)
		(x, y)
	transform
		"id"

