# FAST archetype : simple

This is a very simple project.

Its only goal is to show how FAST works.

## Create a new project

Use the Maven command line :

```
mvn archetype:generate \
	-DarchetypeCatalog=http://smile-sa.github.com/maven-repository/releases/archetype-catalog.xml \
	-DarchetypeGroupId=org.fast.archetype \
	-DarchetypeArtifactId=fast-archetype-simple \
	-DarchetypeVersion=RELEASE
```

You'll have to answer the questions :

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

As the project is a Maven project, it has a standard structure :

- pom.xml : the project descriptor
- src/main
	- assembly : nothing matters here (for now)
	- filters : nothing matters here (for now)
	- resources
		- modules : our HTML modules
		- pages : our page descriptors
- target/generated-html : FAST generated files

The way FAST work is pretty simple : it takes page descriptor (HTML file) from src/main/resources/pages, computes the whole file with module from src/main/resources/modules and generates it into target/generated-html.

Every file other than *.html will be copy *as is* from pages to generated-html.

As files into target are all generated, you won't need to backup those (set this folder to svn or git ignore).

### Modules

This folder contains all the HTML fragment you may need.
There is no constraint to use or not the predefined structure, you're free to do whatever you want.

Still, there is a good practice : try to match the server side file srtucture. That way it will be easier to identify which file (JSP, PPH, Velocity, Freemarker, ...) has to be modified if a fragment change.

The module are plain HTML files.

You can defined placeholders into your module by using the esigate syntax (special HTML comments) :

```html
<!--$beginparam$foobar$-->Default value<!--$endparam$foobar$-->
```

Foobar is the key to that placeholder (of course, you can set it to a more suitable name).

This will allow us to create configurable template, use this first directive (beginparam / endparam) :

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title><!--$beginparam$title$-->Default title<!--$endparam$title$--></title>
	</head>
	<body>
		<div><!--$beginparam$main_content$-->Default main content<!--$endparam$main_content$--></div>
	</body>
</html>
```

### Page descriptor

This folder contains static resources (image, JS, CSS, ...) that will be cloned into target.
It also contains the page descriptors.

Page descriptors describe how to build a page with the module

The page descriptors are plain HTML files.
But the idea is to use modules !

To do so, you need to tell FAST what module you need by using a 2nd directive (includetemplate / endincludetemplate) : 

```html
<!--$includetemplate$modules$skeleton.html$-->
<!--$endincludetemplate$-->
```

That way, we are using the modules/skeleton.html file.
FAST will replace this directive with the skeleton content.

If you have defined placeholder in this skeleton.html, you want to fill them.
If you don't do so, the default values will be displayed.

To define the placeholder, you have to use the 3rd directive you'll need : beginput / endput

```html
<!--$includetemplate$modules$skeleton.html$-->
	<!--$beginput$title$-->Home<!--$endput$-->
	<!--$beginput$main_content$-->
		<!--$includetemplate$modules$header/header.html$--><!--$endincludetemplate$-->
		<!--$includetemplate$modules$content/home.html$--><!--$endincludetemplate$-->
		<!--$includetemplate$modules$footer/footer.html$--><!--$endincludetemplate$-->
	<!--$endput$-->
<!--$endincludetemplate$-->
```

We're filling 2 placeholders here :

- title : with a specific value
- main_content : with the inclusion of 3 others modules header, home, footer.

This is how you can use and reuse your module !

Of course, you can nest the template.
You'll be able to create a pretty fine template structure : skeleton > layout > columns > content modules.

### Assembly

You can create a versioned archive (ZIP format) of the generated files by using the CLI :

```
mvn package
```

It will generate  ZIP archive into target folder.

### Filters

If you want to use variable in your files, you can do so.

You'll find more information here : fast-maven-plugin : [filtering](http://smile-sa.github.io/fast-maven-plugin/2.3/extra-filtering.html).

## What's next ?

When you'll have understand how FAST works and play a little bit with the simple example, you be interested in checking more advanced example or maybe some archetype for a specific product.
To check on those archetype, go to the parent module : [fast-archetype](http://smile-sa.github.io/fast-archetype).
