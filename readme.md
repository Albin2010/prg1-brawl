# Brawl

[Info på kurswebben](https://programmering.jensa.dev/logik-och-repetition/milstolpe-brawl/milstolpe-brawl)

**Kort version:** du bygger ett fightingspel i terminalen, du mot datorn. Varje tur slår båda, skadan
slumpas, och kampen pågår tills någon har noll HP (hälsopoäng) kvar. Först planerar du på papper,
sedan bygger du steg för steg med ett kort i taget på brädet. Sikte: klart till jul.

Resten av den här filen slår du upp i när du behöver.

## Kom igång

1. Forka det här repot och klona ner din fork. Öppna den i VS Code.
2. Har du inte MD Kanban sedan Textäventyret, installera den:
   https://marketplace.visualstudio.com/items?itemName=jeddak.md-kanban
3. Öppna brädet i [brawl.kanban.md](./brawl.kanban.md). Flytta "Forka repot" till Done.

## Så jobbar du

1. **Planera först.** Flytta "Planera kampen" till In Progress och fyll i
   [planering.md](./planering.md). Visa planen för läraren innan du skriver kod.
2. **Ett kort i taget.** Flytta kortet till In Progress, skriv koden i [main.py](./main.py) och kör.
3. **Klart kort betyder commit och push.** Flytta kortet till Done, committa med kortets namn som
   meddelande och pusha direkt. Då hamnar koden och det flyttade kortet i samma commit.
4. **Faserna längs vägen.** Fyll i [faser.md](./faser.md) medan du jobbar, inte i efterhand. Den är
   underlaget i teknik.
5. **Envisa fel** får en rad i [felsökningslog.md](./felsökningslog.md).

Hinner du inte bli klar med ett kort under ett pass är kortet för stort. Dela upp det i två.

## Kraven

**Spelet**

- Programmet frågar efter spelarens namn.
- Spelaren och fienden har varsin HP-variabel, och startvärdena syns när spelet börjar.
- Kampen är en `while`-loop som pågår så länge båda har mer än noll HP. Villkoret använder `and`.
- När loopen är slut avgör programmet vem som vann och skriver ut det.

**Varje tur**

- Spelaren väljer: 1 attackera, 2 försvara. Försvar halverar skadan spelaren tar den turen.
- Valet är kraschsäkert: skriver någon `katt` ska programmet fråga igen, inte krascha.
- Båda slår med slumpad skada, inom var sitt intervall.
- Efter varje tur syns vem som slog, hur hårt och hur mycket HP som är kvar.

**En `for` med ett syfte**, till exempel:

- en HP-stapel, `for i in range(spelare_hp // 10):` som ritar ett tecken per tio HP, eller
- bäst av tre ronder, en `for` runt hela kampen.

**Koden**

- Alla variabler i `snake_case`, till exempel `spelare_hp`, inte `SpelareHP`.
- Kommentarer som förklarar programmets delar.

## Lämna in

Allt pushat till din fork, och de fyra rubrikerna längst ner i den här filen ifyllda. Skicka länken
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

## Det som var svårast

Vilket kort tog längst tid, och hur löste du det?

## Om jag hade mer tid

Minst en sak du skulle vilja förbättra.

## Varför `while` och inte `for` i kampen?

Vad är det i _problemet_, inte i koden, som avgör valet?
