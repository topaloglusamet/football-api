# ⚽ Football Data API Documentation

Professional, fast, and easy-to-use Football Data API providing live scores, match results, standings, and detailed statistics in JSON format.

## Key Features

- **Live Scores:** Real-time updates for ongoing matches.
- **Detailed Stats:** Player and team statistics.
- **Historical Data:** Archive access for past seasons and leagues.
- **Bilingual:** Fully supports Turkish and English documentation.
- **Clean JSON:** Optimized and sanitized response for developers.

## 📖 Access the Documentation

You can view the interactive, bilingual, and detailed API documentation here:

[![View Documentation](https://img.shields.io/badge/VIEW_INTERACTIVE_DOCS-2563eb?style=for-the-badge&logo=read-the-docs&logoColor=white)](https://samettopaloglu.com/futboldoc.html)

---

## 📋 API Endpoints

### Daily Match List

Retrieve all matches for a specific date.

```
https://samettopaloglu.com/futbol.php?date=15/04/2026
```

---

### Single Match Details

Retrieve detailed information for a specific match using its ID.

```
https://samettopaloglu.com/futbol.php?date=15/04/2026&id=4453644
```

---

### Match Statistics

Retrieve detailed player and team statistics for a specific match.

```
https://samettopaloglu.com/futbol.php?id=4453644&stats=1
```

---

### Archive & League Data

**Categories (Groups)**
Retrieve a list of supported countries and groups.

```
https://samettopaloglu.com/futbol.php?op=groups
```

**Season Years**
Get available historical seasons for a specific group.

```
https://samettopaloglu.com/futbol.php?op=years&group=22
```

**Sub-Leagues (Competitions)**
Retrieve all sub-leagues and competitions under a category for a given year to find the required `leagueId`.

```
https://samettopaloglu.com/futbol.php?op=leagues&group=22&year=2025/2026
```

**League Standings (Table)**
Get the detailed league table for a given competition.

```
https://samettopaloglu.com/futbol.php?op=table&league=70870
```

**Weekly Fixtures**
Get match schedules for a specific league and week.
<br>
<br>
```
https://samettopaloglu.com/futbol.php?op=fixtures&league=70870&week=4
```

---

### Team Information

**Team Squad & Market Values**
Retrieve detailed squad data and average age for a team.

```
https://samettopaloglu.com/futbol.php?op=team&id=79&season=2025/2026
```

**Team Full History & Performance**
Get the entire season's matches, results, and Opta performance metrics.

```
https://samettopaloglu.com/futbol.php?op=team&id=79&season=2025/2026&fixtures=1
```

---
