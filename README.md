# FAST archetypes

[Fast ApplicationS Templating archetypes](http://smile-sa.github.io/fast-archetype) that generate a FAST templating project.

FAST is a Maven plugin to build our static HTML file from module.
You'll find more info on its own page : [fast-maven-plugin](http://smile-sa.github.io/fast-maven-plugin).
Also, you'll find information about additional maven plugin use.

Splitting HTML into modules is something we're used to.
Every server side developement has a way to do it (include with PHP or Java JSP for example).
 
FAST is a light system to combine HTML module into a single readable HTML file, without having to install a server to combine our files.

The good thing being a Maven plugin is the Maven ecosystem : there are a lot of available plugins out there : minification, less, sass, lint, embedded server, ...
The best thing is that dependencies are fetched on-the-fly, it will get all the needed tools without any action from developer.

One more good thing is archetype.
An archetype is like a sample project with predefined files.
The idea is to speed up starting on new project.
This is why this project has been created : to gather FAST archetypes.

You'll find here those archetypes :

- [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-simple)
	The simpliest project you can get, useful to start understanding fast
- [fast-archetype-yui3](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-yui3)
	Demo project with embedded YUI3 CSS and some example templates
- [fast-archetype-960gs](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-960gs)
	Demo project with embedded 960gs CSS and some example templates
- [fast-archetype-sass](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-sass)
	Demo project with SASS file generation
- [fast-archetype-twitterbootstrap](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-twitterbootstrap)
	Project with Twitter Bootstrap embedded in its core
- [fast-archetype-liferay-6.1.0-ce](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-liferay-6.1.0-ce)
	Liferay bootstrap, very useful to start a static work on a Lifery project
- [fast-archetype-rbs-3.6.1](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-rbs-3.6.1)
	RBS Change bootstrap, very useful to start a static work on a RBS Change project

All those archetypes use a parent module containing lots of default configuration that will do some configuration for you : [fast-archetype-parent](http://smile-sa.github.io/fast-archetype-parent/).

If you want to contribute, please, do so =)
We'd like to hear from people working on Magento, Drupal, Wordpress, ...


## History

Here are the available versions :

- [fast-archetype-2.12.1](http://smile-sa.github.io/fast-archetype/2.12.1)

Current development documentation :

- [fast-archetype-2.12.2-SNAPSHOT](http://smile-sa.github.io/fast-archetype/2.12.2-SNAPSHOT)
