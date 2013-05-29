# FAST archetype : 960gs example

This is a simple project to show how use grid system like [960gs](http://960.gs).

This is a similar archetype to [fast-archetype-yui3](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-yui3) which is based on YUI3 instead of 960gs.

## Prerequisite

We'll assume that you're familiar with [fast-maven-plugin](http://smile-sa.github.io/fast-maven-plugin).

If you don't, check the [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-simple) at first, it is a very simple eexample, perfect to start.

## Create a new project

Use the Maven command line :

```
mvn archetype:generate \
	-DarchetypeCatalog=http://smile-sa.github.com/maven-repository/releases/archetype-catalog.xml \
	-DarchetypeGroupId=org.fast.archetype \
	-DarchetypeArtifactId=fast-archetype-960gs \
	-DarchetypeVersion=RELEASE
```

You'll have to set the following properties :

- groupId and artifactId : this is the Maven way to identify your project. *org.acme* for the groupId and *foobar* for the artifactId for example.
- version (you can leave the default setting)
- package (leave default, which should be computed from what you set earlier)

*Build success* should appear if everything went OK.

A new folder have been created, its name is the artifactId.

To get all the Maven dependencies, use this command line :

```
mvn compile
```

Again, *Build success* should appear (you may have to wait the first time to get all dependencies).

## Let's take a look inside

The folder hierarchy is the same as the simple example :

- pom.xml
- src/main/assembly and src/main/filters
- src/main/resources/modules and src/main/resources/pages

The HTML fragmentation into src/main/resources/modules is an example.
The good thing to look at, compared to [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-simple) is the src/main/resources/modules/layout folder.
We set in this folder some different layout which will be used as nested template to create our page ark and columns.

This good practice helps us to separate the content from the layout, easing module reuse.

In the src/main/resources/pages, we have multiple page defined that show module reuse and how quickly you can create a new page with a different layout.
Also, you'll find a favicon which is something you must not forget (front end good practice, see [YSlow : best practices for speeding up your web site - favicon](http://developer.yahoo.com/performance/rules.html#favicon).

You can see that all static content are into a *v1* folder. It is handy to have version as part of the path to static resource to help cache management (see [YSlow : best practices for speeding up your web site - expires](http://developer.yahoo.com/performance/rules.html#expires)). You don't have to use it that way, you can also use another version systeme like a timestamp (screen.css?_timestamp=123456879).

Content static file are separate from the UI files (the *v1* folder). That way, you can share the UI file between your 2 projects : FAST project and Integrated project. One modification in one of these project will be reflected into the other. It will ease front and back developers to work hand in hand.

The project defined 2 variables into filter.properties :

- static.path.root
- content.path.root

You can use them into your module : ${static.path.root}, ${content.path.root}.
