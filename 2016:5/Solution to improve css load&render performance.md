#Solution to improve css load&render performance

##Quintessence
This method split the content into different parts and put the required stylesheet import code before html code segment respectively, though the browser will still load all stylesheets at once, the render process will not start until the previous parts complete render.

demo:
```	<body>
		<link rel="stylesheet" href="/site-header.css">
		<header>xxxxx</header>
		<link rel="stylesheet" href="/article.css">
		<main>yyyyyyy</main>
		<link rel="stylesheet" href="/comment.css">
		<section class="comments">zzzzzz</section>
		<link rel="stylesheet" href="/about-me.css">
		<section class="about-me">00000</section>
		<link rel="stylesheet" href="/site-footer.css">
		<footer>333333</footer>
	</body>```

##Strength
* the different performance between projects that attach this method to load and render page with those which load stylesheets by parallel action is that by this way defering follow-up parts' render smooth the whole loading process and thus provides better user experience.
* completely compatible with Streaming

##Weakness
* Probability of malposition occurrence goes up in projects that adopt layout tools like table and flexbox in which content decides layouts.