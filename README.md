# ⚽ Football API Documentation

Professional, fast, and easy-to-use JSON API providing live scores, match results, standings, and detailed Opta statistics for football enthusiasts and developers.

---

## 🚀 Quick Start
All requests are made to the following base URL:
`https://samettopaloglu.com/futbol.php`

---

## 📋 Endpoints

### 1. Daily Match List
Retrieve all matches for a specific date.
- **Request:** `GET /futbol.php?date=DD/MM/YYYY`
- **Example:** `https://samettopaloglu.com/futbol.php?date=09/02/2026`

<details>
<summary>View Response Example</summary>

```json
{
    "date": "09/02/2026",
    "matches": [
        {
            "id": 4308508,
            "home": "Kayserispor",
            "homeGoals": 1,
            "away": "Kocaelispor",
            "awayGoals": 2,
            "status": "MS",
            "score": "1-2",
            "matchTime": "17:00",
            "matchDate": "09/02/2026",
            "leagueName": "Türkiye",
            "leagueType": "Süper Lig",
            "detailUrl": "https://arsiv.mackolik.com/Match/Default.aspx?id=4308508"
        }
    ]
}
```
</details>

---

### 2. Single Match Details
Retrieve detailed information for a specific match using its ID.
- **Request:** `GET /futbol.php?date=DD/MM/YYYY&id={matchId}`
- **Example:** `https://samettopaloglu.com/futbol.php?date=09/02/2026&id=4308507`

---

### 3. Match Statistics (Opta)
Retrieve detailed player and team statistics (Opta data) for a specific match.
- **Request:** `GET /futbol.php?id={matchId}&stats=1`
- **Example:** `https://samettopaloglu.com/futbol.php?id=4308507&stats=1`

---

### 4. Archive & League Data
Access historical data, competition categories, and standings.

#### Categories (Groups)
- **Request:** `GET /futbol.php?op=groups`
- **Returns:** List of supported countries and global groups (e.g., Turkey ID: 1).

#### League Table (Standings)
- **Request:** `GET /futbol.php?op=table&league={leagueId}`
- **Example:** `https://samettopaloglu.com/futbol.php?op=table&league=70381`

#### Weekly Fixtures
- **Request:** `GET /futbol.php?op=fixtures&league={leagueId}&week={weekNum}`
- **Example:** `https://samettopaloglu.com/futbol.php?op=fixtures&league=70381&week=25`

---

### 5. Team Information
Detailed squad data, player market values, and statistics.

#### Team Squad & Basic Stats
- **Request:** `GET /futbol.php?op=team&id={teamId}&season={season}`
- **Example:** `https://samettopaloglu.com/futbol.php?op=team&id=2&season=2025/2026`

#### Full Season Fixtures & Performance
- **Request:** `GET /futbol.php?op=team&id={teamId}&season={season}&fixtures=1`
- **Example:** `https://samettopaloglu.com/futbol.php?op=team&id=2&season=2025/2026&fixtures=1`

<details>
<summary>View Response Example</summary>

```json
[
    {
        "competition": "Türkiye Süper Lig",
        "fixtures": [
            {
                "date": "16.08.2025",
                "home": "Göztepe",
                "score": "0 - 0",
                "away": "Fenerbahçe",
                "matchId": "4308334",
                "stats": {
                    "possessionPercentage": "60",
                    "shots": "12",
                    "shotsOnTarget": "1",
                    "passPercentage": "85",
                    "accuratePasses": "337"
                }
            }
        ]
    }
]
```
</details>

---

## ⚠️ Error Handling
The API returns a JSON object with an `error` key if a request fails:
- `{"error": "Date parameter is required."}`
- `{"error": "Invalid date format."}`
- `{"error": "Failed to retrieve Opta data."}`

---

## 📝 License
Built by [Samet Topaloğlu](https://samettopaloglu.com). This project is MIT licensed.

---
*Last Updated: April 2026*
