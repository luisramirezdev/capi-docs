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