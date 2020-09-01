# DOCUMENTATION

Welcome to the Documentation for the UW Solar Website! If you're looking for information on how to make an edit on the website, this is the place to be. If you're brand new to the club and are looking to get set up to make changes to the website, you'll need to follow the following steps. 

**IF YOU HAVE NO EXPERIENCE WITH HTML, CSS, JAVASCRIPT OR GIT, DO NOT MAKE ANY CHANGES TO THIS WEBSITE!** This website is a fairly complex project that will be overwhelming to anyone with no experience in the aformentioned programming languages. Ideally, students who work on this website should have taken CSE 142, 143, 154 and 391 **AT MINIMUM**.

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

For editing this website, we **HIGHLY RECOMMEND** using Visual Studio (VS) Code to edit the code for the website. It comes with an integrated Command Line and highlights the code nicely. Using Visual Studio Code will make your life much easier. Trust us. You can download it here: https://code.visualstudio.com/.

## 3. Create a GitHub Account

In order to make changes to the website, you'll need a GitHub account. Go to https://github.com/ and create an account. I'd recommend using an email other than your UW email for this account, since your UW email expires once you graduate. Once you do this, have one of the UW Solar administrators invite you to be a collaborator on the [UW Solar Account on GitHub](https://github.com/UW-Solar). Once you're invited, you should get a notification on your account dashboard. Accept the invitation and now you have access to UW Solar's GitHub projects!

## 4. Downloading the files for the Website

Now that you have Node JS, Git, and VS Code Installed, you're ready to begin working on the website. The only thing missing now are the actual files that the website is made of. 

Open up the [UW Solar Website Repository on GitHub](https://github.com/UW-Solar/Website). Click the **Fork** button in the top right corner. You may see a window pop up when you click the Fork button asking you to Fork as your own account or as the UW Solar Account. If this happens click on your account, otherwise do nothing. Now go to your GitHub dashboard, and you should see the forked version of the Website Repository in your account. This will be where you will make all your changes to the website. You'll be able to see if your changes work and in the event that for some reason, the website completely breaks because of your changes, you always have the option of deleting **YOUR VERSION** of the repository and forking the original version again.

Go to the folder where you would like to store the Website on your computer. Right click inside of this website folder and open with **Git Bash**. This will open a command line type terminal where you will enter all the commands shown below.

On your repository, you should see a Green **Code** button. When you click on it, a pop up should appear, and it should say **Clone with HTTPS**. You should see a URL, copy this URL to use later. Then execute the following commands one after another. Wherever it says **URL**, paste the URL from the GitHub page.

```
git init
git remote add origin URL
git pull origin master
```

#### Uploading Changes to your GitHub Repository

Whenever you make changes to the website and would like to update your repository on GitHub, open Git Bash inside of your website folder and enter the following commands:

```
git add .
git commit -m 'DESCRIBE YOUR UPDATE HERE'
git push origin master
```

## 6. Making Changes to the Official UW Solar Website Repository

Now that you've made your changes and you want to update the actual UW website, there's a few things you need to do. Open the website project with Visual Studio Code, and in the Terminal located at the bottom of the screen, type the following command:

```
npm run dev
```

If there is no terminal at the bottom of the screen, go up to the menu bar and select **Terminal**, then select **New Terminal** and a new terminal will appear for you. You can then enter the command shown above.

The website will take a bit to compile, and when it is finished, you will see a message that the website is currently running on the localhost. You'll see a link that looks something like: https://localhost:XXXX, where the XXXX represents a number that is the port the website is hosted on your machine. Usually this number will be 3000, however it may change. Open this URL and check the website in the browser, **MAKE SURE EVERYTHING WORKS!** Once you have made sure all your changes work and the website still functions, show this to one of the UW Solar administrators. When they give you the thumbs up, look at the instructions below on how to add your changes to the official website.

#### Follow these steps:

Run all the commands given in these steps in the VS Code Terminal.

0. Open your website project in Visual Studio Code.
1. Delete the existing `dist` folder.
2. Run `npm install`
3. Run `npm audit`. This command may tell you to run other commands, do whatever it tells you to do.
4. Continue to run `npm audit` until there are very few vulnerabilities (ideally 0, but OK if not).
5. Run `npm install` again
6. Run `npm update`
7. Run `npm run generate`. **This may take a while!** Ignore any errors that don't stop this command from running.
8. 

### IF YOU'RE USING GIT, READ HERE: