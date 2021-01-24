# Milestones

## Module[¶](milestones.md#module) <a id="module"></a>

> [➡ **Details**](https://pandainfo.github.io/community/wiki/de/Module/Ziele)

Das Projekt wird in fünf Module oder Milestones unterteilt. Jedes Modul wiederum besteht aus mehreren Entwicklungsphasen.

1. [Prototyp](milestones.md#prototyp)
2. [Theme-Entwicklung](milestones.md#theme-entwicklung)
3. [CRM-System](milestones.md#crm-system)
4. [Produktimporter](milestones.md#produktimporter)
5. [EDI-Schnittstelle](milestones.md#edi-schnittstelle)
6. [Kalkulation](milestones.md#kalkulation)

### Prototyp[¶](milestones.md#prototyp) <a id="prototyp"></a>

> [➡ **pandastic.press**](https://pandastic.press/)

Konzeption, Installation und öffentliche Demo-Version eines Webshops mit Default-Theme und ohne Schnittstellen für CRM-System, Produktimport \(ONIX\) und B2B-Bestellung \(EDI\).

*  Öffentliche Beta zum Testen durch die Community samt Staging-Instanz
*  Suche, Darstellung und Bestellung von Büchern \(Artikel\)
*  Als SKU / Artikelnr. soll die ISBN/EAN verwendet werden.
*  Zudem existieren Artikel ohne ISBN/EAN wie antiquarische Bücher oder Büchergutscheine.
*  Anbindung zu SumUp, PayPal, Klarna und Stripe für die Bezahlung
*  Module und Themes müssen FLOSS-Software sein.
*  Freie Software / "Open Source": GPL, AGPL, MIT, Apache 2.0 etc.
*  Für Prototyp optional \(reicht in einem späteren Schritt\):
*  CRM
*  Kassensystem
*  ERP/WaWi
*  FiBU

### Theme-Entwicklung[¶](milestones.md#theme-entwicklung) <a id="theme-entwicklung"></a>

> [➡ **pandastic-Theme**](https://github.com/pandainfo/pandastic)

*  Light und Dark Theme mit roter Akzentfarbe \(Secondary\)
*  [Material Design for Bootstrap](https://mdbootstrap.com/)
*  Customized Header samt [Karussell](https://www.w3schools.com/bootstrap/bootstrap_ref_js_carousel.asp) auf allen [Seiten](https://pandainfo.github.io/community/wiki/de/Module/Seiten)
*  Statische Landing Page

### CRM-System[¶](milestones.md#crm-system) <a id="crm-system"></a>

> [➡ **Details**](https://pandainfo.github.io/community/wiki/de/Module/CRM)

*  Konzeption, Installation und Demo-Version eines CRM-Systems
*  Erfassung von Kundenaccounts
*  Newsletter-Verwaltung für Marketingkampagnen und Veranstaltungseinladungen
*  Social-Media-Marketing \(Facebook, Instagram, Google, Twitter, Yelp\)
*  Bestellmanagement

### Produktimporter[¶](milestones.md#produktimporter) <a id="produktimporter"></a>

> [➡ **Details**](https://pandainfo.github.io/community/wiki/de/Module/Produktimport)

*  Ablage von Artikeln in einer eigenen MySQL-Datenbank mit und ohne ISBN/EAN
*  Import von Büchern via ONIX-Schnittstelle
*  Import von Metadaten \(Titelbilder, Klappentexte, Preise
*  Bestandskatalog der Auslieferungen samt Meldenummern

### EDI-Schnittstelle[¶](milestones.md#edi-schnittstelle) <a id="edi-schnittstelle"></a>

> [➡ **Details**](https://pandainfo.github.io/community/wiki/de/Module/Buchbestellungen)

*  Automatischer Datenaustausch bei Bestellungen via [EDI-Schnittstelle](https://www.seeburger.com/de/info/was-ist-edifact/)
*  Implementierung der [EDIfact-Nachrichtentypen](http://www.unece.org/trade/untdid/d10b/trmd/trmdi1.htm) ORDERS, ORDRSP, INVOIC, DESADV
*  Bereitstellung elektronischer Lieferscheine \(ELS\) via FTP, E-Mail etc.
*  Abfrage von Katalogdaten und Bestandsdaten bei der Auslieferung
*  Einbindung einer gängigen EDIfact-Bibliothek für [PHP](https://packagist.org/package/search?query=EDIFACT) oder [JS](https://asset-packagist.org/package/search?query=EDIFACT&platform=bower%2Cnpm) \(für Parser & Generator\)
*  Referenz: [Tools to process EDI messages in UN/EDIFACT format](https://github.com/php-edifact/edifact)

### Kalkulation[¶](milestones.md#kalkulation) <a id="kalkulation"></a>

Die Module werden hintereinander abgearbeitet. Die Projektlaufzeit beträgt zwei Jahre.

| **ID** | **Beschreibung** | **Menge** | **Einzelpreis** | **Gesamtpreis** |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Prototyp | 10,00 Std. | 40,00 EUR | 400,00 EUR |
| 2 | Theme | 20,00 Std. | 40,00 EUR | 800,00 EUR |
| 3 | CRM | 10,00 Std. | 40,00 EUR | 400,00 EUR |
| 4 | Importer | 20,00 Std. | 40,00 EUR | 800,00 EUR |
| 5 | EDI-Modul | 345,00 Std. | 40,00 EUR | 13.800,00 EUR |
| – | Budgetrahmen | 405,00 Std. | exkl. 20% USt. | 16.200,00 EUR |

 Last update: January 22, 2021

