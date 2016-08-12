#A hack with jQuery one method
I was getting into trouble when completing a function to handle event with an element in accordance with specific condition, I was assuming a simple if...else... construction would work:

HTML:

	<ul class="btnList">
		<li><button restrictType="number">number</button></li>
		<li><button restrictType="all">all</button></li>
	</ul>
	
	<input id="test" textType=""/>
	

JavaScript:


	$(".btnList").find("li").find("button").unbind("click").click(function(){
		var type = $(this).attr("restrictType");
		$("#test").attr("textType",type);
	});
	
	restrictInput();
	
	function restrictInput(){
		var testInput = $("#test").attr("textType");
		if(testInput === "number"){
			$(this).on("blur",function(){
				this.value=this.value.replace(/\D/g,'');
			});
		}else{
			$(this).unbind();
		}
	}

However, contrary to expection, it seemed that the unbind method hadn't remove events bind the input element as I expected. I did try to find out the reason but got nothing, what I expected was the regex only work at the time when `testInput === "number"`, finally I came up with jQuery one() method, after I changed `... $(this).on("blur",function(){ ...` into `... $(this).one("blur",function(){ ...` the problem resolved.

Considering this temporary solution did not reach the essence of problem, I am continuing work on it till make it out.
