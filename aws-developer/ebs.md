Elastic Block Store

* Network drive, wiec latency
* moga persystowac dae nawet jak ec2 jest terminowana
* ec2 <-- one2one --> ebs
* ec2 <-- one2many "multi-attach" --> some ebs | 1 ec2 moze miec wiele swoich ebs
* ebs moze byc unattached
* spiete do AZ
* "network USB drive"
* latwo przypinalne ale w ramach etgo samego az
* dla miedzy az - trzeba snapshota
* ma capacity (GB i IOPS) in advance
* mozna zwiekszac capacity
* placi sie za capacity
* w ec2 root vol by defaut jest usuwany (by ec2 termination), a kolejne juz nie, ale mozna to zmieniac


Snapshoty
* mozna kopiowac miedzy AZ i Regionami

ebs -> snapshot -> restore -> ebs

* Snapshot Archive - 75% tier tanszy, 24-72h do restora z archivum, cza czekac
* Recycle bin -  reguly do trzymania snapshotow (retencja 1d - 1y)
* FSR - bardzo szybki i drogi


AMI - Amazon Machine Image

* kustomizacja ec2
* szybszy start ec2
* spiety do regionu, ale moze byc kopiowany

rodzaje:
* public - od AWS
* wlasny
* aws marketplace ami - ktos inny zrobil i spyla
* 

