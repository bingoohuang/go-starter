# go-starter

<del>build a starter project for golang, including log, config, ctl, [statiq](https://github.com/bingoohuang/statiq) and etc.</del>

## functions

1. [viper]() 聚合配置使用
1. [logrus](https://github.com/spf13/viper) 日志使用
1. res 资源内嵌
1. [gin](https://github.com/gin-gonic/gin) 框架使用
1. pprof 支持

    * `./go-starter --pprof-addr localhost:6060`
    * open `http://localhost:6060/debug/pprof` in explorer
    * or 可视化数据（火焰图），见如下：
    * `curl http://localhost:6060/debug/pprof/heap > heap.prof`
    * `go get -u github.com/google/pprof`
    * `pprof -http=:8080heap.prof`

## build

for release:

1. `./gb.sh` for local
1. `./gb.sh -t linux` for linux version
 
```bash
$ ./gb.sh -h
Usage: ./gb.sh [OPTION]...

  -t target   linux/local, default local
  -u yes/no   enable upx compression if upx is available or not
  -b          binary name, default go-starter
  -h          display help
```

for dev:

1. `go get github.com/bingoohuang/statiq`
1. `./gr.sh`
1. `statiq -src=res`
1. `go fmt ./...;sh gb.sh`

## start

run `./go-starter -o=false -u`.

