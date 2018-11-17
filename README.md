moot
====

A shell script to easily select, download and run the versions of Maven and JDK you want for your build.

moot stands for "Maven boot". It allows to bootstrap a maven build by using (and downloading if required) a given version of Maven and JDK.
These versions are indicated in the file moot.properties (cf. commented example in this repository).

### Use cases

moot can be used in the following use cases:
* you want a reproducible build, so you use the [reproducible-build-maven-plugin](http://zlika.github.io/reproducible-build-maven-plugin/), but you need a way to impose an exact version of Maven and JDK,
* you want a way to easily test your project with different versions of Maven and JDK,
* you want to be able to build your project from anywhere, even if Maven and JDK are not installed.

### Compatibility

Currently, the script is working on Linux and "should" work on MacOS. For Windows users, it would be interesting to have an equivalent PowerShell script: feel free to propose a Pull Request!

### Usage

* put moot.sh and moot.properties at the root of your maven project
* give execute permissions to moot.sh
* configure moot.properties to select the Maven and JDK versions you want
* use moot instead of mvn to run the build:

```
./moot.sh clean install
```

### JDK vendors

Currently, JDK are downloaded from the AdoptOpenJDK project. However, I plan to add other vendors (AWS Corretto, Oracle OpenJDK...) in the future.

