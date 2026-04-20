# ⚽ Football Data API Documentation

Professional, fast, and easy-to-use Football Data API providing live scores, match results, standings, and detailed Opta statistics in JSON format.

## 🚀 Key Features
- **Live Scores:** Real-time updates for ongoing matches.
- **Detailed Stats:** Opta-powered player and team statistics.
- **Historical Data:** Archive access for past seasons and leagues.
- **Bilingual:** Fully supports Turkish and English documentation.
- **Clean JSON:** Optimized and sanitized response for developers.

## 📖 Access the Documentation
You can view the interactive documentation here:
[https://samettopaloglu.com/futboldoc.html](https://samettopaloglu.com/futboldoc.html)

## 📋 API Endpoints

### 📅 Daily Match List
Retrieve all matches for a specific date.
```http
GET https://samettopaloglu.com/futbol.php?date=DD/MM/YYYY
```

---

### 🔍 Single Match Details
Retrieve detailed information for a specific match using its ID.
```http
GET https://samettopaloglu.com/futbol.php?date=DD/MM/YYYY&id={matchId}
```

---

### 📊 Match Statistics (Opta)
Retrieve detailed player and team statistics for a specific match.
```http
GET https://samettopaloglu.com/futbol.php?id={matchId}&stats=1
```

---

### 🌍 Archive & League Data

**Categories (Groups)**
Retrieve a list of supported countries and groups.
```http
GET https://samettopaloglu.com/futbol.php?op=groups
```

**Season Years**
Get available historical seasons for a specific group.
```http
GET https://samettopaloglu.com/futbol.php?op=years&group=1
```

**League Standings (Table)**
Get the detailed league table for a given competition.
```http
GET https://samettopaloglu.com/futbol.php?op=table&league={leagueId}
```

**Weekly Fixtures**
Get match schedules for a specific league and week.
```http
GET https://samettopaloglu.com/futbol.php?op=fixtures&league={leagueId}&week={weekNum}
```

---

### 🛡️ Team Information

**Team Squad & Market Values**
Retrieve detailed squad data and average age for a team.
```http
GET https://samettopaloglu.com/futbol.php?op=team&id={teamId}&season=2025/2026
```

**Team Full History & Performance**
Get the entire season's matches, results, and Opta performance metrics.
```http
GET https://samettopaloglu.com/futbol.php?op=team&id={teamId}&season=2025/2026&fixtures=1
```

---

## ⚠️ Error Responses
Standard error format for failed requests:

```json
{ "error": "Date parameter is required." }
{ "error": "Invalid date format." }
{ "error": "Data not found / Service blocked." }
```

## 📝 License & Author
Developed by **[Samet Topaloğlu](https://samettopaloglu.com)**.
This project is licensed under the MIT License.
