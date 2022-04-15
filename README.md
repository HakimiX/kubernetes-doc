# Kubernetes Documentation

* [Service](#service)
  * [NodePort](#nodeport) 

## Service
### NodePort
![](resources/images/service-nodeport.png)
Service configuration:
```yaml
apiVersion: v1
kind: Service
metadata:
  name: client-node-port
spec:
  type: NodePort
  ports:
    - port: 3050
      targetPort: 3000
      nodePort: 31515
  selector:
    component: web
```
