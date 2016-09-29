ego (extended Go)
------

(EXPERIMENT EXPERIMENT EXPERIMENT THIS IS WIP AND DOESN'T EXIST YET)

`ego` is a Go _distribution_ that exactly tracks upstream Go, uses all of the
tooling and standard releases of Go, but provides a stable, extended standard
library, perfect for building large scale applications that need a bit more than
what is in the standard library, while keeping the same API stability and
compatibility assurances.

This is heavily inspired by the (Rust Platform)[https://aturon.github.io/blog/2016/07/27/rust-platform/]

### Extensions (planned)

```
database/
    sql/
        ext/ (from github.com/jmoiron/sqlx)
        postgres/ (from github.com/lib/pq)
        mysql/ (from https://github.com/go-sql-driver/mysql/)
        sqlite3/ (from github.com/mattn/sqlite3)

net/
    http/
        mux/ (from github.com/julienschmidt/httprouter)

os/
    fs/ (modified from github.com/spf13/afero, virtual FS package)

logkit/ (modified from github.com/go-kit/kit/log)
```

### Installation

The only change required to use `ego` is to run -

```
go get -u github.com/fortytw2/ego && ego install latest
```

Ego installs itself into your $GOPATH, working seamlessly and transparently with
your existing Go workflow.

To remove `ego`, simply run `ego uninstall`.

To check which version of `ego` you're running, simply run `ego version`

### LICENSE

The `ego` tool and scripts surrounding it are licensed under terms of the Unlicense,
present in `LICENSE`

External libraries that are part of `ego`
