## Knowledge required.

https://kubernetes.io/docs/concepts/configuration/assign-pod-node/#nodeselector

### Steps:

- Label the one of the node as `disk=fastssd` 

```command
kubectl label nodes node2 disk=fastssd
```

- Deploy the pod.

```command
kubectl apply -f code/pod.yaml
```

- Get the list of the pod.

```
kubectl get pod
NAME                  READY     STATUS             RESTARTS   AGE
nginx-ns              0/1       Pending            0          7s
```

`Problem: Find out why pod is in pending state and find out. Fix it!!`

Skills Needed:

- Pod Spec
- Node Selector
- Node labels
