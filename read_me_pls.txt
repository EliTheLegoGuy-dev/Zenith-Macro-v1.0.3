--------------------------------------------------------------------------------------------
MAKE SURE THE GRAPHICS QUALITY IS 'MANUAL' AND YOU HAVE A SPRINKLER IN YOUR 1ST HOTBAR SLOT!
--------------------------------------------------------------------------------------------
This is required for the macro to actually run properly.


Hi!

Because I haven't added info buttons to the macro app yet, I'm just covering some stuff here.

The Zenith Macro is built around getting maximum honey. Everything is designed with speed in mind
purely for honey, so it is lacking in material collection at the moment. This means it is not the
best macro for progressing in the game, but it is really good for climbing leaderboards. The GUI
also isn't very pretty, but looks don't make you more honey. Non-honey modifications will likely
come after a full release. It still has many options for getting mats so you don't miss out on
getting those easy mats, just you can't choose to get more mats over more honey.

There is a liscense attached, so please read that so you know your rights and such.

Key Bindings:					logo color
F1: start the main macro		purple
F2: pause all processes 		cyan
F3: stop all processes			orange
F4: start the auto clicker		green
F5: start the aid macro			violet

Make sure the Roblox window is on a single monitor! The macro will have some problems if it is
stretched between multiple monitors. Also, the macro has been tested mostly with a 1920x1080px
monitor (without F11 for a full screen), so that size should be the most consistent, although other
screen sizes should work fine. Another thing is that if you want extra range to look for things
like targets, you can make the window a little shorter and wider, so the camera includes more
peripheral area.

The command prompt that shows up can be ignored, but is linked to the macro window so it can't be
closed without stopping the macro. If there is ever an error, it would be cool if you copied the
command prompt text and sent it to me.


Status Tab:
	The status box is mostly for me for debugging, later on I might go through and make it a bit
	clearer, but either way it tell you what the macro is doing.

	The placed planters box has the datetimes for when the planters will be harvested with no
	timezone attached, so changing them would be a little complicated.

	I haven't tested it, but if you put in a field without a planter or a planter without a field
	when manually adding planters, an error will probably happen at some point. I should add a
	dialogue if you input it wrong...

	The reset planters button sets all of the datetimes to now and removes all the planters. It
	also does some internal setting switching where it sets degredation values and planter
	harvested times, so you don't have to worry about that if you manually harvest planters without
	using the macro to do it.

	The three buttons are bound to the function keys stated, although the pause button currently
	doesn't work properly.

Gather Tab:
	WARNING: You MUST have a sprinkler in your first hotkey slot, or the macro paths will fail! It
	checks if one has been placed to confirm complete field paths. The macro also needs you to have
	the supreme saturator because of the limited gathering options.

	Currently, you should be using the target sense or mark pattern because that is what makes this
	app truely unique, and using another pattern would not make as much sense. Advanced blue and
	white hive gathering haven't been added yet, although I don't know why anyone would use
	advanced white gathering because of the low honey amounts and need for mats.
	
	The field can be any field other than the Hive Hub and Ant Field (hub coming at some point, ant
	field would probably reside in a different tab), but be wary of gathering in fields next to
	cliffs as the character could fall off. If the character does fall off, they will stop
	gathering after not collecting pollen or seeing a sprinkler for a few seconds.
	
	The duration is the amount of time gathering before doing other tasks or converting. Currently,
	only the mondo chick or the 'always after' balloon portion can inturrupt your gathering.
	
	
	The convert dropdown has a few options. You can have it never convert, convert once the convert
	time has passed, convert after gathering and with the timers, or always convert.
	
	The convert after value is how often your character will convert the balloon. The always after
	is how long after refreshing your balloon before it inturrupts gathering to force a conversion.
	Make sure the convert after value is less than the always convert after setting to avoid bugs.
	
	
	The shiftlock option makes it toggle the shiftlock when gathering.
	
	'Duped Tokens' makes it pause under duped tokens when gathering, which is prioritized
	lower than getting targets and other objects, but higher than plain movement and going to the center of the field.
	
	The max capacity is how high the capacity % can be before the macro starts a 10-second bag full
	timer. If the bag is above the threshold for that full duration, the character will reset. If
	micro converters are turned on it will try to use those instead of forcing a reset, but it will
	reset if you run out. It also prioritizes hit targets when the bag is full.
	
	
	The target sense options are pretty confusing, but here we go.
	
	The scorching timer values are 'Get prec marks' and 'Build flames'. 'Get prec marks' indicates
	how long after the scorch starts does the macro get the precise targets instead of hitting all
	three targets. 'Build flames' is how long after the start will it pause on a new X-Flame to
	help build the star.
	
	The 'Scorch stack counts' indicate how it prioritizes hitting targets over ignoring them. The
	cycle starts when a scorching star goes off cooldown and ends when it is on cooldown. These
	values essentially make a graph of X-Flame counts vs Scorching Star counts. The first value,
	'Once x off cd (1)' is the goal/ideal amount for when the X-Flame count starts at 0. 'By x on
	cd' is the idea scorching value when the X-Flame starts its cooldown. Then, it draws a line and
	tries to keep your count difference within the acceptable range value of that line. When the
	macro is in that acceptable range, it tries to get precise marks, otherwise it either gets all
	or avoids all targets. 'Once x on cd' is like a jump in the graph, so once the X-Flame
	activates, it uses a line between this value and 'By x off cd'. This way you can make it either
	get more red boost tokens for the beginning of the X-Flame cooldown or the end of it. 'Once of
	cd (2)' is the second jump in the graph, and this makes a line with the final Scorching Star
	value of 30, which it tries to time with the X-Flame value of 25.
	
	That was a lot, really you should only change it if you know what you're doing.
	
	'No hits until' is a separate value for while it's doing the timing. This is the number of
	seconds targets have to be on the field before it decides to stand under one of the hit spots
	to use as a token link, and 'then hits until' is how long it tries to get those before cycling
	back to not getting them (you don't need back to back token links).

Boost Tab:
	This tab is pretty intuitive. There are spots for each hotkey, and the duration in minutes
	after them. 
		Micro: uses micro converters in field when your bag is full
		Every: uses the mat whenever the mat timer is up
		Gathering: uses the mat whenever the mat timer is up and you are gathering
		Converting: uses the mat whenever the mat timer is up and you are converting
		
	Stack turns on the sticker stack with tickets
	
	red turns on the red booster (other boosters will be added in a later version)
	
	Gather in boosted fields makes it gather in field when it is boosted by one of the field
	boosters.
	
	Extendable Fields are the fields the glit extension can be used in. This is so you can maximize
	you glitter value by only extending a the best field but still take advantage of all the free
	boosters. It only extends fields in this and Gather in boosted fields
		
Collect Tab:
	This tab collects some maching and dispensor mats when they are off their cooldown.
	
	Polar bear just makes it cycle through the polar bear dialogue whenever the feast is collected,
	it doesnt actually do the quests. This is so you don't lose out on free polar power.

Mobs Tab:
	Bug runs are not functional yet...
	
	The mondo option makes you stop gathering and go to the mountain top field 'Prepare time'
	seconds before the hour turns. This is so that you don't have dead time where you are waiting
	for your bees to get to the field after the mondo chick spawns.
	
	The max damage time is only used when you have the damage option selected.
	
	The kill option kills the Mondo Chick, the loot option loots it.
	
Planter Tab:
	WARNING: If you do not have at least the number of planter types selected equal to the number
	of allowed planters, the macro will probably fail.

	When harvest full is on, the planters placed will always be harvested once they are full
	despite the min and max planter times.The min time is used for nectars above the min % value,
	up to the max time is used for the planters below that threshold. The highest nectar
	field/planter combos are used when all of the nectars are above the threshold but the better
	field/planter combos are used for the first prioritized nectars below the threshold.
	
	Below the planter options are the allowed planters and fields to place them in.
	
Settings Tab:
	The preferred hive slot is the slot the macro will try to choose when joining a server. The
	first hive slot is optimal for honeymaking.
	
	The max framerate is the max framerate the macro will run at. It is pointless for this to
	exceed the framerate of the Roblox window.
	
	The movespeed is your character's movespeed with no buffs active. There are a few problem
	numbers where two different movespeed compositions make up the same base movespeeds, but for
	anyone with endgame boosts it will accurately determine your movespeed composition for
	calculation purposes.
	
	The key delay is the delay after pressing and releasing certain keys. It only impacts certain
	parts of the macro, so it won't do things like slow down the sense cycling.
	
	Task tries is how many times it will retry a task before giving up until the next gather cycle.
	
	Scroll chunk is how much (1=0.044 of the window height) the scrollbar should be moved at a time
	when searching for planters and mats in your inventory. This value can be increased with many
	different mats and can be decreased when you have fewer unique mats.
	
	Either version of the private server link can be entered. If the macro fails to join a private
	server three times in a row, it will attempt to join a public server instead.
	
	
	The 'Role' setting is this copy of the macro's role relative to your other copies.
		'solo' acts on its own apart from your other macro instances
		'main' sends the 'field alt_' accounts to it's gathering field
		'field alt_'s follow wherever the 'main' macro tells them to. While the main does the task
			cycle that has the red field booster in it, 'field alt1' stays in your preferred gather
			field, 'field alt2' goes to the secondary field (either straw or pepper for red), and
			'field alt3' goes to the last field to get the flowers pre pollinated. Once 'main'
			knows the field, all the field alts go to it. Also, the 'field alt_'s don't ever go to
			their own boosted fields, they stay either in their specific field given with the
			setting or a 'main' boosted field.
		
		Attack, guiding, and general alt options are to be added later, and those would swap in/out
		of the server depending on what the priority is.

Aid Tab:
	This is a built-in boosting macro that will be improved upon in the future.
	
	An auto clicker that runs at the max framerate is linked to the F4 key, which isn't really
	indicated anywhere but there you go. F3 is used to stop all macro processes.
	
	The hotkeys are basically the same as in the boosting tab, but it can send the 'o' key to zoom
	out whenever the camera gets blocked in case you are doing something like rbc in the mushroom,
	and the delays are in seconds. The other gather hotkeys will not be sent for this gathering
	
	If the gather option is selected, it will start doing the regular gather pattern that you have
	set for it without resetting the character ever. This is good for something like puffs if you
	need to do something else for a few seconds but don't want to completely stop gathering. It can
	still drift out of a field and will keep doing the pattern until you stop it, it doesn't care
	if it sees the sprinkler or not.
	
	The shiftlock and get duped options are the same as in the gather tab but for this gathering
	specifically.
	
	The auto holder is a replacement for an auto clicker in some senses. Instead of using an auto
	clicker to use the tool, which always has a chance of going wild if you forget about it, the
	auto holder just holds down the left click whenever you right click. This way you can still
	play the game like normal but be able to release the mouse whenever doing things like puffs or
	boosting.