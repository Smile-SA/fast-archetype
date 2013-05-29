# FAST archetype : RBS Change

This is a project to start working with [RBS Change](http://www.rbschange.fr).

## Prerequisite

We'll assume that you're familiar with [fast-maven-plugin](http://smile-sa.github.io/fast-maven-plugin).

If you don't, check the [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/2.12.1/fast-archetype-simple) at first, it is a very simple eexample, perfect to start.

## Create a new project

Use the Maven command line :

```
mvn archetype:generate \
	-DarchetypeCatalog=http://smile-sa.github.com/maven-repository/releases/archetype-catalog.xml \
	-DarchetypeGroupId=org.fast.archetype \
	-DarchetypeArtifactId=fast-archetype-rbs-3.6.1 \
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

The modules into src/main/resources/modules follow the PHP project file structure.

You'll find some example page :

- contentPage.html
- home.html
- productList.html
- productPage.html
- store.html
- storeList.html
- storeLocator.html

These pages should be similar to the default template in RBS Change.

[<img src="content/ContentPage.jpg" width="200" />](content/ContentPage.jpg)
[<img src="content/Home.jpg" width="200" />](content/Home.jpg)
[<img src="content/ProductList.jpg" width="200" />](content/ProductList.jpg)
[<img src="content/ProductPage.jpg" width="200" />](content/ProductPage.jpg)
[<img src="content/Store.jpg" width="200" />](content/Store.jpg)
[<img src="content/StoreList.jpg" width="200" />](content/StoreList.jpg)
[<img src="content/StoreLocator.jpg" width="200" />](content/StoreLocator.jpg)
