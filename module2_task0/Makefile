build: ##compile the source code of the application to a binary named awesome-api
	go get -u github.com/gorilla/mux
	go build

run: ##Run the application in background by executing the binary awesome-api, and write logs into a file named awesome.log
	./awesome-api >./awesome.log 2>&1 &

stop: ##Stop the application with the command kill XXXXX where XXXXX is the Process ID of the application
	kill  $$(pgrep -f "awesome-api")

PHONY: clean
clean: ##Delete the binary awesome-api and the log file awesome-api.log
	rm -rf ./awesome-api ./awesome.log

test: ##ensure that it behaves as expected
	curl http://localhost:9999 http://localhost:9999/health

help: ##provee informacion de cada uno de los comandos de Makefile
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'

