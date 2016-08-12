#Solution to autocomplete input case according to existing text immediately

##Require jQuery and back-end support
bind a setInterval method for the focused input case 
`setInterval(autocomplete,500);
var autocomplete = function(){
	....
	};`

and in the autocomplete function you can define how to get the input value, less request times are necessary if you may using ajax or other request method considering the project performance.

to reduce the request frequency, checkout whether there is a necessary request before execute interact  function with back-end:

* checkout whether there is any change of the input value
* fliter meaningless characters before send parameter to the interact function( RegEx )