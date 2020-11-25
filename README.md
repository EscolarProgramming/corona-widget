# Corona Inzidenz Widget für iOS (Scriptable)

Widget zeigt die Inzidenz, tägl. neue Fälle, sowie den Verlauf für 21 Tage an.

![IMG_5438](https://raw.githubusercontent.com/rphl/corona-widget/master/screenshots/screenshot.jpg)

_Dank der positiven Resonanz, jetzt im Repo zur einfacheren Wartung/Erweiterung ( [Mein original GIST](https://gist.github.com/rphl/0491c5f9cb345bf831248732374c4ef5) ) Feedback, PRs, etc. sind Willkommen._

**☕️ Einen Kaffee ausgeben 🙃:** https://ko-fi.com/rapha

# Features

* _Inzidenz_ + Trend für Stadt/Kreis, Bundesland, Bund
* _Neue tägl. Fälle_ für Stadt/Kreis, Bundesland, Bund
* 21 Tage Diagram für _Neue tägl. Fälle_ je Stadt/Kreis, Bundesland, Bund
* 7 Tage Schätzwert für _Reproduktionszahl (R)_
* iCloud Sync
* Automatischer Offlinemodus
* Dark/Lighmode unterstützung
* Autoupdate (Siehe Installation/Update)
* ...

_ALTE ICLOUD VERSION siehe: https://github.com/rphl/corona-widget/blob/master/incidence_icloud_old.js_

![IMG_5438](https://raw.githubusercontent.com/rphl/corona-widget/master/screenshots/info.jpg)

# Installation/Update

**Manuell**
* Safari öffnen: https://raw.githubusercontent.com/rphl/corona-widget/master/incidence.js
* Skripttext kopieren
* Scriptable öffnen, kopierten Skripttext als neues Scriptablescript einfügen oder altes erstzen.

**Update**
* Das Skript aktualisiert sich im Intervall selbst (Kann via `CFG.scriptSelfUpdate: false` abgestellt werden)
* ...andere Option: https://scriptdu.de/


# Konfiguration

* Daten werden unter **Dateien (App)** > **iCloud** > **Scriptable** > **coronaWidgetNext** > *.json zwischengespeichert.
* Die allgemeine Konfiguration erfolgt mittels **WidgetParameter**:

![IMG_5438](https://raw.githubusercontent.com/rphl/corona-widget/master/screenshots/widgetparameter.jpg)


## Statische Standort Koordinaten

Das Widget erkennt automatisch den Standort. Es ist jedoch möglich den Standort fest zu setzten. Die Koordinaten können z.B. über die Karten App ermittelt werden. Format: `{POSITION},{LAT},{LON};{POSITION},{LAT},{LON}`

* `{POSITION}` = Position im Widget. z.B: 0=ErsterStandrt, 1=ZweiterStandort (Zweispaltes MediumWidget)
* `{LAT}` = Breitengrad. z.B: 51.1234 _(NICHT 51,1234 - Kein Komma!)_
* `{LON}` = Längengrad. z.B: 11.1234 _(NICHT 11,1234 - Kein Komma!)_

**Beispiele**

* Erster Standort statisch (SmallWidget): `0,51.1244,6.7353`
* Zweiter Standort ist statisch (MediumWidget): `1,51.1244,6.7353`
* Beide Standorte sind statisch (MediumWidget): `0,51.1244,6.7353;1,51.1244,6.7353`
* Nur zweiter Standort ist statisch (MediumWidget): `1,51.1244,6.7353`
 

## Eigene Standortnamen

Standorte selbst bennenen. Format: `{POSITION},{LAT},{LON},{NAME};{POSITION},{LAT},{LON},{NAME}`

* `{NAME}` = Name der anstalle der offizielen Bezeichnung aus der API verwendet wird.

**Beispiele**

 * Eigener Name z.B "Home" für den ersten Standort: `0,51.1244,6.7353,Home`
 * Eigener Name z.B "Work" für den zweiten Standort: `1,51.1244,6.7353,Work`

