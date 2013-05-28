# FAST archetype : Twitter bootstrap

This is a project to start working with [Twitter bootstrap](http://twitter.github.io/bootstrap/).

## Prerequisite

We'll assume that you're familiar with [fast-maven-plugin](http://smile-sa.github.io/fast-maven-plugin).

If you don't, check the [fast-archetype-simple](http://smile-sa.github.io/fast-archetype/fast-archetype-simple) at first, it is a very simple eexample, perfect to start.

## Create a new project

Use the Maven command line :

```
mvn archetype:generate \
	-DarchetypeCatalog=http://smile-sa.github.com/maven-repository/releases/archetype-catalog.xml \
	-DarchetypeGroupId=org.fast.archetype \
	-DarchetypeArtifactId=fast-archetype-twitterbootstrap \
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
You'll find some layout example into src/main/resources/modules/layout, some navigation variant into src/main/resources/modules/navigation ... nothing fancy here.
Modules into src/main/resources/modules/content are just the Twitter boostrap doc split into module : [Base CSS](http://twitter.github.io/bootstrap/base-css.html) and [Compenents](http://twitter.github.io/bootstrap/components.html).

The src/main/resources/pages contains 2 new folders :

- *lesscss* contains less.js which allow you to work with [LESS](http://lesscss.org) without the compilation (it is done into the browser through javascript ; don't use in for your live website).
- *twitter-bootstrap* contains the official distribution (in [LESS](http://lesscss.org) format to allow you modifying theme)

The idea is to have an official separate [Twitter bootstrap](http://twitter.github.io/bootstrap/) folder to ease upgrade. If you don't change anything into this folder, upgrade should be a piece of cake.

Into src/main/resources/pages/v1/less, you'll find the [LESS](http://lesscss.org) files used for our project :

- bootstrap.less and responsive.less comes from the Twitter Bootstrap distribution (if you upgrade [Twitter bootstrap](http://twitter.github.io/bootstrap/), you may have to upgrade those files too) ; they are the master files that will aggregate TB CSS files.
- variables.less contains all the variables for customizing [Twitter bootstrap](http://twitter.github.io/bootstrap/)
- screen.less contains your own CSS

You'll find lots of HTLM page descriptor.
It is, in fact, the official documentation split into smaller HTML page.
