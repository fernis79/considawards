# Consid Awards 2026 at VENUE81

Interaktiv webbsida för Consid Awards den 4 december 2026 på VENUE81, Drottninggatan 81.
Gästerna kliver in genom en tecknad entré, viskar lösenordet till värdarna Andreas och Anton,
går genom foajén och hittar sitt bord i en 3D-modell av festsalen. Sidan har också agenda,
meny, gala-bingo, bordsquiz och låtönskningar.

Hela sajten är en enda fil: `index.html`.

## Publicera med GitHub Pages

1. Gå till **Settings → Pages** i det här repot.
2. Under **Build and deployment** väljer du **Source: Deploy from a branch**.
3. Välj grenen **main** och mappen **/ (root)** och klicka **Save**.
4. Efter en minut eller två finns sajten på `https://fernis79.github.io/considawards/`.

## Vad fungerar på GitHub Pages

| Funktion | Fungerar |
|---|---|
| Entrén, foajén, gardinerna och 3D-festsalen | Ja |
| Lösenordet vid dörren och den krypterade gästlistan | Ja |
| Tidslåset (dörrarna öppnar 4 december kl. 18.00) | Ja |
| Agenda, meny, bingo, quiz och låtönskningar | Ja |
| Påskäggen | Ja |
| Redigeringsläget och "Spara för alla" | Nej, kräver claude.ai |
| Knappen "Gå in som administratör" före kl. 18.00 | Nej, kräver claude.ai |

Ändringar av placering, agenda, meny eller kodord görs i originalet på claude.ai.
Spara där och ersätt sedan `index.html` i det här repot med den nya versionen.

## Säkerhet

- Gästlistan är krypterad med kodordet (AES-GCM, nyckel från PBKDF2). Namn och bord går inte
  att läsa i källkoden utan kodordet. Kodordet finns inte i repot.
- Agendan, menyn och länken till låtönskningarna ligger i klartext.
- Sidan ber sökmotorer att inte indexera den (`robots.txt` och `noindex`), men den är ändå
  publik för alla som har adressen.
- Tidslåset sitter i webbläsaren. Det håller borta de flesta, men är inget riktigt skydd.

## Efter galan

Avpublicera sidan (Settings → Pages → Unpublish) eller ta bort repot när festen är över,
så att gästlistan inte ligger kvar i onödan.
