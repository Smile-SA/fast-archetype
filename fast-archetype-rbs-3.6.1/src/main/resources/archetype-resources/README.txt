#set( $symbol_pound = '#' )
#set( $symbol_dollar = '$' )
#set( $symbol_escape = '\' )
This project is an XHTML 1.0 transitional project.

It uses 960gs as CSS framework, for RBS Change.
You can find more informations here : http://960.gs/
and here : http://www.rbschange.fr/

jQuery is used for the javascript side.
You can find more informations here : http://jquery.com

More things :
CSS and Javascript may not be merged and minified.
If you want to put this files live on the internet, you may want to do so, don't forget about performance good practices !
More informations : http://developer.yahoo.com/performance/rules.html

As a rule of thumb, keep the default RBSChange CSS.
Add your custom CSS in the corresponding module /style directory. Then include it in .../css/screen.css
By doing so, you can keep CSS to a minimum while complying to RBS Change development standards

Read folder-walkthrough.readme for more details regarding src/main/resources/modules subfolders