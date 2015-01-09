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
      <version>4</version>
    </parent>


## Development Guide

Check für plugin updates by running

    mvn -U versions:display-plugin-updates

Update the plugins and mention the plugin updates in the commit message.
Now release the POM.    

## Release Guide

You can release the library to
[Maven Central](http://search.maven.org/) with two steps.

* Run `mvn clean deploy`
* Run `mvn nexus-staging:release`

Afterwards please update the `Installation` section of this readme with
the new version.
