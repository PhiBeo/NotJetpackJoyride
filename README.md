![logo](NotJetpackJoyrideProject/Assets/Sprites/UI/MainMenu/main-menu.png)

# About the Project
- A clone of the famous mobile game "Jetpack Joyride" where player need go through obstacles in a 2D side scroll setting. Player need to try try alive to earn the highest score.

# Project Information
- Unity Editor Version: 2022.3.23f1
- Project clone command:
  `
git clone https://github.com/The-Odd-Institute/NotJetpackJoyride.git
  `

  OR
- [Download](https://github.com/The-Odd-Institute/NotJetpackJoyride/archive/refs/heads/main.zip) the repository
- Folder to open and start: Scenes -> 00_Menu
  ### Packages for my parts
  - Authentication
  - Leaderboards

# Contribution to the project:
- Simple profile system setup (unity Authentication Service)
- Leaderboard system
- Local save and load system

# How are they implemented:

## Simple profile:
- Using Unity's Aunthentication Package
- The Authenticate service needed to be initialize first
- Player will be sign-in anonymous since there are no data transfering system in the current state
- It will give a random name which can be update using UpdateName method

<p align="center">
  <img src="NotJetpackJoyrideProject/Assets/Sprites/Profile.gif" width="720">
</p>

## Leaderboard system/UI:
- Using Unity's Leaderboards Package
- A leaderboard need to be create on Unity's Cloud first, an ID which was named will be the thing to retrieve and push datas on the cloud
- Metadata was used so there will be some small change from the default function to push and give extra datas
- A JSON formated string will be return when request information from the Leaderboard which need to be deserialize
- Certain amount of top highscore can be retrieve
- There a prefab of the UI that have texts that can be change according the top scorers
- Those prefab objects will be instantiate and then change according to the top players from a list

### The player score before the update
<p align="center">
  <img src="NotJetpackJoyrideProject/Assets/Sprites/Leaderboard_Before.gif" width="720">
</p>



### Player's score will be update if their score is higher than the previous highest score and store it on Cloud
<p align="center">
  <img src="NotJetpackJoyrideProject/Assets/Sprites/Leaderboard_After.gif" width="720">
</p>



### Player's information like ID, highest score, metadata will be store and display for easier observe and adjust
<p align="center">
  <img src="NotJetpackJoyrideProject/Assets/Sprites/Leaderboard_On_Cloud.png" width="720">
</p>



## Local save and load system:
- Have a main object to handle save and load
- This will go over save and load override functions finded in the classes that inheritance from IDataPersistence class
- It will be saved to the default path for different OS
- This will be inititalize everytime the game start to load the datas that been saved before


# Challenges encounter:
- Learn how Unity Cloud work and how to request and store datas being send back
- Need to get a little more familiar with aysnc since I personal have not use much before
- Scores storing on the cloud is easy but send and store metadata required a bit of time to understand and implement

# Other Contributors:
- Project Manager: Ivan Lavrentyev [<img src="https://github.com/NicholasOkovic/NotJetpackJoyride/assets/139954443/c822852d-919a-49d6-b377-ee0781258936" width="16">](https://github.com/SleepingDragon0) 
- Tech and System Lead: Leah Taurisano [<img src="https://github.com/NicholasOkovic/NotJetpackJoyride/assets/139954443/742280df-39a0-47c9-8665-f5733e589e7f" width="16">](https://github.com/LeahTaurisano) 
- Gameplay and Visual Programmer:
  - Character control: Taylor Daviss [<img src="https://github.com/NicholasOkovic/NotJetpackJoyride/assets/139954443/0ac794c1-d76e-4cc7-be9f-8a6e3dc693dc" width="16">](https://github.com/twdaviss) 
  - Particle and lasers: Nicholas Okovic [<img src="https://github.com/NicholasOkovic/NotJetpackJoyride/assets/139954443/f2c4675a-b38a-4551-8ac2-e0234ec5df36" width="16">](https://github.com/NicholasOkovic) 
  - Art and coin generator: Tin Ly [<img src="https://github.com/NicholasOkovic/NotJetpackJoyride/assets/139954443/7c19a2af-05cf-49fa-9c1e-d1d088b4a17c" width="16">](https://github.com/CultyMarble) 
  - Player controller: Miguel Ayala [<img src="https://github.com/NicholasOkovic/NotJetpackJoyride/assets/139954443/3ddd6336-0f50-485b-8698-ac1541474f4a" width="16">](https://github.com/MiguelAyala25) 
- Instructor: Amir Jahanlou [<img src="https://avatars.githubusercontent.com/u/15884402?v=4" width="16">](https://github.com/AmirJahan) 
