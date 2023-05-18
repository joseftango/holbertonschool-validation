## Prerequisites
You should have a basic knowledge of the following concepts:

Shell terminal basics, using command lines:

Navigating in a Unix file-system
Understanding how stdin/stdout redirection and piping
Showing and searching the content of a text files
Defining and using Environment Variables
Adding command lines to your terminal using the apt-get package manager and/or with the PATH variable
Writing and executing a shell script
Git with the command line (and also a graphical interface)

Retrieving or creating a repository
Manipulating changes locally with Git’s 3 steps process (workspace, staging, history)
Distributing changes history with remotes repositories
Make/Makefile usage:

Executing tasks through make targets
Default target and PHONY target
Makefile’s variables and macro syntax

## Lifecycle
* "build": compile the source code of the application to a binary named awesome-api
* "clean": Stop the application. Delete the binary awesome-api and the log file awesome-api.log.
* "post": Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.
* "help": Provides help about the commands.
* "test": You want to test it to ensure that it behaves as expected
* "run": Run the application in background by executing the binary awesome-api
* "stop": Stop the application with the command kill XXXXX where XXXXX is the Process ID of the application
* "lint": linter is able to catch such errors
* "unit-tests": should be implemented and should be executed
