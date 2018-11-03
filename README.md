# codepath-week-8

Time spent: 4 hours total


## Blue

### Session Hijacking
![sessionhijacking](https://user-images.githubusercontent.com/40126473/47613448-f6aec100-da65-11e8-8b79-49109e1e72f1.gif)

In chrome, I opened the session ID changing tool and the blue site. I also opened a different broswer(safari) and opened the same two sites. In chrome, I logged in using the given credentials. I copied the sessionID from chrome and pasted as new sessionID in Safari. Then I was able to log in to the blue site in safari without entering any credentials. 

### SQLinjection
![sqli](https://user-images.githubusercontent.com/40126473/47613443-d979f280-da65-11e8-936d-c5921813d25b.gif)

I injected ' OR SLEEP(5)=0--' at the end of the URL for salespeople. In other words, I replaced the question marks in the following with ' OR SLEEP(5)=0--' : public/staff/salespeople/show.php?id=??
This resulted in a 5 second delay before displaying Daron Burke's information.

## Red

### IDOR
![idor](https://user-images.githubusercontent.com/40126473/47613450-01695600-da66-11e8-898c-994192309d5f.gif)
I first logged in and got the admin’s list of salespeople. It included some people who weren’t supposed to be on the list of salespeople publically, such as Lazy Lazyman who was fired for stealing. After clicking on show, I saw that his ID was 11. I then logged out of the admin account, looked through the publically available salespeople list, and tried to look for Lazy Lazyman, but he was not available. I clicked on a different salesman (Daron Burke)’s profile and changed the URL so the ID would be set to 11. Then I was able to view Lazy Lazyman’s profile, even though it’s not supposed to be accessible to non-admins.


### CSRF
![csrf](https://user-images.githubusercontent.com/40126473/47613455-0cbc8180-da66-11e8-8e11-eec6fc023c57.gif)
![csrfpart2](https://user-images.githubusercontent.com/40126473/47955498-6a256680-df6f-11e8-92db-d9e5eb337a3f.gif)

I created an HTML file that would load a Ken Barker file with changed info. His last name would appear as Maybe not and his phone number would appear as 123-456-789. His email would appear as under_attack_really@gmail.com if the attack is successful. I submitted a contact form and the feedback was just the link to the file file:///Users/oliviaryu/Documents/rumours_imy.html. Prior to opening this page, I saw the un-updated salespeople list. Ken Barker appeared normal. After checking feedback, I opened the previous html file I had created. Then I went back to check Ken Barker’s profile. It was changed. 


## Green

### XSS
![cross-site scripting](https://user-images.githubusercontent.com/40126473/47613456-16de8000-da66-11e8-9c7d-2da1edbdd81f.gif)
I submitted a contact form and used the given code: <script>alert('Olivia found the XSS!');</script> as the feedback. Once I logged in as the admin and accessed the feedback page, I got the message Olivia found the XSS!


### User Enumeration
![usernameenumeration](https://user-images.githubusercontent.com/40126473/47613459-21991500-da66-11e8-945e-193e4fa9c92c.gif)
I tried different usernames, both valid and invalid ones.
The valid ones resulted in a bolded error message, while the invalid ones resulted in normal text. This is a vulnerability because if an attacker realizes that the usernames that resulted in bolded error messages were valid ones, they would target that specific username and try to find its corresponding password until they find it. 
