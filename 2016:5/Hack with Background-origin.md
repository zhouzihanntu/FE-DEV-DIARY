#Hack with Background-origin

Commonly by operating pseudo-element like after could realize a iOS-style listbox.

css:

	ul{
		width:300px;
		border:2px solid red;
		padding:0;
	}
	
	.demo li{
		position:relative;
		line-height:40px;
		padding-left:15px;
		list-style-type:none;
	}
	
	.demo li::after{
		position:absolute;
		right:0;
		bottom:0;
		left:0;
		border-bottom:1px solid blue;
		content:"";
	}
	
	.demo li:not(:last-child)::after{
		left:15px;
	}
	
	.demo li:hover{
		background-color:grey;
	}
	

html:

	<ul class="demo">
		<li>joint1</li>
		<li>joint2</li>
		<li>joint3</li>
		<li>joint4</li>
		<li>joint5</li>
		<li>joint6</li>
	</ul>