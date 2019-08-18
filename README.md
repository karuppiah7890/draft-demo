# draft-demo

Below are the steps to try things out locally in minikube. If you have kubernetes cluster remotely, you can jump ahead minikube related steps

1. Install [draft](https://draft.sh)
2. Install [helm](https://helm.sh)
3. Install [minikube](https://github.com/kubernetes/minikube)
4. Install [kubectl](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG-1.15.md#client-binaries)
5. Install [docker](https://docker.com)
6. Have an account in [Docker Hub](https://hub.docker.com)

Except docker, everything can be installed using [gofish](https://gofi.sh) 🐠 😁

```
$ gofish install helm minikube draft
$ minikube start
$ minikube status
$ helm init
$ git clone https://github.com/karuppiah7890/draft-demo
$ cd draft-demo
$ # login to your docker hub account using your credentials
$ docker login
$ draft config set registry docker.io/<your-username>
$ draft up
$ # check if you application pods have come up
$ kubectl get pod
$ # connect to it from local. use the port given by this command
$ draft connect
```
