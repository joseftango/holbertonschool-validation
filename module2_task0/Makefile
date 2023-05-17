build:  ## command that build our website
	hugo
	go build -o awesome-api

run:  ## Run the application in background by executing the binary awesome-api
	./awesome-api >./awesome.log 2>&1 &

stop: ## Stop the application
	pkill awesome-api

clean:  ## cmmand that remove the dist directory
	pkill awesome-api
	rm -rf dist
	rm -f awesome-api awesome.log

test:  ## test it to ensure that it behaves as expected
	curl http://localhost:9999
	curl http://localhost:9999/health

post:  ## command that create a new post with two env variables
	hugo new posts/$(POST_NAME).md
	sed -i 's/title: .*/title:"$(POST_TITLE)"/' content/posts/$(POST_NAME).md

help:  ## list of targets and their usage
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'
