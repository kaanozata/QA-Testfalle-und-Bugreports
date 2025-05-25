
# Testfall – API Login

## Ziel  
Überprüfung der Login-API auf korrektes Verhalten bei gültigen und ungültigen Eingaben.

---

## API-Informationen

- **Methode:** POST  
- **URL:** `https://example.com/api/login`  
- **Content-Type:** `application/json`

---

## Positiver Test

### Beschreibung  
Ein Benutzer mit gültigen Anmeldedaten sendet eine Anfrage.

### Request Body

```json
{
  "email": "testuser@mail.com",
  "password": "Test1234!"
}
```

### Erwartung

- Status Code: `200 OK`
- Response enthält: `token`, `user_id`, `expires_in`

---

## Negativer Test 1 – Ungültige E-Mail

### Beschreibung  
Login mit nicht registrierter E-Mail-Adresse.

```json
{
  "email": "falsch@mail.com",
  "password": "Test1234!"
}
```

### Erwartung

- Status Code: `401 Unauthorized`
- Response: `{"error": "Ungültige Anmeldedaten"}`

---

## Negativer Test 2 – Leere Felder

### Beschreibung  
E-Mail und/oder Passwort fehlen.

```json
{
  "email": "",
  "password": ""
}
```

### Erwartung

- Status Code: `400 Bad Request`
- Response: `{"error": "Felder dürfen nicht leer sein"}`

---

## Testumgebung

- Testsystem: Staging
- Authentifizierung: Keine Token erforderlich
- Tool: Postman oder REST-Client
- Datenbank: Testdatenbank mit Dummy-User

---

**Datum:** 24. Mai 2025
