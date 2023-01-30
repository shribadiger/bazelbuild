# Bazel Build for C++ Software Application
Bazel Tool is developed by google to automate the build process. Now Its an open source and it can be used by anyone. Many companies are using it for there day to day build automations. Its very helpful to integrate with CI/CD pipeline. GoogleTest frame work can be integrated easily for Unit Testing of an application.

### Features of Bazel
* **Speedup Build and Test:** It has very good features for rebuilding the application in optimized way with local and distributed cache technique. Optimized dependency analysis and concurrent execution of builds. These feature boost the regular builds and provides the build results in well defined time.  
* **Multiple Language and Multi Platfrom Support:** It can build the Java, Go,C++ and many more languages in different platform like Windows,Linux and Mac
* **Scalable**: Bazel helps you scale your organization, codebase, and continuous integration solution. It handles codebases of any size, in multiple repositories or a huge monorepo.

### Advantages from bazel in modern build process
1) The build is competely depend on the input which is provided. Your input can decide which part of code need to rebuild and produce constant output.
![Alt text](./build.png?raw=true "Chained Build")
2) Easy to integrate with Docker and Kubernetes. If you have monorepo and multiple micro services, then It can build each container and host it for test environment. Further it can provide incremental build and perfrom deployment by using any orchastration tools like AWS and Kubernetes.
![Alt text](./chainbuild.png?raw=true "Chained Build")
3) Bazel can handle the large projects. Bazel provides a uniform interface to building and testing across projects and programming languages, which is beneficial to CI/CD Process.
4) Bazel used internal caching mechanism. It caches the builds and rebuild the content only which developer made the changes. It compares the privous build whcih is cached and newly built content and produce the final binary. This cache technique speedup the build process.

### Bazel Build Structure:
* **workspace**: 
     1. A workspace is a directory tree on your filesystem that contains the source files for the software you want to build. Each workspace has a text file named WORKSPACE which may be empty, or may contain references to external dependencies required to build the outputs. 
     2.  Directories containing a file called WORKSPACE are considered the root of a workspace. Therefore, Bazel ignores any directory trees in a workspace rooted at a subdirectory containing a WORKSPACE file, as they form another workspace. 
     3. Bazel also supports WORKSPACE.bazel file as an alias of WORKSPACE file. If both files exist, WORKSPACE.bazel is used.
![Alt text](./dir.png?raw=true "Chained Build")
* **Package**:
     1.  The primary unit of code organization in a repository is the package. A package is a collection of related files and a specification of how they
     can be used to produce output artifacts.
     2. This folder will contain the *BUILD* and *BUILD.bazel* file. Its holds all other folders which required for build.
* **Target**:
     1. A package is a container of targets, which are defined in the package's BUILD file. Most targets are one of two principal kinds, files and rules.
     2. Files are further divided into two kinds. Source files are usually written by the efforts of people, and checked in to the repository. Generated files, sometimes called derived files or output files, are not checked in, but are generated from source files.
     ![Alt text](./rules.png?raw=true "Chained Build")
     
### Labels: ###

All targets belong to exactly one package. The name of a target is called its label. Every label uniquely identifies a target. A typical label in canonical form looks like:

 `@myrepo//my/app/main:app_binary`
