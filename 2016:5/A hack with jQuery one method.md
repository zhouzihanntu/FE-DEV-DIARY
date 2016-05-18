#A hack with jQuery one method
I was getting into trouble when completing a function to handle event with an element in accordance with specific condition, I was assuming a simple if...else... construction would work:

HTML:

	<input id="test" textType=""/>

JavaScript:

	function(){
		var testInput = $("#test").attr("textType");
		if(testInput === "number"){
			$(this).bind(function(){
				this.value=this.value.replace(/\D/g,'');
			});
		}else{
			$(this).unbind();
		}
	}();
