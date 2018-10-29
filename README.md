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



### CSRF
![csrf](https://user-images.githubusercontent.com/40126473/47613455-0cbc8180-da66-11e8-8e11-eec6fc023c57.gif)


## Green

### XSS
![cross-site scripting](https://user-images.githubusercontent.com/40126473/47613456-16de8000-da66-11e8-9c7d-2da1edbdd81f.gif)


### User Enumeration
![usernameenumeration](https://user-images.githubusercontent.com/40126473/47613459-21991500-da66-11e8-945e-193e4fa9c92c.gif)
