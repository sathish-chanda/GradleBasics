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

### Plugins
- Reusable common functionality
- Plugins can be applied to gradle configurations
- Extend gradle capabilities
  - Add new configuration model : plugins { id('com.gradle.upload') }
  - Initialize configuration : testResultsConfig { server = 'https://...' }
  - Add new tasks : gradle testResultsConfig
- Types
  - core : java,java-library,application
    - Shipped with gradle distribution
  - community
    - Downloaded from plugin repository
    - Developed by developers in the community
    - Have to specify the version
  - Local
    - Common functionality specific to the project developed by you.
    - Implemented locally.

### Tasks
- INPUTS -> ACTION -> OUTPUTS
- Basis unit of work in Gradle
  - Compile
  - Test
  - Generate Docs
- Tasks belong to projects
  - Different projects or subproject can have different tasks because subprojects can have different plugins.
- Ways to run
  - Using terminals - gradle taskName
  - Using Gradle Tab on the right of the IDE - choose the task and click run!
  
### plugins 
- Plugins will give add more functionality by adding new tasks. // id("org.gradle.hello-world")
- Do a good research about the plugin before using it. Only safe plugins should be added.
- After adding the plugin
- Check for the newly added tasks. // app:helloWorld

### Dependency Management
- libraries needed by a gradle project.
- Types
  - Modules :can change overtime. :can have many versions.
  - Other gradle projects
  - Local files
- Dependencies will be downloaded from the trusted repositories
- Command *gradle app:dependencies* will display not only dependencies from build.gradle, but it also displays the transitive dependencies as well. which we can check the pom.xml file in dependency plugin on the site.
- Bucket Dependency :Direct dependencies you define.
- Resolved Dependency :Also include transitive dependencies.

### Most common dependency configuration
- testImplementation :Required to compile and run tests, eg. junit
- runtimeOnly :Required when running application, eg. specific logging library.
- implementation :internally used
- api :public facing specification























