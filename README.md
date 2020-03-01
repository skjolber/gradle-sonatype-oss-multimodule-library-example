# gradle-sonatype-oss-multimodule-library-example
Real-world template for open-source libraries with the [Gradle] build system and OSS Sonatype using the [gradle-maven-publish-plugin]:
  
  * core libraries (my-jwt)
  * framework adaptions of core libraries
  * examples using the above
    * part of the multi-module build, but still
    * standalone, and easily copied as-is

The examples are not published. 

Bugs, feature suggestions and help requests can be filed with the [issue-tracker].

## License
[Apache 2.0]

## Usage
Add the following properties to your global gradle properties at `~/.gradle/gradle.properties`:

```
SONATYPE_NEXUS_USERNAME=<email>
SONATYPE_NEXUS_PASSWORD=<passord>
```

Build using command

> ./gradlew clean build --info

Publish is performed using the command 

> ./gradlew build uploadArchives --info

### Signing
For signing, add the following properties to your global gradle properties at `~/.gradle/gradle.properties`:

```
signing.keyId=12345678
signing.password=some_password
signing.secretKeyRingFile=/Users/yourusername/.gnupg/secring.gpg
```

See plugin [gradle-maven-publish-plugin] for further details.

# See also

  * Corresponding example using JFrog Artifactory: [gradle-jfrog-artifactory-multimodule-library-example]

# History

 - 1.0.0: Initial version

[Apache 2.0]:          			http://www.apache.org/licenses/LICENSE-2.0.html
[issue-tracker]:       			https://github.com/skjolber/gradle-foss-library-template/issues
[Gradle]:              		 	https://gradle.org/
[gradle-maven-publish-plugin]:                  https://github.com/vanniktech/gradle-maven-publish-plugin/
[gradle-jfrog-artifactory-multimodule-library-example]: https://github.com/skjolber/gradle-jfrog-artifactory-multimodule-library-example


