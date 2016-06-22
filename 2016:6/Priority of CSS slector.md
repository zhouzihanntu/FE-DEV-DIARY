#Priority of CSS slector
HTML


		<ul id="nav">
			<li class="hhh"><a href="#">111111</a></li>
			<li class="hhh"><a href="#">111111</a></li>
			<li class="hhh"><a href="#">555555</a></li>
			<li class="hhh"><a href="#">111111</a></li>
			<li class="hhh"><a href="#">222222</a></li>
		</ul>


css

		div{
			width: 200px;
		}
		#nav>li{
			height: 30px;
		}
		#nav>li>a{
			color: red;
			
		}
now in order to add a :hover style, `.hhh>a:hover{color: green;}` seems not work while things all goes fine by the following style selector

		#nav>li>a:hover{
			color: green;
		}

this strange phenomenon did have puzzled me for a while, then I came round and checked if it has anything to do with selectors' priority, which means by adding !important tag we could also transform the element's style.

	.hhh>a:hover{
			color: green !important;
		}

but the most reliable practice is setting style for all common status that may came up.
