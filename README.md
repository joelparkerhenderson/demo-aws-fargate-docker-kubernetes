# Demo AWS Fargate with Docker and Kubernetes


## macOS

Install Docker:

```sh
$ brew install docker docker-machine
$ brew cask install virtualbox
$ docker-machine create --driver virtualbox default
$ docker-machine env default
$ eval "$(docker-machine env default)"
$ docker run hello-world
$ docker-machine stop default
```

Follow: https://docs.docker.com/get-started/


### Kube pod

Create:

```sh
$ kubectl apply -f pod.yaml
pod/demo created
```

Verify:

```sh
$ kubectl get pods
NAME   READY   STATUS    RESTARTS   AGE
demo   1/1     Running   0          81s
```

Look at logs:

```sh
$ kubectl logs demo
PING 8.8.8.8 (8.8.8.8): 56 data bytes
```

Delete:

```sh
$ kubectl delete -f pod.yaml
pod "demo" deleted
```

## Credits

* [A complete one-by-one guide to install Docker on your Mac OS using Homebrew](https://medium.com/@yutafujii_59175/a-complete-one-by-one-guide-to-install-docker-on-your-mac-os-using-homebrew-e818eb4cfc3)
