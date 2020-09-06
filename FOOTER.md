# MAKING CHANGES TO THE FOOTER

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

The documentation for the footer is limited for a reason. Any changes beyond adding social media icons would mean structural change to the footer, which is impossible to document given the large number of creative avenues you could go down. Always remember that when making changes to this website, there will be future students who will be editing your changes, and if you make them too complex, that doesn't help anyone.

## I want to add/remove a social media icon

Navigate to the `components` folder. Inside here you will see a file called `Footer.vue`. This is where the footer is. Locate the following code block in `Footer.vue`:

```html
<!-- Social media and email information. -->
<div id="footerDiv">
    <a href="https://www.facebook.com/UW-Solar-251198231673083/" class="footerImg" target="_blank"><img class="w-100 m-auto" src="~/static/facebook.png"></a>
    <a href="https://www.instagram.com/uwsolar/" class="footerImg" target="_blank"><img class="w-100 m-auto" src="~/static/instagram.png"></a>
    <a href="https://www.google.com/maps/place/Gould+Hall/@47.6549618,-122.3149216,490m/data=!3m2!1e3!4b1!4m5!3m4!1s0x549014f2574c64b3:0xa7800607c2811e5e!8m2!3d47.6549618!4d-122.3127329" class="footerImg" target="_blank"><img class="w-100 m-auto" src="~/static/map.png"></a>
    <a href="mailto:solaruw@uw.edu" class="footerImg"><img class="w-100 m-auto" src="~/static/email.png"></a>
</div>
```

Austin Miller is the person who made all the icons for this website. Ask a UW Solar Administrator for his contact information and ask him if he can make you a png file that is a white icon with transparent background of whatever social media you'd like to add. Once you have this icon, add it to the `static` folder and use the template below to add the icon to the footer:

```html
<a href="URL" target="_blank"><img class="w-100 m-auto" src="~/static/ICON.png"></a>
```

Replace `URL` with the link to the social media platform and `ICON` with the file name of the icon.