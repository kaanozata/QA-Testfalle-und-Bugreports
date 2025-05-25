# Testfälle – Login-Formular

Dieses Dokument enthält mehrere Testszenarien für ein typisches Login-Formular mit den Feldern „E-Mail“ und „Passwort“.

---

## 🔹 Test Case 1 – Erfolgreiche Anmeldung

- **Test-ID:** TC001  
- **Beschreibung:** Anmeldung mit gültiger E-Mail und Passwort  
- **Eingabe:**  
  - E-Mail: user@mail.com  
  - Passwort: test123  
- **Erwartetes Ergebnis:** Weiterleitung zum Dashboard

---

## 🔹 Test Case 2 – Leeres E-Mail-Feld

- **Test-ID:** TC002  
- **Beschreibung:** E-Mail-Feld bleibt leer  
- **Eingabe:**  
  - E-Mail: *(leer)*  
  - Passwort: test123  
- **Erwartetes Ergebnis:** Fehlermeldung: „E-Mail erforderlich“

---

## 🔹 Test Case 3 – Leeres Passwort-Feld

- **Test-ID:** TC003  
- **Beschreibung:** Passwort-Feld bleibt leer  
- **Eingabe:**  
  - E-Mail: user@mail.com  
  - Passwort: *(leer)*  
- **Erwartetes Ergebnis:** Fehlermeldung: „Passwort erforderlich“

---

## 🔹 Test Case 4 – Ungültiges E-Mail-Format

- **Test-ID:** TC004  
- **Beschreibung:** E-Mail ohne „@“  
- **Eingabe:**  
  - E-Mail: usermail.com  
  - Passwort: test123  
- **Erwartetes Ergebnis:** Fehlermeldung: „Ungültige E-Mail-Adresse“

---

## 🔹 Test Case 5 – Passwort zu kurz

- **Test-ID:** TC005  
- **Beschreibung:** Passwort hat weniger als 6 Zeichen  
- **Eingabe:**  
  - E-Mail: user@mail.com  
  - Passwort: 123  
- **Erwartetes Ergebnis:** Fehlermeldung: „Passwort zu kurz“

---

## 🔹 Test Case 6 – Beide Felder leer

- **Test-ID:** TC006  
- **Beschreibung:** Keine Eingabe in beiden Feldern  
- **Eingabe:**  
  - E-Mail: *(leer)*  
  - Passwort: *(leer)*  
- **Erwartetes Ergebnis:** Fehlermeldungen für beide Felder

---

## 🔹 Test Case 7 – Nicht registrierter Benutzer

- **Test-ID:** TC007  
- **Beschreibung:** E-Mail existiert nicht im System  
- **Eingabe:**  
  - E-Mail: nicht@existiert.com  
  - Passwort: test123  
- **Erwartetes Ergebnis:** Fehlermeldung: „Benutzer nicht gefunden“

---

**Hinweis:** Die tatsächlichen Systemreaktione können je nach Implementierung leicht variieren.
