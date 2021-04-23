---
layout: post
title: Install GoLang using HomeBrew in MacOS Sierra 10.12
---

This is the easiest way to install Golang in your machine is OSX instead of using default manual installation. I am recomended using homebrew for MacOS.

![Hello Golang]({{ site.baseurl }}/assets/images/ss_golang.png)

## Setup Go Using Brew

{% highlight bash linenos %}
$ brew install go
==> Downloading https://downloads.sf.net/project/machomebrew/Bottles/go-1.7.3.sierra.bottle.ta
######################################################################## 100.0%
==> Pouring go-1.7.3.sierra.bottle.tar.gz
==> Caveats
As of go 1.2, a valid GOPATH is required to use the `go get` command:
  http://golang.org/doc/code.html#GOPATH

`go vet` and `go doc` are now part of the go.tools sub repo:
  http://golang.org/doc/go1.2#go_tools_godoc

To get `go vet` and `go doc` run:
  go get golang.org/x/tools/cmd/vet
  go get golang.org/x/tools/cmd/godoc

You may wish to add the GOROOT-based install location to your PATH:
  export PATH=$PATH:/usr/local/opt/go/libexec/bin
==> Summary
?  /usr/local/Cellar/go/1.4: 4557 files, 134M
{% endhighlight %}

if you get error like failed with exit-2 or something like that, you must update/upgrade first, because I had those issue when installing on my machine using legacy homebrew, you can try with :

```
$ brew upgrade
```
or
```
$ brew update
```

## Set Path for Go

If all process finish, just add PATH to your .bashrc or .zshrc if you are using ohmyzsh :

{% highlight bash linenos %}
# .zshrc
# go
export GOROOT=/usr/local/opt/go/libexec
export GOPATH=$HOME/.go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
{% endhighlight %}

## Run Test with Hello World!

To test, lets try with helloworld.go :

{% highlight bash linenos %}
~/projectfolder
$ vi helloworld.go
{% endhighlight %}

{% highlight go linenos %}
// helloworld.go
package main
import "fmt"

func main() {
  fmt.Printf("Hello, world!")
}
{% endhighlight %}

{% highlight bash linenos %}
~/projectfolder
▶ go run helloworld.go
Hello, world!%
{% endhighlight %}

All passed and done. Happy coding!