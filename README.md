# cc-crazy-monkey
A Single Pya Line Slot Machine made with (love and...) Cocos Creator :)


# What is this?
Crazy Monkey is a 5-reel single-line slot machine developed with the new (amazing) game development tool Cocos Creator.

![ScreenShot](https://raw.github.com/alchimya/cc-crazy-monkey/master/screenshots/cc-crazy-monkey.png)

<br/>
Cocos Creator, released as public beta in march 2016, is a complete package of game development tools and workflow, including a game engine (based on Cocos2d-x), resource management, scene editing, game preview, debug and publish one project to multiple platforms.
In this project/tutorial, I'm going to show some useful Cocos Creator features and at the same time I'll speak about some basic slot machines concept.
For further informations about Cocos Craetor visit http://cocos2d-x.org


# The slot machine
The slot machine discussed here, is a 5-reel single-line slot machine where each reel, made with a set of 9 symbols, has 32 stops.
Here the symbols used to make the reels

1) BANANA
<br/>
2) BEGEMOT
<br/>
3) BONUS
<br/>
4) COCKTAIL
<br/>
5) COCODRILE
<br/>
6) KAKADU
<br/>
7) LION
<br/>
8) MAN
<br/>
9) MONKEY
<br/>

<b>Specs</b>

                            |
----------------------------|--------------
Number of reels       		  | 5            
Number of Symbols     		  | 9
Number of stops per reel    | 32
Slot combinations    		    | 355.554.32
Wild symbols    			      | NONE
Single Betting value    	  | 1
Max Betting value    		    | 5

<b>Symbol Distribution</b>

Symbol       | Reel 1 | Reel 2 | Reel 3 | Reel 4 | Reel 5 | Total
-------------|--------|--------|--------|--------|--------|--------
BONUS		     |	1	    |	1	     | 1	    | 1      | 1	  | 5
BANANA		   |	4	    |	4	     | 3	    | 3      | 3 	  | 17
BEGEMOT      |	4	    |	3	     | 3	    | 5      | 4      | 19
COCKTAIL     |	3	    |	5	     | 4	    | 4      | 3      | 19
COCODRILE    |	4	    |	3	     | 3	    | 4      | 5      | 19
KAKADU       |	4	    |	3	     | 4	    | 4      | 5      | 20
LION         |	4	    |	5	     | 5	    | 3      | 4      | 21
MAN          |	4	    |	4	     | 4	    | 4      | 4      | 20
MONKEY       |	4	    |	4	     | 5	    | 4      | 3      | 20
<b>TOTAL</b>		      | 32	  | 32     | 32     | 32     | 32     | 160

<b>Reel Strips</b>

Stop       Reel 1 	  | Reel 2      | Reel 3      | Reel 4      | Reel 5    
---------|------------|-------------|-------------|-------------|-----------
1		 |	LION      | KAKADU      | MONKEY	  | MAN		    | COCODRILE
2		 |	MONKEY	  | LION	    | COCODRILE	  | MONKEY	    | COCKTAIL
3		 |	COCODRILE | MAN		    | KAKADU	  | BONUS	    | BEGAMOT
4		 |	BANANA	  | COCKTAIL    | COCKTAIL	  | MAN		    | COCODRILE
5		 |	KAKADU	  | MONKEY	    | BEGAMOT	  | COCODRILE   | LION
6		 |	BANANA	  | MAN		    | LION		  | COCKTAIL	| KAKADU
7		 |	BEGAMOT	  | COCKTAIL    | MAN		  | MONKEY	    | MONKEY
8	 	 |	COCKTAIL  | LION	    | BANANA	  | COCKTAIL	| COCODRILE
9		 |	COCODRILE | BEGAMOT	    | KAKADU	  | LION		| BEGAMOT
10		 |	MAN		  | COCKTAIL    | MAN		  | COCKTAIL	| KAKADU
11		 |	LION	  | COCODRILE   | LION		  | KAKADU	    | MAN
12		 |	BONUS	  | BANANA	    | BEGAMOT	  | BEGAMOT	    | BANANA
13		 |	KAKADU	  | BEGAMOT	    | MONKEY	  | MAN		    | LION
14		 |	MONKEY	  | LION	    | COCKTAIL	  | BANANA	    | COCODRILE
15		 |	COCODRILE | MONKEY	    | KAKADU	  | COCODRILE   | MAN
16		 |	MAN		  | BANANA	    | BANANA	  | BANANA	    | BONUS
17		 |	COCKTAIL  | COCODRILE   | LION		  | KAKADU	    | KAKADU
18		 |	MONKEY	  | KAKADU	    | COCODRILE	  | BEGAMOT	    | MONKEY
19		 |	BEGAMOT	  | COCKTAIL    | BANANA	  | COCODRILE   | COCODRILE		
20		 |	LION	  | BANANA	    | MONKEY	  | MONKEY	    | MAN
21		 |	BANANA	  | MAN		    | BEGAMOT	  | BANANA	    | COCKTAIL
22		 |	BEGAMOT	  | BONUS	    | KAKADU	  | KAKADU	    | BEGAMOT
23		 |	KAKADU	  | LION	    | MAN		  | COCKTAIL	| LION
24		 |	BANANA	  | MONKEY	    | COCKTAIL	  | MONKEY	    | KAKADU
25		 |	MAN		  | COCODRILE   | MONKEY	  | BEGAMOT	    | BANANA
26		 |	COCKTAIL  | KAKADU	    | LION		  | LION		| BEGAMOT
27		 |	LION	  | BEGAMOT	    | COCODRILE	  | BEGAMOT	    | MONKEY
28		 |	BEGAMOT	  | BANANA	    | BONUS		  | MAN		    | BANANA
29		 |	COCODRILE | COCKTAIL    | MONKEY	  | COCODRILE   | MAN
30		 |	MONKEY	  | MAN		    | COCKTAIL	  | LION		| LION
31		 |	KAKADU	  | LION	    | MAN		  | BEGAMOT	    | COCKTAIL
32		 |	MAN		  | MONKEY	    | LION		  | KAKADU	    | KAKADU	
<br/>




# The Cocos Creator Project

<b>The Canvas</b>
<br/>
The project has been made starting with the first public beta version (0.71) and at the moment of this writing I'm using the 1.0.1
<br/>
The main Canvas tree structure, can be described as follow:
<br/>
-->Canvas
<br/>
------>Background layer
<br/>
------>Game layer
<br/>
------>Top layer
<br/>
------>Bottom layer
<br/>

![ScreenShot](https://raw.github.com/alchimya/cc-crazy-monkey/master/screenshots/layers.png)

where:
- Background layer: is a sprite with a Widget component that allowos to autosize the background changing device and resolution
- Top layer: is a node that contains all the UI components placed ont the top of the game layer. Here mainly there are the score UI components.
<>br/The layout of this node is driven by a widget with a Top constraint.
- Bottom layer: is a node that contains all the UI components placed below the game layer. Here mainly there are the game buttons controls.
<>br/The layout of this node is driven by a widget with constraints on the top, bottom,right and left.
- Game layer: this node can be described as the reels container.
<br/> It contains a tree node structure as follow:
<br/>
-->Reels
<br/>
------>Reel 1
<br/>
------>Reel 2
<br/>
------>Reel 3
<br/>
------>Reel 4
<br/>
------>Reel 5

<br/>
To "crop" the reels layer with a proper visible area, has been used a Mask component.

<b>Assets</b>
<br/>
The assets branch, can be described as follow
-->assets
<br/>
------>audio
<br/>
------>prefabs
<br/>
------>scenes
<br/>
------>scripts
---------->controllers
---------->ui
<br/>
------>textures

<br/>
where:
- scripts: contains all the Javascript that define the game logic.
- prefabs: contains all the prefabs components. Her you can find the stops (simbols) reel prefab.
- textures: contains all texture used with the sprites and prefabs

<b>Scripting</b>
<br/>
<b>1.1 Reel</b>
<br/>
A reel is a class taht extends a cc.Component object.
<br/>
It defines the following public properties:

  name                        |     type                    |   description    
------------------------------| ----------------------------|--------------------------------------------------------
stops                     	  | [cc.Prefab]                 | allows to define the reel stops
prngMinRange                  | cc.Integer                  | allows to define the min value for the PRNG
prngMaxRange                  | cc.Integer                  | allows to define the max value for the PRNG

<br/>
The layout logic of the (32) symbols is quite simple to understand.
<br>
Looping throughout the stops array the y value of each node will be decreased of a padding value and the stop node hegiht.
Bear in mind that each anchor point of a stop node has been defined as (0,0).
Besides note that the starting y has been calculated using the reel node height.

<br/>
![ScreenShot](https://raw.github.com/alchimya/cc-crazy-monkey/master/screenshots/stops_layout.png)

<b>1.2 Stops Reel Motion</b>
<br/>
The reel motio is quite esay to understand.
<br/>
Overriding the update() method (cc.Component superclass), each Y node (each item of the stops array property) is increased of an arbitrary value that can be expressed as:
<br/>
StepY=StopHeight/N
<br/>
It's quite easy to understand that if N->0 then StpeY->∞, so for N->0 the reel speed will increase.
<br/>
When a stop Y is greater or equal than the node (reel) height, it will moved after the first item:
<br/>
![ScreenShot](https://raw.github.com/alchimya/cc-crazy-monkey/master/screenshots/stops_motion.png)

<b>1.3 Reel (P)RNG</b>
<br/>
The winning logic of a reel object, is driven by a Pseudo Random Number Generator (PRNG) see prng.js assets script.
<br/>
On each reel it is possible to set the range, as min and max value, where the random number will be generated.
Here the values used for the five reels to generate the winning index.

  reel   |     min        |   max    
---------| ---------------|--------------------
1        | 1              | 1000000000
2        | 1000000001     | 2000000000
3        | 2000000001     | 3000000000
4        | 3000000001     | 4000000000
5        | 4000000001     | 5000000000

Note that the number of how many times the reel will rool, is generated randomly too.

<b>1.4 How the rell winning stop does it work?</b>
This is a slot machine with a single pay line placed ate the center of the reels container.
<br/>
When the reel is rolling its last round, when the Y of the winning stop is equal or greater of the pay line Y, the rolling will be stopped.
<br/>
To place the center of the winning stop exactly on the winning line each reel stop Y will be recalculated subtracting an amount equale to:
<br/>
<b>deltaY=winningStop.y-payLineY+winningStop.height/2</b>
