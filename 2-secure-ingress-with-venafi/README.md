[Link](https://cert-manager.io/docs/tutorials/venafi/venafi/)

```
$ eksctl create cluster
2023-08-24 14:18:09 [ℹ]  eksctl version 0.153.0
2023-08-24 14:18:09 [ℹ]  using region us-west-2
2023-08-24 14:18:11 [ℹ]  setting availability zones to [us-west-2c us-west-2d us-west-2b]
2023-08-24 14:18:11 [ℹ]  subnets for us-west-2c - public:192.168.0.0/19 private:192.168.96.0/19
2023-08-24 14:18:11 [ℹ]  subnets for us-west-2d - public:192.168.32.0/19 private:192.168.128.0/19
2023-08-24 14:18:11 [ℹ]  subnets for us-west-2b - public:192.168.64.0/19 private:192.168.160.0/19
2023-08-24 14:18:11 [ℹ]  nodegroup "ng-ee9ab730" will use "" [AmazonLinux2/1.25]
2023-08-24 14:18:11 [ℹ]  using Kubernetes version 1.25
2023-08-24 14:18:11 [ℹ]  creating EKS cluster "extravagant-creature-1692866888" in "us-west-2" region with managed nodes
2023-08-24 14:18:11 [ℹ]  will create 2 separate CloudFormation stacks for cluster itself and the initial managed nodegroup
2023-08-24 14:18:11 [ℹ]  if you encounter any issues, check CloudFormation console or try 'eksctl utils describe-stacks --region=us-west-2 --cluster=extravagant-creature-1692866888'
2023-08-24 14:18:11 [ℹ]  Kubernetes API endpoint access will use default of {publicAccess=true, privateAccess=false} for cluster "extravagant-creature-1692866888" in "us-west-2"
2023-08-24 14:18:11 [ℹ]  CloudWatch logging will not be enabled for cluster "extravagant-creature-1692866888" in "us-west-2"
2023-08-24 14:18:11 [ℹ]  you can enable it with 'eksctl utils update-cluster-logging --enable-types={SPECIFY-YOUR-LOG-TYPES-HERE (e.g. all)} --region=us-west-2 --cluster=extravagant-creature-1692866888'
2023-08-24 14:18:11 [ℹ]  
2 sequential tasks: { create cluster control plane "extravagant-creature-1692866888", 
    2 sequential sub-tasks: { 
        wait for control plane to become ready,
        create managed nodegroup "ng-ee9ab730",
    } 
}
2023-08-24 14:18:11 [ℹ]  building cluster stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:18:14 [ℹ]  deploying stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:18:44 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:19:15 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:20:16 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:21:18 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:22:19 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:23:21 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:24:22 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:25:24 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:26:27 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:27:29 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:28:30 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 14:30:43 [ℹ]  building managed nodegroup stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 14:30:45 [ℹ]  deploying stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 14:30:45 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 14:31:16 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 14:32:02 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 14:34:00 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 14:34:00 [ℹ]  waiting for the control plane to become ready
2023-08-24 14:34:00 [✔]  saved kubeconfig as "/Users/javedalam/.kube/config"
2023-08-24 14:34:00 [ℹ]  no tasks
2023-08-24 14:34:00 [✔]  all EKS cluster resources for "extravagant-creature-1692866888" have been created
2023-08-24 14:34:03 [ℹ]  nodegroup "ng-ee9ab730" has 2 node(s)
2023-08-24 14:34:03 [ℹ]  node "ip-192-168-28-127.us-west-2.compute.internal" is ready
2023-08-24 14:34:03 [ℹ]  node "ip-192-168-56-81.us-west-2.compute.internal" is ready
2023-08-24 14:34:03 [ℹ]  waiting for at least 2 node(s) to become ready in "ng-ee9ab730"
2023-08-24 14:34:03 [ℹ]  nodegroup "ng-ee9ab730" has 2 node(s)
2023-08-24 14:34:03 [ℹ]  node "ip-192-168-28-127.us-west-2.compute.internal" is ready
2023-08-24 14:34:03 [ℹ]  node "ip-192-168-56-81.us-west-2.compute.internal" is ready
2023-08-24 14:34:06 [ℹ]  kubectl command should work with "/Users/javedalam/.kube/config", try 'kubectl get nodes'
2023-08-24 14:34:06 [✔]  EKS cluster "extravagant-creature-1692866888" in "us-west-2" region is ready
```


```
$ kubectl get pods --all-namespaces
NAMESPACE     NAME                       READY   STATUS    RESTARTS   AGE
kube-system   aws-node-g2l4x             1/1     Running   0          34m
kube-system   aws-node-qmrxt             1/1     Running   0          34m
kube-system   coredns-67f8f59c6c-2khq7   1/1     Running   0          42m
kube-system   coredns-67f8f59c6c-d7kfx   1/1     Running   0          42m
kube-system   kube-proxy-5cpc8           1/1     Running   0          34m
kube-system   kube-proxy-q5blx           1/1     Running   0          34m
```


```
$ kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.12.0/cert-manager.yaml
namespace/cert-manager created
customresourcedefinition.apiextensions.k8s.io/certificaterequests.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/certificates.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/challenges.acme.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/clusterissuers.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/issuers.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/orders.acme.cert-manager.io created
serviceaccount/cert-manager-cainjector created
serviceaccount/cert-manager created
serviceaccount/cert-manager-webhook created
configmap/cert-manager-webhook created
clusterrole.rbac.authorization.k8s.io/cert-manager-cainjector created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-issuers created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-clusterissuers created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-certificates created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-orders created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-challenges created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-ingress-shim created
clusterrole.rbac.authorization.k8s.io/cert-manager-view created
clusterrole.rbac.authorization.k8s.io/cert-manager-edit created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-approve:cert-manager-io created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-certificatesigningrequests created
clusterrole.rbac.authorization.k8s.io/cert-manager-webhook:subjectaccessreviews created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-cainjector created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-issuers created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-clusterissuers created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-certificates created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-orders created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-challenges created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-ingress-shim created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-approve:cert-manager-io created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-certificatesigningrequests created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-webhook:subjectaccessreviews created
role.rbac.authorization.k8s.io/cert-manager-cainjector:leaderelection created
role.rbac.authorization.k8s.io/cert-manager:leaderelection created
role.rbac.authorization.k8s.io/cert-manager-webhook:dynamic-serving created
rolebinding.rbac.authorization.k8s.io/cert-manager-cainjector:leaderelection created
rolebinding.rbac.authorization.k8s.io/cert-manager:leaderelection created
rolebinding.rbac.authorization.k8s.io/cert-manager-webhook:dynamic-serving created
service/cert-manager created
service/cert-manager-webhook created
deployment.apps/cert-manager-cainjector created
deployment.apps/cert-manager created
deployment.apps/cert-manager-webhook created
mutatingwebhookconfiguration.admissionregistration.k8s.io/cert-manager-webhook created
```


```
$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/aws/deploy.yaml
namespace/ingress-nginx created
serviceaccount/ingress-nginx created
serviceaccount/ingress-nginx-admission created
role.rbac.authorization.k8s.io/ingress-nginx created
role.rbac.authorization.k8s.io/ingress-nginx-admission created
clusterrole.rbac.authorization.k8s.io/ingress-nginx created
clusterrole.rbac.authorization.k8s.io/ingress-nginx-admission created
rolebinding.rbac.authorization.k8s.io/ingress-nginx created
rolebinding.rbac.authorization.k8s.io/ingress-nginx-admission created
clusterrolebinding.rbac.authorization.k8s.io/ingress-nginx created
clusterrolebinding.rbac.authorization.k8s.io/ingress-nginx-admission created
configmap/ingress-nginx-controller created
service/ingress-nginx-controller created
service/ingress-nginx-controller-admission created
deployment.apps/ingress-nginx-controller created
job.batch/ingress-nginx-admission-create created
job.batch/ingress-nginx-admission-patch created
ingressclass.networking.k8s.io/nginx created
validatingwebhookconfiguration.admissionregistration.k8s.io/ingress-nginx-admission created
```


```
$ kubectl get service -n ingress-nginx
NAME                                 TYPE           CLUSTER-IP      EXTERNAL-IP                                                                     PORT(S)                      AGE
ingress-nginx-controller             LoadBalancer   10.100.42.154   a7cfb185727874a808e8e83ace8e49ef-59e64b00791cb8b9.elb.us-west-2.amazonaws.com   80:30683/TCP,443:31707/TCP   38s
ingress-nginx-controller-admission   ClusterIP      10.100.88.204   <none>                                                                          443/TCP                      38s
```


```
$ curl http://a7cfb185727874a808e8e83ace8e49ef-59e64b00791cb8b9.elb.us-west-2.amazonaws.com/
curl: (6) Could not resolve host: a7cfb185727874a808e8e83ace8e49ef-59e64b00791cb8b9.elb.us-west-2.amazonaws.com
```


```
$ kubectl get namespace
NAME              STATUS   AGE
cert-manager      Active   12m
default           Active   56m
demo              Active   82s
ingress-nginx     Active   4m53s
kube-node-lease   Active   56m
kube-public       Active   56m
kube-system       Active   56m
```


```
$ cat demo-deployment.yaml 
apiVersion: v1
kind: Service
metadata:
  name: hello-kubernetes
  namespace: demo
spec:
  type: ClusterIP
  ports:
  - port: 80
    targetPort: 8080
  selector:
    app: hello-kubernetes
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: hello-kubernetes
  namespace: demo
spec:
  replicas: 2
  selector:
    matchLabels:
      app: hello-kubernetes
  template:
    metadata:
      labels:
        app: hello-kubernetes
    spec:
      containers:
      - name: hello-kubernetes
        image: paulbouwer/hello-kubernetes:1.5
        resources:
          requests:
            cpu: 100m
            memory: 100Mi
        ports:
        - containerPort: 8080
```


```
$ kubectl apply -n demo -f demo-deployment.yaml 
service/hello-kubernetes created
deployment.apps/hello-kubernetes created
```


```
$ kubectl get po,svc -n demo
NAME                                    READY   STATUS    RESTARTS   AGE
pod/hello-kubernetes-5c49fddb59-ngx92   1/1     Running   0          56s
pod/hello-kubernetes-5c49fddb59-xn7qn   1/1     Running   0          56s

NAME                       TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)   AGE
service/hello-kubernetes   ClusterIP   10.100.119.112   <none>        80/TCP    57s
```


```
kubectl create secret generic \
       venafi-tpp-secret \
       --namespace=demo \
       --from-literal=username='javed.alam1303@gmail.com' \
       --from-literal=password=‘Unix__@@123456’
```


```
$ kubectl create secret generic \
>        venafi-tpp-secret \
>        --namespace=demo \
>        --from-literal=username=‘javed.alam1303@gmail.com’ \
>        --from-literal=password=‘Unix’__@@123456

secret/venafi-tpp-secret created
```

# Wrong here need to create the crews here 

```
$ kubectl create secret generic \
>        venafi-tpp-secret \
>        --namespace=demo \
>        --from-literal=username='javed.alam1303@gmail.com' \
>        --from-literal=password=‘Unix__@@123456’
error: failed to create secret secrets "venafi-tpp-secret" already exists
```


```
$ kubectl delete secret venafi-tpp-secret -n demo
secret "venafi-tpp-secret" deleted
```


```
$ kubectl create secret generic \
>        venafi-tpp-secret \
>        --namespace=demo \
>        --from-literal=username='javed.alam1303@gmail.com' \
>        --from-literal=password=‘Unix__@@123456’
secret/venafi-tpp-secret created
```


```
$ kubectl apply -n demo -f venafi-issuer.yaml
Error from server (BadRequest): error when creating "venafi-issuer.yaml": admission webhook "webhook.cert-manager.io" denied the request: illegal base64 data at input byte 0
```


```
$ kubectl delete secret venafi-tpp-secret -n demo
secret "venafi-tpp-secret" deleted
```


```
eksctl delete nodegroup --cluster=<cluster-name> --name=<nodegroup-name>
eksctl delete cluster --name=<cluster-name>

```


```
$ eksctl get nodegroup --cluster extravagant-creature-1692866888
CLUSTER                         NODEGROUP       STATUS  CREATED                 MIN SIZE        MAX SIZE        DESIRED CAPACITY     INSTANCE TYPE   IMAGE ID        ASG NAME                                                TYPE
extravagant-creature-1692866888 ng-ee9ab730     ACTIVE  2023-08-24T09:01:05Z    2               2               2   m5.large AL2_x86_64      eks-ng-ee9ab730-18c51363-49c8-0cc5-da92-20f9a4158397    managed
```


```
$ eksctl delete nodegroup --cluster=extravagant-creature-1692866888 --name=ng-ee9ab730
2023-08-24 16:04:38 [ℹ]  1 nodegroup (ng-ee9ab730) was included (based on the include/exclude rules)
2023-08-24 16:04:38 [ℹ]  will drain 1 nodegroup(s) in cluster "extravagant-creature-1692866888"
2023-08-24 16:04:38 [ℹ]  starting parallel draining, max in-flight of 1
2023-08-24 16:04:41 [ℹ]  cordon node "ip-192-168-28-127.us-west-2.compute.internal"
2023-08-24 16:04:41 [ℹ]  cordon node "ip-192-168-56-81.us-west-2.compute.internal"
2023-08-24 16:05:13 [✔]  drained all nodes: [ip-192-168-28-127.us-west-2.compute.internal ip-192-168-56-81.us-west-2.compute.internal]
2023-08-24 16:05:13 [ℹ]  will delete 1 nodegroups from cluster "extravagant-creature-1692866888"
2023-08-24 16:05:14 [ℹ]  1 task: { 1 task: { delete nodegroup "ng-ee9ab730" [async] } }
2023-08-24 16:05:15 [ℹ]  will delete stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 16:05:15 [ℹ]  will delete 0 nodegroups from auth ConfigMap in cluster "extravagant-creature-1692866888"
2023-08-24 16:05:15 [✔]  deleted 1 nodegroup(s) from cluster "extravagant-creature-1692866888"
```

```
$ eksctl delete cluster --name=extravagant-creature-1692866888
2023-08-24 16:06:17 [ℹ]  deleting EKS cluster "extravagant-creature-1692866888"
2023-08-24 16:06:21 [ℹ]  will drain 0 unmanaged nodegroup(s) in cluster "extravagant-creature-1692866888"
2023-08-24 16:06:21 [ℹ]  starting parallel draining, max in-flight of 1
2023-08-24 16:06:23 [ℹ]  deleted 0 Fargate profile(s)
2023-08-24 16:06:25 [✔]  kubeconfig has been updated
2023-08-24 16:06:25 [ℹ]  cleaning up AWS load balancers created by Kubernetes objects of Kind Service or Ingress
2023-08-24 16:06:35 [ℹ]  
2 sequential tasks: { delete nodegroup "ng-ee9ab730", delete cluster control plane "extravagant-creature-1692866888" [async] 
}
2023-08-24 16:06:35 [ℹ]  will delete stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 16:06:35 [ℹ]  waiting for stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730" to get deleted
2023-08-24 16:06:35 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 16:07:06 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 16:08:07 [ℹ]  waiting for CloudFormation stack "eksctl-extravagant-creature-1692866888-nodegroup-ng-ee9ab730"
2023-08-24 16:08:08 [ℹ]  will delete stack "eksctl-extravagant-creature-1692866888-cluster"
2023-08-24 16:08:09 [✔]  all cluster resources were deleted
```