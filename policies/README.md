# policies

Privatumo politikos plėtiniams. Viešas repo, serverio nereikia — GitHub
Pages atiduoda statinius HTML failus nemokamai ir neribotam laikui.

**Kodėl ne Artifact ir ne Notion:** politikos URL eina į Chrome Web Store
listingą ir Google jį tikrina per kiekvieną peržiūrą, taip pat ir po metų.
Nuoroda, pririšta prie vienos paskyros ar vieno įrankio, yra skola. Ši —
tavo domenas, tavo failai, perkeliama bet kada.

## Struktūra

```
index.html                 bendras sąrašas (repo šaknis nebūna 404)
tab-sessions/index.html    klonas #1
<kito-klono-vardas>/index.html
```

Kiekvienas klonas gauna savo aplanką. URL tada yra
`https://designbyugnius-lab.github.io/policies/<klono-vardas>/`

## Kaip paleisti (per naršyklę, git nereikia)

1. github.com → **New repository** → pavadinimas `policies` → **Public** → Create.
2. **Add file → Upload files** → užtempk `index.html` ir aplanką `tab-sessions`.
3. **Settings → Pages** → Source: *Deploy from a branch* → `main` / `(root)` → Save.
4. Palauk ~1 min. Patikrink, ar atsidaro:
   `https://designbyugnius-lab.github.io/policies/tab-sessions/`
5. **Tą URL** klijuok į Chrome Web Store → Privacy practices → Privacy policy URL.

## Kaip pridėti kitą kloną

1. Nukopijuok `tab-sessions/` į naują aplanką nauju vardu.
2. Pakeisk pavadinimą, datą, leidimų lentelę ir „What it stores" sąrašą.
   Visa kita — ta pati struktūra.
3. Pridėk eilutę į `index.html` sąrašą.
4. Commit. Nuoroda pradeda veikti per minutę.

## Dažna klaida keliant

GitHub „Upload files" ima **failus**, ne aplankus, jei užtempi tik failus.
Tada šaknyje atsiranda politika vietoj sąrašo, o `tab-sessions/` nebūna.
Užtempk **aplanką** `tab-sessions` visą, atskiru įkėlimu nuo `index.html`.

Patikra po įkėlimo — abu turi atsidaryti:

- `https://designbyugnius-lab.github.io/policies/` → sąrašas
- `https://designbyugnius-lab.github.io/policies/tab-sessions/` → politika

## Taisyklės

- **Data keičiama kiekvieną kartą, kai keičiasi tai, ką plėtinys saugo.**
  Google lygina politiką su leidimais per kiekvieną peržiūrą.
- Politika neturi žadėti daugiau, nei daro kodas. Kiekvienas „does not"
  sakinys `tab-sessions` politikoje yra patikrinamas: nėra tinklo užklausų
  (tikrina 12-as `klono_testas.py` testas), nėra `host_permissions`, nėra
  content script'ų.
- „Single purpose" politikoje ir dashboard'e turi sutapti žodis į žodį.
