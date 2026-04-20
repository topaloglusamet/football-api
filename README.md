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
GET https://samettopaloglu.com/futbol.php?date=15/04/2026
```

---

### 🔍 Single Match Details

Retrieve detailed information for a specific match using its ID.

```http
GET https://samettopaloglu.com/futbol.php?date=15/04/2026&id=4453644
```

---

### 📊 Match Statistics (Opta)

Retrieve detailed player and team statistics for a specific match.

```http
GET https://samettopaloglu.com/futbol.php?id=4453644&stats=1
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
GET https://samettopaloglu.com/futbol.php?op=years&group=22
```

**Sub-Leagues (Competitions)**
Retrieve all sub-leagues and competitions under a category for a given year to find the required `leagueId`.

```http
GET https://samettopaloglu.com/futbol.php?op=leagues&group=22&year=2025/2026
```

<details>
<summary>View Response Example</summary>

```json
{
    "l": [
        {
            "league": 70870,
            "leagueName": "Lig Aşaması"
        }
    ]
}
```
</details>

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
GET https://samettopaloglu.com/futbol.php?op=team&id=79&season=2025/2026&fixtures=1
```

---

## 📝 License & Author

Developed by **[Samet Topaloğlu](https://samettopaloglu.com)**.
This project is licensed under the MIT License.
