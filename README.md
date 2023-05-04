# Demo

```
$ go version
go version go1.20.4 darwin/arm64

$ go test tailscale.com/net/dns/resolver
# github.com/miekg/dns
embedding interface element ~[]string requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/msg.go:549:12: type parameter requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/msg.go:549:14: embedding interface element ~[]byte | ~string requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/msg.go:553:16: type parameter requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/types.go:1605:17: type parameter requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/types.go:1605:19: predeclared any requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/types.go:1605:26: embedding interface element ~[]E requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/clientconfig.go:71:25: implicit function instantiation requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/defaults.go:211:12: implicit function instantiation requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/edns.go:523:63: implicit function instantiation requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/edns.go:523:63: too many errors
FAIL	tailscale.com/net/dns/resolver [build failed]
FAIL

$ go get github.com/miekg/dns@v1.1.54

$ go test tailscale.com/net/dns/resolver
ok  	tailscale.com/net/dns/resolver	0.160s

$ go mod tidy

$ go test tailscale.com/net/dns/resolver
# github.com/miekg/dns
embedding interface element ~[]string requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/msg.go:549:12: type parameter requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/msg.go:549:14: embedding interface element ~[]byte | ~string requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/msg.go:553:16: type parameter requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/types.go:1605:17: type parameter requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/types.go:1605:19: predeclared any requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/types.go:1605:26: embedding interface element ~[]E requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/clientconfig.go:71:25: implicit function instantiation requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/defaults.go:211:12: implicit function instantiation requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/edns.go:523:63: implicit function instantiation requires go1.18 or later (-lang was set to go1.16; check go.mod)
../go/pkg/mod/github.com/miekg/dns@v1.1.54/edns.go:523:63: too many errors
FAIL	tailscale.com/net/dns/resolver [build failed]
FAIL
```

