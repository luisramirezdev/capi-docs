# Install
```sh
npm install call-of-duty-api
```

# Usage
```js
const API = require('call-of-duty-api')();
```
or
```js
const API = require('call-of-duty-api')({ platform: "battle" });
```

# Platforms

- psn
- steam
- xbl
- battle
- acti 
- uno ( numerical identifier )

# Login :id=login
!> Login is required to remove any restrictions on certain endpoints.
```js
try {
    await API.login(<username>, <password>);
 } catch(Error) {
     //Handle Exception
 }
```

# Leaderboards :id=leaderboards

 <h2> Example </h2>

 ```js
 try {
    let data = await API.MWLeaderboard(<page>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Output </h2>

```json
{
  title: 'mw',
  platform: 'psn',
  leaderboardType: 'core',
  gameMode: 'career',
  page: 1,
  resultsRequested: 20,
  totalPages: 3816174,
  sort: null,
  columns: [
    'prestige',   'xp',
    'xp',         'score',
    'timePlayed', 'gamesPlayed',
    'wins',       'losses',
    'kills',      'deaths',
    'killstreak', 'assists',
    'headshots',  'hits',
    'misses',     'shots',
    'accuracy'
  ],
  entries: [
    {
      rank: 1,
      username: 'kinglinsjames#7665287',
      updateTime: 300542,
      rating: 0,
      values: [Object]
    },
    {
      rank: 2,
      username: '大帅财#1286178',
      updateTime: 14803882,
      rating: 0,
      values: [Object]
    },
    {
      rank: 3,
      username: 'weav_13#1674785',
      updateTime: 319348,
      rating: 0,
      values: [Object]
    },
    {
      rank: 4,
      username: 'iTz Carlit0s#6152832',
      updateTime: 299550,
      rating: 0,
      values: [Object]
    },
    {
      rank: 5,
      username: 'HalfChicken#11125',
      updateTime: 6104808,
      rating: 0,
      values: [Object]
    },
    {
      rank: 6,
      username: 'FireToaster6134#6244699',
      updateTime: 10427393,
      rating: 0,
      values: [Object]
    },
    {
      rank: 7,
      username: 'PixelyPlazma#2151886',
      updateTime: 14784035,
      rating: 0,
      values: [Object]
    },
    {
      rank: 8,
      username: 'USR_Matrix',
      updateTime: 12593588,
      rating: 0,
      values: [Object]
    },
    {
      rank: 9,
      username: 'UkraineSaiyan#3810058',
      updateTime: 3904293,
      rating: 0,
      values: [Object]
    },
    {
      rank: 10,
      username: 'humanpolarbear#9108073',
      updateTime: 4020673,
      rating: 0,
      values: [Object]
    },
    {
      rank: 11,
      username: 'Master#2556096',
      updateTime: 1113281,
      rating: 0,
      values: [Object]
    },
    {
      rank: 12,
      username: 'the_hollyster#9796860',
      updateTime: 401957,
      rating: 0,
      values: [Object]
    },
    {
      rank: 13,
      username: 'rallying_oval771#4436708',
      updateTime: 1016111,
      rating: 0,
      values: [Object]
    },
    {
      rank: 14,
      username: 'xXxPR3DATOR#6075491',
      updateTime: 6943,
      rating: 0,
      values: [Object]
    },
    {
      rank: 15,
      username: '动次克打次#2716388',
      updateTime: 14002736,
      rating: 0,
      values: [Object]
    },
    {
      rank: 16,
      username: 'ali_01#7407223',
      updateTime: 47757,
      rating: 0,
      values: [Object]
    },
    {
      rank: 17,
      username: 'Kalem#1808520',
      updateTime: 2995151,
      rating: 0,
      values: [Object]
    },
    {
      rank: 18,
      username: 'XxETxxX#1881233',
      updateTime: 64108,
      rating: 0,
      values: [Object]
    },
    {
      rank: 19,
      username: 'EvilGenius13#3069213',
      updateTime: 4090812,
      rating: 0,
      values: [Object]
    },
    {
      rank: 20,
      username: 'Eimo#2528837',
      updateTime: 14756690,
      rating: 0,
      values: [Object]
    }
  ]
}
 ```

# MP Match Details :id=mp-match-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWcombatmp(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Output </h2>
  
```json
{
  summary: {
    all: {
      matchXp: 32058,
      scoreXp: 47350,
      accuracy: 0.19376770538243626,
      losses: 13,
      shotsLanded: 1026,
      objectiveMedalModeXDefendScore: 42,
      objectiveMedalModeXAssaultScore: 28,
      score: 54630,
      totalXp: 191870,
      objectiveMedalModeHpSecureScore: 6,
      rank: 1080,
      deaths: 297,
      wins: 7,
      kdRatio: 1.1313131313131313,
      shotsMissed: 4269,
      scorePerGame: 2731.5,
      timePlayed: 7915,
      headshotPercentage: 0.13392857142857142,
      objectiveKillConfirmed: 18,
      matchesPlayed: 20,
      suicides: 2,
      objectiveKothInObj: 110,
      wlRatio: 0.5384615384615384,
      percentTimeMoving: 1647.6980039999999,
      damageDone: 42873,
      shotsFired: 5295,
      kills: 336,
      medalXp: 27110,
      averageSpeedDuringMatch: 2810.352036,
      objectiveMedalModeDomSecureScore: 14,
      avgLifeTime: 24.968454258675077,
      objectiveMedalModeDomSecureAssistScore: 10,
      objectiveSurvivor: 29,
      headshots: 45,
      assists: 140,
      scorePerMinute: 414.12507896399245,
      objectiveMedalScoreSsKillWhitePhosphorus: 1,
      distanceTraveled: 103348.34275000001,
      objectiveMunitionsBoxTeammateUsed: 1,
      objectiveKillDenied: 6,
      objectiveMedalModeDomSecureNeutralScore: 2,
      objectiveKcFriendlyPickup: 4,
      executions: 0,
      seasonRank: 328,
      objectiveObjProgDefend: 6,
      miscXp: 0,
      objectiveUavAssist: 92,
      longestStreak: 12,
      objectiveMedalScoreSsKillHoverJet: 2,
      objectiveCaptureKill: 8,
      objectiveMedalModeKcOwnTagsScore: 1,
      damageTaken: 35450
    },
    dom: {
      kills: 118,
      medalXp: 14695,
      matchXp: 9685,
      averageSpeedDuringMatch: 868.03847,
      scoreXp: 15285,
      accuracy: 0.19944082013047532,
      objectiveMedalModeDomSecureScore: 14,
      losses: 2,
      avgLifeTime: 21.721311475409838,
      shotsLanded: 428,
      objectiveMedalModeDomSecureAssistScore: 10,
      objectiveMedalModeXDefendScore: 37,
      objectiveMedalModeXAssaultScore: 18,
      score: 20395,
      totalXp: 67776,
      headshots: 14,
      assists: 49,
      rank: 270,
      scorePerMinute: 461.77358490566036,
      distanceTraveled: 35863.6706,
      deaths: 117,
      wins: 3,
      kdRatio: 1.0085470085470085,
      shotsMissed: 1718,
      objectiveMedalModeDomSecureNeutralScore: 2,
      scorePerGame: 4079,
      timePlayed: 2650,
      headshotPercentage: 0.11864406779661017,
      matchesPlayed: 5,
      executions: 0,
      suicides: 1,
      seasonRank: 65,
      wlRatio: 1.5,
      objectiveObjProgDefend: 6,
      percentTimeMoving: 458.388676,
      miscXp: 0,
      objectiveUavAssist: 36,
      longestStreak: 12,
      damageDone: 14937,
      shotsFired: 2146,
      objectiveMedalScoreSsKillHoverJet: 2,
      objectiveCaptureKill: 8,
      damageTaken: 14002
    },
    war: {
      kills: 64,
      medalXp: 2370,
      matchXp: 4819,
      averageSpeedDuringMatch: 929.5503160000001,
      scoreXp: 9635,
      accuracy: 0.16083916083916083,
      losses: 5,
      avgLifeTime: 19.142857142857142,
      shotsLanded: 230,
      score: 9610,
      totalXp: 33648,
      headshots: 10,
      assists: 32,
      rank: 324,
      scorePerMinute: 430.2985074626866,
      distanceTraveled: 10199.214269999999,
      deaths: 64,
      wins: 1,
      kdRatio: 1,
      shotsMissed: 1200,
      scorePerGame: 1601.6666666666667,
      timePlayed: 1340,
      headshotPercentage: 0.15625,
      matchesPlayed: 6,
      executions: 0,
      suicides: 1,
      seasonRank: 106,
      wlRatio: 0.2,
      percentTimeMoving: 563.767423,
      miscXp: 0,
      objectiveUavAssist: 1,
      longestStreak: 4,
      damageDone: 9011,
      shotsFired: 1430,
      damageTaken: 7216
    },
    koth: {
      kills: 107,
      medalXp: 6475,
      matchXp: 9976,
      averageSpeedDuringMatch: 684.35519,
      scoreXp: 12825,
      accuracy: 0.21994884910485935,
      losses: 1,
      avgLifeTime: 24.49397590361446,
      shotsLanded: 258,
      objectiveMedalModeXAssaultScore: 10,
      objectiveMedalModeXDefendScore: 5,
      score: 15225,
      totalXp: 52149,
      headshots: 15,
      assists: 40,
      objectiveMedalModeHpSecureScore: 6,
      rank: 216,
      scorePerMinute: 449.33595671421546,
      distanceTraveled: 28718.426999999996,
      deaths: 79,
      objectiveMunitionsBoxTeammateUsed: 1,
      wins: 3,
      kdRatio: 1.3544303797468353,
      shotsMissed: 915,
      scorePerGame: 3806.25,
      timePlayed: 2033,
      headshotPercentage: 0.14018691588785046,
      matchesPlayed: 4,
      executions: 0,
      suicides: 0,
      seasonRank: 62,
      objectiveKothInObj: 110,
      wlRatio: 3,
      percentTimeMoving: 384.241776,
      miscXp: 0,
      objectiveUavAssist: 25,
      longestStreak: 5,
      damageDone: 13217,
      shotsFired: 1173,
      damageTaken: 9532
    },
    conf: {
      kills: 36,
      medalXp: 1465,
      matchXp: 2110,
      averageSpeedDuringMatch: 286.15036,
      scoreXp: 6280,
      accuracy: 0.21359223300970873,
      losses: 2,
      avgLifeTime: 24.423076923076923,
      shotsLanded: 88,
      score: 6175,
      totalXp: 16501,
      headshots: 6,
      assists: 16,
      rank: 108,
      scorePerMinute: 583.4645669291339,
      distanceTraveled: 4119.09864,
      deaths: 24,
      wins: 0,
      kdRatio: 1.5,
      shotsMissed: 324,
      objectiveKillDenied: 6,
      scorePerGame: 3087.5,
      objectiveKcFriendlyPickup: 4,
      timePlayed: 635,
      headshotPercentage: 0.16666666666666666,
      matchesPlayed: 2,
      executions: 0,
      objectiveKillConfirmed: 18,
      suicides: 0,
      seasonRank: 31,
      wlRatio: 0,
      percentTimeMoving: 182.000935,
      miscXp: 0,
      objectiveUavAssist: 30,
      longestStreak: 4,
      damageDone: 4057,
      shotsFired: 412,
      objectiveMedalModeKcOwnTagsScore: 1,
      damageTaken: 3328
    },
    arena: {
      kills: 8,
      medalXp: 1845,
      matchXp: 812,
      averageSpeedDuringMatch: 0,
      scoreXp: 875,
      accuracy: 0.19230769230769232,
      losses: 2,
      avgLifeTime: 29.4,
      shotsLanded: 20,
      score: 850,
      totalXp: 7064,
      headshots: 0,
      assists: 2,
      rank: 108,
      scorePerMinute: 115.64625850340137,
      distanceTraveled: 1748.21224,
      deaths: 13,
      wins: 0,
      kdRatio: 0.6153846153846154,
      shotsMissed: 84,
      scorePerGame: 425,
      timePlayed: 441,
      headshotPercentage: 0,
      matchesPlayed: 2,
      executions: 0,
      suicides: 0,
      seasonRank: 46,
      wlRatio: 0,
      percentTimeMoving: 0,
      miscXp: 0,
      longestStreak: 2,
      damageDone: 1002,
      shotsFired: 104,
      damageTaken: 1300
    },
    infect: {
      kills: 3,
      medalXp: 260,
      matchXp: 4656,
      averageSpeedDuringMatch: 42.2577,
      scoreXp: 2450,
      accuracy: 0.06666666666666667,
      losses: 1,
      avgLifeTime: 816,
      shotsLanded: 2,
      score: 2375,
      totalXp: 14732,
      objectiveSurvivor: 29,
      headshots: 0,
      assists: 1,
      rank: 54,
      scorePerMinute: 174.63235294117646,
      objectiveMedalScoreSsKillWhitePhosphorus: 1,
      distanceTraveled: 22699.72,
      deaths: 0,
      wins: 0,
      kdRatio: 3,
      shotsMissed: 28,
      scorePerGame: 2375,
      timePlayed: 816,
      headshotPercentage: 0,
      matchesPlayed: 1,
      executions: 0,
      suicides: 0,
      seasonRank: 18,
      wlRatio: 0,
      percentTimeMoving: 59.299194,
      miscXp: 0,
      longestStreak: 1,
      damageDone: 649,
      shotsFired: 30,
      damageTaken: 72
    }
  },
  matches: [
    {
      utcStartSeconds: 1588528804,
      utcEndSeconds: 1588529023,
      map: 'mp_m_cargo',
      mode: 'arena',
      matchID: '7521393282491174058',
      duration: 219000,
      playlistName: null,
      version: 1,
      gameType: 'mp',
      result: 'loss',
      winningTeam: 'axis',
      gameBattle: false,
      team1Score: 1,
      team2Score: 5,
      isPresentAtEnd: false,
      player: [Object],
      playerStats: [Object],
      weaponStats: [Object],
      allPlayers: null,
      arena: false,
      privateMatch: false
    }, { ... }
  ]
}
```

# WZ Match Details :id=wz-match-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWcombatwz(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Output </h2>
  
```json
{
  summary: {
    all: {
      kills: 38,
      objectiveTeamWiped: 9,
      objectiveLastStandKill: 17,    
      avgLifeTime: 853.0847457627119,
      objectivePlunderCashBloodMoney: 7,
      score: 35705,
      headshots: 9,
      assists: 0,
      objectiveDestroyedVehicleLight: 1,
      killsPerGame: 1.9,
      scorePerMinute: 42.56337916236192,
      distanceTraveled: 6262707.830000001,
      deaths: 39,
      objectiveBrLootChopperBoxOpen: 1,
      objectiveDestroyedEquipment: 3,
      objectiveBrDownEnemyCircle2: 2,
      kdRatio: 0.9743589743589743,
      objectiveBrDownEnemyCircle1: 11,
      objectiveBrMissionPickupTablet: 13,
      objectiveReviver: 6,
      objectiveBrKioskBuy: 13,
      gulagDeaths: 13,
      objectiveBrDownEnemyCircle6: 4,
      timePlayed: 50332,
      headshotPercentage: 0.23684210526315788,
      executions: 0,
      matchesPlayed: 20,
      gulagKills: 7,
      objectiveBrCacheOpen: 104,
      damageDone: 15208,
      damageTaken: 7792
    },
    br_dmz_104: {
      kills: 8,
      objectiveTeamWiped: 2,
      objectiveLastStandKill: 4,
      avgLifeTime: 1407.6666666666667,
      objectivePlunderCashBloodMoney: 7,
      score: 6230,
      headshots: 0,
      assists: 0,
      killsPerGame: 4,
      scorePerMinute: 88.51527350224958,
      distanceTraveled: 668368.24,
      deaths: 1,
      objectiveBrLootChopperBoxOpen: 1,
      objectiveDestroyedEquipment: 1,
      kdRatio: 8,
      objectiveBrMissionPickupTablet: 2,
      objectiveReviver: 1,
      scorePerGame: 3115,
      objectiveBrKioskBuy: 3,
      timePlayed: 4223,
      headshotPercentage: 0,
      executions: 0,
      matchesPlayed: 2,
      objectiveBrCacheOpen: 20,
      damageDone: 2759,
      damageTaken: 708
    },
    br_87: {
      kills: 10,
      kdRatio: 0.625,
      objectiveBrMissionPickupTablet: 2,
      scorePerGame: 878.125,
      avgLifeTime: 766.625,
      gulagDeaths: 6,
      score: 7025,
      timePlayed: 18399,
      headshotPercentage: 0.3,
      headshots: 3,
      executions: 0,
      matchesPlayed: 8,
      assists: 0,
      gulagKills: 2,
      objectiveBrCacheOpen: 43,
      objectiveDestroyedVehicleLight: 1,
      killsPerGame: 1.25,
      scorePerMinute: 22.9088537420512,
      distanceTraveled: 2024378.3299999998,
      damageDone: 4532,
      deaths: 16,
      objectiveDestroyedEquipment: 1,
      damageTaken: 2129
    },
    br_25: {
      kills: 20,
      objectiveTeamWiped: 7,
      objectiveLastStandKill: 13,
      avgLifeTime: 865.9375,
      score: 22450,
      headshots: 6,
      assists: 0,
      killsPerGame: 2,
      scorePerMinute: 48.61060988812703,
      distanceTraveled: 3569961.26,
      deaths: 22,
      objectiveDestroyedEquipment: 1,
      objectiveBrDownEnemyCircle2: 2,
      kdRatio: 0.9090909090909091,
      objectiveBrDownEnemyCircle1: 11,
      objectiveBrMissionPickupTablet: 9,
      objectiveReviver: 5,
      scorePerGame: 2245,
      objectiveBrKioskBuy: 10,
      gulagDeaths: 7,
      objectiveBrDownEnemyCircle6: 4,
      timePlayed: 27710,
      headshotPercentage: 0.3,
      executions: 0,
      matchesPlayed: 10,
      gulagKills: 5,
      objectiveBrCacheOpen: 41,
      damageDone: 7917,
      damageTaken: 4955
    }
  },
  matches: [
    {
      utcStartSeconds: 1588522262,
      utcEndSeconds: 1588523954,
      map: 'mp_donetsk',
      mode: 'br_25',
      matchID: '5535034381462720275',
      duration: 1692000,
      playlistName: null,
      version: 1,
      gameType: 'wz',
      playerCount: 151,
      playerStats: [Object],
      player: [Object],
      teamCount: 57,
      rankedTeams: null,
      draw: false,
      privateMatch: false
    }, {...}
  ]
}
```

# MP Details :id=mp-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWmp(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Output </h2>
  
```json
{
  "title": "mw",
  "platform": "battle",
  "username": "<gamertag>",
  "type": "mp",
  "level": 55,
  "maxLevel": 0,
  "levelXpRemainder": 3000,
  "levelXpGained": 7000,
  "prestige": 0,
  "prestigeId": 0,
  "maxPrestige": 0,
  "totalXp": 960000,
  "paragonRank": 0,
  "paragonId": 0,
  "s": 1,
  "p": 1,
  "lifetime": {
    "all": {
      "properties": {
        "recordLongestWinStreak": 21,
        "recordXpInAMatch": 40950,
        "accuracy": 0.17821714282035828,
        "losses": 340,
        "totalGamesPlayed": 995,
        "score": 2657371,
        "winLossRatio": 1.7294117212295532,
        "totalShots": 346566,
        "bestScoreXp": 0,
        "gamesPlayed": 995,
        "bestSquardKills": 0,
        "bestSguardWave": 0,
        "bestConfirmed": 35,
        "deaths": 14453,
        "wins": 588,
        "bestSquardCrates": 0,
        "kdRatio": 1.1902027130126953,
        "bestAssists": 39,
        "bestFieldgoals": 0,
        "bestScore": 14475,
        "recordDeathsInAMatch": 79,
        "scorePerGame": 2670.7246231155777,
        "bestSPM": 2162,
        "bestKillChains": 0,
        "recordKillsInAMatch": 124,
        "suicides": 129,
        "wlRatio": 1.7294117212295532,
        "currentWinStreak": 0,
        "bestMatchBonusXp": 0,
        "bestMatchXp": 0,
        "bestSguardWeaponLevel": 0,
        "bestKD": 8.5,
        "kills": 17202,
        "bestKillsAsInfected": 9,
        "bestReturns": 0,
        "bestStabs": 0,
        "bestKillsAsSurvivor": 15,
        "timePlayedTotal": 421017,
        "bestDestructions": 1,
        "headshots": 2480,
        "bestRescues": 3,
        "assists": 4618,
        "ties": 5,
        "recordKillStreak": 25,
        "bestPlants": 2,
        "misses": 284802,
        "bestDamage": 0,
        "bestSetbacks": 0,
        "bestTouchdowns": 0,
        "scorePerMinute": 378.70741561504644,
        "bestDeaths": 79,
        "bestMedalXp": 0,
        "bestDefends": 32,
        "bestSquardRevives": 0,
        "bestKills": 124,
        "bestDefuses": 1,
        "bestCaptures": 19,
        "hits": 61764,
        "bestKillStreak": 25,
        "bestDenied": 12
      }
    },
    "mode": {
      "gun": {
        "properties": {
          "kills": 31,
          "score": 3306,
          "timePlayed": 893,
          "kdRatio": 1.0333333333333334,
          "setBacks": 0,
          "scorePerMinute": 222.12765957446808,
          "stabs": 0,
          "deaths": 30
        }
      },
      "dom": {
        "properties": {
          "kills": 1616,
          "score": 462255,
          "timePlayed": 70554,
          "kdRatio": 1.015075376884422,
          "captures": 377,
          "defends": 319,
          "scorePerMinute": 393.1074070924398,
          "deaths": 1592
        }
      },
      "war": {
        "properties": {
          "kills": 889,
          "score": 219845,
          "timePlayed": 47444,
          "kdRatio": 1.0854700854700854,
          "assists": 250,
          "scorePerMinute": 278.02672624567913,
          "deaths": 819
        }
      },
      "hq": {
        "properties": {
          "kills": 1480,
          "score": 325830,
          "timePlayed": 52614,
          "kdRatio": 1.420345489443378,
          "captures": 99,
          "defends": 13,
          "scorePerMinute": 371.5703044816969,
          "deaths": 1042
        }
      },
      "hc_dom": {
        "properties": {
          "kills": 352,
          "score": 126865,
          "timePlayed": 18088,
          "kdRatio": 1.217993079584775,
          "captures": 70,
          "defends": 71,
          "scorePerMinute": 420.8259619637329,
          "deaths": 289
        }
      },
      "hc_conf": {
        "properties": {
          "kills": 20,
          "score": 14125,
          "timePlayed": 1518,
          "kdRatio": 0.9090909090909091,
          "confirms": 10,
          "scorePerMinute": 558.300395256917,
          "denies": 6,
          "deaths": 22
        }
      },
      "koth": {
        "properties": {
          "kills": 1368,
          "score": 519215,
          "timePlayed": 53273,
          "kdRatio": 1.294228949858089,
          "defends": 102,
          "objTime": 1668,
          "scorePerMinute": 584.7784055713025,
          "deaths": 1057
        }
      },
      "conf": {
        "properties": {
          "kills": 1300,
          "score": 416835,
          "timePlayed": 48951,
          "kdRatio": 1.352757544224766,
          "confirms": 854,
          "scorePerMinute": 510.92112520683946,
          "denies": 275,
          "deaths": 961
        }
      },
      "hc_hq": {
        "properties": {
          "kills": 365,
          "score": 57700,
          "timePlayed": 10103,
          "kdRatio": 1.5082644628099173,
          "captures": 12,
          "defends": 7,
          "scorePerMinute": 342.6704939126992,
          "deaths": 242
        }
      },
      "arena": {
        "properties": {
          "kills": 926,
          "score": 254550,
          "timePlayed": 83266,
          "damage": 124295,
          "kdRatio": 0.9615784008307373,
          "assists": 285,
          "scorePerMinute": 183.42420675906132,
          "deaths": 963
        }
      },
      "br_dmz": {
        "properties": {
          "wins": 0,
          "kills": 51,
          "kdRatio": 1.7586206896551724,
          "downs": 56,
          "topTwentyFive": 0,
          "topTen": 0,
          "contracts": 8,
          "revives": 0,
          "topFive": 0,
          "score": 34652,
          "timePlayed": 14165,
          "gamesPlayed": 12,
          "scorePerMinute": 146.77867984468762,
          "cash": 929,
          "deaths": 29
        }
      },
      "br": {
        "properties": {
          "wins": 3,
          "kills": 250,
          "kdRatio": 1.0638297872340425,
          "downs": 221,
          "topTwentyFive": 72,
          "topTen": 35,
          "contracts": 59,
          "revives": 0,
          "topFive": 20,
          "score": 236975,
          "timePlayed": 107875,
          "gamesPlayed": 84,
          "scorePerMinute": 131.80533024333718,
          "cash": 0,
          "deaths": 235
        }
      },
      "sd": {
        "properties": {
          "kills": 50,
          "score": 12575,
          "timePlayed": 17817,
          "kdRatio": 0.5494505494505495,
          "plants": 6,
          "scorePerMinute": 42.34719649772689,
          "defuses": 1,
          "deaths": 91
        }
      },
      "grnd": {
        "properties": {
          "kills": 0,
          "score": 5865,
          "timePlayed": 867,
          "kdRatio": 0,
          "defends": 0,
          "objTime": 0,
          "scorePerMinute": 405.88235294117646,
          "deaths": 0
        }
      },
      "cyber": {
        "properties": {
          "kills": 45,
          "score": 25125,
          "timePlayed": 10801,
          "kdRatio": 0.9375,
          "plants": 7,
          "scorePerMinute": 139.57041014720858,
          "revives": 0,
          "deaths": 48
        }
      },
      "hc_war": {
        "properties": {
          "kills": 200,
          "score": 21935,
          "timePlayed": 7378,
          "kdRatio": 0.970873786407767,
          "assists": 36,
          "scorePerMinute": 178.38167525074545,
          "deaths": 206
        }
      },
      "br_all": {
        "properties": {
          "wins": 3,
          "kills": 301,
          "kdRatio": 1.1401515151515151,
          "downs": 277,
          "topTwentyFive": 72,
          "topTen": 35,
          "contracts": 67,
          "revives": 0,
          "topFive": 20,
          "score": 271627,
          "timePlayed": 122040,
          "gamesPlayed": 96,
          "scorePerMinute": 133.5432645034415,
          "cash": 929,
          "deaths": 264
        }
      },
      "hc_sd": {
        "properties": {
          "kills": 1,
          "score": 125,
          "timePlayed": 1132,
          "kdRatio": 0.07692307692307693,
          "plants": 0,
          "scorePerMinute": 6.625441696113074,
          "defuses": 0,
          "deaths": 13
        }
      },
      "arm": {
        "properties": {
          "kills": 213,
          "score": 41525,
          "timePlayed": 12462,
          "kdRatio": 0.9906976744186047,
          "captures": 52,
          "defends": 24,
          "scorePerMinute": 199.92778045257583,
          "deaths": 215
        }
      },
      "hc_cyber": {
        "properties": {
          "kills": 0,
          "score": 0,
          "timePlayed": 0,
          "kdRatio": 0,
          "plants": 0,
          "scorePerMinute": 0,
          "revives": 0,
          "deaths": 0
        }
      },
      "infect": {
        "properties": {
          "kills": 536,
          "score": 294350,
          "infected": 213,
          "timePlayed": 49360,
          "kdRatio": 0.8535031847133758,
          "scorePerMinute": 357.79983792544573,
          "time": 26547,
          "deaths": 628
        }
      }
    },
    "map": {},
    "itemData": {
      "weapon_sniper": {
        "iw8_sn_alpha50": {
          "properties": {
            "hits": 94,
            "kills": 95,
            "kdRatio": 1.4615384615384615,
            "headshots": 22,
            "accuracy": 0.27485380116959063,
            "shots": 342,
            "deaths": 65
          }
        },
        "iw8_sn_hdromeo": {
          "properties": {
            "hits": 84,
            "kills": 90,
            "kdRatio": 0.989010989010989,
            "headshots": 19,
            "accuracy": 0.25149700598802394,
            "shots": 334,
            "deaths": 91
          }
        },
        "iw8_sn_delta": {
          "properties": {
            "hits": 46,
            "kills": 33,
            "kdRatio": 0.9166666666666666,
            "headshots": 6,
            "accuracy": 0.19574468085106383,
            "shots": 235,
            "deaths": 36
          }
        },
        "iw8_sn_xmike109": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        }
      },
      "tacticals": {
        "equip_gas_grenade": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_snapshot_grenade": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_decoy": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_smoke": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_concussion": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_hb_sensor": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_flash": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_adrenaline": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        }
      },
      "lethals": {
        "equip_frag": {
          "properties": {
            "hits": 0,
            "kills": 83,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_thermite": {
          "properties": {
            "hits": 0,
            "kills": 6,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_semtex": {
          "properties": {
            "hits": 0,
            "kills": 866,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_claymore": {
          "properties": {
            "hits": 0,
            "kills": 20,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_c4": {
          "properties": {
            "hits": 0,
            "kills": 4,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_at_mine": {
          "properties": {
            "hits": 0,
            "kills": 3,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_throwing_knife": {
          "properties": {
            "hits": 0,
            "kills": 221,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        },
        "equip_molotov": {
          "properties": {
            "hits": 0,
            "kills": 47,
            "shots": 0,
            "deaths": 0,
            "headShots": 0
          }
        }
      },
      "weapon_lmg": {
        "iw8_lm_kilo121": {
          "properties": {
            "hits": 138,
            "kills": 42,
            "kdRatio": 0.9130434782608695,
            "headshots": 2,
            "accuracy": 0.12223206377325066,
            "shots": 1129,
            "deaths": 46
          }
        },
        "iw8_lm_mkilo3": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_lm_mgolf34": {
          "properties": {
            "hits": 26,
            "kills": 9,
            "kdRatio": 0.9,
            "headshots": 2,
            "accuracy": 0.07669616519174041,
            "shots": 339,
            "deaths": 10
          }
        },
        "iw8_lm_lima86": {
          "properties": {
            "hits": 31,
            "kills": 11,
            "kdRatio": 1.1,
            "headshots": 3,
            "accuracy": 0.12015503875968993,
            "shots": 258,
            "deaths": 10
          }
        },
        "iw8_lm_pkilo": {
          "properties": {
            "hits": 20,
            "kills": 12,
            "kdRatio": 1.2,
            "headshots": 1,
            "accuracy": 0.09259259259259259,
            "shots": 216,
            "deaths": 10
          }
        },
        "iw8_lm_mgolf36": {
          "properties": {
            "hits": 6543,
            "kills": 1487,
            "kdRatio": 1.2289256198347107,
            "headshots": 229,
            "accuracy": 0.16558269011767685,
            "shots": 39515,
            "deaths": 1210
          }
        }
      },
      "weapon_launcher": {
        "iw8_la_gromeo": {
          "properties": {
            "hits": 1,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0.5,
            "shots": 2,
            "deaths": 1
          }
        },
        "iw8_la_rpapa7": {
          "properties": {
            "hits": 33,
            "kills": 173,
            "kdRatio": 1.130718954248366,
            "headshots": 2,
            "accuracy": 0.052884615384615384,
            "shots": 624,
            "deaths": 153
          }
        },
        "iw8_la_juliet": {
          "properties": {
            "hits": 0,
            "kills": 2,
            "kdRatio": 2,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_la_kgolf": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_la_mike32": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        }
      },
      "weapon_pistol": {
        "iw8_pi_cpapa": {
          "properties": {
            "hits": 76,
            "kills": 43,
            "kdRatio": 0.6515151515151515,
            "headshots": 14,
            "accuracy": 0.25418060200668896,
            "shots": 299,
            "deaths": 66
          }
        },
        "iw8_pi_mike9": {
          "properties": {
            "hits": 10,
            "kills": 1,
            "kdRatio": 0.07692307692307693,
            "headshots": 0,
            "accuracy": 0.10989010989010989,
            "shots": 91,
            "deaths": 13
          }
        },
        "iw8_pi_mike1911": {
          "properties": {
            "hits": 289,
            "kills": 117,
            "kdRatio": 0.6190476190476191,
            "headshots": 24,
            "accuracy": 0.19063324538258575,
            "shots": 1516,
            "deaths": 189
          }
        },
        "iw8_pi_golf21": {
          "properties": {
            "hits": 100,
            "kills": 22,
            "kdRatio": 0.4583333333333333,
            "headshots": 4,
            "accuracy": 0.12610340479192939,
            "shots": 793,
            "deaths": 48
          }
        },
        "iw8_pi_decho": {
          "properties": {
            "hits": 368,
            "kills": 180,
            "kdRatio": 0.5590062111801242,
            "headshots": 50,
            "accuracy": 0.25051055139550715,
            "shots": 1469,
            "deaths": 322
          }
        },
        "iw8_pi_papa320": {
          "properties": {
            "hits": 100,
            "kills": 27,
            "kdRatio": 0.48214285714285715,
            "headshots": 3,
            "accuracy": 0.15220700152207,
            "shots": 657,
            "deaths": 56
          }
        }
      },
      "weapon_assault_rifle": {
        "iw8_ar_falima": {
          "properties": {
            "hits": 1247,
            "kills": 342,
            "kdRatio": 0.76,
            "headshots": 43,
            "accuracy": 0.21341776484682526,
            "shots": 5843,
            "deaths": 450
          }
        },
        "iw8_ar_tango21": {
          "properties": {
            "hits": 3606,
            "kills": 800,
            "kdRatio": 1.3179571663920921,
            "headshots": 142,
            "accuracy": 0.17136339875493037,
            "shots": 21043,
            "deaths": 607
          }
        },
        "iw8_ar_mike4": {
          "properties": {
            "hits": 8709,
            "kills": 1723,
            "kdRatio": 1.239568345323741,
            "headshots": 268,
            "accuracy": 0.19523841549532583,
            "shots": 44607,
            "deaths": 1390
          }
        },
        "iw8_ar_falpha": {
          "properties": {
            "hits": 15,
            "kills": 7,
            "kdRatio": 1.75,
            "headshots": 6,
            "accuracy": 0.15463917525773196,
            "shots": 97,
            "deaths": 4
          }
        },
        "iw8_ar_mcharlie": {
          "properties": {
            "hits": 1885,
            "kills": 295,
            "kdRatio": 1.1614173228346456,
            "headshots": 71,
            "accuracy": 0.20149652592196687,
            "shots": 9355,
            "deaths": 254
          }
        },
        "iw8_ar_akilo47": {
          "properties": {
            "hits": 471,
            "kills": 134,
            "kdRatio": 2.7346938775510203,
            "headshots": 15,
            "accuracy": 0.16833452466047177,
            "shots": 2798,
            "deaths": 49
          }
        },
        "iw8_ar_kilo433": {
          "properties": {
            "hits": 8077,
            "kills": 1490,
            "kdRatio": 1.09478324761205,
            "headshots": 214,
            "accuracy": 0.19145254574760595,
            "shots": 42188,
            "deaths": 1361
          }
        },
        "iw8_ar_scharlie": {
          "properties": {
            "hits": 25,
            "kills": 4,
            "kdRatio": 0.5,
            "headshots": 0,
            "accuracy": 0.12376237623762376,
            "shots": 202,
            "deaths": 8
          }
        },
        "iw8_ar_asierra12": {
          "properties": {
            "hits": 22,
            "kills": 14,
            "kdRatio": 14,
            "headshots": 3,
            "accuracy": 0.15714285714285714,
            "shots": 140,
            "deaths": 1
          }
        },
        "iw8_ar_galima": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_ar_sierra552": {
          "properties": {
            "hits": 3311,
            "kills": 668,
            "kdRatio": 1.0620031796502385,
            "headshots": 98,
            "accuracy": 0.1935125657510228,
            "shots": 17110,
            "deaths": 629
          }
        }
      },
      "weapon_other": {
        "iw8_me_riotshield": {
          "properties": {
            "hits": 0,
            "kills": 5,
            "kdRatio": 0.2777777777777778,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 18
          }
        }
      },
      "weapon_shotgun": {
        "iw8_sh_mike26": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_sh_charlie725": {
          "properties": {
            "hits": 91,
            "kills": 63,
            "kdRatio": 0.7,
            "headshots": 11,
            "accuracy": 0.5384615384615384,
            "shots": 169,
            "deaths": 90
          }
        },
        "iw8_sh_oscar12": {
          "properties": {
            "hits": 1217,
            "kills": 556,
            "kdRatio": 1.3365384615384615,
            "headshots": 59,
            "accuracy": 0.4798895899053628,
            "shots": 2536,
            "deaths": 416
          }
        },
        "iw8_sh_romeo870": {
          "properties": {
            "hits": 104,
            "kills": 66,
            "kdRatio": 2.4444444444444446,
            "headshots": 14,
            "accuracy": 0.5360824742268041,
            "shots": 194,
            "deaths": 27
          }
        },
        "iw8_sh_dpapa12": {
          "properties": {
            "hits": 1533,
            "kills": 729,
            "kdRatio": 0.9504563233376793,
            "headshots": 77,
            "accuracy": 0.5140845070422535,
            "shots": 2982,
            "deaths": 767
          }
        }
      },
      "weapon_smg": {
        "iw8_sm_mpapa7": {
          "properties": {
            "hits": 8456,
            "kills": 1262,
            "kdRatio": 1.1158267020335986,
            "headshots": 273,
            "accuracy": 0.19115652409801973,
            "shots": 44236,
            "deaths": 1131
          }
        },
        "iw8_sm_augolf": {
          "properties": {
            "hits": 4977,
            "kills": 1125,
            "kdRatio": 1.0683760683760684,
            "headshots": 192,
            "accuracy": 0.17884864165588615,
            "shots": 27828,
            "deaths": 1053
          }
        },
        "iw8_sm_papa90": {
          "properties": {
            "hits": 4477,
            "kills": 987,
            "kdRatio": 1.426300578034682,
            "headshots": 172,
            "accuracy": 0.17192120118275028,
            "shots": 26041,
            "deaths": 692
          }
        },
        "iw8_sm_charlie9": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_sm_mpapa5": {
          "properties": {
            "hits": 120,
            "kills": 23,
            "kdRatio": 0.6052631578947368,
            "headshots": 2,
            "accuracy": 0.17725258493353027,
            "shots": 677,
            "deaths": 38
          }
        },
        "iw8_sm_smgolf45": {
          "properties": {
            "hits": 659,
            "kills": 155,
            "kdRatio": 1.25,
            "headshots": 8,
            "accuracy": 0.18726911054276782,
            "shots": 3519,
            "deaths": 124
          }
        },
        "iw8_sm_beta": {
          "properties": {
            "hits": 6107,
            "kills": 1529,
            "kdRatio": 1.1023792357606346,
            "headshots": 266,
            "accuracy": 0.17980273811276315,
            "shots": 33965,
            "deaths": 1387
          }
        },
        "iw8_sm_victor": {
          "properties": {
            "hits": 0,
            "kills": 0,
            "kdRatio": 0,
            "headshots": 0,
            "accuracy": 0,
            "shots": 0,
            "deaths": 0
          }
        },
        "iw8_sm_uzulu": {
          "properties": {
            "hits": 39,
            "kills": 4,
            "kdRatio": 0.4,
            "headshots": 0,
            "accuracy": 0.14772727272727273,
            "shots": 264,
            "deaths": 10
          }
        }
      },
      "weapon_marksman": {
        "iw8_sn_sbeta": {
          "properties": {
            "hits": 120,
            "kills": 67,
            "kdRatio": 1.046875,
            "headshots": 23,
            "accuracy": 0.30848329048843187,
            "shots": 389,
            "deaths": 64
          }
        },
        "iw8_sn_crossbow": {
          "properties": {
            "hits": 9,
            "kills": 17,
            "kdRatio": 0.9444444444444444,
            "headshots": 4,
            "accuracy": 0.16071428571428573,
            "shots": 56,
            "deaths": 18
          }
        },
        "iw8_sn_kilo98": {
          "properties": {
            "hits": 151,
            "kills": 134,
            "kdRatio": 0.9436619718309859,
            "headshots": 39,
            "accuracy": 0.2710951526032316,
            "shots": 557,
            "deaths": 142
          }
        },
        "iw8_sn_mike14": {
          "properties": {
            "hits": 91,
            "kills": 40,
            "kdRatio": 1.1428571428571428,
            "headshots": 4,
            "accuracy": 0.2161520190023753,
            "shots": 421,
            "deaths": 35
          }
        },
        "iw8_sn_sksierra": {
          "properties": {
            "hits": 251,
            "kills": 112,
            "kdRatio": 1.2584269662921348,
            "headshots": 21,
            "accuracy": 0.19263238679969302,
            "shots": 1303,
            "deaths": 89
          }
        }
      },
      "weapon_melee": {
        "iw8_knife": {
          "properties": {
            "hits": 6,
            "kills": 1083,
            "kdRatio": 0.6267361111111112,
            "headshots": 0,
            "accuracy": 6,
            "shots": 0,
            "deaths": 1728
          }
        }
      }
    },
    "scorestreakData": {
      "lethalScorestreakData": {
        "precision_airstrike": {
          "properties": {
            "extraStat1": 89,
            "uses": 104,
            "awardedCount": 87
          }
        },
        "cruise_predator": {
          "properties": {
            "extraStat1": 9,
            "uses": 6,
            "awardedCount": 0
          }
        },
        "manual_turret": {
          "properties": {
            "extraStat1": 3,
            "uses": 7,
            "awardedCount": 0
          }
        },
        "white_phosphorus": {
          "properties": {
            "extraStat1": 6,
            "uses": 1,
            "awardedCount": 0
          }
        },
        "hover_jet": {
          "properties": {
            "extraStat1": 50,
            "uses": 16,
            "awardedCount": 15
          }
        },
        "chopper_gunner": {
          "properties": {
            "extraStat1": 16,
            "uses": 3,
            "awardedCount": 2
          }
        },
        "gunship": {
          "properties": {
            "extraStat1": 11,
            "uses": 1,
            "awardedCount": 0
          }
        },
        "sentry_gun": {
          "properties": {
            "extraStat1": 0,
            "uses": 0,
            "awardedCount": 0
          }
        },
        "toma_strike": {
          "properties": {
            "extraStat1": 7,
            "uses": 26,
            "awardedCount": 11
          }
        },
        "nuke": {
          "properties": {
            "extraStat1": 0,
            "uses": 0,
            "awardedCount": 0
          }
        },
        "juggernaut": {
          "properties": {
            "extraStat1": 0,
            "uses": 0,
            "awardedCount": 0
          }
        },
        "pac_sentry": {
          "properties": {
            "extraStat1": 1,
            "uses": 1,
            "awardedCount": 0
          }
        },
        "chopper_support": {
          "properties": {
            "extraStat1": 6,
            "uses": 2,
            "awardedCount": 0
          }
        },
        "bradley": {
          "properties": {
            "extraStat1": 0,
            "uses": 0,
            "awardedCount": 0
          }
        }
      },
      "supportScorestreakData": {
        "airdrop": {
          "properties": {
            "extraStat1": 0,
            "uses": 0,
            "awardedCount": 0
          }
        },
        "radar_drone_overwatch": {
          "properties": {
            "extraStat1": 0,
            "uses": 16,
            "awardedCount": 10
          }
        },
        "scrambler_drone_guard": {
          "properties": {
            "extraStat1": 0,
            "uses": 6,
            "awardedCount": 0
          }
        },
        "uav": {
          "properties": {
            "extraStat1": 856,
            "uses": 189,
            "awardedCount": 179
          }
        },
        "airdrop_multiple": {
          "properties": {
            "extraStat1": 0,
            "uses": 0,
            "awardedCount": 0
          }
        },
        "directional_uav": {
          "properties": {
            "extraStat1": 6,
            "uses": 1,
            "awardedCount": 0
          }
        }
      }
    },
    "accoladeData": {
      "properties": {
        "classChanges": 45,
        "highestAvgAltitude": 85,
        "killsFromBehind": 186,
        "lmgDeaths": 53,
        "riotShieldDamageAbsorbed": 0,
        "flashbangHits": 222,
        "meleeKills": 231,
        "tagsLargestBank": 0,
        "shotgunKills": 51,
        "sniperDeaths": 87,
        "timeProne": 184,
        "killstreakWhitePhosphorousKillsAssists": 1,
        "shortestLife": 106,
        "deathsFromBehind": 115,
        "higherRankedKills": 141,
        "mostAssists": 154,
        "leastKills": 103,
        "tagsDenied": 23,
        "killstreakWheelsonKills": 0,
        "sniperHeadshots": 40,
        "killstreakJuggernautKills": 0,
        "smokesUsed": 29,
        "avengerKills": 170,
        "decoyHits": 0,
        "killstreakCarePackageUsed": 0,
        "molotovKills": 31,
        "gasHits": 9,
        "comebackKills": 121,
        "lmgHeadshots": 52,
        "smgDeaths": 113,
        "carrierKills": 0,
        "deployableCoverUsed": 36,
        "thermiteKills": 8,
        "arKills": 107,
        "c4Kills": 0,
        "suicides": 73,
        "clutch": 2,
        "survivorKills": 14,
        "killstreakGunshipKills": 1,
        "timeSpentAsPassenger": 0,
        "returns": 0,
        "smgHeadshots": 90,
        "launcherDeaths": 2,
        "oneShotOneKills": 54,
        "ammoBoxUsed": 22,
        "spawnSelectSquad": 1,
        "weaponPickups": 110,
        "pointBlankKills": 182,
        "tagsCaptured": 30,
        "killstreakGroundKills": 1,
        "distanceTraveledInVehicle": 0,
        "longestLife": 137,
        "stunHits": 68,
        "spawnSelectFlag": 0,
        "shotgunHeadshots": 39,
        "bombDefused": 3,
        "snapshotHits": 1,
        "noKillsWithDeath": 14,
        "killstreakAUAVAssists": 0,
        "killstreakPersonalUAVKills": 3,
        "tacticalInsertionSpawns": 36,
        "launcherKills": 5,
        "spawnSelectVehicle": 1,
        "mostKillsLeastDeaths": 38,
        "mostKills": 143,
        "defends": 46,
        "timeSpentAsDriver": 0,
        "bombDetonated": 1,
        "arHeadshots": 83,
        "timeOnPoint": 7,
        "lmgKills": 60,
        "killstreakUAVAssists": 22,
        "carepackagesCaptured": 17,
        "mostKillsLongestStreak": 89,
        "killstreakCruiseMissileKills": 2,
        "longestStreak": 167,
        "destroyedKillstreaks": 43,
        "hipfireKills": 132,
        "stimDamageHealed": 39,
        "skippedKillcams": 105,
        "leastAssists": 254,
        "mostMultikills": 132,
        "highestRankedKills": 176,
        "killstreakAirstrikeKills": 37,
        "distanceTravelled": 71,
        "killstreakKills": 21,
        "semtexKills": 167,
        "penetrationKills": 148,
        "explosionsSurvived": 120,
        "highestMultikill": 225,
        "arDeaths": 98,
        "longshotKills": 117,
        "proximityMineKills": 3,
        "tagsMegaBanked": 0,
        "mostKillsMostHeadshots": 52,
        "firstInfected": 11,
        "killstreakCUAVAssists": 5,
        "throwingKnifeKills": 86,
        "executionKills": 24,
        "lastSurvivor": 14,
        "reconDroneMarks": 0,
        "deadSilenceKills": 37,
        "revengeKills": 173,
        "infectedKills": 26,
        "killEnemyTeam": 142,
        "sniperKills": 44,
        "killstreakCluserStrikeKills": 2,
        "meleeDeaths": 116,
        "timeWatchingKillcams": 39,
        "killstreakTankKills": 0,
        "noKillNoDeath": 10,
        "shotgunDeaths": 88,
        "killstreakChopperGunnerKills": 2,
        "shotsFired": 255,
        "stoppingPowerKills": 2,
        "pistolPeaths": 94,
        "killstreakShieldTurretKills": 1,
        "timeCrouched": 89,
        "noDeathsFromBehind": 949,
        "bombPlanted": 2,
        "setbacks": 0,
        "smgKills": 90,
        "claymoreKills": 23,
        "kills10NoDeaths": 1,
        "pistolHeadshots": 55,
        "killstreakVTOLJetKills": 12,
        "headshots": 130,
        "mostDeaths": 103,
        "adsKills": 124,
        "empDroneHits": 4,
        "defenderKills": 126,
        "launcherHeadshots": 2,
        "timesSelectedAsSquadLeader": 0,
        "killstreakAirKills": 21,
        "assaults": 0,
        "fragKills": 28,
        "killstreakEmergencyAirdropUsed": 0,
        "captures": 89,
        "killstreakChopperSupportKills": 2,
        "spawnSelectBase": 0,
        "noKill10Deaths": 3,
        "leastDeaths": 183,
        "killstreakSentryGunKills": 0,
        "longestTimeSpentOnWeapon": 2,
        "lowerRankedKills": 158,
        "trophySystemHits": 9,
        "clutchRevives": 0,
        "lowestAvgAltitude": 82,
        "pickups": 0,
        "pistolKills": 181,
        "reloads": 166
      }
    }
  },
  "weekly": {
    "all": {
      "properties": null
    },
    "mode": {},
    "map": {}
  },
  "engagement": null
}
```