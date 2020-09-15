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
# Modern Warfare
## - Leaderboards :id=leaderboards

 <h2> Example </h2>

 ```js
 try {
    let data = await API.MWLeaderboard(<page>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWLeaderboard.json ':include :type=code')

## - MP Match Details :id=mp-match-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWcombatmp(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWcombatmp.json ':include :type=code')

## - WZ Match Details :id=wz-match-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWcombatwz(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWcombatwz.json ':include :type=code')

## - MP Details :id=mp-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWmp(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWmp.json ':include :type=code')

## - WZ Details :id=wz-details

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWwz(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWwz.json ':include :type=code')

## - Battle Royale Information  :id=br-info

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWBattleData(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWBattleData.json ':include :type=code')

## - Weekly Stats  :id=weekly-stats

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWweeklystats(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWweeklystats.json ':include :type=code')

## - Loot  :id=mw-loot

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWloot(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWloot.json ':include :type=code')

## - Analysis  :id=mw-analysis

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWAnalysis(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWAnalysis.json ':include :type=code')

## - Map List  :id=map-list

<h2> Example </h2>

 ```js
 try {
    let data = await API.MWMapList();
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/MWMapList.json ':include :type=code')

## - Get Battle Pass :id=battle-pass-loot

<h2> Example </h2>

 ```js
 try {
    let data = await API.getBattlePassLoot(<season>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/getBattlePassLoot.json ':include :type=code')

## - Fuzzy Search  :id=fuzzy-search
!> To search all platforms, pass in 'all'
<h2> Example </h2>

```js
 try {
    let data = await API.FuzzySearch(<text>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
```

<h2> Response </h2>

[filename](_json/FuzzySearch.json ':include :type=code')

## - Get Store Loot :id=store-loot

<h2> Example </h2>

 ```js
 try {
    let data = await API.getPurchasable(<platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/getPurchasable.json ':include :type=code')

## - Get Cod Points  :id=cod-points
!> Logged in user only
<h2> Example </h2>

 ```js
 try {
    let data = await API.getCodPoints(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```
<h2> Response </h2>

[filename](_json/getCodPoints.json ':include :type=code')

## - Logged In User Info  :id=user-info
!> Logged in user only
<h2> Example </h2>

 ```js
 try {
    let data = await API.getLoggedInUserInfo();
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/getLoggedInUserInfo.json ':include :type=code')

## - Connected Accounts  :id=connected-accounts
!> Logged in user only
<h2> Example </h2>

 ```js
 try {
    let data = await API.ConnectedAccounts(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/ConnectedAccounts.json ':include :type=code')

## - Event Feed  :id=event-feed
!> Logged in user only
<h2> Example </h2>

 ```js
 try {
    let data = await API.getEventFeed();
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/getEventFeed.json ':include :type=code')

## - Logged In Identities  :id=identities
!> Logged in user only
<h2> Example </h2>

 ```js
 try {
    let data = await API.getLoggedInIdentities();
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/getLoggedInIdentities.json ':include :type=code')

## - Account Settings  :id=settings
!> Logged in user only
<h2> Example </h2>

 ```js
 try {
    let data = await API.Settings(<gamertag>, <platform>?);
 } catch(Error) {
     //Handle Exception
 }
 ```

<h2> Response </h2>

[filename](_json/Settings.json ':include :type=code')