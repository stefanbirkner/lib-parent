# lib-parent

The common parent POM of Stefan Birkner's Java libraries. This POM

* sets the current version for all standard plugins
* provides configuration for a simple release workflow
* adds plugins that I always use

The POM is published under the
[MIT license](http://opensource.org/licenses/MIT).

## Usage

Use this POM as parent POM of your project by adding the following
snippet to your `pom.xml`.

    <parent>
      <groupId>com.github.stefanbirkner</groupId>
      <artifactId>lib-parent</artifactId>
      <version>9</version>
    </parent>


## Development Guide

Check for plugin updates by running

    mvn -U versions:display-plugin-updates

Update the plugins and mention the plugin updates in the commit message.
Now release the POM.    

## Release Guide

You can release the POM to
[Maven Central](http://search.maven.org/) with a few steps.

* Set the new version in `pom.xml` and in the installation section of
  this document.
* Commit the updated `pom.xml` and `README.md`.
* Run `mvn clean deploy`
* Add a tag for the release: `git tag lib-parent-XX`
