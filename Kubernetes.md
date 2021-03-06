# Contributing to Kubernetes
* Sign the CLA: https://github.com/kubernetes/community/blob/master/CLA.md
* Install go
* Find an issue
* Follow this workflow, except fork from VandyFOSS/kubernetes: https://github.com/kubernetes/community/blob/master/contributors/guide/github-workflow.md

```
fork
working_dir=$GOPATH/src/k8s.io
user=github username
mkdir -p $working_dir
cd $working_dir
git clone https://github.com/$user/kubernetes
cd $working_dir/kubernetes

git remote add upstream https://github.com/kubernetes/kubernetes.git
git remote set-url --push upstream no_push
git fetch upstream
git checkout master
git rebase upstream/master
git checkout -b pkg-api-testing
```
