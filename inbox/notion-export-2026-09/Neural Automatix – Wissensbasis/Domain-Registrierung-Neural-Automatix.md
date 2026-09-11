# Domain-Registrierung-Neural-Automatix

Bereich: C-Betrieb
Schutzklasse: intern
Soll-Knoten: C-Struktur
Status: Draft

# Domain-Registrierung & Betrieb – Neural Automatix (Checkliste)

**Erstelldatum (fix):** 12.07.2026, 00:06 (Europe/Berlin)

**Letzte Aktualisierung:** 12.07.2026, 00:06 (Europe/Berlin)

**Status:** Draft (Handlungs-Checkliste)

**Zweck:** Entscheidungs- und Handlungsgrundlage, um den Domainnamen [neuralautomatix.ai](http://neuralautomatix.ai) (plus Nebendomains) zu registrieren und anschließend auf dem Hetzner-Server in Betrieb zu nehmen. **Registrar-Entscheidung ist getroffen: Spaceship** (günstigster .ai-Preis, transparente Preise ohne Upsells). Ersetzt das Zurücksuchen im Chatverlauf.

**Fehlt (kurz):** Finale Registrar-Wahl + finalen Preis an der Kasse verifizieren (Preise ändern sich quartalsweise) + IP-Adresse des Hetzner-Servers für den A-Record bereithalten.

**KI-Referenz:** DOMAIN-REGISTRIERUNG-BETRIEB-NEURAL-AUTOMATIX

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 12.07.2026, 00:06 (Europe/Berlin) | Initiale Checkliste; Weg "extern registrieren, bei Hetzner betreiben" |
| 12.07.2026, 00:10 (Europe/Berlin) | Registrar-Entscheidung nachgetragen: Spaceship (getroffen Fr, 10.07.2026) |

Standard: siehe Dokumentations-Styleguide (Global). Preise sind Momentaufnahmen (~2026) und vor Kauf zu verifizieren. Keine Rechts-/Vertragsberatung.

## Zielsetzung

ID: DOM-ZIEL-0001

- Name [**neuralautomatix.ai**](http://neuralautomatix.ai) bei einem externen Registrar registrieren.
- Domain anschließend auf dem **Hetzner-Server** (bestehendes Ubuntu-System) in Betrieb nehmen.
- Optional Nebendomains [**neuralautomatix.de**](http://neuralautomatix.de) und **.eu** (Marken-/Namensschutz).

## Registrar-Preisvergleich (.ai, ~2026)

ID: DOM-PREISE-0001

.ai wird fast überall nur für **2 Jahre** registriert/verlängert. Relevante Zahl ist die Verlängerung, nicht der Erstpreis.

| Registrar | .ai-Preis (2 Jahre) | Hinweis |
| --- | --- | --- |
| **Spaceship** ✓ | ~137,96 $ | **GEWÄHLT** – günstigster, Reg. = Verlängerung, keine Upsells |
| Porkbun | ~144,80 $ | transparent, freie WHOIS-Privacy, breite TLD-Abdeckung |
| Dynadot | ~149,80 $ | Reg. = Verlängerung, viele Extras |
| Namecheap | ~159,96 $ (Verl. ~179,96 $) | breite TLD-Abdeckung |
| hosttech (DE) | ~116,90 €/Jahr | "günstigster in DE" laut Eigenangabe |
| Hetzner | ~136,85 €/2 Jahre | via konsoleH; alles bei einem Anbieter mit Server |
| Cloudflare | Registry-Selbstkostenpreis | ccTLD .ai vorher auf Verfügbarkeit prüfen; .de wird meist nicht geführt |

Meiden für Neuregistrierung: GoDaddy (aggressive Verlängerungserhöhungen).

## .ai-Besonderheiten (wichtig)

ID: DOM-AI-REGELN-0001

- **2-Jahres-Pflicht:** Registrierung und Verlängerung nur für 2 Jahre; Kündigung nur zum Ende der Periode.
- **Keine Umlaute, keine Leerzeichen, keine Sonderzeichen** im Namen. Länge 2–63 Zeichen, Buchstaben/Zahlen/Bindestriche.
- Konsequenz für den Namen: [**neuralautomatix.ai**](http://neuralautomatix.ai) (zusammengeschrieben, klein) – im Fließtext bleibt die Marke "Neural Automatix" (zwei Wörter).
- "Reservieren" im unverbindlichen Sinn gibt es nicht – die Domain wird registriert (gekauft) oder nicht.

## Weg: extern registrieren, bei Hetzner betreiben

ID: DOM-BETRIEB-0001

Registrar (Domain-Eigentum/Verwaltung) und Hosting (Server) müssen nicht beim selben Anbieter liegen. Ablauf:

1. **Registrieren** beim gewählten externen Registrar (Marke/Domain wurde bereits als frei geprüft).
2. **WHOIS-Privacy** aktivieren (bei den empfohlenen Registraren kostenlos) – Schutz der Inhaberdaten.
3. **DNS auf Hetzner zeigen** – zwei Varianten:
    - a) **A-Record** beim Registrar auf die IP-Adresse des Hetzner-Servers setzen (einfachste Variante). Für www zusätzlich A- oder CNAME-Record.
    - b) **Nameserver auf Hetzner umstellen** (Domain in Hetzner Console/konsoleH als Zone anlegen, dann die Hetzner-Nameserver beim Registrar eintragen). Sinnvoll, wenn die gesamte DNS-Verwaltung bei Hetzner liegen soll.
4. **Propagation abwarten:** DNS-Änderungen sind i. d. R. nach einigen Stunden, spätestens 24–48 h weltweit aktiv.
5. **TLS/HTTPS** auf dem Server einrichten (z. B. Let's Encrypt) – passt zur bestehenden Reverse-Proxy-Konfiguration.

## Alternative: direkt bei Hetzner registrieren

ID: DOM-HETZNER-0001

Falls "alles an einem Ort" gewünscht: Hetzner registriert .ai über **konsoleH** (~136,85 €/2 Jahre) und .de/.eu über den **Domain-Robot**. Vorteil: Domain, DNS und Server in einem Konto, kein externer DNS-Schritt nötig. Nachteil: kein Preisvergleichs-Vorteil gegenüber den günstigsten externen Anbietern. Diese Option ist gleichwertig – die Wahl ist eine Abwägung zwischen minimalem Preis (extern) und minimaler Verwaltung (alles bei Hetzner).

## Nebendomains

ID: DOM-NEBEN-0001

- **.de** und **.eu** als Namens-/Markenschutz registrieren (günstig, meist einstellig bis niedrig zweistellig pro Jahr).
- Hinweis zur Registrar-Wahl: Spaceship (für .ai gewählt) hat eine schmalere TLD-Abdeckung. Prüfen, ob Spaceship .de führt. Falls nicht, zwei praktikable Wege: (a) .de/.eu direkt bei Hetzner über den Domain-Robot registrieren (du bist ohnehin Hetzner-Kunde), oder (b) bei einem breiten Registrar wie Namecheap/Porkbun. Getrennte Anbieter für .ai und .de sind unproblematisch.
- Empfehlung: als Weiterleitung auf die Hauptdomain einrichten, damit niemand den Namen unter anderer Endung besetzt (konsistent mit IP-Schutz-Konzept G8).
- Naheliegende Falschschreibungen (z. B. "automatics"/"automatiks") bedenken – nicht zwingend kaufen, aber bewusst entscheiden.

## Handlungsreihenfolge

ID: DOM-NEXT-0001

1. Registrar final wählen (Preis vs. Verwaltung).
2. Hetzner-Server-IP bereithalten (für A-Record) bzw. Zone in Hetzner anlegen (für Nameserver-Variante).
3. [neuralautomatix.ai](http://neuralautomatix.ai) registrieren, WHOIS-Privacy an.
4. DNS auf Hetzner zeigen (A-Record oder Nameserver).
5. .de/.eu registrieren, Weiterleitung einrichten.
6. TLS/HTTPS auf dem Server für die neue Domain einrichten.
7. Beleg der Registrierung (Datum/Screenshot) für den Prioritätsnachweis aufbewahren (G8).