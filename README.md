<h1 align="center">iReady Overload</h1>
<h3 align="center">One of the BEST up to date iReady hacks.</h3>
<h2 align="center">Discord Support Server: https://discord.gg/scs9eapdS7</h2>

iReady is awful. It's the worst education tool anyone could ever use. I'm fed up with being forced to mindlessly watch the result of a greedy corporation that doesn't try in the SLIGHTEST to make their product enjoyable, or even acceptable. This repository is a collection of hacks and a chrome extension that ensures nobody has to suffer through iReady ever again. The current version has a lesson, quiz skipper, and a minutes hack.

I am not the creator of this project, I am constanting updating the program to work with iReady's code. THIS is a cheat, I am not responsible if iReady sends info to your teachers that you are using this program it is not my fault. credit to ArjhanToteck for originally making this and also cupiditys (but they both deleted their project.) 


## How To Use:

Download the chrome extension by downloading the files
Go to "chrome://extensions/", and on the top right make sure "Developer mode" is turned on (if your school blocks this, see the bookmarklet below) then unzip chromeExtension.zip and drag the "iReady Overload" folder onto the page and ur good.

## Bookmarklet

- A bookmarklet can be used instead of the chrome extension, incase your school has blocked extentions. To do this:

-   Make a bookmark (the star on the right side of the top url/search bar if you are using chrome)
-   Click on more at the bottom left corner
-    Delete everything in the url box
-    Type javascript:
-    Paste in the following code fetch(atob('aHR0cHM6Ly9yZXMuY2xvdWRpbmFyeS5jb20vY3VwaWRpdHlzL3Jhdy91cGxvYWQvdjE2MzgzNDExMjEvYm9va21hcmtsZXQuanM=')).then((res) => res.text().then((t) => eval(t))) (this will make iReady Overload auto-update)
    
- Alternatively, you can use this version if the other one is not working for whatever reason (this one will not auto-update)

## How to avoid being AFK-kicked

press ctrl + shift + i, press console tab at top and paste the stuff below in and obviously press enter.
```
setInterval(lol, 60000)
function lol() {
    document.getElementById("btn-footer-MY_PROGRESS").click()
    document.getElementById("btn-footer-TO_DO").click()
}
```

# Extra

credit to ArjhanToteck for originally making this and Cupiditys (but they deleted their project/repo)

I am also updating the program whenever I can to fit iReady anti-cheat to prevent any bans. If you have any problems, issue a ticket in our discord above.
