---
layout: page
title: Tiler - Getting Started
---

# Getting Started

## Prerequisites

* Install Oracle JDK 1.8+
* Install Maven 3.2+
* Install Redis 2.8+

## Creating a dashboard project

Tiler provides a Maven Archetype for generating a new dashboard project.

To generate a project run:

``` bash
$ mvn archetype:generate -Dfilter=io.tiler:tiler-maven-archetype
```

Maven will ask you which archetype you want to use and then ask you to choose a version of that archetype.

Once you select the archetype, you'll be prompted for the following information:

* `groupId`. Maven groupId for the project that will be created.  For example `org.example`
* `artifactId`. Name of the project.  For example `example-dashboards`
* `version`. Initial version of the project.  For example `0.1.0-SNAPSHOT`
* `package`. Java package for the classes in the project.  For `org.example.dashboards`

After entering above the information and confirming you want to proceed, the new project will be created in a subdirectory of your current directory.  The subdirectory will be named after the `artifactId` you entered.

Once the project has been created, change directory to the project's directory:

``` bash
$ cd my-project
```

You can now build and run your new dashboard project:

``` bash
$ mvn package vertx:runMod
```

Once the project is running, open your browser to `http://localhost:8080`
