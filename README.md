# hello_grpc

How to start the sever
```
cd cmd/server
go run main.go
```

Checking list of services
```
grpcurl -plaintext localhost:8088 list
```

Checking list of methods for any service
```
grpcurl -plaintext localhost:8088 list myapp.GreetingService
```

Call method
```
grpcurl -plaintext -d '{"name": "Alice"}' localhost:8088 myapp.GreetingService.Hello
```