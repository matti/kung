# kung

Kung of Kubernetes

## install

```bash
git clone github.com/matti/kung
ln -s $(pwd)/kung/kung /usr/local/bin
```

requires yq, envsubst, kubectl (asdf install, brew install )

## usage

```bash
kung merge example | DOMAIN=example.com kung apply --prune mynamespace test
```
