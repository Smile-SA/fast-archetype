This project is an HTML5 project.

It uses Twitter Bootstrap as CSS framework.
You can find more informations here : http://twitter.github.com/bootstrap

Twitter bootstrap files are located into src/main/resources/pages/twitter-bootstrap.
If you want to update Bootstrap, replace this directory.
You may do so without fear as no development should have been made into this directory.

It uses LESS to generate CSS files.
LESS files are located into src/main/resources/pages/v1/less (it can be modified into pom.xml).
CSS are generated into target/generated-html/v1/css-generated (it can be modified into pom.xml).

If you prefer to use less.js to avoid CSS generation :
- into your skeleton.html, add :
	<link rel="stylesheet/less" href="v1/less/bootstrap.less" />
	<script src="lesscss/less-1.3.3.min.js"></script>

One more thing :
CSS and Javascript may not be merged and minified.
If you want to put this files live on the internet, you may want to do so, don't forget about performance good practices !
More informations : http://developer.yahoo.com/performance/rules.html

About this archetype :
Twitter Bootstrap (TB) is a generic framework.
Templates provided in this archetype are examples of what you can do with TB.

Of course, you don't have to use fluid container if you don't want.
In that case, you may have to edit src/main/resources/modules/skeleton.html and some layout (src/main/resources/modules/layout/*.html).