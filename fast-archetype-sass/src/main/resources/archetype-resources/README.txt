This project is an HTML5 project.

It uses Yahoo UI 3 as CSS framework.
You can find more informations here : http://yuilibrary.com
- Grids : http://yuilibrary.com/yui/docs/cssgrids/
- Fonts : http://yuilibrary.com/yui/docs/cssfonts/
- Base : http://yuilibrary.com/yui/docs/cssbase/
- Reset : http://yuilibrary.com/yui/docs/cssreset/
- SASS : http://sass-lang.com/

It uses SASS to generate CSS files.
SCSS files are located into src/main/resources/v1/scss (it can be modified into pom.xml).
CSS are generated into target/generated-html/v1/css-generated (it can be modified into pom.xml).
Compass is not available as it is not handle by the sass-maven-plugin.

One more thing :
CSS and Javascript may not be merged and minified while developping.
If you want to put this files live on the internet, you may want to do so, so don't forget about performance good practices !
More informations : http://developer.yahoo.com/performance/rules.html
