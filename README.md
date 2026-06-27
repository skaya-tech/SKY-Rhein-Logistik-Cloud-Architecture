# 🌐 SKY-Rhein-Logistik GmbH: Cloud-Transformation und ISO 27001 ISMS-Architektur

**Projektarchitekt:** S. Kaya

**Projektzeitraum:** Juni 2026 – September 2026

**Schwerpunkte:** Cloud Infrastructure (AZ-104), Modern Endpoint Management (MD-102), Enterprise Security & Compliance (MS-102)

**Compliance-Standard:** ISO/IEC 27001:2022 Information Security Management System (ISMS)

---

## 📌 Projektziel und Vision

Dieses Projekt ist eine umfassende Fallstudie (Case Study). Es beschreibt, wie die europaweit agierende und schnell wachsende **SKY-Rhein-Logistik GmbH** von einer veralteten lokalen (On-Premises) IT-Infrastruktur in ein modernes, sicheres und skalierbares Cloud-Ökosystem (Modern Workplace) wechselt.

Diese Arbeit geht weit über einfache Laborübungen hinaus. Sie vereint die Bereiche Infrastruktur, Geräteverwaltung und Cybersicherheit in einem einzigen, realistischen Unternehmensszenario. Jeder technische Schritt wurde nach dem Prinzip "Security by Design" geplant und direkt in die ISO 27001 ISMS-Prüfstandards (Annex A-Controls) integriert.

---

## ⚠️ Aktuelle Situation und Geschäftsproblem

Die Logistikbranche hat ein sehr komplexes Netzwerk. Es gibt einen ständigen Datenfluss, Tausende von Mitarbeitern im Außendienst und viele externe Lieferanten (wie Zoll und Subunternehmer). Die größten Herausforderungen für SKY-Rhein-Logistik sind:

* **Identitäts- und Zugriffschaos:** Die manuelle Verwaltung von Rechten für Mitarbeiter und externe Berater führt zu Sicherheitslücken und langsamen Abläufen.
* **Nicht verwaltete Geräte (Shadow IT):** Laptops und Tablets der Fahrer und Lagerarbeiter haben keine einheitlichen Sicherheitsrichtlinien.
* **Gefahr von Datenlecks:** Sensible Kundendaten und internationale Frachtverträge sind nicht ausreichend gegen Cyberangriffe (wie Phishing) oder interne Bedrohungen geschützt.
* **Compliance-Verstöße:** Die IT-Systeme sind nicht so aufgebaut, dass sie internationale Informationssicherheitsstandards (wie ISO 27001 oder DSGVO) bei Audits nachweisbar erfüllen.

---

## 💡 Lösungsarchitektur: Die 3 Hauptsäulen

Um diese Probleme zu lösen und das Unternehmen zukunftssicher zu machen, basiert die neue Architektur auf drei Säulen:

### 1. Cloud-Infrastruktur und Kernnetzwerk (AZ-104)

Das digitale Rückgrat des Unternehmens wurde in Azure neu entworfen. Für eine hohe Verfügbarkeit (SLA) wurden Virtual Machine Scale Sets (VMSS) eingerichtet. Für den sicheren Datenverkehr zwischen den Abteilungen haben wir isolierte virtuelle Netzwerke (VNet-Topologien) aufgebaut. Azure Backup und Site Recovery sorgen dafür, dass der Betrieb auch bei Katastrophen nahtlos weiterläuft.

### 2. Modernes Endpunkt- und Flottenmanagement (MD-102)

Alle Geräte, vom Hauptbüro bis zum LKW-Fahrer, werden nun mit Microsoft Intune kontrolliert. Dank Windows Autopilot werden neue Geräte per "Zero-Touch" verteilt. Sobald die Geräte das erste Mal gestartet werden, erhalten sie automatisch die Sicherheitsstandards der Firma (wie BitLocker-Verschlüsselung und den Kiosk-Modus für Tablets).

### 3. Cybersicherheit, Identität und Informationsschutz (MS-102)

In dieser neuen, grenzenlosen Arbeitsumgebung gilt die "Zero Trust"-Philosophie (Vertraue niemandem). Mit Microsoft Entra ID (früher Azure AD) werden alle Benutzerkonten und Sicherheitsgruppen zentral konfiguriert und verwaltet. Externe Lieferanten bekommen über sichere Gastzugänge (B2B) einen kontrollierten Zugang zum System. Gegen externe Bedrohungen setzen wir Microsoft Defender ein, gegen Datenlecks hilft Microsoft Purview (mit Richtlinien zur Verhinderung von Datenverlust und Sensibilitätsbezeichnungen).

---

## ⚖️ ISO 27001 ISMS-Integration

Keine Konfiguration in diesem Portfolio wurde zufällig vorgenommen. Jeder technische Schritt ist mit den Vorgaben aus ISO 27001 Annex A verknüpft. Das Projekt dient somit auch als technischer "Compliance-Bericht":

* **A.9 Zugangssteuerung (Access Control):** Nutzung von Entra ID, rollenbasierter Zugriffskontrolle (RBAC), dynamischen Gruppen und Multi-Faktor-Authentifizierung (MFA).


* **A.10 Kryptographie:** Automatische Verschlüsselung aller Endgeräte mit BitLocker.
* **A.12 & A.13 Betriebs- und Kommunikationssicherheit:** Einsatz von Defender XDR, VNet-Isolation und Richtlinien zur Verhinderung von Datenverlust (DLP).

---

## 📂 Portfolio-Navigation (Phasen)

Damit das Projekt leicht zu lesen und für Audits gut nachvollziehbar ist, wurde es in logische Phasen unterteilt. Jede Phase enthält die technischen Schritte, PowerShell/JSON-Codes für die Automatisierung und Erklärungen zur Fehlerbehebung (Troubleshooting):

* **Phase 1:** Identitäts- und Zugriffsverwaltung (Identity & Access)
* **Phase 2:** Zero-Touch-Gerätebereitstellung und Endpunktsicherheit (Endpoint Management)
* **Phase 3:** Cloud-Infrastruktur, Netzwerk-Isolation und Hochverfügbarkeit (Infrastructure & Networking)
* **Phase 4:** Bedrohungsschutz und Daten-Governance (Threat Protection & Information Governance)
* **Phase 5:** Betriebskontinuität, Überwachung und Notfallwiederherstellung (BCDR & Monitoring)

*(Indem Sie dieses Projekt lesen, können Sie Schritt für Schritt verfolgen, wie ich die digitale Transformation und Sicherheitsarchitektur der SKY-Rhein-Logistik GmbH gestaltet habe.)*
