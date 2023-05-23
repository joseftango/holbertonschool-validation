build:  ## command that build our website
	go build -o awesome-api
	hugo -d dist/

run:  ## Run the application in background by executing the binary awesome-api
	./awesome-api >./awesome.log 2>&1 &

post:  ## create a post
	hugo new posts/$(POST_NAME).md
	sed -i 's/title: .*/title:"$(POST_TITLE)"/' content/posts/$(POST_NAME).md

stop: ## Stop the application
	pkill awesome-api

clean:  ## cmmand that remove the dist directory
	rm -f awesome-api awesome-api.log coverage-units.out coverage-integrations.out
	rm -rf ./dist

test:  ## test it to ensure that it behaves as expected
	curl http://localhost:9999
	curl http://localhost:9999/health

lint:  ## linter is able to catch such errors
	golangci-lint run ./main.go

unit-tests:	## using Unittest
	go test -v -short -coverprofile=coverage-units.out

integration-tests:	## using Integration-tests
	go test -v -tags=integration -coverprofile=coverage-integrations.out

check: ## Check markdown of all the files
	markdownlint README.md content/posts/
	markdown-link-check README.md content/posts/

validate: ## command to validate the file ./dist/index.html
	make build
	python3 /opt/W3C-Validator/w3c_validator.py dist/index.html

help:  ## list of targets and their usage
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'

