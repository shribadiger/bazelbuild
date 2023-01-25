# Bazel Build for C++ Software Application
Bazel Tool is developed by google to automate the build process. Now Its an open source and it can be used by anyone. Many companies are using it for there day to day build automations. Its very helpful to integrate with CI/CD pipeline. GoogleTest frame work can be integrated easily for Unit Testing of an application.

### Features of Bazel
* **Speedup Build and Test:** It has very good features for rebuilding the application in optimized way with local and distributed cache technique. Optimized dependency analysis and concurrent execution of builds. These feature boost the regular builds and provides the build results in well defined time.  
* **Multiple Language and Multi Platfrom Support:** It can build the Java, Go,C++ and many more languages in different platform like Windows,Linux and Mac
* **Scalable**: Bazel helps you scale your organization, codebase, and continuous integration solution. It handles codebases of any size, in multiple repositories or a huge monorepo.

### Advantages from bazel in modern build process
1) The build is competely depend on the input which is provided. Your input can decide which part of code need to rebuild and produce constant output.
![Alt text](./chainedbuild.png?raw=true "Chained Build")
2) Easy to integrate with Docker and Kubernetes. If you have monorepo and multiple micro services, then It can build each container and host it for test environment. Further it can provide incremental build and perfrom deployment by using any orchastration tools like AWS and Kubernetes.
![Alt text](./flow-bazel.png?raw=true "Chained Build")
