<h1><b> Python grpc </b></h1>

With gRPC we can define our service once in a .proto file and generate clients and servers in any of gRPC’s supported languages, which in turn can be run in environments ranging from servers inside a large data center to your own tablet — all the complexity of communication between different languages and environments is handled for you by gRPC.

## Protocol buffers
Protocol buffers provide a language-neutral, platform-neutral, extensible mechanism for serializing structured data in a forward-compatible and backward-compatible way. It’s like JSON, except it's smaller and faster, and it generates native language bindings.
Protocol buffers are a combination of the definition language (created in .proto files), the code that the proto compiler generates to interface with data, language-specific runtime libraries, and the serialization format for data that is written to a file (or sent across a network connection).

## Defining the gRPC service
To define a service, you specify a named service in your `.proto` file:
```proto
service RouteGuide {
   // (Method definitions)
}
```
Then you define `rpc` methods inside your service definition, specifying their request and response types. gRPC lets you define four kinds of service method, all of which are used in the `RouteGuide` service:
