

How to expose a pod ? (Load Balancer)
- Service - it means Load Balancer
* kubectl expose pod --type=NodePort kuard-pod-lp-enabled 
* kubectl get services
* kubectl get nodes -o wide  (take IP address and add the port, you must see the next app running)

<img width="477" alt="Screenshot_1561" src="https://user-images.githubusercontent.com/13994900/86950899-6966af80-c116-11ea-94d0-2af1d16fe93d.png">

