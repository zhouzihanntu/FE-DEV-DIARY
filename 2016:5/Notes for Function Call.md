#Notes for Function Call
###Several Function Invoking Mechanism
* Invoke function as function
* Invoke function as method
* Invoke function as constructor
* Invoke function with apply()/call()

##Parameters
Functions pass implicit parameters during invoking
###Arguments
######Arguments is a gather of parameters, which has a like-array structure but only has certain characters of array.
* arguments[].length equals to arguments number
* arguments[n] results (n+1)th parameter
* traverse arguments[] with `for` circulation 

###this
######‘this’ parameter references function context 
##Function Invoke
###Invoke function as function
	function joint(){};
	joint()；

	var zhouzi = function(){};
	zhouzi();

"this" references the global context.
###Invoke function as method
	var o = {};
	o.joint = function(){};
	o.whatever();
###Invoke function as constructor
	function joint(){ return this;}
	new joint();
	var zhouzi = new joint();
###Invoke function with apply()/call()
	