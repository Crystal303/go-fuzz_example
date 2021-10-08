## go-fuzz example

### cmd

```shell
$ go get -u github.com/dvyukov/go-fuzz/go-fuzz@latest github.com/dvyukov/go-fuzz/go-fuzz-build@latest
$ go install github.com/dvyukov/go-fuzz/go-fuzz-build@latest
```

```shell
$ go-fuzz-build {fullpath}/go-fuzz_example
$ mkdir -p wordir/corpus
$ go-fuzz -bin=go_fuzz_example-fuzz.zip -workdir=workdir -procs=8
```

### result
```text
2021/10/08 16:26:55 workers: 8, corpus: 59 (0s ago), crashers: 0, restarts: 1/8223, execs: 641449 (42760/sec), cover: 236, uptime: 15s
2021/10/08 16:26:58 workers: 8, corpus: 64 (0s ago), crashers: 0, restarts: 1/8759, execs: 867230 (48177/sec), cover: 237, uptime: 18s
2021/10/08 16:27:01 workers: 8, corpus: 66 (0s ago), crashers: 0, restarts: 1/9201, execs: 1094919 (52136/sec), cover: 238, uptime: 21s
2021/10/08 16:27:04 workers: 8, corpus: 67 (0s ago), crashers: 0, restarts: 1/9231, execs: 1320151 (55004/sec), cover: 238, uptime: 24s
```
