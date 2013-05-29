# FAST archetype : SASS example

This is an example project to demonstratehow to use the [Maven SASS plugin](http://smile-sa.github.io/fast-maven-plugin/2.3/extra-sass.html).

## Prerequisite

We'll assume that you're familiar with [fast-maven-plugin](http://smile-sa.github.io/fast-maven-plugin).

If you don't, check the [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-simple) at first, it is a very simple eexample, perfect to start.

## Create a new project

Use the Maven command line :

```
mvn archetype:generate \
	-DarchetypeCatalog=http://smile-sa.github.com/maven-repository/releases/archetype-catalog.xml \
	-DarchetypeGroupId=org.fast.archetype \
	-DarchetypeArtifactId=fast-archetype-sass \
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

This example project has [fast-archetype-yui3](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-yui3) as base.
The HTML file content and structure are the same.

The difference comes from the CSS management.

Located into src/main/resources/pages/v1/scss, the CSS are written in SASS and build with the [Maven SASS plugin](http://smile-sa.github.io/fast-maven-plugin/2.3/extra-sass.html).
