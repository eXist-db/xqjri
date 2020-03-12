# XQJ RI
This is a copy of Oracle's XQJ RI (XQuery for Java Reference Implementation).

The code was downloaded from the JCP page [JSR-000225 XQuery API for Java (Final Release)](https://jcp.org/aboutJava/communityprocess/final/jsr225/index.html),
specifically the file [xqjri-20080114-133351.zip](http://www.oracle.com/technetwork/database/features/xmldb/xqjri-20080114-133351.zip). 

The [license](LICENSE) for the RI has some similarity to a conventional BSD-style open source license.

## Packaged for Maven
eXist-db makes use of the XQJ RI to provide its XQJ API. As eXist-db is built using Maven, the XQJ RI needs to be
available as a Maven artifact. We have placed the XQJ RI in a standard Maven project layout, and devised a 
suitable [Maven Project file](pom.xml) that allows us to package the XQJ RI as a Maven artifact and publish it.

### Building
To build, you need Maven 3.6+, you can then run from within the project:

```bash
mvn clean package
```

### Releasing
Assuming you have already registered and setup an account for Maven Central,
see: (OSSRH Guide - The Central Repository)[https://central.sonatype.org/pages/ossrh-guide.html].

To build and release to Maven Central, you can run from within the project:

```bash
mvn clean
mvn release:prepare
mvn release:perform
```
 