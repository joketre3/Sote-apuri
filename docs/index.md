---
title: Kirjausapuri – ohjaajan lähdesivusto
---

# Kirjausapuri

Tämä sivusto on lähde Microsoft 365 Copilot -agenteille. Jokainen sivu sisältää yhden asiakirjarakenteen sellaisenaan, agentin toimintaohjeen ja hyvän kirjaamisen periaatteet. Agentti lukee sivun ja muotoilee muistiinpanosi rakenteen mukaiseksi luonnokseksi.

## Sivut (yksi per asiakirja → yksi agentti per sivu)

| Asiakirja | Sivu |
|---|---|
| Työikäisten palvelutarpeen arvio (PTA) | `/pta` |
| Työikäisten palvelujen asiakassuunnitelma | `/asiakassuunnitelma` |
| Monialainen palvelutarpeenarviointi (MOTY) | `/moty` |

Korvaa pohjaosoite omallasi: `https://KÄYTTÄJÄ.github.io/REPO/pta` jne.

## Tärkein sääntö: tälle sivustolle ei tule asiakastietoa

Sivustolla on vain tyhjät rakenteet ja ohjeet. Muistiinpanosi — joissa voi olla asiakastietoa — menevät vain työpaikan Copilotiin, eivät koskaan tähän repoon tai GitHubiin.

## Agentin pystytys (per asiakirja)

1. Luo uusi agentti.
2. Lisää sen lähteeksi / luettavaksi sivuksi kyseisen asiakirjan URL (esim. `.../pta`).
3. Liitä agentin ohjekenttään lyhyt ohje:

```
Olet sosiaaliohjaajan kirjausapuri. Lue lähdesivu ja toimi sen
"Toimintaohje"- ja "Hyvä kirjaaminen" -osioiden mukaan. Muotoile
käyttäjän muistiinpanot sivun asiakirjarakenteen mukaiseksi
luonnokseksi, kenttä kentältä. Älä keksi tietoa: merkitse puuttuvat
kohdat [PUUTTUU]. Älä arvaa koodistokoodeja. Tuota vain valmis
sisältö, ei kommentteja prosessista.
```

## Käyttö arjessa

Liitä keskusteluun vain omat muistiinpanot, esim:

```
Tee näistä muistiinpanoista luonnos lähdesivun rakenteen mukaan:
<muistiinpanot tähän>
```

Agentti palauttaa kenttä kentältä -luonnoksen. **Luet sen läpi ja vastaat sisällöstä** ennen kuin se menee Sagaan.

## Päivitys

Rakennesivut (`pta.md`, `asiakassuunnitelma.md`, `moty.md`) on koottu lähdetiedostoista (`_toimintaohje.md`, `_hyva-kirjaaminen.md`, `_rakenne_*.md`) skriptillä `build_rakenteet.py`. Jos virallinen rakenne muuttuu, päivitä lähde ja kokoa sivut uudelleen.
