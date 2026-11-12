# Fitlog

**Ernährungstagebuch, Gewichtsverlauf, Training und Körperwerte – in einer App, ehrlich und ohne Druck.**

Fitlog ist eine private Android-App zum Abnehmen und Fitbleiben. Sie rechnet mit einem **Kalorienbereich statt einer starren Zahl**, bewertet das Gewicht über den **Trend statt über einzelne Tage** und holt Werte von **Waage und Uhr automatisch über Health Connect**. Alle Daten bleiben auf dem Handy.

> In diesem Repository liegen nur die fertigen Installationsdateien (APK). Die App fragt hier nach neuen Versionen.

---

## Inhalt

- [Funktionen](#funktionen)
- [Installation](#installation)
- [Updates](#updates)
- [Erste Schritte](#erste-schritte)
- [Waage und Uhr verbinden](#waage-und-uhr-verbinden-health-connect)
- [Persönlicher KI-Coach (optional)](#persönlicher-ki-coach-optional)
- [Probleme lösen](#probleme-lösen)
- [Datenschutz](#datenschutz)
- [Quellen und Lizenzen](#quellen-und-lizenzen)

---

## Funktionen

### Tagebuch
- Frühstück, Mittag, Abend, Snacks mit kcal, Eiweiß, Kohlenhydraten und Fett.
- Mengen **in Gramm oder als Portion** (Scheibe, Löffel, Handvoll, Stück …).
- **Roh oder gegart:** Bei Nudeln, Reis und Fleisch fragt die App, wie gewogen wurde, und rechnet richtig um.
- **Favoriten mit einem Tipp**, Mahlzeit von gestern übernehmen, Schnelleintrag (z. B. Restaurant).
- **Barcode-Scanner** und Suche in über 7.000 Lebensmitteln (offline) plus Open Food Facts.
- **Essen per Foto schätzen** (Google Gemini kostenlos oder ChatGPT): Teller fotografieren, Bestandteile prüfen, eintragen.
- Kalorien- und Eiweißbalken mit **Orientierungsbereich**; an Trainingstagen steigt der Bereich um das erfasste Training.

### Verlauf
- Gewicht mit **7-Tage-Schnitt**, **Montagswert als offiziellem Wochenwert**, Trend pro Woche und Ziellinie.
- **Diagramme zum Ziehen:** Finger aufs Diagramm legen und seitlich ziehen – Datum und Werte werden angezeigt.
- Kalorien und Eiweiß für 14, 30 oder 90 Tage.
- **Körperzusammensetzung** von der Waage: Körperfett, Muskelmasse, Viszeralfett, fettfreie Masse, Körperwasser, Protein, Knochen, Grundumsatz, Stoffwechselalter – mit 4-Wochen-Veränderung und Verlauf.
- **Schritte, Schlaf und Ruhepuls** von der Uhr.
- Mehrere Gewichte oder einen ganzen Tagebuch-Text auf einmal einfügen (z. B. aus einer alten Liste).

### Training
- Vorlagen mit einem Tipp, eigene Einheiten, **Uhrzeit je Trainingstag**.
- **Übersicht:** Kalender der Trainingstage, Wochenbalken, „Plan erfüllt“, Serie.
- **Trainings der Uhr übernehmen** – auf Knopfdruck, damit nichts doppelt zählt.

### Coach
- Kurze, sachliche Hinweise – offline und regelbasiert.
- Lob nur, wenn es begründet ist; deutlich zu wenig essen wird nie gelobt.
- **Kein Drängen:** weder zum Mehressen noch zum weiteren Kürzen wegen einer Rechengröße.
- Bei kurzem Stillstand: beobachten statt Kalorien senken. Tageswerte sind Orientierung, der Trend zählt.

### Sonstiges
- Helles und dunkles Design, komplett auf Deutsch.
- Sicherung als Datei (Export/Import).
- **Automatische Updates** über dieses Repository.

---

## Installation

1. Auf dem Android-Handy die neueste Version öffnen: **[Releases → Latest](../../releases/latest)**
2. Unter *Assets* auf **`Kalorienwaage-handy.apk`** tippen und herunterladen.
3. Datei öffnen. Beim ersten Mal fragt Android, ob der Browser Apps installieren darf → **Einstellungen → „Aus dieser Quelle zulassen“** → zurück → **Installieren**.
4. Warnt Google Play Protect, dass die App unbekannt ist: **„Trotzdem installieren“**. (Die App stammt nicht aus dem Play Store.)

**Voraussetzungen:** Android 8.0 oder neuer, ein aktuelles Handy mit 64-Bit-Prozessor (arm64 – praktisch alle Geräte der letzten Jahre).

> Der Dateiname enthält noch den früheren Namen „Kalorienwaage“ – das ist Absicht, damit automatische Updates weiter funktionieren.

---

## Updates

- Fitlog prüft beim Öffnen (höchstens alle 3 Stunden), ob es hier eine neuere Version gibt, und zeigt dann **„Neue Version …“**.
- Jederzeit manuell: **Profil → Daten → „Nach Updates suchen“**.
- **Herunterladen → Datei antippen → Aktualisieren.** Alle Daten und Einstellungen bleiben erhalten.
- Was sich geändert hat, steht bei jeder Version unter [Releases](../../releases).

---

## Erste Schritte

Beim ersten Start fragt Fitlog Größe, Geburtsjahr, Geschlecht, aktuelles Gewicht und das gewünschte Abnehmtempo ab. Daraus berechnet die App einen **Startplan**:

- **Kalorienbereich am Ruhetag** (Mifflin-St Jeor, leichte Alltagsaktivität, abzüglich des Wochenziels) – mit sinnvoller Untergrenze.
- **Eiweißziel und -minimum** (ca. 1,5 g je kg Bezugsgewicht).

Alles lässt sich unter **Profil** anpassen. Nach 2–3 Wochen lohnt ein Blick in den Verlauf: Passt die Abnahme zum Ziel, ist der Bereich richtig.

---

## Waage und Uhr verbinden (Health Connect)

Fitlog **liest** Werte aus **Health Connect**, dem Gesundheitsdatenspeicher von Android. Fitlog schreibt dort nichts hinein.

### Verbinden
**Profil → Waage & Uhr → „Verbinden“** und im Fenster **„Alle zulassen“**, dazu **„Vergangene Daten“** und **„Im Hintergrund“** erlauben. Ohne „Vergangene Daten“ sieht die App nur die letzten 30 Tage.

### Waage (z. B. Lepulse mit der App Fitdays)
1. In **Fitdays → Ich → Einstellungen → Health Connect** die Weitergabe einschalten.
2. **Wichtig:** Fitdays überträgt nur **neue** Messungen. Einmal auf die Waage stellen, dann erscheint die Messung in Fitlog.
3. **Älterer Verlauf:** In Fitdays den Verlauf exportieren (Export-Symbol, „Alle“) und in Fitlog unter **Verlauf → Körperzusammensetzung → „Fitdays-Export importieren …“** die Datei aus dem Ordner *Documents* wählen.
4. Körperfett, Muskeln usw. misst die Waage nur **barfuß mit trockenen Füßen**.

Pro Tag zählt die **erste Messung** (morgens nüchtern). **Selbst eingetragene Gewichte werden nie überschrieben.**

**Falsche Messung** (z. B. hat jemand anderes auf der Waage gestanden): **Verlauf → Körperzusammensetzung → Messungen → Mülleimer**. Die Messung wird gelöscht und beim nächsten Abgleich übersprungen. Andere Personen sollten in Fitdays ein eigenes Profil anlegen.

### Uhr (z. B. Galaxy Watch über Samsung Health)
- **Schritte** erscheinen im Tagebuch und im Verlauf – sie gehören zum Alltagsverbrauch und **erhöhen den Kalorienbereich nicht**.
- **Trainings der Uhr** erscheinen mit einem **„+ kcal“-Knopf** zum Übernehmen (oder „Ausblenden“, wenn schon selbst eingetragen).
- **Schlaf und Ruhepuls** im Verlauf.
- In **Samsung Health → Einstellungen → Verbundene Apps und Dienste → Health Connect** müssen Schritte, Training, Schlaf und Herzfrequenz zum Schreiben freigegeben sein.

Abgeglichen wird beim Öffnen der App und einmal täglich im Hintergrund. Manuell: **Profil → Waage & Uhr → „Jetzt abgleichen“**.

---

## Persönlicher KI-Coach (optional)

Der Coach funktioniert immer offline. Zusätzlich kann ein **persönlicher Kommentar** und die **Fotoschätzung** über einen KI-Anbieter laufen – mit eigenem Schlüssel unter **Profil → Persönlicher Coach**:

| Anbieter | Kosten | Schlüssel |
|---|---|---|
| **Google Gemini** (empfohlen) | kostenlos | aistudio.google.com/apikey |
| **Groq** | kostenlos | console.groq.com/keys |
| **ChatGPT (OpenAI)** | nach Verbrauch, Guthaben nötig* | platform.openai.com/api-keys |
| **Claude (Anthropic)** | nach Verbrauch, Guthaben nötig* | console.anthropic.com |

\* Ein ChatGPT- oder Claude-Abo enthält **keine** API-Nutzung; das wird separat abgerechnet.

„Verbindung testen“ zeigt sofort, ob Schlüssel und Modell passen. Gesendet wird nur auf Knopfdruck – eine kurze Zahlenzusammenfassung bzw. das Foto.

---

## Probleme lösen

**Schritte in Fitlog niedriger als in Samsung Health**
Fitlog zeigt, was in Health Connect steht. Prüfen unter *Einstellungen → Health Connect → Daten und Zugriff → Aktivität → Schritte*: Steht dort dieselbe niedrige Zahl, gibt Samsung Health (noch) nicht alles weiter – siehe nächster Punkt.

**Samsung Health oder Fitdays liefern nichts an Health Connect**
- Schreibrechte prüfen: *Health Connect → App-Berechtigungen → Samsung Health bzw. Fitdays*.
- **Akku:** Die App auf **„Nicht eingeschränkt“** stellen (bei einer Uhr auch Galaxy Wearable und das Watch-Plugin).
- **Xiaomi, Redmi, POCO und andere:** zusätzlich **Autostart** erlauben (*Einstellungen → Apps → Apps verwalten → App → Autostart*).
- Danach die App einmal öffnen und ein paar Minuten warten. Samsung Health überträgt auf manchen Handys nur in größeren Abständen.

**Es kommt kein Update-Hinweis**
Fitlog fragt höchstens alle 3 Stunden nach. Sofort geht es über *Profil → Daten → „Nach Updates suchen“*.

**Fotoschätzung meldet „überlastet“ (Gemini)**
Google ist kurz ausgelastet. Die App versucht es automatisch erneut und weicht auf ein leichteres Modell aus; sonst ein paar Minuten warten oder das Modell `flash-lite-latest` wählen.

**Fotoschätzung meldet „Keine Verbindung“**
Internet bzw. VPN prüfen. Die Fehlermeldung nennt den genauen Grund (Zeitüberschreitung, Server nicht gefunden, …).

---

## Datenschutz

- **Alle Daten liegen nur auf dem Handy.** Es gibt kein Konto und keinen Server.
- **Health Connect:** Fitlog liest nur – Gewicht und Körperwerte, Schritte, Trainings, aktive Kalorien, Schlaf und Puls. Berechtigungen lassen sich in Health Connect jederzeit entziehen.
- **Ins Internet** geht nur: die Lebensmittelsuche (Open Food Facts, optional USDA), die Update-Prüfung bei GitHub (ohne persönliche Daten) und – nur auf Knopfdruck – der KI-Kommentar bzw. die Fotoschätzung beim gewählten Anbieter.
- **Sicherung:** *Profil → Daten → Exportieren* speichert alles in eine Datei (ohne API-Schlüssel).

Fitlog ist ein privates Werkzeug und **keine medizinische Beratung**. Kalorienangaben von Uhren und Trainingsgeräten sind Schätzungen und oft zu hoch.

---

## Quellen und Lizenzen

- **Bundeslebensmittelschlüssel (BLS) 4.0** – Max Rubner-Institut (2025), Deutsche Nährstoffdatenbank, Karlsruhe. DOI: [10.25826/Data20251217-134202-0](https://doi.org/10.25826/Data20251217-134202-0). Lizenz: CC BY 4.0
- **Open Food Facts** – Open Database License (ODbL)
- **USDA FoodData Central** – CC0
- Umrechnung roh/gegart: Durchschnittswerte (Nudeln ×2,3, Reis ×2,7, Fleisch ×0,75)
