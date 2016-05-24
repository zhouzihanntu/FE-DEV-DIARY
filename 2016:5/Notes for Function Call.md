#Notes for Function Call
###Several Function Invoking Mechanism
* Invoke function as function
* Invoke function as method
* Invoke function as constructor
* Invoke function with apply()/call()

##Parameters
Functions pass implicit parameters during invoking
###Arguments
######Arguments is a gather of parameters, which has an array-like structure but only has certain characters of array.

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
"this" bound to the new object being constructed.


	function joint(){ this.a = "zzh";}
	new joint();
	var zhouzi = new joint();
	console.log(zhouzi.zzh);
###Invoke function with apply()/call()
	function juggle(){
		var count = 0;
		for(var i=0;i<arguments.length;i++){
			count += arguments[i];
		}
		this.result = result;
	}
	
	var joint1 = {};
	var joint2 = {};
	
	juggle.apply(joint1,[1,2,3,4]);
	juggle.call(joint2,5,6,7,8);

#####apply():
format:`apply(param1,param2);`


param1 refers to the object "this" while params2 is an array which contains all the arguments in the function call.
#####call():
format:`call(param1,param2,param3,param4...);`

param1 refers to the object "this" while the others parameters are passed as arguments in the function call.
