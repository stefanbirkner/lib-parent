# lib-parent

The common parent POM of Stefan Birkner's Java libraries. This POM

* sets the current version for all standard plugins and configures
* provides configuration for a two step release

The POM is published under the
[MIT license](http://opensource.org/licenses/MIT).

## Usage

Use this POM as parent POM of your project by adding the following
snippet to your `pom.xml`.

    <parent>
      <groupId>com.github.stefanbirkner</groupId>
      <artifactId>lib-parent</artifactId>
      <version>5</version>
    </parent>


## Development Guide

Check für plugin updates by running

    mvn -U versions:display-plugin-updates

Update the plugins and mention the plugin updates in the commit message.
Now release the POM.    

## Release Guide

You can release the library to
[Maven Central](http://search.maven.org/) with a few steps.

* Set the new version in `pom.xml` and in the installation section of
  this document.
* Commit the updated `pom.xml` and `README.md`.
* Run `mvn clean deploy`
* Add a tag for the release: `git tag lib-parent-XX`
