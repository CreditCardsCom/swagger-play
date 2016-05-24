# Swagger Play Module

## Overview
This is a module to integrate swagger into [Play Framework](http://www.playframework.org) 2.5.x.

At the time of this writing, support for Play 2.5 was not available in the official
[swagger-play](https://github.com/swagger-api/swagger-play) repository. This repository
is a copy of the Play-2.5 folder in pikel's [fork](https://github.com/pikel/swagger-play).
It was created this way to make it easier to add as a git dependency.

*WARNING:* This repository will be discarded once support is added to the official
swagger-play repo.

## Usage

### As a git dependency

You can include this library as a dependency in your build.sbt file:

```
lazy val root = (project in file(".")).enablePlugins(PlayJava).dependsOn(swagger)
lazy val swagger = RootProject(uri("ssh://git@github.com/CreditCardsCom/swagger-play.git"))
```

### Build from source

```
cd swagger-play

sbt publishLocal
```

This will add the library to your local ivy repo. You can then add a maven-style dependency
to your build file:

```
  "io.swagger" %% "swagger-play2" % "1.5.2-SNAPSHOT"
```
