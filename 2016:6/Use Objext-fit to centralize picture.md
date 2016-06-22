#Use objext-fit to centralize picture

object-fit can only be applied to replaced element which are not manipulated by css.
For example, elements such as img, object, video are replaced element.

before apply object-fix method, make sure the size of element was set.

###optional values:
* fill (default)
* contain
* cover
* none
* scale-down

###Usage

	 .fill{
	 	object-fit:fill;
	 }
	 .contain{
	 	object-fit:contain;
	 }
	 .cover{
	 	object-fit:cover;
	 }
	 .scale-down{
	 	object-fit:scale-down;
	 }
	 
###object-position
to control the position of cropping, the usage is the same as background-position.

###Browser compatibility
* the whole IE series [no support]
* Android 4.4.4+ [support]
* Chrome 29+ [support]
* Safari 7.1+ [support object-fit, no support for object-position]
* iOS8+ [support object-fit, no support for object-position]
