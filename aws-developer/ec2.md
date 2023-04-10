zakupy!

* on-demand -  na sekundy - najwyzszy koszt (linux +win po pierwszej minucie). dobre gdy ciezko przewidziec jak apka dziala, 
dobre dla krotkich i nieprzerywanych workloadow
* reserved (1 & 3 y) - upusty np 72%. wybierasz type, region, os, 1 lub 3 lata, platnosci (steady states apps, np dbs), mozna spylic w Reseved
Instance Marketplace
* saving plans (1&3y) - commitment to usage in $ (10$/h for 3 y) - powyzej jak on demand, long workloads. 
locked to specific instance and family (m5 in us-east-1). Wybierane: OS, instance size (x5, x4), tenancy (host, dedicated, default)
* spot instances - short and cheap, do 90% upustu. Mozna je stracic jesli rachunek wiekszy niz zakladany. NIE DO KRYTYCZNYCH
* dedicated host - book a server, fizyczny server. OnDemand | Reserved. Najdrozszy. Dobre dla softu ze skomplikowana licencja (np na cory itp). 
Najblizej hardwara 
* dedicated instance - no sharing with other customers. Moze sherowac hardware z innymi instancjami. 
* capacity reservation - capacity in AZ for any duration. Bez upustow, trzeba mieszac z reseverd/saving plans.
 Dobre dla krotkich workloadow w specyficznym AZ. Placimy nawet jak nic nie leci. 
