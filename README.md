# nightwatch

###### Assignment
Try this no-fluff guide https://github.com/nightwatchjs/nightwatch/wiki/Windows-Quick-Start
```
This guide is ok but I ran into problems when attempting to run the example tests. 
It doesn't explain the importance of the webdrivers and that they need to be downloaded 
and that the location of these drivers need to be put on the path. It also doesn't set 
you up for how finicky working with Firefox is. The links at the bottom are a bit outdated 
but they did ultimately lead me to the right place. After several hours of frustration I 
finally found the right webdriver for firefox.

Here are the links to the drivers I used. I downloaded each one and extracted them into a 
folder. What folder you put it in doesn't matter but you have to put that folder on the 
System PATH which I did through environment variables.

This site 
http://seleniumhq.github.io/selenium/docs/api/javascript/ 
had the right driver I needed for Firefox 49 (geckodriver).
I also went ahead and downloaded the other drivers as well.
```

1.	Nightwatchjs and prerequisites 
  1. Install nodejs
    * https://nodejs.org/en/
    * Use the 4.6.0 LTS version
      - this will also install npm that you will use to install nightwatchjs
  2. Install nightwatchjs
    * http://nightwatchjs.org/getingstarted#installation
  3. Download this version of selenium.
    * ~~http://selenium-release.storage.googleapis.com/2.53/selenium-server-standalone-2.53.1.jar~~
    * http://selenium-release.storage.googleapis.com/3.0/selenium-server-standalone-3.0.1.jar
      - First one won't work unless using old version of Firefox. Firefox 49 needs 3.0
      - FF 49 also needs [this geckodriver] (https://github.com/mozilla/geckodriver/releases/download/v0.11.1/geckodriver-v0.11.1-win64.zip)
    * Unzip and move to c:\selenium  or something similar    
2. build some test
  1. Follow http://nightwatchjs.org/guide#writing-tests
    * Do the Writing Tests and the Using xpath section
    * Using the example create a set of three test (testname.js) in your ‘tests’ folder
      - Each test should have multiple steps
      - Use their example of doing a google search
  2. Go down to http://nightwatchjs.org/guide#running-tests
    * Play around with the different methods you have for selecting test
    * But at a minimum run all tests in your folder against default and against chrome if you have configured that
