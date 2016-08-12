#Callback Function & Sort Elements

##Callback Function
######Define a useless function which calls another function as a parameter.

	function useless(callback){
		return callback();
	}
	
	var text = "Joint is not a joint!";
	
	assert(useless(function(){ return text; })===text,
		"The useless function works!" + text);

##Sort Elements
######Realize array sort with comparing unit.

	var arrayJ = [......];
	arrayJ.sort(function(a,b){
		return b - a;		//From large to small order(return>0)
		//return a - b;	From small to large order(return<0)
	});