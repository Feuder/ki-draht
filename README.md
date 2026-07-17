# KI-Draht – Dein KI-Nachrichtenticker

Eine installierbare Web-App (PWA), die aktuelle KI-News aus 16 Quellen bündelt: Firmen-Blogs (OpenAI, Google, DeepMind, Microsoft, Hugging Face), Tech-Medien (The Verge, TechCrunch, VentureBeat, MIT Technology Review, Wired, Ars Technica), deutsche Quellen (The Decoder, t3n, heise) und Forschung (arXiv, MIT News). Alles läuft direkt im Browser – kein Server, kein Konto, keine Kosten.

## In 5 Minuten online bringen

Damit die App auf allen Geräten und offline funktioniert, muss sie einmal kostenlos gehostet werden. Zwei einfache Wege:

**Weg A – GitHub Pages (empfohlen)**
1. Auf github.com einloggen → „New repository“ → Name z. B. `ki-draht`, „Public“, „Create repository“.
2. „uploading an existing file“ anklicken → alle Dateien aus diesem Ordner hineinziehen → „Commit changes“.
3. Im Repository: Settings → Pages → unter „Branch“ `main` und `/ (root)` wählen → Save.
4. Nach ca. 1 Minute ist die App erreichbar unter: `https://DEIN-NAME.github.io/ki-draht/`

**Weg B – Netlify**
1. Auf app.netlify.com kostenlos registrieren.
2. „Add new site“ → „Deploy manually“ → den entpackten Ordner per Drag & Drop hineinziehen.
3. Netlify zeigt dir sofort die fertige Adresse an.

## Auf dem Handy installieren

- **iPhone (Safari):** Adresse öffnen → Teilen-Symbol → „Zum Home-Bildschirm“.
- **Android (Chrome):** Adresse öffnen → Menü (⋮) → „App installieren“.

Danach startet KI-Draht wie eine normale App vom Startbildschirm – auf jedem Gerät, auf dem du sie so hinzufügst.

## Was die App kann

- **Aktualisieren (⟳):** ruft alle Quellen ab und mischt die Meldungen chronologisch.
- **Kategorien:** Alle · Firmen · Medien · Deutsch · Forschung · ★ Merkliste.
- **Übersetzen:** Jede englische Meldung hat einen „Übersetzen“-Knopf (Titel + Zusammenfassung auf Deutsch, jederzeit zurück zum Original). Übersetzungen werden gespeichert und kosten beim zweiten Mal keine Anfrage mehr.
- **Merken (★):** legt Meldungen in die Merkliste.
- **Suche:** durchsucht Titel, Zusammenfassungen und Übersetzungen.
- **Einstellungen (⚙):** Quellen ansehen, löschen, eigene RSS-Feeds hinzufügen, Standard wiederherstellen. Grüner/roter Punkt zeigt, ob eine Quelle beim letzten Abruf erreichbar war.
- **Hell/Dunkel (◐):** Farbschema umschalten.

## Offline-Verhalten (wichtig)

- Die App selbst und der **zuletzt geladene Stand** (bis zu 250 Meldungen) sind offline immer lesbar.
- **Neue Meldungen laden**, **Übersetzen** und **Artikel öffnen** brauchen naturgemäß eine Internetverbindung.
- Die Kopfzeile zeigt dir jederzeit „OFFLINE · STAND …“, wenn du ohne Netz liest.

## Gut zu wissen

- **Übersetzung:** läuft über den Gratis-Dienst MyMemory. Der hat ein Tageslimit – für das Übersetzen einzelner Meldungen reicht es locker, für „alles auf einmal“ nicht. Deshalb übersetzt die App bewusst pro Meldung auf Knopfdruck.
- **Feed-Abruf:** Viele Seiten erlauben keinen direkten Abruf aus dem Browser (CORS). Die App probiert deshalb automatisch mehrere Wege (direkt → rss2json → allorigins → corsproxy). Sind Gratis-Proxys gerade ausgelastet, kann eine Quelle mal rot aufleuchten – einfach später erneut aktualisieren.
- **Tote Quellen:** RSS-Adressen ändern sich mit der Zeit. Bleibt eine Quelle dauerhaft rot, in den Einstellungen löschen und die neue Feed-Adresse der Seite eintragen (meist zu finden unter „RSS“ im Footer der jeweiligen Website).
- **Datenschutz:** Alle Daten (Meldungen, Merkliste, Übersetzungen, Quellen) liegen nur lokal in deinem Browser.

## Dateien

- `index.html` – die komplette App (HTML, CSS, JavaScript)
- `sw.js` – Service Worker für die Offline-Fähigkeit
- `manifest.webmanifest` – macht die Seite als App installierbar
- `icon-192.png`, `icon-512.png` – App-Symbole
