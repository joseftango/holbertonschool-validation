build:  ## command that build our website
	go build -o awesome-api

run:  ## Run the application in background by executing the binary awesome-api
	./awesome-api >./awesome.log 2>&1 &

stop: ## Stop the application
	pkill awesome-api

clean:  ## cmmand that remove the dist directory
	pkill awesome-api
	rm -f awesome-api awesome-api.log

test:  ## test it to ensure that it behaves as expected
	curl http://localhost:9999
	curl http://localhost:9999/health

help:  ## list of targets and their usage
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'

lint:  ## linter is able to catch such errors
	golangci-lint run ./main.go

unit-tests:	## using Unittest
	go test -v -short -coverprofile=coverage-units.out

integration-tests:	## using Integration-tests
	go test -v -tags=integration -coverprofile=coverage-integrations.out
