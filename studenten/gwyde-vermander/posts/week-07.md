# Week 7: Geen enkel product volgt het peloton

## Mijn skill
Vroeger moest ik voor elke renner zelf nieuwsberichten zoeken, ze in mijn prompt plakken en de datum invullen. Nu typ ik /vorm met de naam van een renner. De skill leest de regels uit mijn nieuwste prompt, zoekt zelf recente berichten op het web, en geeft een label, een reden en een bron. Ik testte hem met drie renners die niet in mijn testset staan, elk in een eigen sub-agent: Wout van Aert, Mathieu van der Poel en Lotte Kopecky. Twee van de drie waren goed. Bij Kopecky gaf hij "geen info", terwijl ze zelf zegt dat haar lichaam in orde en blessurevrij is en ze koerst. Ik paste de skill aan, en daarna gaf hij "goed". Twee dingen vielen op: in november geeft de skill vaak "geen info", omdat bijna niemand koerst, en Wielerflits en HLN blokkeren de agent, dus hij moet andere bronnen zoeken. Ik maakte ook een tweede skill, /vraag, die eerst vragen stelt als mijn opdracht niet duidelijk is.

## Mijn connector
Ik koppelde Google Agenda aan de Claude-app. Ik gaf toestemming bij het koppelen van de connector. Daarna vroeg ik wanneer ik deze week moet werken en om hoe laat ik aanwezig moet zijn. Claude vond al mijn shifts en de uren waarop ik moet beginnen. Dat vind ik nuttig, maar meestal ken ik mijn agenda goed, dus zelf zou ik het niet vaak nodig hebben. Het nuttigste moment: Claude zag dat een privé-afspraak op zaterdag botst met mijn avondshift.

In Claude Code koppelde ik ook CoinGecko via MCP. Verrassend: ook zonder connector vond Claude de bitcoinkoers van die minuut, omdat hij in de terminal zelf de website van CoinGecko kon aanspreken. Met de connector gebruikte hij een eigen CoinGecko-tool en kreeg hij meer gegevens. De eerste poging mislukte wel, maar Claude las de foutmelding, paste zijn verzoek aan en probeerde opnieuw. Zo zag ik een agent aan het werk.

## Build, Connect, Buy

|  | Voor Sporza | Wat zit er vast? |
|---|---|---|
| **Build** | Mijn skill /vorm: één bestand, dat de regels uit mijn prompt leest. 2 op 3 juist, na één aanpassing ook de derde. | Bijna niets. Het bestand is van mij, en een andere AI kan het ook lezen. |
| **Connect** | /vorm gebruikt web search om zelf recente berichten te zoeken. Later kan een MCP-connector naar een nieuwsdienst of sportdata-aanbieder dat vervangen. | MCP is een open standaard. Andere AI, zelfde stekker. Maar sommige websites (Wielerflits, HLN) blokkeren de agent. |
| **Buy** | Sportradar Cycling API (prijs op aanvraag), Kitman Labs Performance Medicine (USD 100.000 per jaar), Cycling Analytics (€ 6,10 per maand). Prijzen opgezocht op 25 november 2026. | Bij Sportradar en Kitman Labs zitten de data in hun systeem. |

Elk product is op zich nuttig. Sportradar is interessant als ik later machine learning toevoeg om de prijzen per renner accurater te maken. Kitman Labs en Cycling Analytics helpen om de vorm te achterhalen. Maar Kitman Labs is veel te duur, en de data blijft binnen één ploeg. Cycling Analytics is goedkoop, maar werkt alleen met data die renners zelf uploaden, en profploegen geven die niet vrij. Geen enkel product volgt de vorm van het hele peloton op.

**Mijn advies:** Build, met Connect voor het zoeken, want met gratis bronnen maakt mijn skill al een goede schatting, voor ± € 25 per jaar (Sonnet 5.5).
**Wat me van mening doet veranderen:** als een sportdata-aanbieder, zoals Sportradar, een feed met blessures en ziekte voor het hele peloton aanbiedt, met export, en die minder kost dan wat de tijdwinst Sporza oplevert (± € 1.935 per jaar).
