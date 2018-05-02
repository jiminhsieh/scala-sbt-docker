# [Scala & sbt Docker images](https://hub.docker.com/r/jiminhsieh/scala-sbt/)

[![Build Status](https://travis-ci.org/jiminhsieh/scala-sbt-docker-images.svg?branch=master)](https://travis-ci.org/jiminhsieh/scala-sbt-docker-images)
[![](https://img.shields.io/docker/pulls/jiminhsieh/scala-sbt.svg)](https://hub.docker.com/r/jiminhsieh/scala-sbt/)
[![](https://img.shields.io/docker/stars/jiminhsieh/scala-sbt.svg)](https://hub.docker.com/r/jiminhsieh/scala-sbt/)


## Why another Docker images for Scala and sbt?

I know there is a popular Docker image for Scala and sbt already exists. [It](https://hub.docker.com/r/hseeberger/scala-sbt/) is made by [Heiko Seeberger](https://github.com/hseeberger).

The reasons I make another Scala and sbt Docker images:

* It will be great to use JVM that passed [TCK/JCK](https://en.wikipedia.org/wiki/Technology_Compatibility_Kit).
* [AdoptedOpenJDK's OpenJ9 was just passed TCK/JCK](https://blog.adoptopenjdk.net/2018/03/jck-certification-and-an-anniversary-of-sorts). We should give it a try.

## Which JVM do those images use?

* [Azul Zulu](https://www.azul.com/products/zulu-and-zulu-enterprise/)
* [Eclipse OpenJ9](https://www.eclipse.org/openj9/)

## [Available Docker image tags](https://hub.docker.com/r/jiminhsieh/scala-sbt/tags/)
* [Azul Zulu](https://www.azul.com/products/zulu-and-zulu-enterprise/)
    * Java 7
    * Java 8
* [AdoptedOpenJDK](https://adoptopenjdk.net/)
    * OpenJ9 Java 8
    
## The base images I used
* [azul/zulu-openjdk](https://hub.docker.com/r/azul/zulu-openjdk/)
* [adoptopenjdk/openjdk8-openj9](https://hub.docker.com/r/adoptopenjdk/openjdk8-openj9/)