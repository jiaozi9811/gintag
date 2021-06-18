
mkdir protoc  
cd protoc  

wget https://github.com/protocolbuffers/protobuf/releases/download/v3.17.1/protoc-3.17.1-linux-x86_64.zip  

go get -u google.golang.org/protobuf/cmd/protoc-gen-go  
go get -u google.golang.org/grpc/cmd/protoc-gen-go-grpc  
export PATH="$PATH:$(go env GOPATH)/bin":$(pwd)/bin  



protoc --version  
# 运行 protoc -h 命令可以发现内置的只支持以下语言  
protoc -h  


protoc --go_out=. --go_opt=paths=source_relative     --go-grpc_out=. --go-grpc_opt=paths=source_relative user.proto  

## gogo protobuf
