## Install

### Install `go`
> **_TIP:_**  
Go 1.15+ is required for building and installing the StaFiHub software.

Install go by following the [official docs](https://go.dev/doc/install).

Remember to set your `$GOPATH`, `$GOBIN`, and `$PATH` environment variables, for example:
```
mkdir -p $HOME/go/bin
echo "export GOPATH=$HOME/go" >> ~/.bashrc
source ~/.bashrc
echo "export GOBIN=$GOPATH/bin" >> ~/.bashrc
source ~/.bashrc
echo "export PATH=$PATH:$GOBIN" >> ~/.bashrc
source ~/.bashrc
```
Verify that go has been installed successfully
```
go version
```

### Install `stafihubd`
After setting up `go` correctly, you should be able to compile and run `stafihubd`

Make sure that your server can access to google.com because our project depends on some libraries provided by google. (If you are not able to access google.com, you can also try to add a proxy: export GOPROXY=https://goproxy.io)
```
git clone https://github.com/stafihub/stafihub
cd stafihub
git checkout <version>
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands. Now check your `stafihubd` version.
```
stafihubd version
```




 