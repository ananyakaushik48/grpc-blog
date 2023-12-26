# grpc

In this demonstration we will go over installing and using grpc to build out several examples of services in all known grpc configurations.

[GRPC Docs](https://grpc.io/docs/languages/go/quickstart/#prerequisites)
[Error](https://stackoverflow.com/a/63905093/8549431)

Lets get started on installing the protobuf-compiler on your local environment.
> ***NOTE*** : _you will need to have GO installed for this_
#### APT package manager:
- To install the compiler run
```bash
apt install protobuf-compiler
```
- To test installation
```bash
protoc
```
- Install the old go generator plugin to be used by protoc: 
```bash
go get -u google.golang.org/protobuf/cmd/protoc-gen-go
go install google.golang.org/protobuf/cmd/protoc-gen-go
```

> Important note: make sure that the installed plugin can be found in $PATH or add it with
```bash
export PATH=$PATH:$(go env GOPATH)/bin
```
#### To generate the go code for the proto you can run the following 
```protoc --go_out=plugins=grpc:my/relative/output/path ./my_file.proto```.




