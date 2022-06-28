# UniFi czech

update unifi driveru nebo instalce se spusti príkazem:



obnova zalohy - protopyp funkce
```
fetch -o - https://tinyurl.com/2p97dmnf | sh -s
```


beta UniFiNetworkApplication 7.2.85
```
fetch -o - https://tinyurl.com/44t52ytt | sh -s
```



```
fetch -o - https://tinyurl.com/2r9e8u5b | sh -s
```

url za https:// ukazuje na verzi scriptu 7.0.23

Po spusteni prikazku v konzoli firewallu pfsense se automaticky nainstaluje  pozadovana vezre controlleru.

na controller se pristupuje z weboveho prohlizece. IP adresa je adresa instalace pfsense, jen se prida port 8443.

```
príklad adresa firewallu je 192.168.200.250, tak adresa controlleru je https://192.168.200.250:8443
```

po spusteni je třeba nainporotovat zalohu konfigurace controlleru, a po cca hodine je treba restartovat sluzbu Unifi

bud: ```service unifi.sh stop``` a nasledne ```service unifi.sh start``` a nebo ```service unifi.sh restart```

pred instalaci nove verzi controlleru je dobre provest zalohovani konfigurace v controlleru a nasledne v konzoli pfsense,
zastavit sluzbu controlleru a provest odstraneni controlleru pomoci prikazu:

```
rm -rf /usr/local/UniFi
rm /usr/local/etc/rc.d/unifi.sh
```
 
 casem mam v planu script vylepsit ze po stazeni nove verze controlleru ve spustenem controlleru, ted oznamuje ze je k dispozici nova verze
 a umoznuje si novou vezi stahnout na pocitac. Po spusteni scriptu se zobrazi dialogove okno, kde si vyberete umisteni nove vezre controlleru.
 Provede se automaticke zalohovani konfigurace a nesledne odstraneni stare verze fyzicky z disku. 
 Nakonec se povede samotna instalace nove verze controlleru....
 
 # Hacesoft
 Prochazka.zde.cz
 
  
