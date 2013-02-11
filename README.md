Fast ApplicationS Templating archetype that generate a fast templating project.

FAST is a Maven plugin too make our static HTML file as module.
You'll find more info on its own page : http://smile-sa.github.com/maven-repository/doc/org.fast.maven.plugin.fast-maven-plugin

Splitting HTML into module is something we're used to.
Every server side developement has a way to do id (include with PHP or Java JSP for example).
 
We may not want to have to install a server to combine our file.
FAST is a light system to combine HTML module into a single readable HTML file.

The good thing being a Maven plugin is the Maven ecosystem : there are a lot a available plugin out there : minification, less, sass, lint, embedded server, ...
The best thing is that dependecies are fetched on-the-fly, it will get all the needed tool without any action from developer.

The last, but not least, good thing is archetype.
Archetype is like a sample project with predefined files.
The idea is to speed up starting on new project.
This is why this project has been created : to gather fast-archetype.

You'll find here those archetypes :

- [x] fast-archetype-simple
	The simpliest project you can get, useful to start understanding fast
- [x] fast-archetype-yui3
	Demo project with embedded YUI3 CSS and some example templates
- [x] fast-archetype-960gs
	Demo project with embedded 960gs CSS and some example templates
- [x] fast-archetype-liferay-6.1.0-ce
	Liferay bootstrap, very useful to start a static work on a Lifery project
- [x] fast-archetype-sass
	Demo project with SASS file generation
- [x] fast-archetype-twitterbootstrap
	Project with Twitter Bootstrap embedded in its core

More to come :

- [ ] fast-archetype-magento
- [ ] fast-archetype-drupal
- [ ] fast-archetype-wordpress
