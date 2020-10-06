# NGINX Ingress Controller


```sh
$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.40.1/deploy/static/provider/aws/deploy.yaml
```

```sh
$ wget https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.40.1/deploy/static/provider/aws/deploy-tls-termination.yaml
```

**Edit the file and change:**

  1. VPC CIDR in use for the Kubernetes cluster:

  proxy-real-ip-cidr: XXX.XXX.XXX/XX


  2. AWS Certificate Manager (ACM) ID

  arn:aws:acm:us-west-2:XXXXXXXX:certificate/XXXXXX-XXXXXXX-XXXXXXX-XXXXXXXX


```sh
$ kubectl apply -f deploy-tls-termination.yaml
```


## References

[Expose NGINX Behind Network Load Balancer](https://kubernetes.github.io/ingress-nginx/deploy/#aws)

[Expose NGINX Behind Network Load Balancer - TLS Termination Template](https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.40.1/deploy/static/provider/aws/deploy-tls-termination.yaml)


