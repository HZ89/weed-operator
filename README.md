# SeaweedFS Operator

## Installation

## Development

Follow the instructions in https://sdk.operatorframework.io/docs/building-operators/golang/quickstart/

```
$ git clone https://github.com/seaweedfs/seaweedfs-operator
$ cd seaweedfs-operator

# register the CRD with the Kubernetes
$ make install

# run the operator locally outside the Kubernetes cluster
$ make run ENABLE_WEBHOOKS=false 

# From another terminal in the same directory
$ kubectl apply -f config/samples/seaweed_v1_seaweed.yaml

```

## Create API and Controller
Here are the commands used to create customer resource definition (CRD)
```
operator-sdk create api --group seaweed --version v1 --kind Master --resource=true --controller=true
```