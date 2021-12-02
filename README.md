# etcd-cluster-docker

## Getting Started

1. Start docker

``` c
docker-compose up
```

2. Connet with go
lib
``` c
go get go.etcd.io/etcd/clientv3
```
``` c
config := clientv3.Config{
	Endpoints: []string{"localhost:23790", "localhost:23791", "localhost:23782"},
}
cli, err := clientv3.New(config)
if err != nil {
	panic(err)
}
```
