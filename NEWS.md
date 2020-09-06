# MAKING CHANGES TO THE NEWS PAGE

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

## I want to add a news entry for the news page

We've done our best to streamline this process as we anticipate this will be the thing that is most changed on the website. **Make sure to look at other news entries to see how they are formatted. EVERY FILE IN `content/news` MUST BE A MARKDOWN FILE FORMATTED JUST AS THE TEMPLATE BELOW SHOWS.** Follow the steps below:

1. Navigate to the `content` folder. Inside of this folder, theres another folder called `news`, go inside of this folder. The `news` folder contains a number of `.md` files. These are called "Markdown" files.
2. Add a new `.md` file to the `news` folder. Call it whatever you'd like, the name should give other people an idea of what news article is inside it.
3. Copy and paste the template below into the file. The three dashes (---) at the top and bottom are required, so leave those in. Additionally, **ALL** of these attributes (`title`, `date`, `author`, `content`, and `image`) are required. You don't need to specify an image, but you still need to leave `image: ""` in order for everything to work.

```
---
title: ""
date: ""
author: ""
content: ""
image: ""
---
```

4. Begin filling out each section of the code block shown above. The title should be concise, and all the "content" will be displayed as one large paragraph. There is no way around this. The image is not required, if you don't want the news post to have an image, simply leave the image as is (`image: ""`). If you do want to include an image, go to the `static` folder. Inside this folder you'll find a `News` folder. Put your image inside here and then **ONLY PUT THE IMAGE FILE NAME IN THE IMAGE TAG ABOVE**. There's no need to specify a file path for the image, all you need is the file name. **THE DATE HAS VERY STRICT RULES. IT MUST BE OF FORMAT: MONTH DAY, YEAR**. Look at other news entries as an example. Additionally **IT'S CRITICAL THAT THE MONTH IS SPELLED CORRECTLY**. Months are listed below for your reference:

* January
* February
* March
* April
* May
* June
* July
* August
* September
* October
* November
* December

## I want to make a change to an existing news entry

Navigate to the `content` folder, then go to the `news` folder and find the news entry you're looking for. Make any adjustments to the news article but make sure to follow the rules for formatting for the date and image.

## I want a certain news entry to be "pinned" at the top

This is not possible. The only reason why this is listed in the documentation is so that no one attempts to do this. Each entry is sorted automatically by its date. If it's not part of the current academic year, then it is placed in the archive in the academic year it belongs to. This is why the formatting of the date is so critical.

## I want to change the image for a news entry (Multiple images not allowed)

Only one image is allowed per news article. Doing this greatly reduces the complexity of the site and makes it easier for students to edit. If you'd like to change a news entry image, simply navigate to the `static` folder, then go to the `News` folder, delete the old image and replace it with your new image. You may need to change the file name in the news article markdown file (template shown in code block above).