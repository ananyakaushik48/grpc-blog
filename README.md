# grpc-blog
This is a blog on grpc to see how to use it everywhere
For all who aren't much into the topic (like me) and still have trouble to figure out a working solution, here's a step-by-step approach:

```apt install protobuf-compiler``` installs the compiler under ```apt install protobuf-compiler```, available via ```protoc``` from then.
Install the old go generator plugin to be used by protoc: ```go get -u google.golang.org/protobuf/cmd/protoc-gen-go``` and ```go install google.golang.org/protobuf/cmd/protoc-gen-go```. 

### note:
- Also, make sure that the installed plugin can be found in $PATH or add it with ```export PATH=$PATH:$(go env GOPATH)/bin``` if needed.

To tell that plugin not only to generate the protobuf message type information but also the grcp methods, use a command like protoc --go_out=plugins=grpc:my/relative/output/path ./my_file.proto.
Looks kinda trivial once you've figured that out, but it's quite hard to figure that out if you aren't into that topic and only have scarce information about how the go files generator generator and the grcp extension are supposed to work together.
