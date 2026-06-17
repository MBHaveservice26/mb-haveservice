# M&B Haveservice — hjemmeside

Statisk hjemmeside (ren HTML/CSS) klar til GitHub Pages. Fem sider, alle på dansk: Forside, Ydelser, Referencer, Om os og Kontakt.

## Filer

- `index.html` — Forside
- `ydelser.html` — Ydelser
- `referencer.html` — Referencer (før/efter)
- `om-os.html` — Om os + kontaktformular
- `kontakt.html` — Kontakt
- `styles.css` — Fælles design til alle sider

## Inden du går live — udfyld dine oplysninger

Søg og erstat disse pladsholdere i alle `.html`-filer:

- `[telefon]` → dit telefonnummer
- `[email]` → din e-mailadresse
- `[område vi dækker]` → fx "Storkøbenhavn og Nordsjælland"

Billederne er pt. linkede stock-fotos fra Unsplash. Når I har egne billeder, kan I lægge dem i en mappe (fx `billeder/`) og udskifte URL'erne i `src="..."`.

> Bemærk: Kontaktformularen er pt. kun visuel (den sender ikke noget endnu). Skal den virke uden en server, kan jeg sætte den op med en gratis tjeneste som Formspree — sig til.

---

# Sådan kommer du på GitHub fra en MacBook

Følg trinene i rækkefølge. Du skal kun gøre trin 1–4 én gang.

## 1. Opret en GitHub-konto
Gå til https://github.com og opret en gratis konto, hvis du ikke har en.

## 2. Installer Git
Åbn **Terminal** (tryk `Cmd + mellemrum`, skriv "Terminal", tryk Enter) og kør:

```bash
git --version
```

Hvis Git ikke er installeret, åbner macOS automatisk et vindue, der tilbyder at installere det — klik **Installer**. Følg vejledningen, og kør derefter `git --version` igen for at bekræfte.

## 3. Fortæl Git, hvem du er
Skift navn og e-mail ud med dine egne (brug samme e-mail som på GitHub):

```bash
git config --global user.name "Dit Navn"
git config --global user.email "din@email.dk"
```

## 4. Opret et nyt repository på GitHub
1. Log ind på GitHub, klik på **+** øverst til højre → **New repository**.
2. Navngiv det, fx `mb-haveservice`.
3. Vælg **Public**.
4. **Lad være** med at tilføje README (du har allerede en).
5. Klik **Create repository**. Lad siden stå åben — du skal bruge adressen om lidt.

## 5. Gør website-mappen klar
I Terminal: naviger ind i mappen med hjemmesiden. Den letteste måde er at skrive `cd ` (med mellemrum efter) og så trække mappen "M&B Haveservice" ind i Terminal-vinduet fra Finder og trykke Enter:

```bash
cd "/sti/til/M&B Haveservice"
```

Bekræft, at filerne er der:

```bash
ls
```
Du bør se `index.html`, `styles.css` m.fl.

## 6. Send filerne op til GitHub
Kør disse kommandoer én ad gangen. Erstat `DIT-BRUGERNAVN` og `mb-haveservice` med dine egne værdier (adressen står på GitHub-siden fra trin 4):

```bash
git init
git add .
git commit -m "Første version af hjemmesiden"
git branch -M main
git remote add origin https://github.com/DIT-BRUGERNAVN/mb-haveservice.git
git push -u origin main
```

Første gang du "pusher", beder Git dig logge ind. Følg vinduet, der åbner i browseren, og godkend. (Hvis du i stedet bliver bedt om et password i Terminal, skal du bruge et **personal access token** — sig til, så guider jeg dig.)

## 7. Slå GitHub Pages til
1. På dit repository på GitHub: klik **Settings**.
2. I menuen til venstre: klik **Pages**.
3. Under **Source**: vælg **Deploy from a branch**.
4. Vælg branch **main**, mappe **/ (root)**, klik **Save**.
5. Vent 1–2 minutter. Opdatér siden, og din adresse vises øverst:
   `https://DIT-BRUGERNAVN.github.io/mb-haveservice/`

Den adresse er din live hjemmeside. 🎉

## 8. Sådan opdaterer du siden senere
Når du har ændret en fil, kør i samme mappe:

```bash
git add .
git commit -m "Beskrivelse af ændringen"
git push
```

Ændringerne er online efter ca. et minut.

---

### Vil du have et pænere domæne?
GitHub Pages kan bruge dit eget domæne (fx `mbhaveservice.dk`) under **Settings → Pages → Custom domain**. Det kræver, at du køber domænet hos en udbyder. Sig til, hvis du vil have hjælp til det.
