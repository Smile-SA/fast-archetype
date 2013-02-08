This project is an HTML5 project.

It uses Twitter Bootsrap as CSS framework.
You can find more informations here : http://twitter.github.com/bootstrap

One more thing :
CSS and Javascript may not be merged and minified.
If you want to put this files live on the internet, you may want to do so, don't forget about performance good practices !
More informations : http://developer.yahoo.com/performance/rules.html

If you prefer to use less.js to avoid CSS generation :
- to your skeleton.html, add :
	<link rel="stylesheet/less" href="v1/less/bootstrap.less" />
	<script src="lesscss/less-1.3.3.min.js"></script>

It uses LESS to generate CSS files.
LESS files are located into src/main/resources/pages/v1/less (it can be modified into pom.xml).
CSS are generated into target/generated-html/v1/css-generated (it can be modified into pom.xml).

Twitter boostratp files are locate into src/main/resources/pages/twitter-bootstrap.
If you want to update Bootstrap, replace this directory.
You may do so without fear as no development should have been made into this directory.