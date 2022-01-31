# Tarea 0: Crear una aplicación con Make
Let's start with a simple HTTP web server written in the [Golang](https://go.dev/)  language.

This HTTP webserver is expected to listen to incoming HTTP requests on localhost:9999:

If a request hits the path / (e.g. http://localhost:9999/ or http://localhost:9999) then you expect a 404 Not Found (the homepage is not implemented in this task)
If a request hits the path /health (e.g. http://localhost:9999/health) then you expect the server to answer ALIVE if it is up and running

## Project Life-cycle
The life-cycle of this project is the following:
- "Build": compile the source code of the application to a binary named awesome-api (the name awesome-api comes from the command go mod init github.com/<your github handle>/awesome-api) with the command go build.

- "Run": Run the application in background by executing the binary awesome-api, and write logs into a file named awesome.log with the command ./awesome-api >./awesome.log 2>&1 &.

- "Stop": Stop the application with the command kill XXXXX where XXXXX is the Process ID of the application. For instance: kill "$(pgrep awesome-api)".

- "Clean": Delete the binary awesome-api and the log file awesome-api.log

- "Test": You want to test it to ensure that it behaves as expected. With the application started, you may want to use the command line curl 
