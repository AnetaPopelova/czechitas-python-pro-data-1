# CVIČENÍ

## Studenti

Stáhni si datové sety, se kterými budeme pracovat v tomto cvičení: jmena.csv, studenti1.csv, studenti2.csv.

```
import requests

r = requests.get("https://kodim.cz/czechitas/progr2-python/python-pro-data-1/agregace-a-spojovani/excs/studenti/assets/jmena.csv")
open("jmena.csv", "wb").write(r.content)
r = requests.get("https://kodim.cz/czechitas/progr2-python/python-pro-data-1/agregace-a-spojovani/excs/studenti/assets/studenti1.csv")
open("studenti1.csv", "wb").write(r.content)
r = requests.get("https://kodim.cz/czechitas/progr2-python/python-pro-data-1/agregace-a-spojovani/excs/studenti/assets/studenti2.csv")
open("studenti2.csv", "wb").write(r.content)
```

První set už známe z minulé lekce. Druhé dva sety obsahují seznam studentů na nějaké menší IT fakultě. Pozor, tato data nemají žádnou souvislost s výsledky maturity, které jsme procházeli během lekce.

Proveď následující úkoly a zodpověz předložené otázky.

a. Načti dva datové sety studentů do oddělených pandas DataFrame a pomocí funkce concat je spoj do jednoho setu.

b. Pokud studentovi chybí ročník, znamená to, že již nestuduje. Pokud mu chybí číslo skupiny, znamená to, že jde o dálkového studenta. Kolik studentů v datovém setu již nestuduje a kolik jsou dálkoví studenti?

c. Vyčisti data od studentů, kteří nestudují nebo studují jen dálkově. Nadále budeme pracovat pouze s prezenčními studenty.

d. Zjisti, kolik prezenčních studentů je v každém z oborů.

e. Zjisti průměrný prospěch studentů v každém oboru.

f. Načti datový set s křestními jmény. Proveď join s tabulkou studentů tak, abychom věděli pohlaví jednotlivých studentů.

g. Zjisti, zda na naší fakultě studují IT spíše ženy nebo spíše muži.