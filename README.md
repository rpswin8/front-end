# rpse
# Rock-Paper-Scissors (RPS） game
 1. Please use the version after android 4.0
 2. Need to add dependency to build.gradle: dependency {......
 Implement "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0"
 3. Need to add dependency to build.gradle: android {......
         <p>buildFeatures {
              <p>viewBinding = true}
## A front-end Android APP development instructions
<p>1. Front-end development includes code and logic development.

<p>2. This is the simplest online rock-paper-scissors(RPS) game android mobile application, excluding iOS and PC. At present, I have edited the layout page xml, UI and simple page jump logic functions.

<p>3. Please use Kotlin for code writing, which can reduce the amount of code and maintain it appropriately. If you use java to write the program, please convert to Kotlin and verify the debugging. It is recommended to use jetpack components such as ViewModel, DataBinding + ViewBinding, etc., and concatenate resources such as centralized storage and management in resources. 

<p>4. For front-end development, please adhere to the concise code, stable operation, consistent safety protection, and try to use automated operation and maintenance programs.

## B front-end Android APP development content
### 1. registration code function (activiti_main)
1-1. Realize registration and login function.

<p>1-2. Save registration and login with password verification function to the client and server.

<p>1-3. Set the default save(code id /asv1) automatic login function. That is, you can log in automatically without password verification. If user cancel the alternative function, user need to log in with password verification every time.

### 2. Set the user list function (bplayer)
2-1. Set the function of displaying the information on the first line of the user list after the user logs in. Click the "Yes" button on the far right, it will become "No" unclickable

<p>2-2. Set up the function of displaying all user information in the user list, and the data comes from the database. Click the "Yes" button on the far right to apply for the game function to the user individually.

<p>2-3. Realize the single selection box function of the game room (9D-1D) and realize the long-term storage function. The user can set any level lower than the number of "POINTS" of the user, but cannot exceed the number of "POINTS". If the number of "POINTS" is reduced beyond the set level, the level will be automatically lowered to adapt to the actual number of "POINTS". If the number of "POINTS" increases, the set level remains unchanged.

### 3. Invite game function (bplayer)
3-1. Set the function of automatic invitation to the game: click the button "auto apply" under (bplayer), it will automatically apply for the game for users of the same level in the game room (9D-1D) that the user has set, and display the text The box "Applying to other users for matchmaking". Each applicant has a 20-second opportunity to choose. If other users agree, both parties will enter the same game table (cgame). If other users choose not to agree or choose no choice, the next user will automatically apply after 20 seconds. If all users do not choose to agree, the text "Automatic application end" is returned.

<p>3-2. Set up a separate invitation to the game function: the user can click the button that displays "yes" in the user list item "Apply" in the (bplayer) to apply to the user individually, the other party will have 20 seconds to choose the time, the other party clicks to agree Button, the two parties enter the same game table (cgame), if the other party does not respond, it will display "application end".

### 4. Realize the game function (cgame)
4-1. After the two sides enter the game table (cgame), they can click the button "your start" on their side, and the button will become "started". If the opponent also clicks the "Start" button, the user's button will also become "Started". At the same time, the countdown numbers of both sides of the game start to count down and display 20, 19,. . . . . 2, 1, 0. During this period, both parties should choose to click on one of the three RPS images as their own side. After the timer ends, the two "$"-shaped images in the middle will become the RPS images of both parties choices, and the words "WIN" and "LOSE" will be displayed in the countdown. If it is a draw, the countdown numbers of both sides will display the text "Tie is void", and the "$"-shaped RPS images patterns of both sides will turn gray: if the side of the countdown does not click the RPS image, the system will If the user does not choose to replace the RPS image, the system will be judged negative.

<p>4-2. The winner item "POINTS" will be awarded "nDx98%", and the other "nDx2%" will be automatically collected by the RPS game website. At the same time, the winner value of the "WIN" item will add “+1” . The item "POINTS" of the loser side will be deducted "nD" points, and the value of the "LOSE" item of the negative side will be increased by "-1". Others remain unchanged. If it is a tie, the game will be invalid, and the client and database of both parties will not save any data.

<p>4-3. "Time and Date" is set to Greenwich International Standard Time. After the game is over, the time will be fixed and saved on the server in synchronization with the results of the game page. Both parties' respective clients.

<p>4-4.  The small radio button(code id /cspn2,cspn3) on the left side of the button "your start", click it will pop up 3 RPS radio buttons, choosing one of them will be used as a default selection. Please realize the long-term preservation function.

<p>4-5. Current countdown performance deviation, please adjust or replace it. And realize that after the countdown ends, it becomes the letter "Win" or "LOSE".

<p>4-6. If both parties continue to choose "Start", they will enter the next game; if one party chooses to withdraw, the game will end and return to the (bplayer) page.

<p>4-7. After the game is over, the 7 user history function (ehistory) and the 8 actual game page (cgame) and the server side are binding and the result is saved on the client side.

<p>4-8 For the logical judgment of the outcome of the game, please go to GitHub or online to search for many open source code for rock-paper-scissors games.

### 5. Setting function (dsetting)
5-1., 5-2. Realize user transfer function, include bank trasfer,credit card transfer,paypal or wechat pay which you can realize, perhaps need to cooperate with back-end development.

<p>5-3. Display user account  information settings display the user's user name, mobile phone number (account),  password(hide) identification information.

<p>5-4. User history record Click the button to go to the following: 7 User history record function (history)

<p>5-5. User feedback. Set the function for users to send feedback to the server to receive and receive from server reply.

<p>5-6., 5-7. without editing

### 6. User history record function (ehistory)
Set long-term preservation of each game record in the client and database. Click on this historical game record to transfer to its fixed game page (cgame).

### 7. Fixed game page (cgame)
Set long-term preservation of each fixed game page (cgame) in the client and database.
