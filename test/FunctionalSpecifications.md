## Table of Contents
---

### 1. Introduction 
---
#### 1.1 Overview .....................................................2
#### 1.2 Business Context..........................................2
#### 1.3 Glossary.......................................................2

### 2. General Description
---
#### 2.1 Product/System Functions............................4
#### 2.2 User Characteristics.....................................4
#### 2.3 Operational Scenarios..................................4
#### 2.4 Constraints..................................................4

### 3. Functional Requirements
---

### 4. System Architecture
---

### 5. High-level Design
---

### 6. Preliminary Schedule
---

## 2. General Description

**2.1 Product/System Functions**

* *Log-in Database*
    * When launching the application for the first time in the device, the user is asked to log in if they are a pre-existing user or otherwise create a new account. This information will be kept in a SQL Database. Here we can verify if the user’s login credentials are valid. The database would also have information on the user’s in-game statistics and achievements.
* *Settings*
    * The settings menu allows the user to adjust the game’s settings to their liking or the user could sign out if they choose.
* *Creating a Server*
    * After matchmaking, the user is put into a lobby with an opponent. Node.js will create a server for handling authentication and game sessions. 
* *Tutorial and A.I.*
    * If the user prefers to practice or would just prefer not to compete with other users, they can play in a tutorial or bot game. The tutorial session would have instructions, hints, and advice on how to play the game. A bot session is available for users who are having trouble finding an opponent to play within the normal matchmaking lobby.

**2.2 User Characteristics**

Our app will be free to play and installable in the Google PlayStore. This would require our users to own an Android smartphone device to be able to play the game. The multiplayer functionality requires an internet connection in order to match two people into a lobby, otherwise, they can play offline with a bot.

We aim to make the app easy to use and navigate in order to cater to users who are not as skilled or proficient in technology. This means a simpler UI and clearer instructions. Since Battleships is already a well-known game with straightforward rules, we would expect our users to have knowledge about the game before they have even installed it. Regardless, a tutorial lobby is available for those who are unsure or simply unfamiliar with the rules of the game.

**2.3 Operational Scenarios**

The following scenarios assume that the user has successfully installed the application from the Google PlayStore and is able to launch the game:

* **Launching the App:**
    * Once the user launches the app the first screen they would see first would be the log-in screen. Here the user can log in with a current account, create a new account or otherwise jump straight into the home screen.

    * New users have to sign up with their email address and set up a password. The log-in credentials of this new user are kept in the database to store their progress with the game. They then have the option to log in to a different device but using the same account.

    * Existing users just simply have to type in their log-in details and would be directed into the home screen afterward. The database would verify if the details the user typed in were correct and if otherwise invalid, they would prompt the user to type in a different password.

    * The log-in screen is skipped if a registered user is currently signed in to the game. The user is sent to the home screen right away without prompting them to retype their log-in details once more. If the user signs out of the game then they would have to repeat the process of logging in again as a pre-existing user.

* **Home Screen:**
    * Once on the home screen, the user has three lobbies to choose from: ‘Find Game’, ‘Bot Game’ and ‘Tutorial’. Depending on the option the user chooses to tap on would lead them to a different lobby.

    * The ‘Find Game’ lobby pairs two online users to face against each other. Matchmaking usually takes time as other users might not be available. It can only be joined with an internet connection.

    * The ‘Bot Game’ lobby can be played with or without an internet connection. The user is instantly sent into a game with a bot rather than waiting to be matchmade like the ‘Find Game’ lobby.

    * The ‘Tutorial’ lobby is similar to the ‘Bot Game’ lobby bot has more instructions and added hints to teach unfamiliar users how to play the game.

    * Regardless of which lobby the user chooses to join into, the same screen shows up afterward, the Lobby Screen. Here the user actually starts to play the game. They have to first place their ships into their respective boards. After the planning stage, the battle stage starts and each user gets a turn in trying to guess where the opponent’s ships are located. Whoever gets their ships destroyed first, loses the game and the other player is announced the winner of the game session.

* **User Icon:**
    * In the home screen, a user icon can be located in the top right corner. This leads the user to the User screen where they can view their personal stats and achievements. 

    * The user has the option to change their display name here.

* **Settings Icon:**
    * Another icon available to the user is the settings icon. Here the user can adjust the settings of the game to their preference.
    * The user can sign out of their account in the settings screen.

If the user wishes to leave the app, they just simply have to exit like every other app and if the unfortunate case where they choose to or is involuntarily disconnected from the game, the opposing user is declared the winner. If a user fails to attack in three consecutive turns, they are declared the loser.

**2.3 Constraints**

*iOS version unavailable*   
We are afraid we aren't able to please a lot of users with our Android exclusive product. Apple’s AppStore takes a longer and more complicated validation process. Initially, we will ship the game to Google PlayStore and if we have enough time we could add it to the AppStore. The team uses Android phones and testing it out on iOS devices would be difficult. 

*Time Constraint*   
This would be the team’s first time creating a game, creating a server and also building a mobile app. Learning how to do all of these and actually applying it to our project will not be impossible but would just take a lot of time.

## 4. System Architecture
![System Architecture Diagram](./systemArchitecture.png)

## 6. Preliminiary Schedule
![Preliminary Schedule](preliminarySchedule.png)