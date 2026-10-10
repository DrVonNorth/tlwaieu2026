# Teaching and Learning with AI in Europe 2026 – lokal konferensguide

Bygger vidare på NordiCHI-upplägget. Ingen inloggning, Supabase eller synkronisering.

## Publicering på GitHub Pages

1. Lägg **index.html** och **program.json** i roten av ditt GitHub-repository.
2. Aktivera GitHub Pages via Settings → Pages → Deploy from branch.
3. Öppna GitHub Pages-adressen på Mac eller Android. Filerna måste serveras via en webbadress; att dubbelklicka på `index.html` kan blockera hämtning av `program.json`.

## Funktioner

- Konferensprogram för 19–20 oktober med förstahandsval och alternativ.
- 0–3 stjärnor och anteckningar per presentation lagras i webbläsarens **localStorage**.
- **Flera bilder per presentation** lagras som originalfiler i webbläsarens **IndexedDB**. Varje bild kan öppnas och tas bort separat.
- **Exportera komplett backup** skapar en JSON-fil som innehåller anteckningar, stjärnor och bildfiler kodade i Base64. Backupen kan bli stor om många bilder lagts till.
- **Importera backup** återställer dessa data i en annan webbläsare. Anteckningar och stjärnor med samma sessions-ID ersätts; bilder med samma bild-ID uppdateras. Befintliga andra bilder behålls.

## Integritet och begränsningar

- Personliga uppgifter lämnar inte webbläsaren genom appen. Programmet är offentligt på GitHub Pages.
- Data synkroniseras **inte** automatiskt mellan Mac och Android. Exportera/importera JSON manuellt för att flytta dem.
- Lagringen är knuten till **webbplatsens adress och webbläsarprofil**. Rensning av webbplatsdata, privat läge eller byte av webbadress kan göra lokala data otillgängliga. Säkerhetskopiera regelbundet.
- IndexedDB har större kapacitet än localStorage men är inte obegränsad. Vid fullt utrymme visas felmeddelande.
- Exportfilen är **inte krypterad**. Förvara den privat. Uppladdade bilder blir inte offentliga på GitHub.
- Kontrollera tider, rum och titlar mot officiellt konferensprogram.

Filerna `config.js` och `supabase.sql` från den tidigare versionen behövs **inte** och ska inte publiceras.
