build:  ## command that build our website
	hugo
clean:  ## cmmand that remove the dist directory
	rm -rf dist
post:  ## command that create a new post with two env variables
	hugo new posts/$(POST_NAME).md
	sed -i 's/title: .*/title:"$(POST_TITLE)"/' content/posts/$(POST_NAME).md
help:  ## list of targets and their usage
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'
