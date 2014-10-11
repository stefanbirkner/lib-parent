lib-parent
==========

The common parent POM of Stefan Birkner's Java libraries. This POM

* sets the current version for all standard plugins and configures
* provides configuration for a two step release

Usage
-----

Add this as parent POM to your project.

    <parent>
      <groupId>com.github.stefanbirkner</groupId>
      <artifactId>lib-parent</artifactId>
      <version>1</version>
    </parent>

You can release your library to
[Maven Central](http://search.maven.org/) with two steps.

    mvn release:prepare
    mvn release:perform

