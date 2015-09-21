# shellEffects
A simple javascript plugin that allows users to mimic shell interactions on the web. 



Setup is very simple. 

Step 1:
	Add required CDN's.  
		
	First include jQuery and jQuery UI libs.
	```
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
		<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.3/jquery-ui.min.js"></script> 
	```
	Then include type.js and type.css cdn's as follows:
	```
		<link rel="stylesheet" type="text/css" href="<WebsiteRoot>/<PathToCssFiles>/type.css"></link>
		<script type="text/javascript" src= "<WebsiteRoot>/<PathToJSFiles>/type.js"></script>
	```
Step2: Write a few lines of Javascript!

Just make note of the id assigned to the container element you wish to make a shell. And then setup is as simple as:

```javascript
	//Need jquery to tell us when document is ready (assures) target will be available on the DOM and run time
	$(document).ready(function (){
		//A simple javascript array to hold the text that you wish to be typed out. Each set of text in quotes is its own line.
		var shellTextArray = ["Hello! The following text will appear on a single line", "This is now a new line", "And this is yet another line"];

		//Create a console (shell object) and specify the text. "target" is the container to hold the shell.
		var terminal = new Console({text: shellTextArray, target: $("#shell")});

		//now run the text being typed animation.
		terminal.RunConsole();
	});
```

There are many configurable features with type.js

1. Typing Speed:
	To Change Typing Speed The Line:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell")}); 
		```
	Changes to:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell"), speed:100});
		```
	where the numerical value '100' is in milliseconds.

2. Cursor Blink Speed:
	To Change The  Cursor Blink Speed:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell")}); 
		```
	Changes to:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell"), cursorBlinkSpeed: 50}); 
		```
	where the numerical value '50' is in milliseconds

3. Cursor Color:
	To Change The  Cursor Blink Speed:
		```javascript
			var terminal = new Console({text: shellTextArray, target: $("#shell")}); 
		```
	Changes to:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell"), cursorColor: "blue"}); 
		```

4. Text Color:
	To Change The  Cursor Blink Speed:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell")}); 
		```
	Changes to:
		```javascript 
			var terminal = new Console({text: shellTextArray, target: $("#shell"), textColor: "red"}); 
		```

Of Course all 4 of these features can be used at the same time as well. 


Future Enhancements:

Check back later for a type response feature where the "shell" gets something typed out and instead of a response being type, it is a response like a shell would give. An example of how
this would work can be found on my website at www.oscarmenjivar.ca

Also users typing into shell and having their text being echoed back to them.

