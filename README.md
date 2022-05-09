# kung

Kung of Kubernetes

## install

```bash
git clone github.com/matti/kung
ln -s $(pwd)/kung/kung /usr/local/bin
```

requires yq, envsubst, kubectl

## usage

merge all files in "example/" root, substitute envs and apply removing any previous resources defined with the same app name in the same namespace

```bash
kung merge example | DOMAIN=example.com kung eval | kung apply --prune=yes mynamespace test
```

merge only subpath "example/web/" with root "example/"
```bash
kung merge example web
```

get all revisions for an app
```bash
kung revisions mynamespace test
```

delete a revision
```bash
kung delete mynamespace test 2022-05-09-18-52-03
```

delete all revisions
```bash
kung delete-all mynamespace test
```

delete all revisions except one
```bash
kung prune mynamespace test 2022-05-09-18-52-03
```

get apps deployed in namespace
```bash
kung namespace mynamespace
```

delete all apps deployed in namespace
```bash
kung namespace-delete mynamespace
```

get all apps ever deployed with kung
```bash
kung all
```

delete all apps ever deployed with kung
```bahs
kung all-delete
```