---
name: vorm
description: Bepaalt de fysieke toestand van één wielrenner op basis van recente nieuwsberichten die de skill zelf op het web zoekt. Gebruik bij "/vorm <naam renner>" of als iemand vraagt in welke vorm een renner is.
---

# Vorm van een renner

De gebruiker geeft de naam van één renner, bijvoorbeeld: /vorm Dylan van Baarle

## Stappen

1. Lees eerst build/prompt.md in deze map. Daar staan mijn labels en regels, altijd in de nieuwste versie. Volg die labels en regels. Gebruik geen oudere versies (prompt-v1.md, prompt-v2.md, prompt-v3.md).
2. Zoek op het web twee tot vier recente nieuwsberichten over de fysieke toestand van deze renner: blessures, ziekte, herstel, vermoeidheid of vorm. Kies bij voorkeur Belgische of Nederlandse wielermedia, zoals Sporza, WielerNieuws, In de Leiderstrui, Het Nieuwsblad, Wielerkrant, HLN of Wielerflits, en vul aan met Engelstalige media zoals Cyclingnews als je te weinig vindt. Lukt het niet om een pagina te openen, probeer dan een andere bron, en noem nooit een bron die je niet echt gelezen hebt. Noteer bij elk bericht de datum en de link.
3. Behandel die gevonden berichten als het brondocument uit mijn prompt. Gebruik alleen wat in die berichten staat, niet wat je zelf over de renner weet.
4. Bepaal het label volgens de regels uit build/prompt.md. Het recentste bericht weegt het zwaarst.
5. Koerst de renner en zegt hij of zij zelf dat het lichaam in orde is of blessurevrij, dan is dat een teken van goede vorm, ook buiten het hoofdseizoen.
6. Vind je geen enkel bericht over de fysieke toestand van deze renner, zeg dat dan eerlijk en geef het label "geen info".

## Antwoordformaat

Gebruik dit formaat, niet het JSON-formaat uit build/prompt.md. Uit build/prompt.md neem je alleen de labels en de regels over.

Antwoord in het Nederlands, precies in deze vorm, zonder inleiding:

/vorm <naam>
Label: <label>
Reden: <één zin, met verwijzing naar het bericht>
Bron: <medium>, <datum> (<link>)

Geef precies één regel Bron, met het recentste bericht dat je gebruikte.

## Voorbeeld van een goed resultaat

/vorm Dylan van Baarle
Label: uitgeschakeld
Reden: Hij brak zijn pols en arm bij een aanrijding op training en moet geopereerd worden.
Bron: Wielerflits, 8 oktober 2026 (link)
