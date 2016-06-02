# A convention for Android libraries

The file system structure in this repo defines the conventions for a shared Android library.

    LibraryName/
      .editorconfig           <- Libraries are expected to follow a standard format.
      build.gradle            <- Libraries should support the Gradle build system.

      LICENSE                 <- License.
      README.md               <- Essential installation and usage guide.
      CONTRIBUTING.md         <- Details for external contributors.

      library/                  <- The library module.
        build.gradle            <- Gradle build file for the library.
        src/
          main/                 <- The code for the library.
            AndroidManifest.xml <- The manifest for the library.
            java/               <- Java source files.
            res/                <- Android resources.
          androidTest/          <- Tests.

      sample/                  <- The sample module.
        build.gradle            <- Gradle build file for the sample.
        src/
          main/                 <- The code for the sample.
            AndroidManifest.xml <- The manifest for the sample.
            java/               <- Java source files.
            res/                <- Android resources.

## Bootstrap script

The bootstrap script creates the skeletal directory structure for an
Android library repo.
This script must be provided a library name, package name, github group,
and github repo.

Example usage:

    # Create ~/MyLibrary and populate with this repo.
    cd ~/MyLibrary
    ./bootstrap.sh MyLibrary com.example.library github-username github-repo
