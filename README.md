# GrpcElixir

**TODO: Add description**

Tutorial found on: https://blog.appsignal.com/2020/03/24/how-to-use-grpc-in-elixir.html

## Installation

**TODO**

## Request Examples

```bash

$ grpcurl -plaintext -proto grpc_elixir.proto -d '{"first_name": "Bob", "last_name": "Smith", "age": 40}' localhost:50051 grpc_elixir.User.Create
{
  "id": 1,
  "firstName": "Bob",
  "lastName": "Smith",
  "age": 40
}

$ grpcurl -plaintext -proto grpc_elixir.proto -d '{"id": 1}' localhost:50051 grpc_elixir.User.Get
{
  "firstName": "Bob",
  "lastName": "Smith",
  "age": 40
}

$ grpcurl -plaintext -proto grpc_elixir.proto -d '{"id": 2}' localhost:50051 grpc_elixir.User.Get
ERROR:
  Code: NotFound
  Message: Some requested entity (e.g., file or directory) was not found

```
