NotJetpackJoyride

Contribute to the project:
- Simple profile system setup (unity Authentication Service)
- Leaderboard system
- Local save and load system

==========================================================================================================================
How are they implemented:

Simple profile:
- Using Unity's SDK in order to store player information
- The Authenticate service needed to be initialize first
- Player will be sign-in anonymous since there are no data transfering system in the current state
- It will give a random name which can be update using UpdateName method

Leaderboard system/UI:
- Using Unity's Leaderboard SDK
- A leaderboard need to be create on Unity's Cloud first, an ID which was named will be the thing to retrieve and push datas on the cloud
- Metadata was used so there will be some small change from the default function to push and give extra datas
- A JSON formated string will be return when request information from the Leaderboard which need to be deserialize
- Certain amount of top highscore can be retrieve
- There a prefab of the UI that have texts that can be change according the top scorers
- Those prefab objects will be instantiate and then change according to the top players from a list

Local save and load system:
- Have a main object to handle save and load
- This will go over save and load override functions finded in the classes that inheritance from IDataPersistence class
- It will be saved to the default path for different OS
- This will be inititalize everytime the game start to load the datas that been saved before

==========================================================================================================================
Challenges encounter:
- Learn how Unity Cloud work and how to request and store datas being send back
- Need to get a little more familiar with aysnc since I personal have not use much before
- Scores storing on the cloud is easy but send and store metadata required a bit of time to understand and implement