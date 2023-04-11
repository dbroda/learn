**ELB Elastic Load Balancer**

* Zarzadzany przez AWS
* Zintegrowany z uslugami AWS
* Uzywa health checkow do EC2 (HTTP:4567 /health)

Rodzaje:
* CLB - Classic load balancer (v1) - deprecated
* ALB - Application load balancer (v2) http/s, ws
* NLB - Network Load Balancer (v2) tcp, tls, udp
* GWLB - Gateway Load Balancer
  *  Network Layer 3 - IP Protocol

Moga byc public/private 

SecurityGroups (SG)

Users <-SG-> LB <-SG-> EC2
