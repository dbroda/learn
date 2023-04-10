dziala jako **firewall**

kontroluje tylko reguly `allow`

moga sie odnosic do innych SG

moga sie odnosic po IP

kontroluja
* protokol
* porty
* ip ranges (v4 v6)
* inbound (do ec2)
* outbound (z ec2)

SG <-- many2many --> ec2

Sa dopisane do regionu/vpc

hint: osobna dla dostepu po ssh

inbound jest DOMYSLNIE **blokowany**

outbound jest DOMYSLNIE **dozwolony**

uzycie innego security group, pozwala na wjazd tym ec2, ktore sa do tego innego podpiete

sftp = ssh + ftp (port 22)
3389 = RDP 
