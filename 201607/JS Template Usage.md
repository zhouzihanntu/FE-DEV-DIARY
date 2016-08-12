#JS Template Usage

A JavaScript lightweight JavaScript templatig engine.

##Client Side

* Include script in HTML markup.
`<script src="js/tmpl.min.js"></script>`
* Add a script section set the id property and template definition.

		<script type="text/x-tmpl" id="tmpl-demo">
		<h3>{%=o.title%}</h3>
		<p>Released under the
		<a href="{%=o.license.url%}">{%=o.license.name%}</a>.</p>
		<h4>Features</h4>
		<ul>
		{% for (var i=0; i<o.features.length; i++) { %}
		    <li>{%=o.features[i]%}</li>
		{% } %}
		</ul>
		</script>

######"o" refer to the data parameter of this template function.

* Create data for the template (JS object format)
	
		var data = {
		    "title": "JavaScript Templates",
		    "license": {
		        "name": "MIT license",
		        "url": "http://www.opensource.org/licenses/MIT"
		    },
		    "features": [
		        "lightweight & fast",
		        "powerful",
		        "zero dependencies"
		    ]
		};
* render the template call tmp() method with id of template & data object as arguments.