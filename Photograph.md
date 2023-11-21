# CTF Write-Up: OSINT Challenge

## Challenge Information
- **Name:** PHOTOGRAPH
- **Category:** OSINT
- **Description:** Can you help us track down this photographer? 📸

## Challenge Overview
Author provide us a picture of a secret photographer. The objective is to find out who took the photo in order to obtain the flag

## Solution

### Step 1: Gather metadata
Upon visiting the provided URL, I found a given picture. 
![picture](https://i.imgur.com/etMCJVR.jpg)
When come up with these challenge, I often try to gather information about it as much as i can. 
Some tools you can use: 
Aperisolve: https://www.aperisolve.com/
Exiftool: https://github.com/exiftool/exiftool
After that, we can check metadata contain in the picture
![metadata](https://i.imgur.com/X0cTqK2.png)
Bingo, found the artist: **fl0pfl0p5**


### Step 2: It's OSINT time
after a quick search on google, we can find some of her profile accross social media
First on the list, i find a link of her bio: https://about.me/fl0pfl0p5
![bio](https://i.imgur.com/hdUH4hS.png)
Hmm, a *photographer* and *software engineer*. One of a popular website a "software engineer" often use is GitHub. So i give it a try
![github](https://i.imgur.com/3NNeGsU.png)
Luckily, she did have an account: https://github.com/fl0pfl0p5
And it also link to her twitter:https://twitter.com/fl0pfl0p5

Sadly, nothing useful in her profile, so i just search her name on searchbar, and something pop up
![new clue](https://i.imgur.com/WcQMC5O.png)
A new clue appear: **m4r64r1n3**

I also found **fl0pfl0p5's** reddit, which we once again saw our new friend
![reddit](https://i.imgur.com/Xya1p6p.png)
### Step 3: New Identity ?
Base on information we just gather, **fl0pfl0p5** and **m4r64r1n3** is the same person

### Step 4: URL Manipulation
Following the decoded URL led me to another page, where I encountered a URL parameter. By manipulating the parameter, I discovered that setting it to "admin" granted access to an admin dashboard, which contained the final flag.

## Flag
Congratulations! You've successfully navigated the WebAdventure!
- **Flag:** `CTF{WebAdventuresAreFun}`

## Conclusion
The WebAdventure challenge was an interesting journey through various web exploitation techniques, including authentication bypass, hidden input field analysis, and URL manipulation. It demonstrated the importance of source code analysis and creative thinking in CTF challenges.
