### What are Build and Package Manager Tools?
* Application needs to be deployed on a production server
* For that, we want to package application into a single moveable file (artifact), also called "building the code"
* This is what a build tool or package manager tool does

#### What is an "artifact"?
* Includes application code and all its dependencies

#### What does "building the code" mean?
* Compiling the code
* Compressing the code
* Package hundred of files to 1 single file

#### What is an "artifact repository"?
* Storage for artifacts
artifact repository
* To deploy it for example multiple times, have backup etc.
* Examples: Nexus, Jfrog Artifactory

#### Artifacts
* Artifact files look different for each programming language
    * Zip or Tar file
    * JAR or WAR file
* JAR = Java Archive Includes whole code plus dependencies, like Spring framework, datetime libraries, pdf processing libraries
* JavaScript's artifact can be a zip or tar file

#### Different Build Tools for different programming languages
* Java Build Tools: Gradle and Maven
* JavaScript Package Manager: npm

#### Installation and Setup of Projects
* In this module you need to install following technologies and setup following projects:
* Technologies
    * Java gradle
    * Java maven
    * Node npm
* Projects
    * java gradle application
    * java maven application
    * nodejs application
* Download IntelliJ = Code Editor
* Install OS Package Manager (like Homebrew for Mac)
* Install Java, Maven, Node, npm

#### Clone Git Projects & Open in Intellij:
* Setup Java-Maven Project in IntelliJ
* Setup Java-Gradle Project in IntelliJ
* Setup Node.js-npm Project in IntelliJ

#### Build an Artifact
* With a Build Tool you can build the artifact
* Specific to the programming language
* Build Tools have command line tool and commands to execute the tasks

#### "Build" Process in Maven or Gradle:
* Installs dependencies
* Compiles and compresses your code
* Example Build Tools for Java: Gradle and Maven
* Artifact: JAR or WAR file