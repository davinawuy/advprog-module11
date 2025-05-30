# Reflection

### Application logs before vs. after exposing as a Service

Before running the expose for the service it will only show the ports and not any HTTP requests as shown here,

![img1](images/pic1.png)

After exposing the pod and open its URL through the use of the minikube service. Every time a HTTP GET is made it generates a new log line in the Pod stdout results. So for every time the URL is hit it will generate another entry and this increments in the log for every HTTP GET made. As shown here

![img2](images/pic2.png)

### Purpose of -n kube-system vs. no -n

By default, kubectl get pods or kubectl get services uses the default. All objects live in that default namespace, so they appear under a plain kubectl get however if the -n kube-system tells the kubectl to list objects in the kube-system namespace and not the default. This shows the core add-ons and etc. This is why items like hello-node do not show up because they were not created in the system namespace.

![img3](images/pic3.png)

