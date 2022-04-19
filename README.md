# kung

Kung of Kubernetes

## install

```bash
git clone github.com/matti/kung
ln -s $(pwd)/kung/kung /usr/local/bin
```

requires yq, envsubst, kubectl

## usage

merge all files in "example/" root

```bash
kung merge example | DOMAIN=example.com kung eval | kung apply --prune mynamespace test
```

merge only subpath "example/web/" with root "example/"

```
kung merge example web
```
