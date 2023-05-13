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

## lifcycle
make build: Builds the static website files using Hugo. make serve: Runs a local development server to preview the website. make clean: Cleans the built website files and cache. make help: Show help for all command. make deploy: Deploys the website to the production server or platform. For additional commands and options, refer to the Makefile in the repository.

Source Code Comments The source code of the Awesome Inc. website contains comments to provide clarity and guidance. Here are some important comments to note:

In config.toml, modify the configuration options such as site title, description, and navigation menu. Content files are located in the content/ directory. Each content page or blog post has a YAML front matter section at the top. Layout files are located in the layouts/ directory. Customize the templates according to your design requirements. Static assets like images, CSS, and JavaScript files can be placed in the static/ directory. For more detailed information about the code structure and specific functionalities, please refer to the comments within the source code files.




