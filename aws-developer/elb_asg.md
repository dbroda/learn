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

**Application Load Balancer**

* Layer 7 - http
* http/2 + ws
* rounting
  *  url path
  *  hostname
  *  headers, query strings
* dobre dla microserwisow i kontenerow
* 1 ALB dla calej aplikacji
* target groups: 
  *  lambda, ec2, ec2 tasks, private IP addresses
  * takze do wielu target groups (health cehck na poziomie target groups)
  
naglowki
* X-Forwarded-For
* X-Forwarded-Port
* X-Forwarded-Proto

**Network Load Balancer**

Layer 4 - tcp/udp

* wysoka wydajnosc
* mniejsze latency (~100ms)
* 1 statyczne IP na AZ
* nie ma go w FreeTier

Target Groups:
* EC2 instances
* private IP Addresses
* ALB
* Health checks: TCP, http, https

Problem z brakiem dostepu moze wynikac z tego ze security group na ec2 nie wpuszcza ruchu z LB

**Gateway Load Balancer**

Inspekcja trafficu wchodzacego o apki
* firewalle
* detekcja wlaman
* manipulacja payloada
* 3rd party security VirtualAppliances
  * traffic: User -> GLB -> VA -> GLB -> Application 
* Layer 3 - IP
* Transparent Network Gateway (caly ruch idzie przez gate) + Load Balancer
* Uzywa protokolu GENEVE : 6081

Target Groups:
* EC2 instances
* private IP Addresses

**ELB Sticky Sessions**

* dziala z ALB i NLB
* Cookies:
  * App-based:
    * Custom: tworzone przez apke
    * Application Cookie: tworzone przez LB




