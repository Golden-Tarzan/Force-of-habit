# Force of Habit — Uppladdningsguide för Google Play

Allt du behöver finns i denna mapp. Följ stegen i ordning.

---

## 📁 Vad mappen innehåller

```
force-of-habit/
├── index.html              ← Själva appen
├── manifest.webmanifest    ← App-info (namn, ikon, färger)
├── sw.js                   ← Offline-stöd (service worker)
├── privacy.html            ← Integritetspolicy (krävs av Google)
├── icons/                  ← Alla appikoner (kronan), 19 storlekar
└── LADDA-UPP-GUIDE.md       ← Denna fil
```

Alla filer hör ihop och måste ligga i **samma mapp/repo**. Flytta dem inte isär.

---

## ✅ STEG 1 — Lägg upp på GitHub Pages (gratis, ger HTTPS)

1. Logga in på GitHub (ditt konto `den-tarzan`).
2. Skapa ett nytt repo, t.ex. **`Force-of-Habit`**.
3. Ladda upp **alla** filer ur denna mapp (inklusive `icons/`-mappen).
4. Gå till repo → **Settings** → **Pages**.
5. Under "Branch" välj `main` och mappen `/ (root)`, tryck **Save**.
6. Vänta 1–2 minuter. Du får då två adresser:
   - **Appen:** `https://den-tarzan.github.io/Force-of-Habit/`
   - **Policyn:** `https://den-tarzan.github.io/Force-of-Habit/privacy.html`

👉 Testa app-länken på din telefon först — den ska gå att installera via "Lägg till på hemskärmen".

---

## ✅ STEG 2 — Skapa app-paketet med PWABuilder (gratis)

1. Gå till **https://www.pwabuilder.com**
2. Klistra in din app-länk (`https://den-tarzan.github.io/Force-of-Habit/`) och tryck **Start**.
3. PWABuilder analyserar appen (manifest, service worker, ikoner ska alla bli gröna ✓).
4. Tryck **Package For Stores** → välj **Android / Google Play**.
5. Ladda ner det genererade paketet (en `.aab`-fil + en signeringsnyckel).

⚠️ **VIKTIGT:** Spara signeringsnyckeln (`.keystore` / `signing key`) på ett säkert ställe.
Tappar du den kan du aldrig uppdatera appen senare. Gör en backup.

---

## ✅ STEG 3 — Registrera Google Play-utvecklarkonto

1. Gå till **https://play.google.com/console**
2. Betala engångsavgiften (~25 USD) och fyll i dina uppgifter.
3. Granskning av kontot tar oftast någon/några dagar.

---

## ✅ STEG 4 — Skapa appen i Play Console

1. Tryck **Create app**, fyll i:
   - Appnamn: **Force of Habit**
   - Språk: Svenska (eller engelska)
   - App eller spel: **App**
   - Gratis eller betald: **Gratis** (rekommenderas att börja med)
2. Ladda upp `.aab`-filen från PWABuilder under **Production → Create release**.

---

## ✅ STEG 5 — Fyll i butikssidan

| Fält | Vad du anger |
|------|--------------|
| Kort beskrivning | "Bygg vanor som ett spel för livet. Tjäna XP, stig i graderna, nå Legend." |
| Fullständig beskrivning | Beskriv funktionerna (XP, ranger, attribut, streak, prestige, 4 språk) |
| Appikon | `icons/icon-512.png` |
| Skärmbilder | Ta 2–8 skärmdumpar i appen (telefon) |
| Kategori | Hälsa & fitness / Livsstil |
| **Integritetspolicy** | Klistra in policy-länken från Steg 1 |
| Kontakt-e-post | **Forcebyhabit@gmail.com** |

---

## ✅ STEG 6 — Data safety-formuläret

Google frågar vilken data appen samlar in. För Force of Habit:

- **Samlar appen in data?** → **Nej**
- **Delas data med tredje part?** → **Nej**
- All data lagras lokalt på enheten.

Detta gör formuläret enkelt och ärligt — appen är bland de säkraste som finns att publicera.

---

## ✅ STEG 7 — Skicka in för granskning

1. Gå igenom alla checklistor i Play Console (de markeras gröna när de är klara).
2. Tryck **Send for review**.
3. Googles granskning tar oftast 1–7 dagar. Sedan är appen live! 🎉

---

## 🔁 Uppdatera appen senare

När du vill uppdatera:
1. Ändra filerna i GitHub-repot.
2. Höj cache-versionen i `sw.js` (t.ex. `foh-v2` → `foh-v3`) så användare får nya versionen.
3. Kör PWABuilder igen, ladda ner nytt `.aab`, **signera med samma nyckel**, ladda upp ny release.

---

## 📋 Snabb checklista

- [ ] Filer uppladdade till GitHub-repo
- [ ] GitHub Pages aktiverat → app-länk fungerar
- [ ] App testad på telefon (går att installera)
- [ ] Policy-länk fungerar
- [ ] `.aab`-paket skapat i PWABuilder
- [ ] Signeringsnyckel säkert sparad (backup!)
- [ ] Google Play-konto registrerat & godkänt
- [ ] App skapad + `.aab` uppladdad
- [ ] Butikssida ifylld + policy-länk + kontakt-mejl
- [ ] Data safety = "samlar ingen data"
- [ ] Skickad för granskning

---

*Force of Habit · Branding by Force · Forcebyhabit@gmail.com*
