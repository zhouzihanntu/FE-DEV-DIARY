#Alternative to operate background-position with Image Sprite 

When it comes to meeting requirements that contain too much picture, the common solution is to splice pictures into a big one, then display the specific part by setting elements' background-position property. However, we could reach the same destination by operate parameters of a div and the img tag inside. 

html:

	<div><img src="spriteImg.jpg"/></div>
	
css:

	div{
	width:200px;
	height:80px;
	position:relative;
	overflow:hidden;
	}
	
	img{
	position:absolute;
	}