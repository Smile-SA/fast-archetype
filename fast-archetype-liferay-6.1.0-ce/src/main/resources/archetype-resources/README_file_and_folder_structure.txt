#set( $symbol_pound = '#' )
#set( $symbol_dollar = '$' )
#set( $symbol_escape = '\' )
Into src/main/resources/pages :

dynamic_images :
	Liferay serves some images through a servlet.
	This is where those images are put.
external_portlet :
	Some portlet are set outside Liferay, they are not embedded into Liferay webapp.
	A usual example is the chat portlet.
html :
	It supposed to reflect the code inside Liferay root folder "html".

Into src/main/resources/modules :

footer
	All file for the footer definition.

header
	All file for the header definition. 
	You'll find navigation in it.

layouttpl
	It contains all layout you can use in your page.
	Beware of difference between IE6 and 7 and the new-gen-browser (see README_layout.txt)

navigation
	It contains breadcrumbs files.

portal
	It contains HTML code for portlet skeleton :
		- with border
		- without border
		- maximized

portlet
	It contains portlet content.
	
