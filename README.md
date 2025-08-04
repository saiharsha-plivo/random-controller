Sample Input 


---
apiVersion: k8s.io/v1beta1
kind: RandomItem
metadata:
  name: test
spec:
  item: joke
  
---
apiVersion: k8s.io/v1beta1
kind: RandomItem
metadata:
  annotations:
    kubectl.kubernetes.io/last-applied-configuration: >
      {"apiVersion":"k8s.io/v1beta1","kind":"RandomItem","metadata":{"annotations":{},"name":"test","namespace":"default"},"spec":{"item":"joke"}}
  creationTimestamp: '2025-08-02T10:12:26Z'
  generation: 1
  name: test
  namespace: default
  resourceVersion: '7511562'
  uid: 3a62d149-a935-41b4-8c1a-fc3859aec127
  selfLink: /apis/k8s.io/v1beta1/namespaces/default/randomitems/test
status:
  item: joke
  value: >-
    Have you heard about that hot Thai lounge singer? Yeah. They call him *Frank
    Sriracha.*
spec:
  item: joke



---
TO Test the controller : apply the cr and crd in artifacts/examples 

To run the controller locally go run . --kubeconfig <Path to kubeconfig>