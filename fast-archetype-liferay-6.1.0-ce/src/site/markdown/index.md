# FAST archetype : RBS Change

This is a project to start working with [Liferay Portal](http://www.liferay.org).

## Prerequisite

We'll assume that you're familiar with [fast-maven-plugin](http://smile-sa.github.io/fast-maven-plugin).

If you don't, check the [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-simple) at first, it is a very simple eexample, perfect to start.

## Create a new project

Use the Maven command line :

```
mvn archetype:generate \
	-DarchetypeCatalog=http://smile-sa.github.com/maven-repository/releases/archetype-catalog.xml \
	-DarchetypeGroupId=org.fast.archetype \
	-DarchetypeArtifactId=fast-archetype-liferay-6.1.0-ce \
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

The modules folder contains an example of file structure :

- footer and header : page ark
- layouttpl contains different sets of columns
- navigation
- portal contains code coming from the portal itself (not the portlet), mostly portlet containers
- portlet contains different portlet example
- skeleton.html

This is just an idea, if you want to do it diffrently, you may do so.

You'll find lots of example pages.
The idea was to highlight the high combination of pages you can get with a portal.
There are a lot of variant because of layout (how many columns ?), portlet container (with or without border), portlet content (text with image, text without image, ...).
It is a good thing to do quickly and early test of content combination.

These pages should be similar to the default template in Liferay.

[<img src="content/layout__1_2_1_columns.jpeg" width="200" />](content/layout__1_2_1_columns.jpeg)
[<img src="content/layout__2_columns_iii.jpeg" width="200" />](content/layout__2_columns_iii.jpeg)
[<img src="content/layout__3_columns.jpeg" width="200" />](content/layout__3_columns.jpeg)
[<img src="content/maximized_portlet.jpeg" width="200" />](content/maximized_portlet.jpeg)
[<img src="content/portlet__assetpublisher.jpeg" width="200" />](content/portlet__assetpublisher.jpeg)
[<img src="content/portlet__bookmarks.jpeg" width="200" />](content/portlet__bookmarks.jpeg)
[<img src="content/portlet__calendar.jpeg" width="200" />](content/portlet__calendar.jpeg)
[<img src="content/portlet__documentandmediadisplay.jpeg" width="200" />](content/portlet__documentandmediadisplay.jpeg)
[<img src="content/portlet__webcontentdisplay.jpeg" width="200" />](content/portlet__webcontentdisplay.jpeg)
