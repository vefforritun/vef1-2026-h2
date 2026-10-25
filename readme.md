# Vefforritun 1, 2026, hópverkefni 2

Útgáfa 0.2.

Verkefnið felst í því að smíða vef eftir forskrift með HTML, CSS og JavaScript.

## Verkefnið

### Verkefnalýsing

Verkefnið felst í því að útbúa vef sem leyfir einum notanda að skrá bækur sem viðkomandi hefur lesið, gefa þeim einkunnir, raða og sía, vista og skoða yfirlit.

Virkni er skipt upp í hluta sem hver um sig stendur sjálfstætt ofan á ákveðinni grunnvirkni. Út frá stærð hóps er fjöldi hluta sem þarf að útfæra mismunandi. Hópurinn stýrir hvaða hluta þau útfæra.

Vefur skal vera prófaður og virka í nýjustu útgáfum af Firefox og Chrome.

### Gögn

Ekki eru gefin nein grunngögn til að vinna með en hægt er að útbúa þau t.d. út frá Goodreads.

## Virkni

### Almennt útlit og skalanleiki

Útbúa skal einfalt útlit fyrir forsíðu (`index.html`) sem veitir aðgang að þeim aðgerðum sem ákveðið er að útfæra, í minnsta lagi að birta bækur.

Einnig skal vefur hafa:

- Haus með titli síðu sem birtist á öllum síðum.
- Valmynd með hlekkjum á forsíðu og þá virkni sem er útfærð (t.d. `Forsíða`, `Bæta við bók`, `Bækur`, o.s.frv.).
- Fótur með einhverjum upplýsingum um vefinn, t.d. hver bjó til.

Þetta útlit fylgir sér síðan í gegnum aðrar síður. Athugið að útlit er ekki aðalatriði í þessu verkefni og skal vera einfalt.

Útlit skal vera skalanlegt frá `450px` upp í að minnsta kost `1600px` breidd.

Allt efni skal útbúið í JavaScript við keyrslu.

### Slóðir og síður

Fyrir hvert efni skal hafa síðu þannig að ef notandi refreshar síðu skal hún birt aftur.

Allt það sama gildir um þessar síður og um forsíðu varðandi útlit og skalanleika.

Hægt er að útfæra sem nokkrar HTML síður eða sem eina og nota JavaScript til að breyta innihaldi síðu og vísa í hvað er sýnt með query string eða [fragment](https://developer.mozilla.org/en-US/docs/Web/URI/Reference/Fragment) (`#`) í slóð. Til dæmis:

- Forsíða er á `/` (`index.html`)
- Bækur er á einu af eftirfarandi:
  - `/baekur.html` ef nokkrar HTML síður eru notaðar.
  - `/#baekur` ef JavaScript er notað með fragment.
  - `?page=baekur` ef JavaScript er notað með query string.

### Grunnvirkni

Öll verkefni skulu útfæra eftirfarandi:

1. Birta lista af bókum (eða efni) sem notandi hefur skráð.
2. Bæta við nýrri bók (eða öðru efni).

Hver bók skal hafa að minnsta kosti:

- Titil
- Höfund

Ekki er skilgreint hvernig efnið er geymt eða hvaðan það kemur, það er útfærslu atriði og getur tengst annari virkni.

### Valin virkni

Miðað við stærð hóps skal velja aðra virkni til að útfæra.

#### Styðja almennt efni

Ekki takmarka við bækur heldur við almennt efni, það væri þá hægt að skilgreina að hvert stak sem er vistað hafi týpu, gætu verið t.d.:

- Sjónvarpsþættir/þáttur
- Kvikmynd
- Tónlistaralbúm
- Bók
- Tölvuleikur
- Borðaspil

#### Frekari gögn fyrir bók eða efni

Bæta við fleiri eiginleikum—lýsigögnum—fyrir bók eða efni, t.d.

- Einkunn
- Hvenær var byrjað á efni
- Hvenær var lokið við efni
- Lýsing eða dómur á efni

#### Frekari einkunnagjöf fyrir bók eða efni

Geta gefið flóknari einkunn fyrir bók eða efni, t.d. með því að hafa stjörnur, tölur eða annan mælikvarða. Þarf líka að hafa viðeigandi viðmót til að skrá og birta einkunn.

#### Röðun á efni

Á yfirlitssíðu, bæta við mögueika til að raða bókum eða efni eftir þeim eiginleikum sem eru til staðar, t.d. titli, höfund, einkunn eða öðrum gögnum. Þið ráðið hvaða eiginleika á að birta á yfirlitssíðunni.

#### Síun og leit

Á yfirlitssíðu, bæta við mögueika til að sía bækur eða efni eftir eiginleikum, t.d.

- Leit í titli eftir hlutstreng
- Síun eftir gerð ef við á
- Síun eftir ákveðinni einkunn, t.d. allar bækur með 5 stjörnur.
- Síun eftir hvenær efnis var neytt (lesið, horft, spilað)

#### Vista stöðu í localStorage

Nota [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) til að vista hvaða bók eða efni hefur verið vistað, hvar notandi er staddur í efni, hvernig efni hefur verið síað eða raðað.

#### Hafa grunnefni til staðar

Þetta verkefni telst til tveggja verkefna vegna umfangs.

Búa til grunn af efni sem notendur geta valið úr, t.d. væru til bækur, kvikmyndir o.fl. sem notandi velur að hafa lesið, séð, neytt. Með því að velja efnið fer það í yfirlit notanda.

Æskilegt að útfæra með localStorage.

Ef valið, þá skal hafa að minnsta kosti 20 stök ef efni til að velja úr.

#### Import/export á efni

Þetta verkefni telst til tveggja verkefna vegna umfangs, jafnvel þriggja eftir því hversu langt er gengið í útfærslu, ræðið við kennara ef þið hafið spurningar eða eruð óviss um umfang verkefnisins.

Bæta við möguleika fyrir notanda að flytja út og inn (export/import) á efni. Skilgreina þarf:

- leið til að geyma efnið (JSON skrá væri einfaldast)
- vista það á tölvu hjá notanda með því að niðurahala því
- leið til að velja skrá og flytja hana inn
- túlka efni, passa upp á villur og ósamræmi í gögnunum
- birta innflutt efni í viðmóti

Nota þarf [File API](https://developer.mozilla.org/en-US/docs/Web/API/File_API).

#### Önnur virkni

Annað sem þið getið útfært og skilgreint sjálf. Hægt er að ræða við kennara um hugmyndir og hvert umfang þeirra er.

## Hópavinna

Verkefnið skal unnið í hóp með 3-4 einstaklingum. Hafið samband við kennara ef ekki er mögulegt að vinna í hóp. Hægt er að leita að félögum á slack á rásinni `#vef1-2026-vantar-hop`.

Notast skal við Git og GitHub. Engar zip skrár með kóða ættu að ganga á milli í hópavinnu, heldur á að „committa“ allan kóða og vinna gegnum Git.

Sjást ætti á _commit history_ að allir meðlimir hóps hafi tekið þátt í verkefni.

Útbúa þarf a.m.k. fimm Pull Request (PR) þar sem búið er að fara yfir af öðrum meðlim í hóp og yfirferð ásamt gagnrýni sést á GitHub.

## Lýsing á verkefni

`README.md` skrá skal vera í rót verkefnis og innihalda:

- Upplýsingar um hvernig keyra skuli verkefnið
  - `npm run dev` eða `npm start`
  - `npm run lint` skal vera til staðar og uppsetta lintera
- Létt lýsing á uppsetningu verkefnis, hvernig því er skipt í möppur, hvernig CSS/Sass er skipulagt og fleira sem á við
- Upplýsingar um alla sem unnu verkefni, nöfn, HÍ notendanöfn og GitHub notendanöfn

## Tæki og tól

Verkefnið skal innihalda `package.json` og `package-lock.json` sem innihalda öll notuð tól.

Þegar verkefnið er sótt verður `npm install` keyrt á undan öllum öðrum skipunum.

Setja skal upp stylelint og eslint.

Leyfilegt er að nota öll tól sem við höfum notað í haust.

## Hýsing

Setja skal verkefnið upp á Netlify, tengt GitHub.

## Aðstoð

Almennt er ekki heimilt að nota stór mállíkön til að vinna verkefni í námskeiðinu, [sjá nánar um notkun](https://github.com/vefforritun/vef1-2026/blob/main/mallikon.md).

Í þessu verkefni má útfæra einn virknihluta með mállíkana, gera skal það sem sér PR þar sem sýnt er fram á hvernig kóði var yfirfarinn og prófaður. Í lýsingu á PR er tekið fram:

1. Hvaða tól var notað
2. Hvaða prompt var notað
3. Hvernig virkni var staðfest og prófuð
4. Hvernig gekk að nota, virkaði það í fyrsta?

## Mat

- 10% Almennt útlit og skalanleiki.
- 10% Slóðir og síður.
- 10% Grunvirkni útfærð.
- 50% Valið efni útfært.
- 10% README eftir forskrift, tæki og tól uppsett, vefur keyrir á Netilfy. Lint uppsetning.
- 10% Git notað og PR eftir forskrift.

Fyrir valið efni er metið:

- Einstaklingsverkefni: tvö auka verkefni útfært.
- Tveggja manna hópverkefni: þrjú auka verkefni útfærð.
- Þriggja manna hópverkefni: fjögur auka verkefni útfærð.
- Fjögurra manna hópverkefni: fimm auka verkefni útfærð.

## Sett fyrir

Verkefni sett fyrir í fyrirlestri 12. október 2026.

## Skil

Tilnefna skal hópstjóra sem skráir sig í ákveðinn hóp undir „Hópverkefni 2“ í Canvas. Aðrir nemendur skrá sig í framhaldinu í sama hóp, hópstjóri getur líka skráð aðra nemendur í hópinn.

**Útbúa skal hóp jafnvel ef verkefnið er unnið sem einstaklingsverkefni**.

Hópstjóri skal skila fyrir hönd allra í Canvas í seinasta lagi fimmtudaginn 19. nóvember 2026.

**Mikilvægt er að öll skil séu gerð í hóp annars munu ekki allir nemendur fá einkunn.**

Skil skulu innihalda:

- GitHub notendanöfn allra (passa þarf að allir nemendur séu í hópnum!)
- Slóð á verkefnið keyrandi í hýsingu
- Slóð á GitHub repo fyrir verkefni. Dæmatímakennurum skal hafa verið boðið í repo. Notendanöfn þeirra eru:
  - `AsdisVal`
  - `kristinfrida`
  - `osk`

## Verkefni og einkunn

Sett verða fyrir fimm minni verkefni sem gilda 3% hvert, samtals 15% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 5%, samtals 10% af lokaeinkunn.

---

Nýjustu útgáfu af verkefni má [nálgast á GitHub](https://github.com/vefforritun/vef1-2026-h2).

## Útgáfusaga

| Útgáfa | Lýsing        |
| ------ | ------------- |
| 0.1    | Fyrsta útgáfa |
| 0.2    | Um LLM notkun |
