
# Changelog

This is the changelog for SpotBugs Gradle Plugin. This follows [Keep a Changelog v1.0.0](http://keepachangelog.com/en/1.0.0/).

Currently the versioning policy of this project follows [Semantic Versioning](http://semver.org/) from version 1.6.0.

## Unreleased - 2019-??-??

## 2.0.1 - 2019-10-16

### Fixed

* Avoid needless task creation (#165)

## 2.0.0 - 2019-05-13

### Removed

* Gradle 5.0 support

## 1.7.1 - 2019-03-14

### Fixed

* Treat `projectName` and `release` as task input ([#131](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/131))

## 1.7.0 - 2019-03-14

### Added

* Add `-projectName` option ([#111](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/111))
* Add `-release` option ([#111](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/111))
* Add `setStylesheet(String)` that accepts relative path from the root of `spotbugs.jar` ([#107](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/107))

## 1.6.11 - 2019-03-10

### Changed

* Use SpotBugs 3.1.12 by default
* Upgrade SLF4J to 1.8.0-beta4

## 1.6.10 - 2019-02-18

### Fixed

* "Trying to add already registered factory" problem reported as [a spotbugs issue](https://github.com/spotbugs/spotbugs/issues/819)
* Result caching works across checkouts. Previously it was using absolute paths and therefore didn't work. ([#96](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/96))
* Support text type bug report ([#31](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/31))

### Removed

* Usage of worker API introduced at [#57](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/57)
* Drop support for Gradle 4, that causes [SLF4J related problem](https://github.com/gradle/gradle/issues/2657)

### Changed

* Use SpotBugs 3.1.11 by default

## 1.6.9 - 2019-01-04

### Fixed

* `classes` filtering that was broken at 1.6.2 ([#54](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/54))

## 1.6.8 - 2018-12-21

### Changed

* Use SpotBugs 3.1.10 by default

## 1.6.7 - 2018-12-18

### Changed

* Keep track of top-level source set folders [#59](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/59)

### Fixed

* Analyze runtime classpath instead of compile classpath. [#62](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/62)

## 1.6.6 - 2018-12-08

## Fixed

* Prevent NPE in unexpected situations where no reports are enabled, despite xml being set by default using convention mapping (See [#61](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/61), [#68](https://github.com/spotbugs/spotbugs-gradle-plugin/issues/68))

## 1.6.5 - 2018-10-17

### Changed

* Replace usage of internal Gradle APIs with supported [Worker API](https://guides.gradle.org/using-the-worker-api/). [#58](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/58)

## 1.6.4 - 2018-09-26

### Changed

* Use SpotBugs 3.1.7 by default
* Replace usage of internal class ClosureBackedAction [#51](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/51)

## 1.6.3 - 2018-09-08

* Use SpotBugs 3.1.6
* Added support for passing JVM arguments to the JavaExecHandleBuilder when creating a SpotBugsTask.
* Support Gradle 4.10 that cause problem with problematic method reference. ([#40](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/40))

## 1.6.2 - 2018-05-23

* Use SpotBugs 3.1.3
* Add `showProgress` option to task mapping.
* Added a minor fix to handle multiple output source directories. With the release of gradle 4.0 the default location of classes changed from "build/classes/main" -> "build/{java, groovy, scala}/main". This caused a bug where the plugin would ignore any classes compiled which were not located within "build/classes/" or for clean groovy/scala projects the plugin would outright fail to perform an analysis due to NO-SOURCE.([#12](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/12))
* Support Gradle 4.8 [#22](https://github.com/spotbugs/spotbugs-gradle-plugin/pull/22)

## 1.6.1 - 2018-02-25

* Use SpotBugs 3.1.2
* Fixed "loud output" [#506](https://github.com/spotbugs/spotbugs/issues/506) by adding an option to show progress and disabling it by default, matching the behaviour of the FindBugs Gradle Plugin

## 1.6.0 - 2017-10-25

* Use SpotBugs 3.1.0

## 1.5 - 2017-10-14

* Use SpotBugs 3.1.0-RC7
* Make build failed when user uses unsupported Gradle version ([#357](https://github.com/spotbugs/spotbugs/issues/357))
* Make error message human readable ([#428](https://github.com/spotbugs/spotbugs/pull/428))
* Fix missing dependency on compile task ([#440](https://github.com/spotbugs/spotbugs/issues/440))

## 1.4 - 2017-09-25

* Use SpotBugs 3.1.0-RC6
* Fix "Cannot convert the provided notation to a File or URI: classesDirs" error ([#320](https://github.com/spotbugs/spotbugs/issues/320))
* Support working with Android Gradle Plugin 2.3 ([#256](https://github.com/spotbugs/spotbugs/issues/256))

## 1.3 - 2017-08-16 [YANKED]

* Use SpotBugs 3.1.0-RC5
* Stop using [single class directory](https://docs.gradle.org/4.0.2/release-notes.html#multiple-class-directories-for-a-single-source-set) to prepare for Gradle v5 ([#299](https://github.com/spotbugs/spotbugs/issues/299))
* Print 'SpotBugs' instead of 'FindBugs' ([#291](https://github.com/spotbugs/spotbugs/issues/291))

## 1.2 - 2017-07-21

* Use SpotBugs 3.1.0-RC4
* Fixed [#214](https://github.com/spotbugs/spotbugs/issues/214)

## 1.1 - 2017-06-10

* Use SpotBugs 3.1.0-RC2

## 1.0 - 2017-05-16

* First release which uses FindBugs 3.0.1
