## DECOUPAGE RESEAUX  

- Service **INFORMATIQUE** = 50 équipements  
- Service **DEVELOPPEMENT** = 12 equipements  
- Service **ADMINISTRATION** = 20 équipements
- Service **TECHNIQUE** =15 équipements


### DECOUPAGE SYMETRIQUE  


Pôle           |  Adresse Réseau | Adresse Broadcast | Addresse Début | Adresse Fin  
:---:          |     :---:       |       :---:       |     :---:      | :---: 
INFORMATIQUE   |  172.16.1.0/26  |    172.16.1.63    |   172.16.1.1   | 172.16.1.62 
DEVELOPPEMENT  |  172.16.1.64/26 |   172.16.1.127    |   172.16.1.65  | 172.16.1.126  
ADMINISTRATION | 172.16.1.128/26 |   172.16.1.191    |   172.16.1.129 | 172.16.1.190  
TECHNIQUE      | 172.16.1.192/26 |   172.16.1.255    |   172.16.1.193 | 172.16.1.254


Pour le calcul du _CIDR_ :  
2^6 = 64  
32 - ^6 = 26  
CIDR = /26

64 - 2 = 62  
62 adressages possible par sous-réseaux


### DECOUPAGE ASYMETRIQUE


Pôle           |  Adresse Réseau  | Adresse Broadcast | Addresse Début | Adresse Fin  
:---:          |      :---:       |       :---:       |     :---:      | :---: 
INFORMATIQUE   |  172.16.1.0/26   |    172.16.1.63    |   172.16.1.1   | 172.16.1.62 
ADMINISTRATION |  172.16.1.64/27  |    172.16.1.95    |   172.16.1.65  | 172.16.1.94  
TECHNIQUE      |  172.16.1.96/27  |    172.16.1.97    |   172.16.1.97  | 172.16.1.126
DEVELOPPEMENT  |  172.16.1.128/28 |    172.16.1.143   |   172.16.1.129 | 172.16.1.142  


Pour le calcul du _CIDR_ :  INFORMATIQUE  
2^6 = 64  
32 - ^6 = 26  
CIDR = /26

64 - 2 = 62  
62 adressages possible  

Pour le calcul du _CIDR_ :  ADMINISTRATION  
2^5 = 32  
32 - ^5 = 27  
CIDR = /27

32 - 2 = 30  
30 adressages possible  

Pour le calcul du _CIDR_ :  TECHNIQUE  
2^5 = 32  
32 - ^5 = 27  
CIDR = /27

32 - 2 = 30  
30 adressages possible  

Pour le calcul du _CIDR_ :  DEVELOPPEMENT  
2^4 = 16  
32 - ^4 = 28  
CIDR = /28

16 - 2 = 14  
14 adressages possible  