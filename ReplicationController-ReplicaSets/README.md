* Replication Controller 
* Replica Set
* Horizontal Autoscalling
* Vertical Autoscalling 

 CLI Horizontal Autoscalling command 
  -  kubectl autoscale rs kuard-rs-test --name=kuard-rs-test-hpa --min=1 --max=5 --cpu-percent=50 
  - kubectl get pod    (memory / cpu ) CAdvicer is responsabile for memory, cpu
  
  
