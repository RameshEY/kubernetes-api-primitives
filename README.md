Kubernetes has a collection of API that defines the objects & services that you can interact with in kubernetes. API are versioned (v1 / v1alpha1 / v1beta1 etc). These verisons have atleast one GA version and rest are usually in alpha or beta. Note that as and when kubernetes brings out latest versions of the software, these versions might change or get deprecated. 

Kubernetes API are RESTful and kubernetes provides the following ways to consume these APIs 

1. kubectl CLI 

2. dashboard 

3. Programmatic interface (curl / java etc)

In order to secure / authorize API access kubernetes uses a role based access control (RBAC) to ensure only authorized personnels can make these API calls. There are multiple ways of authentications like SAML, OIDC, username/password, tokens and certificates. Certificates are the most widely used method to provide RBAC to kubernetes API. 


* Get all API resources

`kubectl api-resources`

* Get all kube-api versions 

` kubectl api-versions`

* Verify that you can consume an API 

```
kubectl auth can-i create pods
kubectl auth can-i create deployments
kubectl auth can-i create pods --as otheruser
```

Try running - `kubectl auth can-i create deployment -n asdsa` and see what answer you get
