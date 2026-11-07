# 360 ⚽ Football tracker for Android

Fixtures, results, league tables, every club and full squads, using live data from
[TheSportsDB](https://www.thesportsdb.com).

| Tab | What it shows |
|---|---|
| **Matches** | Upcoming fixtures for the next week and recent results, grouped by day, in your phone's time zone. Live scores are marked ● LIVE. Tap a match for venue, referee, round, attendance, highlights and the match report. |
| **Table** | The full standings with played, won, drawn, lost, goal difference and points. Champions League, Europa League and relegation places are coloured. |
| **Teams** | Every club in the league as a badge grid. Tap a club for its stadium, next 5 matches, last 5 results, the full squad grouped by position, the manager and the club history. Tap a player for their photo, number, position, nationality, age, height, weight and biography. |

**Leagues:** La Liga, Premier League, Saudi Pro League, Champions League, Serie A, Bundesliga,
Ligue 1, Europa League, Eredivisie, Primeira Liga and MLS.

**★ My teams:** open any club and tap the star to follow it. The *My teams* chip then shows all
your clubs' fixtures and results in one list.

**Search** (magnifier icon) finds any club or player worldwide.

Other features: pull down to refresh, works offline from cache, dark mode, Android 8.0+.

## Get the APK, no Android Studio needed

1. Create a new repository on GitHub and upload everything in this folder (keep the `.github` folder).
2. Open the **Actions** tab. The **Build APK** workflow runs automatically (or press *Run workflow*).
3. When it finishes (about 3–5 minutes), open the run and download **360-Football-APK**.
   Unzip it and install `360-Football.apk` (allow "Install unknown apps" when asked).

To publish a release with the APK attached, push a tag: `git tag v1.0.0 && git push --tags`.

## Data

TheSportsDB's free public key (`123`) is built in. The free plan can make some lists shorter,
for example squads for some clubs. If you have a TheSportsDB Patreon key, enter it in
**About 360 (ⓘ) › API key** for full data.

## Project layout

```
app/src/main/java/com/threesixty/football/
  MainActivity.kt    leagues, Matches / Table / Teams tabs, search, settings
  DetailActivity.kt  team, player, match and search screens
  RowAdapter.kt      every list row (matches, table, players, badges…)
  Api.kt             TheSportsDB calls
  Models.kt          leagues, matches, standings, teams, players
  Net.kt, Images.kt  HTTP + disk cache, image loading
```

## License

App code: MIT. Football data and images © TheSportsDB and their respective owners.
