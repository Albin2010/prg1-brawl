# Brawl

[Info på kurswebben](https://programmering.jensa.dev/logik-och-repetition/milstolpe-brawl/milstolpe-brawl)

**Kort version:** du bygger ett fightingspel i terminalen, du mot datorn. Varje tur slår båda, skadan
slumpas, och kampen pågår tills någon har noll HP (hälsopoäng) kvar. Kraven är samma för alla, men
spelet är ditt: du bestämmer vem som slåss, vad spelaren kan välja och minst två egna idéer. Först
planerar du och skriver dina kort, sedan bygger du ett kort i taget. Sikte: klart till jul.

Resten av den här filen slår du upp i när du behöver.

## Kom igång

1. Forka det här repot och klona ner din fork. Öppna den i VS Code.
2. Har du inte MD Kanban sedan Textäventyret, installera den:
   https://marketplace.visualstudio.com/items?itemName=jeddak.md-kanban
3. Öppna brädet i [brawl.kanban.md](./brawl.kanban.md). Flytta "Forka repot" till Done.

## Så jobbar du

1. **Planera och skriv dina kort.** Flytta "Planera och skriv dina kort" till In Progress och fyll
   i [planering.md](./planering.md). Där gör du om kravkorten till dina egna, mindre kort och lägger
   till minst två med egna idéer. Visa planen och korten för läraren innan du skriver kod.
2. **Ett kort i taget.** Flytta kortet till In Progress, skriv koden i [main.py](./main.py) och kör.
3. **Klart kort betyder commit och push.** Flytta kortet till Done, committa med kortets namn som
   meddelande och pusha direkt. Då hamnar koden och det flyttade kortet i samma commit.
4. **Kravkorten flyttas sist.** Ett kravkort går till Done när kravet är uppfyllt, alltså när dina
   kort för det är klara. Då fungerar kravkorten som checklista.
5. **Faserna längs vägen.** Fyll i [faser.md](./faser.md) medan du jobbar, inte i efterhand. Den är
   underlaget i teknik.
6. **Envisa fel** får en rad i [felsökningslog.md](./felsökningslog.md).

Brädet är ditt. Hinner du inte bli klar med ett kort under ett pass är kortet för stort, dela upp
det. Kommer du på något nytt, skriv ett kort. Visar sig ett kort onödigt, ta bort det. Bara
kravkorten ligger fast.

## Kraven

**Spelet**

- Programmet frågar efter spelarens namn.
- Spelaren och fienden har varsin HP-variabel, och startvärdena syns när spelet börjar.
- Kampen är en `while`-loop som pågår så länge båda har mer än noll HP. Villkoret använder `and`.
- När loopen är slut avgör programmet vem som vann och skriver ut det.

**Varje tur**

- Spelaren väljer mellan minst två alternativ, och du bestämmer vilka. Till exempel 1 attackera,
  2 försvara, där försvar halverar skadan spelaren tar den turen.
- Valet är kraschsäkert: skriver någon `katt` ska programmet fråga igen, inte krascha.
- Båda slår med slumpad skada, inom var sitt intervall.
- Efter varje tur syns vem som slog, hur hårt och hur mycket HP som är kvar.

**En `for` med ett syfte**, till exempel:

- en HP-stapel, `for i in range(spelare_hp // 10):` som ritar ett tecken per tio HP, eller
- bäst av tre ronder, en `for` runt hela kampen.

**Mitt spel**

- Minst två kort med dina egna idéer, byggda och klara. De får vara små.

**Koden**

- Alla variabler i `snake_case`, till exempel `spelare_hp`, inte `SpelareHP`.
- Kommentarer som förklarar programmets delar.

## Vill du mer

Allt det här är frivilligt och kommer efter kraven. Plocka, gör om eller hitta på egna:

- **Kritiska träffar:** med 20 procents chans gör spelaren dubbel skada. Titta på `random.random()`.
- **Hälsopotion:** ett begränsat antal, som ett av valen varje tur.
- **Fler ronder:** en ny och starkare fiende när den förra besegrats. Hur många klarar du?
- **Poäng:** baserat på antal turer och HP som är kvar.

## Lämna in

Allt pushat till din fork, och rubrikerna längst ner i den här filen ifyllda. Skicka länken
till repot på kurswebben.

## Bedömning

Läraren tittar på fyra saker: att spelet uppfyller kraven, att du namnger mönstren du använt och var
de sitter, att Git-historiken visar att spelet växte fram kort för kort, och att koden går att läsa.
Sedan ett kort samtal om ett val du gjort i koden: inte vad du visste, utan varför du valde som du
gjorde.

---

## Vad programmet gör

Två meningar.

## Mönster jag använde

Ett mönster från Mönsterkortet per rad, och raden eller variabeln där det sitter.

## Mina egna idéer

Vilka kort hittade du på själv, och varför just de?

## Det som var svårast

Vilket kort tog längst tid, och hur löste du det?

## Om jag hade mer tid

Minst en sak du skulle vilja förbättra.

## Varför `while` och inte `for` i kampen?

Vad är det i _problemet_, inte i koden, som avgör valet?
