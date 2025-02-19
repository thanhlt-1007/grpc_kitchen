# grpc_kitchen

- Complete Golang and gRPC Microservices (Project Course)

- Reference: https://www.youtube.com/watch?v=ea_4Ug5WWYE

## gvm

```sh
gvm install go1.24.0
gvm use go1.24.0
```

## go get

```sh
go get ./...
```

## gofumpt

- Install

```sh
go install mvdan.cc/gofumpt@latest
```

- Run

```sh
gofumpt -l -w .
```

## golangci-lint

- Install

```sh
go install github.com/golangci/golangci-lint/cmd/golangci-lint@v1.63.4
```

- Run

```sh
golangci-lint run
```

## protoc

```sh
sudo apt install -y protobuf-compiler
protoc --version # libprotoc 29.3
```

## protoc-gen-go

```sh
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.36.5
protoc-gen-go --version # protoc-gen-go v1.36.5
```

## protoc-gen-go-grpc

```sh
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.5.1
protoc-gen-go-grpc --version # protoc-gen-go-grpc 1.5.1
```

# Layouts
```
|___protobuf
|   |___orders.proto
|       |___message Order
|       |___message GetOrdersRequest
|       |___message GetOrdersResponse
|       |___message CreateOrderRequest
|       |___message CreateOrderResponse
|       |___service OrderService
|           |___CreateOrder
|___services
    |___common
        |___genproto
            |___orders
                |___orders_grpc.pb.go
                |___orders.pb.go
```

