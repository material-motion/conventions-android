# A convention for Android libraries

The file system structure in this repo defines the conventions for a shared Android library.

    LibraryName/
      .editorconfig             <- Libraries are expected to follow a standard format.
      build.gradle              <- Libraries should support the Gradle build system.

      LICENSE                   <- License.
      README.md                 <- Essential installation and usage guide.
      CONTRIBUTING.md           <- Details for external contributors.

      library/                  <- The library module.
        build.gradle            <- Gradle build file for the library.
        src/
          main/                 <- The code for the library.
            AndroidManifest.xml <- The manifest for the library.
            java/               <- Java source files.
            res/                <- Android resources.
          androidTest/          <- Tests.

      sample/                   <- The sample module.
        build.gradle            <- Gradle build file for the sample.
        src/
          main/                 <- The code for the sample.
            AndroidManifest.xml <- The manifest for the sample.
            java/               <- Java source files.
            res/                <- Android resources.

## Creating a new Material Motion Android library

Run the following commands to create a new Android library:

    mdm new repo <name>
    cd $(mdm dir <name>)

- [Documentation for `mdm`](https://github.com/material-motion/material-motion-team/tree/develop/contributor_tools/mdm)
- [Documentation for `mdm new`](https://github.com/material-motion/material-motion-team/tree/develop/contributor_tools/new)

## License

Licensed under the Apache 2.0 license. See LICENSE for details.
