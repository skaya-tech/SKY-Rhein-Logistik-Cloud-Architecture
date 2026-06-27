# 🛡️ Phase 1: Identitäts- und Zugriffsverwaltung (ISO 27001 A.9)

Willkommen in Phase 1 des Cloud-Transformationsprojekts der **SKY-Rhein-Logistik GmbH**. 

In dieser Phase legen wir das wichtigste Fundament für die Cloud-Sicherheit: die digitale Identität und die Unternehmensführung (Governance). Bevor wir physische Server oder Netzwerke aufbauen, müssen wir genau definieren, **wer** auf **welche** Ressourcen zugreifen darf und **wie** diese Ressourcen verwaltet werden.

Alle technischen Implementierungen in dieser Phase basieren auf dem "Zero Trust"-Modell (Vertraue niemandem) und sind direkt mit den Prüfstandards der **ISO 27001 (Annex A.9 - Zugangssteuerung)** verknüpft.

---

## ⚖️ ISO 27001 ISMS-Compliance

Die Konfigurationen in dieser Phase erfüllen die folgenden ISO-Sicherheitskontrollen:

* **A.9.1.1 Zugangssteuerungspolitik:** Durch den Einsatz von *Azure Policy* und *Role-Based Access Control (RBAC)* wird sichergestellt, dass Zugriffsrechte nach dem Prinzip der "geringsten Privilegien" (Least Privilege) vergeben werden.
* **A.9.2.1 Benutzerregistrierung und -abmeldung:** Die Erstellung von Cloud-Benutzern (interne Mitarbeiter) und die sichere Einladung von externen Logistikberatern über *Azure B2B (Guest Accounts)*.
* **A.9.2.2 Bereitstellung des Benutzerzugangs:** Berechtigungen werden niemals einzelnen Benutzern, sondern immer zentral über *Sicherheitsgruppen (Security Groups)* zugewiesen.

---

## 🛠️ Technische Umsetzung & Laborarbeiten

Diese Phase ist entsprechend unserem Projektzeitplan in verschiedene Kurse (AZ-104, MD-102, MS-102) unterteilt. Aktuell befindet sich das Projekt im **Monat 1 (AZ-104)**.

### 🟢 Teil 1: AZ-104 Cloud-Fundament (Aktuell durchgeführt)
Die technischen Beweise (Screenshots) und Automatisierungsskripte für diese Schritte finden Sie im Ordner `Part1-AZ104-Base-Governance/`.

1. **Microsoft Entra ID Identitäten (Lab 01):** * Erstellung von Benutzerkonten für verschiedene Abteilungen (z.B. IT und Flottenmanagement).
   * Aufbau von Sicherheitsgruppen zur zentralen Verwaltung von Rechten.
2. **Abonnements und RBAC (Lab 02a):** * Strukturierung der IT-Umgebung mit *Management Groups*.
   * Zuweisung von benutzerdefinierten RBAC-Rollen, damit Support-Mitarbeiter nur begrenzte Aktionen (wie das Neustarten von virtuellen Maschinen) durchführen können.
3. **Azure Policy und Ressourcensperren (Lab 02b):** * Durchsetzung von Kostenstellen-Tags (`CostCenter: Logistics`) für alle neuen Ressourcen.
   * Aktivierung von Ressourcensperren (*Resource Locks*), um kritische Cloud-Komponenten vor versehentlichem Löschen zu schützen.

---

### ⏳ Zukünftige Integrationen (Monat 2 & 3)

Dieses Repository wird in den kommenden Monaten organisch wachsen. Die folgenden Komponenten werden demnächst hinzugefügt:

* **🟡 Teil 2 (MD-102):** Vorbereitung der Identitäten für die automatische Geräteanmeldung (Windows Autopilot) und Intune-Registrierung. *(Geplant für Monat 2)*
* **🔴 Teil 3 (MS-102):** Synchronisierung der lokalen Server mit der Cloud (AD Connect), Einführung von Multi-Faktor-Authentifizierung (MFA) und Privileged Identity Management (PIM). *(Geplant für Monat 3)*
