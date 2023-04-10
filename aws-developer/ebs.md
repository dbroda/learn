**Elastic Block Store**

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


**Snapshoty**
* mozna kopiowac miedzy AZ i Regionami

ebs -> snapshot -> restore -> ebs

* Snapshot Archive - 75% tier tanszy, 24-72h do restora z archivum, cza czekac
* Recycle bin -  reguly do trzymania snapshotow (retencja 1d - 1y)
* FSR - bardzo szybki i drogi


**AMI - Amazon Machine Image**

* kustomizacja ec2
* szybszy start ec2
* spiety do regionu, ale moze byc kopiowany

rodzaje:
* public - od AWS
* wlasny
* aws marketplace ami - ktos inny zrobil i spyla


**EC2 Instance store**

* gdy potrzeba performance
* hardware w fizycznym serwerze
* lepszy IO, throughput
* ephemeral :( 
* dobre dla cache, temp, bufor
* backup i replikacja spada na nas


**EBS Volumes**

* gp2/gp3 - GeneralPurpose ssd balans price i performance [tylko jako BOOT]
  * 1-16GB
  * gp3: 3k iops-16k, nowszy, Thro 125Mibs - 1000Mibs niezaleznie od wielkosci dysku ?
  * gp2: max iops = 16k, male gp2 max 3k iops, powiazane z wielkoscia dysku (5,3GB przy max iops)
* io1/op2 - provisioned iops-  ssd low latency i high throughput [tylko jako BOOT]
  * 16k+ iops
  * supcio dla db
  * io1/io2 4GB-16TB 64k iops (nitro), 32k inne
  * io2 block express - do 64TB, ultra fast, 256k iops
  * wspiera multi-attach 
* st1 - hdd, tani do czestego dostepu 
  * 128GB-16TB
  * maxiops 500
  * high thro optimized
* sc1 - hdd, najtanszy do rzadkiego dostepu
  * cold hdd 
  * dla archive data, rzadki access
* paramsy: size/througput/iops

**EBS Multi Attach**






