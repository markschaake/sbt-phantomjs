# sbt-phantomjs  [![Build Status](https://travis-ci.org/saturday06/sbt-phantomjs.png?branch=master)](https://travis-ci.org/saturday06/sbt-phantomjs)

An automated PhantomJS Installer for sbt

## Setup

`project/plugins.sbt`
```scala
addSbtPlugin("jp.leafytree.sbt" % "sbt-phantomjs" % "0.1.1")
```

`build.sbt`
```scala
val rootProject = (project in file(".")).enablePlugins(SbtPhantomJs)
```

## Tasks

### installPhantomJs task

```bash
$ sbt installPhantomJs
```

- Install PhantomJS to `target/phantomjs/`
- Write properties for Selenium PhantomJS Driver to ...
  - `target/phantomjs.properties` file
  - System Property using `System.setProperty()`
  - `javaOptions` of sbt