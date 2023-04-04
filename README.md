# DOCUMENTATION

Welcome to the Documentation for the UW Solar Website! If you're looking for information on how to make an edit on the website, this is the place to be. If you're brand new to the club and are looking to get set up to make changes to the website, you'll need to follow the following steps.

**IF YOU HAVE NO EXPERIENCE WITH HTML, CSS, JAVASCRIPT OR GIT, DO NOT MAKE ANY CHANGES TO THIS WEBSITE!** This website is a fairly complex project that will be overwhelming to anyone with no experience in the aformentioned programming languages. Ideally, students who work on this website should have taken CSE 142, 143, 154 and 391 **AT MINIMUM**.

You'll also want a plan. Talk to UW Solar administrators and figure out exactly what they'd like to change/add on the website.

#### Note

Sometimes, during development, you may notice that you make a change to the website but that change does not appear when you reload the website. This is because your browser is most likely caching certain files (JavaScript files and Images are often cached). Your browser does this to improve performance. If you notice that you're making changes and they're not reflected, clearing the cache will most likely solve the problem. This article does a good job of explaining how to clear the cache on multiple browsers: https://www.pcmag.com/how-to/how-to-clear-your-cache-on-any-browser.

# Resources

To get a solid foundation in HTML, CSS, JavaScript, Git, Node JS, Vue and VS Code, I recommend the following websites/videos:

## HTML

* https://www.w3schools.com/html/
* https://www.youtube.com/watch?v=UB1O30fR-EE
* https://www.geeksforgeeks.org/html-basics/

## CSS

* https://www.w3schools.com/css/default.asp
* https://www.youtube.com/watch?v=yfoY53QXEnI

## JavaScript

* https://www.w3schools.com/js/
* https://www.youtube.com/watch?v=hdI2bqOjy3c

## Git

* https://rogerdudler.github.io/git-guide/
* https://www.youtube.com/watch?v=SWYqp7iY_Tc

## Node JS and Vue

* https://www.w3schools.com/whatis/whatis_vue.asp
* https://www.youtube.com/watch?v=Wy9q22isx3U (Vue)

## VS Code

* https://code.visualstudio.com/docs/introvideos/basics
* https://www.youtube.com/watch?v=VqCgcpAypFQ

# Contents

0. Open your command line
1. Download Node.js and Git
2. Choosing the correct editor
3. Create a GitHub Account
4. Set up Git on your machine
5. Downloading the files for the Website
6. Checking your changes
7. Making Changes to the Official UW Solar Website Repository

## 0. Open your command line

When working on this website, you'll want to get familiar with the command line. There's no way around it. On Windows, press the start button and type **cmd**. You'll see an app show up in the search results called **Command Prompt**. Click on it. This is the place where you will be typing the commands given in this documentation. On Mac, the command line is called the Terminal. To access it, press the Command button and the space bar at the same time, and then type **Terminal** in the search box. Click on the app to open it. You'll also want to pin the terminal app to your toolbar since you'll be using it a lot. From now on, whenever I mention **Command Line**, it'll be the same thing as **Terminal** if you're using a Mac.

## 1. Download Node.js and Git

The first thing to do is to download Node.js. This is what is used to build the website, and is required. You can download it here: https://nodejs.org/en/. Follow all the steps required. To make sure you installed Node.js correctly, open the **Command Line** and type the following command:

```
node --version
```

You should see something that looks like this. The numbers may be different, and that's fine!

```
v10.16.3
```

If you dont't see something like that, then Node.js has not been correctly installed and you'll need to try again until you get the result seen above.


Git is a version control software that you'll use to interact with the GitHub repository. Git will be difficult at first, so please take your time and master the basics of Git. You can download Git here: https://git-scm.com/downloads. As shown above, type the following command in the **Command Line** to ensure Git has been installed properly on your machine.

```
git --version
```

You should see something like this if Git was successfully installed: (The numbers may be different and `windows` might be different as well. That's fine!)

```
git version 2.22.0.windows.1
```

If you don't see something like that, then Git was not installed correctly. Try installing again and then keep checking until you get the correct output.

## 2. Choosing the correct editor

For editing this website, we **HIGHLY RECOMMEND** using Visual Studio (VS) Code to edit the code for the website. It comes with an integrated Command Line and highlights the code nicely. The documentation will assume you are using VS Code and using VS Code will make your life much easier. Trust us. You can download it here: https://code.visualstudio.com/.

Additionally, a few VS Code extensions will come in handy when developing/debugging the code. First, I would use the Vetur extension to help VS Code style and color .vue files. This makes looking over code nicer and plays well with VS Code's IntelliSense functionality: https://marketplace.visualstudio.com/items?itemName=octref.vetur

Second, I recommend using the live server extension when testing if the statically-generated site works (from the dist folder): https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer. 

## 3. Create a GitHub Account

In order to make changes to the website, you'll need a GitHub account. Go to https://github.com/ and create an account. I'd recommend using an email other than your UW email for this account, since your UW email expires once you graduate. Once you do this, have one of the UW Solar administrators invite you to be an **OWNER** on the [UW Solar Account on GitHub](https://github.com/UW-Solar). **MAKE SURE YOU ARE AN OWNER (NOT A COLLABORATOR) OF THE UW SOLAR ORGANIZATION ON GITHUB, OR ELSE YOU WILL NOT BE ABLE TO EDIT THE WEBSITE**. Once you're invited, you should get a notification on your account dashboard or email. Accept the invitation and now you have access to UW Solar's GitHub projects!

## 4. Set up Git on your machine

If this is your first time installing git on your computer, you'll need to do some minor setup. Open the command line and enter the following commands. For `USER NAME HERE` use the user name you used to create your GitHub account. For `EMAIL HERE`, use the email you used for your GitHub account.

```
git config --global user.name "USER NAME HERE"
git config --global user.email "EMAIL HERE"
```

## 5. Downloading the files for the Website

Now that you have Node JS, Git, and VS Code Installed, you're ready to begin working on the website. The only thing missing now are the actual files that the website is made of.

Now, create a folder called something like `UW-Solar-Website` in whatever folder you'd like to store the website files in. Now, open the command line and navigate to this folder. There is something called the `cd` command which stands for **change directory**. This will allow you to navigate to certain folders from the command line. Find the `UW-Solar-Website` file path and paste it in where `FILE_PATH` is shown below:

```
cd FILE_PATH
```

#### IT'S CRITICAL THAT YOU `cd` INTO THE CORRECT DIRECTORY BEFORE DOWNLOADING THE FILES, MAKE SURE YOU DO THIS RIGHT

Example: If you put your `UW-Solar-Website` folder in the Documents folder and you're on Windows, your `cd` command might look something like this:

```
cd C:\Users\USER\Documents\UW-Solar-Website
```

In Mac, it might look like this:

```
cd ~/Documents/UW-Solar-Website
```

Open up the [UW Solar Website Repository on GitHub](https://github.com/UW-Solar/Website). On this repository, you should see a Green **Code** button. When you click on it, a pop up should appear, you should see a menu with several options: **HTTPS**, **SSH**, or **GitHub CLI**. There may be more options depending on when you read this documentation, however you always want to select the **HTTPS** option and use the link associated with that. Copy this URL to use later. Open the command line inside of the folder you created to store the website (remember you can change directories using the `cd` command). Then execute the following commands one after another. Wherever it says **URL**, paste the URL from the GitHub page.

When you type `git pull origin master`, you may be asked to enter a username and password, enter the credentials you used to create your github account if a window pops up asking you to enter a username and password.

```
git init
git remote add origin URL
git pull origin master
```

Now you should see the file explorer on the left side of the screen begin to fill up with files for the website. Wait for these commands to finish running. Once they complete with no errors, you've successfully got all the files for the Website! You may or may not see that VS Code is trying to recommend things for you to download in the bottom right corner. **IF VS CODE SUGGESTS ANYTHING, ACCEPT EVERYTHING VS CODE SUGGESTS AND INSTALL. OTHERWISE IGNORE THIS MESSAGE**. All the add-ons VS Code is suggesting are meant to help improve your experience editing the website. Now you can make the adjustments/edits you need to make. Unless you are a high level HTML, CSS, and JavaScript programmer, please only follow the documentation for making edits to every page. If you follow this documentation closely, you will not run into any errors.

## 6. Checking your Changes

Now that you've made your changes and you want to update the actual UW website, there's a few things you need to do. Open the website folder with the command line (remember to `cd` into the correct directory) and enter the following command:

```
npm run dev
```

The website will take a bit to compile, and when it is finished, you will see a message that the website is currently running on the localhost. You'll see a link that looks something like: https://localhost:XXXX, where the XXXX represents a number that is the port the website is hosted on your machine. Usually this number will be 3000, however it may change. Open this URL and check the website in the browser, **MAKE SURE EVERYTHING WORKS!** Once you have made sure all your changes work and the website still functions, show this to one of the UW Solar administrators. When they give you the thumbs up, look at the instructions below in the **MAKING EDITS** section on how to add your changes to the official website.

#### IF NPM RUN DEV IS NOT WORKING

If `npm run dev` is not working (for example you see "'nuxt' is not recognized as an internal or external command" in the terminal), do this (making sure you're in the top layer of the git directory with the website inside):
1. Run `npm cache clean --force` in the terminal.
2. Delete node_modules by `rm -rf node_modules` folder or delete it manually by going into the directory and right-click > delete. Delete `package-lock.json` file too.
If the `node_modules` folder doesn't exist, run `npm install --save nuxt --force` in the terminal. Then remove `node_modules` and the `package-lock.json` file.
3. Run `npm install` in the terminal. (Try `npm install --force` if this doesn't work)
4. Try running `npm run dev` in the terminal again.

Note: if `npm run dev` works fine but when you try to push the changes to origin, an error occurs, such as `cannot read properties of undefined (reading: hook)` when you try `npm run generate`, the issue might be with you running `npm audit fix --force`. So, I would highly advise against running `npm audit fix --force` unless absolutely necessary, just run `npm audit fix`.

#### SHOW YOUR CHANGES TO A UW SOLAR ADMIN AND GET THEM APPROVED BEFORE DEPLOYING TO OFFICIAL WEBSITE

Below are key things you need to check before pushing your changes to the official UW Solar website, show this to a UW Solar Admin:

1. All images load (Background Image, Icons, Projects Page Images, News Article Images).
2. Check that the Map on the Map page works properly.
3. Click through all pages and skim them to make sure everything looks fine.
4. Click the RSS Link at the bottom of the news page to show that it works.
5. Make sure the archive on the news page has the correct news entries for each academic year.
6. Refresh each page to make sure there are no errors with loading.
7. Resize the page, make sure the navigation bar works properly and that every page looks normal at different page sizes.

## 7. Making Changes to the Official UW Solar Website Repository

Now that you've made your edits and got them approved from UW Solar admins, you can push your changes to the official UW Solar website at `uwsolar.be.uw.edu`. Follow the steps below.

Run all the commands given in these steps in the VS Code Terminal.

And again, we'd like to emphasize that it's critical to follow the guides in this documentation **EXACTLY** when making changes. Otherwise, you will get an error in step 7 below that will be very frustrating to debug. **DON'T SKIM** and read every word of the tutorials.

0. Open your website project in Visual Studio Code and open the terminal in VS Code.
1. Delete the existing `dist` folder.
2. Run `npm install`
3. Run `npm audit`. This command may tell you to run other commands, do whatever it tells you to do. If it doesn't tell you to run any other commands, thats fine as well.
4. If running `npm audit` from the previous step prompted you to run certain commands, then continue to run `npm audit` until there are very few vulnerabilities (ideally 0, but OK if not). **If running `npm audit` from the previous step did not prompt you to run anything, skip this step**.
5. Run `npm install` again
6. Run `npm update`
7. Run `npm run generate`. **This may take a while!** Ignore any errors that don't stop this command from running. If an error does stop this from running you'll see a red error box appear and it is because a mistake was made somewhere in the code you wrote. Go back through every tutorial you followed in this documentation and re-trace the steps you took.
8. Now there should be a new `dist` folder. Open the folder in VS Code (easiest in a new window) and press the 'Go Live' button on the bottom right. This will open the website in your browser. Again, test that every page still works. This step is extremely important if the changes you made go beyond simply adding new content, but additionally change the website's functionality!
9. Run `git add .`
10. Run `git commit -m 'Updated Website DESCRIBE CHANGES'`. In place of `DESCRIBE CHANGES`, write a short, descriptive message of what changes you made. Only use letters and numbers here, no other characters.
11. Run `git push origin master`
12. Run `npm run deploy`. **This will take a while to run.**

Once you complete these steps, the site will automatically update itself. Go back to step 5 and go through the checklist again on the completed site. Make sure everything still works. If you follow all the instructions in this documentation, you should not get any errors. **IF YOU DO GET AN ERROR, MAKE NO CHANGES TO THE WEBSITE AND LOOK AT THE TROUBLESHOOTING SECTION AT THE BOTTOM OF THIS DOCUMENT**.

Depending on the amount of changes you made, the website may take **up to 24 hours** to update. All of these updates are server side, meaning that once `npm run deploy` finishes running, you're free to close all website related things and simply wait for the updates to deploy.

# Making Edits

If you want to make changes to any part of the website, look below. You'll notice that there are several other files in this folder whose names correspond to the headers below. Each of the headers below has a list of things that that document will show you how to edit.

## [HOME PAGE](https://github.com/UW-Solar/Website-Reference/blob/master/HOMEPAGE.md)

* I want to change the content in the "About" section
* I want to change the content in the "Meeting Details" or the "Contact" sections
* I want to add a new section to the UW Solar Home page

## [PROJECTS](https://github.com/UW-Solar/Website-Reference/blob/master/PROJECTS.md)

* I want to add a new Project to "Current" or "Completed"
* I want to update the description of a project
* I want to add/remove an image carousel to a project
* I want to add/remove images from an image carousel
* I want to move a project from "Current" to "Completed"

## [MAP/DATA](https://github.com/UW-Solar/Website-Reference/blob/master/MAP_DATA.md)

* There's a problem with the map. It's not loading/displaying properly
* I'd like to update the map/data visualizations

## [NEWS](https://github.com/UW-Solar/Website-Reference/blob/master/NEWS.md)

* I want to add a news entry for the news page
* I want to make a change to an existing news entry
* I want a certain news entry to be "pinned" at the top
* I want to change the image for a news entry (Multiple images not allowed)

## [PEOPLE](https://github.com/UW-Solar/Website-Reference/blob/master/PEOPLE.md)

* I want to add/remove Faculty, Students, Alumni or Partners
* I want to add a new section

## [FOOTER](https://github.com/UW-Solar/Website-Reference/blob/master/FOOTER.md)

* I want to add/remove a social media icon

## [MISC](https://github.com/UW-Solar/Website-Reference/blob/master/MISC.md)

* I want to change the background image

If what you want to change is not listed above, it most likely requires larger structural changes to the website. If you are a high level web programmer and feel confident in applying these changes, go ahead! If not, then do not make these changes. Either take the time to learn the relevant skills or ask someone else with more web programming knowledge to help you out. Always make sure to check that your changes work!

# Troubleshooting

If for some reason you made changes to the website and everything has completely crashed, you've come to the right place. Below are some ways to fix the website.

## Revert to an earlier version

Git is a version control software, which makes it useful when trying to revert to a previous version of the project. This will be your first option when trying to fix the website. Open the website folder in VS Code and enter the following command.

```
git log --pretty=oneline
```

You may notice that not all commits are shown to you in the output, to see more press enter. To exit out of the log menu, type `wq` in the terminal. This is shown in the large sample code block below.

This will show you a log of all the "commits" (versions) of the website. Shown below is an example of what the output will look like for this project. There will be more commits as time goes on, and you will see those at the top of this list. You should see the commit you wrote in Step 6 on Step 9 where you wrote `git commit -m 'Update Website (Current Date)`. If the website crashes after you committed this, then this is the commit that needs to go. Always choose the commit that comes **BEFORE** the commit that caused the error. Never select the commit that caused the error because that won't bring you anywhere. Otherwise, if you are unsure, the following commit code will always be stable: `73b7cc23cc979f945f8c2b00d6e76870898b7c15`.

You need to copy and paste the commit code (series of letters and numbers at the beginning) of the commit you'd like to revert to. As mentioned, the commit code given above will always work, so if you're unsure about which commit might have messed up the website, use the commit code shown above.

```
73b7cc23cc979f945f8c2b00d6e76870898b7c15 (HEAD -> develop, origin/master, master) Update Website
88e51224544b2ddd26b9512446e7cde8473866ab Update Website
b87eefca81a29f4cf93fe119bf3523eea5a9c2d7 Update Website
2a5cc2de186aae47df6d38a94d13d478f8dc7a66 Update Website
0b3835d65d50dfd4b54e32b53555a7087a89b0c1 current dist folder
a26092c810bdb30d55b46675092802c89e957a89 no .
ed0098131a9518e8e0e505543753f16062f47291 added . to cname
fe11d362f6f1ffb2aa775db8a76ca8a178d6259e custom cname file
43795bda94784288047c57fc3604e68e57a915d3 pre-deploy 1
10d550b1e472070b258ce8c9f44d4e75082a9fad Added cname, fixed date function
993328edebeee8570f5e69b3c82e48fa70b9c1d0 pre deploy commit
: (This is where you press enter to see more commits, or type "wq" to exit out of this menu)
```

Now that you've chosen a commit code, enter the following commands one at a time. Paste your commit code where it says **CODE**.

```
git revert CODE
git push origin master
```

Go to the [UW Solar Website Repository on GitHub](https://github.com/UW-Solar/Website). You should see a commit that says something like `revert "(COMMIT MESSAGE HERE)"`. If you see this, then the reversion has been successful. Follow the steps in Step 6 above to reapply these changes to the official website.

## Other Issues

If the website appears in any capacity, then you know there is an issue with GitHub pages. This means you're seeing the website, but it's obvious something isn't right because the background image isn't showing or there is an error message but the navigation bar still works. If you're seeing something like that, then revert to a previous commit as shown in the previous troubleshooting section.

If you open the website and your browser is showing you a 404 error or a "This site can't be reached" error, then something is wrong with the servers. The person to contact for this is **Brian Vogt (bvogt@uw.edu)**. Let him know there is an error with the UW Solar website (uwsolar.be.uw.edu) and he'll get back to you with some ideas.
