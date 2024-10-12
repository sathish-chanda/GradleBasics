# GradleBasics

### Notes
- Gradle is a build automation tool.
- It is open source build automation tool
- Manages the project dependencies (donwloading and adding the dependencies including the transitive dependencies) from the repositories, These dependencies will be consumed in the code.
- Automates the task
  - Compiling
  - Testing
  - publishing
- Plugin framework
- large and active community

### Requirements 
- Java
- Download latest gradle binary from the gradle.org

### commands
- mkdir lab
- cd lab
- gradle --version
- gradle help
- gradle init
- gradle tasks - displays the list of tasks
- gradle tasks --all - displays all the tasks
- gradle app:run 

### About Gradle Wrapper
- Gradle wrapper contains gradle binary version which needs to be used in the project. 
- When we run any task first it will get/download the gradle version specified in the gradle-wrapper.properties file. Then the task will be executed by it.
- This will be checked into the version control. so, that other developers will also have a consistent behavior of the project. Otherwise some functionality which is used in the project from the gradle might be deprecated in the new version, this make the project builds to fails.
