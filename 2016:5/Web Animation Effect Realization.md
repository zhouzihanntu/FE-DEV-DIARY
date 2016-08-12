#Web Animation Effect Realization


##requestAnimationFrame

	var initialTop = 0;
	function animate(){
		element.style.top = (initialTop += 1/60);
	}
	window.requestAnimationFrame(animate);



It seems that apply requestAnimationFrame method could improve the project performance to some extent by avoiding high frequency calculating of element property.
##CSS Transition(property of css3)</h2>

* good performance in project (DOM optimization)
* similar mechanism to RAF

* a bit poor IE support (IE10+)
* 
