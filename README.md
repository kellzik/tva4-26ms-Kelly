# tva4-26ms-Kelly

Author: Kelly Tragel

## Veebiserver vs rakendusserver

Mõlema puhul on tegemist arvuti/arvutitarkvaraga, mis tegelevad kasutajate päringutega, kuid seda erineval viisil. Veebiserver võtab esimesena vastu kasutajalt saadud päringu ning on mõeldud peamiselt lihtsama ehk staatilise sisu (HTML/CSS, pildid/videod jmt) kasutajani toomiseks. See-eest rakendusserver saab oma sisendi veebiserverilt ning genereerib keerukamat ehk dünaamilist sisu, mida käitab rakendusserveris jooksev programm. Näide: Veebiserver toob kasutajani e-poe lehed (HTML), kujunduse (CSS) ja pildid täpselt sellistena, nagu need on salvestatud. Rakendusserver aga tegeleb maksete töötlemise ning pangaga suhtlemisega (nt pangalinkide API-de kaudu), suhtleb e-poe andmebaasiga ja saadab tulemuse veebiserverile tagasi, mis omakorda toimetab tulemuse kasutaja veebilehitsejani.

## Error 404 vs Error 502

Error 404 (Not Found) puhul on probleem otsitavas sisus ehk kasutaja poolt otsitud lehte/faili ei leitud serverist. Tavaliselt juhtub siis, kui link on aegunud (sh kustutatud/mujale ümber liigutatud) või URL-is on tehtud kirjaviga. 
Error 502 (Bad Gateway) puhul on probleem serveritevahelises suhtluses ehk veebiserver ei saa ootuspärasel moel ühendust rakendusserveriga. Seda võib ette tulla puhkudel, kui näiteks rakendusserver on üle koormatud/välja lülitatud või serverite vahel esineb võrguprobleeme.