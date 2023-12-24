# grpc

In this demonstration we will go over installing and using grpc to build out several examples of services in all known grpc configurations.

[REF](https://stackoverflow.com/a/63905093/8549431)

Lets get started on installing the protobuf-compiler on your local environment.
> #### NOTE: 
>> you will need GO installed for this
#### APT package manager:
- To install the compiler run
```bash
apt install protobuf-compiler
```
- To test installation
```bash
protoc
```
Install the old go generator plugin to be used by protoc: ```go get -u google.golang.org/protobuf/cmd/protoc-gen-go``` and ```go install google.golang.org/protobuf/cmd/protoc-gen-go```. 

> Important note: make sure that the installed plugin can be found in $PATH or add it with
```bash
export PATH=$PATH:$(go env GOPATH)/bin
```

```protoc --go_out=plugins=grpc:my/relative/output/path ./my_file.proto```.

Looks kinda trivial once you've figured that out, but it's quite hard to figure that out if you aren't into that topic and only have scarce information about how the go files generator generator and the grpc extension are supposed to work together.


Try to put a blank line before...

> This is a blockquote

...and after a blockquote.
