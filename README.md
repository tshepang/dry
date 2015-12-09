# dry
[![License MIT](https://img.shields.io/badge/license-MIT-lightgrey.svg?style=flat)](https://github.com/moncho/dry#license-mit)
[![wercker status](https://app.wercker.com/status/66c3ab71a46c0c8841f34a526fc23189/s/master "wercker status")](https://app.wercker.com/project/bykey/66c3ab71a46c0c8841f34a526fc23189)
[![Go Report Card](http://goreportcard.com/badge/moncho/dry)](http://goreportcard.com/report/moncho/dry)


**dry** is an interactive console application that connects to a Docker host, shows the list of containers and offers a few Docker commands to run on them.

[![asciicast](https://asciinema.org/a/31436.png)](https://asciinema.org/a/31436)

It can be used as alternative to the following commands of the official Docker cli:

* inspect
* kill
* logs
* ps
* rm
* stats
* start
* stop

### Installation

#### Binaries

- **darwin** [386](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-darwin-386) / [amd64](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-darwin-amd64)
- **freebsd** [386](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-freebsd-386) / [amd64](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-freebsd-amd64)
- **linux** [386](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-linux-386) / [amd64](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-linux-amd64)
- **windows** [386](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-windows-386) / [amd64](https://github.com/moncho/dry/releases/download/v0.1.0-beta/dry-windows-amd64)

#### Go

Make sure that $GOPATH exists.

```
$ go get github.com/moncho/dry
$ cd $GOPATH/src/github.com/moncho/dry
$ make install
```

### Usage

Open a console, type ```dry```. It will connect to whatever host defined in **$DOCKER_HOST** environment variable.

```dry -p``` launches dry with [pprof](https://golang.org/pkg/net/http/pprof/) package active.

### Debug

Debugging can be done using [godebug](https://github.com/mailgun/godebug).

Install it, then insert a breakpoint anywhere you want:
```
_ = "breakpoint"
```
Then, run the debugger:
```
godebug run -instrument github.com/moncho/dry,github.com/moncho/dry/app,github.com/moncho/dry/docker,github.com/moncho/dry/ui,github.com/moncho/dry/appui main.go
```
### Contributing
All contributions are welcome.

* Fork the project.
* Make changes on a topic branch.
* Pull request.

## Copyright and license

Code released under the MIT license. See
[LICENSE](https://github.com/moncho/dry/blob/master/LICENSE) for the full license text.

## Credits

Built on top of:
* [termbox](https://github.com/nsf/termbox-go)
* [go-dockerclient](https://github.com/fsouza/go-dockerclient)

Also reused some code and ideas from the [Docker project](https://github.com/docker/docker) and [mop](https://github.com/michaeldv/mop).
