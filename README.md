Hangman TV Game
============

##### By: [Afshin Mokhtari](https://github.com/afshinator), Aug 2013
[Click here](http://) to check it out!


There are two distinct parts to this implementation:

* The game itself is written ruby and so runs in a ruby interpreter, it can be played all by itself.
However, I 'broadcast' the game into the cloud using [Firebase](https://www.firebase.com/).
You can watch a game live or pre-recorded from the browser. ( They are saved to my Firebase account.)


* This is a super-sized implmentation of the Hangman exercise from the Odin project:
Details:  [TheOdinProject.com](http://www.theodinproject.com/courses/ruby-programming/lessons/files-and-serialization)

![alt text][logo]


To run my code,

 - To see a live or pre-recorged game, run the front-end... **pull index.html into your browser**

 - For the backend (which lets u play & broadcast a live game), you need to run the ruby code...

 -- you don't need a firebase account yourself, the code uses mine - for now.
 -- But you need to install the following gem: 
 ---  BigBertha - [Ruby wrapper for the Firebase backend API](http://derailed.github.io/bigbertha/)

 -- After you've pulled down the code, under the game directory, 
 -- go in irb:

>load "hangman.rb"

then to set the game up, 
>h = Hangman.new({ playerId => "Your Name"});

	#	Here are all the options for .new(): 
	#		:verbose => true 			To get debugging/interesting output
	#  		:dict => "fname.txt"		Dictionary filename, defaults to "5desk.txt"
	# 		:answer => "5to12charword"  Set your own word instead of relying on random word
	#  		:turnLimit => number		How many turns before game is over, defaults to 10
	#  		:debug => true				More verbose messages, sets :verbose to true too
	#  		:push => true				Send live updates of each turn to Firebase as an event, default true
	#  		:firebaseURI 				firebase is our data-store in the cloud, default below
	# 		:id                         Used to namespace session in Firebase
	#  		:playerId => string 		Name of player (broadcast to frontend)


and then to start the game and start broadcasting as you play automatically:
>h.play

<hr>
Created by [Afshin Mokhtari](http://www.github.com/afshinator)

[logo]:http://24.media.tumblr.com/09ddacd6ec02e06fe5b1e57c5eb379fd/tumblr_mwdlag98LX1sh230co1_1280.jpg "Hangman snapshot"