# [Scala & sbt Docker images](https://hub.docker.com/r/jiminhsieh/scala-sbt/)

[![Build Status](https://travis-ci.org/jiminhsieh/scala-sbt-docker-images.svg?branch=master)](https://travis-ci.org/jiminhsieh/scala-sbt-docker)
[![](https://img.shields.io/docker/pulls/jiminhsieh/scala-sbt.svg)](https://hub.docker.com/r/jiminhsieh/scala-sbt/)
[![](https://img.shields.io/docker/stars/jiminhsieh/scala-sbt.svg)](https://hub.docker.com/r/jiminhsieh/scala-sbt/)


## Why another Docker images for Scala and sbt?

I know there is a popular Docker image for Scala and sbt already exist.
[It](https://hub.docker.com/r/hseeberger/scala-sbt/) was made by [Heiko Seeberger](https://github.com/hseeberger).

The reasons I make another Scala and sbt Docker images:

* It will be great to use JVM that passed [TCK/JCK](https://en.wikipedia.org/wiki/Technology_Compatibility_Kit).
* [AdoptedOpenJDK's OpenJ9 was just passed TCK/JCK](https://blog.adoptopenjdk.net/2018/03/jck-certification-and-an-anniversary-of-sorts). We should give it a try.

## Which JVM do those images use?

* [Azul Zulu](https://www.azul.com/products/zulu-and-zulu-enterprise/)
* [Eclipse OpenJ9](https://www.eclipse.org/openj9/)

## Available Docker image tags
* [Azul Zulu](https://www.azul.com/products/zulu-and-zulu-enterprise/)
    * 7
        * [zulu_7-0.13.x-2.11.x](zulu_7/0.13.x/2.11.x/Dockerfile)
    * 8
        * [zulu_8-1.x-2.12.x](zulu_8/1.x/2.12.x/Dockerfile)
        * [zulu_8-1.x-2.11.x](zulu_8/1.x/2.11.x/Dockerfile)
        * [zulu_8-0.13.x-2.12.x](zulu_8/0.13.x/2.12.x/Dockerfile)
        * [zulu_8-0.13.x-2.11.x](zulu_8/0.13.x/2.11.x/Dockerfile)
* [AdoptedOpenJDK](https://adoptopenjdk.net/)
    * OpenJ9 8
        * [openj9_8-1.x-2.12.x](openj9_8/1.x/2.12.x/Dockerfile)
        * [openj9_8-1.x-2.11.x](openj9_8/1.x/2.11.x/Dockerfile)
        * [openj9_8-0.13.x-2.11.x](openj9_8/0.13.x/Dockerfile)
    
## The actual base images I used
* [azul/zulu-openjdk](https://hub.docker.com/r/azul/zulu-openjdk/)
* [adoptopenjdk/openjdk8-openj9](https://hub.docker.com/r/adoptopenjdk/openjdk8-openj9/)