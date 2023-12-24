# grpc-blog

This is a blog on grpc to see how to use it everywhere

This post 
[StackOverFlow](https://stackoverflow.com/a/63905093/8549431) helped me figure out a lot about how to setup the environment on ubunut 22.04

Lets get started on installing the protobuf-compiler on your local environment.

- APT package manager:
- To install the compiler run:
```bash
apt install protobuf-compiler
```
- To use, run the command:
```bash
protoc
```
Install the old go generator plugin to be used by protoc: ```go get -u google.golang.org/protobuf/cmd/protoc-gen-go``` and ```go install google.golang.org/protobuf/cmd/protoc-gen-go```. 

### IMPORTANT:
> Also, make sure that the installed plugin can be found in $PATH or add it with
```bash
export PATH=$PATH:$(go env GOPATH)/bin
```

To tell that plugin not only to generate the protobuf message type information but also the grcp methods, use a command like ```protoc --go_out=plugins=grpc:my/relative/output/path ./my_file.proto```.

Looks kinda trivial once you've figured that out, but it's quite hard to figure that out if you aren't into that topic and only have scarce information about how the go files generator generator and the grpc extension are supposed to work together.


Without blank lines, this might not look right.
> This is a blockquote
Don't do this!
