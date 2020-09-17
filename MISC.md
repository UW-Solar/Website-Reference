# MISC


Always make sure to open your Website project in Visual Studio Code before following these tutorials.

Any miscellaneous website changes are here.

## I want to change the background image

Background images are usually large files, so it's best to only have one such file in the project at all times. Follow the steps below to change the background image:

1. Navigate to the `static` folder. Find the image called `UWSolarBackground.png`. Save a copy of this image to the UW Solar Google Drive (somewhere logical, like the Website folder). 
2. Once you've saved a copy, delete the image and replace it with a new image. If the new image is a `png`, then name it `UWSolarBackground.png`, **if the file type of the image is different, then follow the steps below**.
3. Navigate to the `default.vue` file in the `layouts` folder. Inside of `default.vue`, go down to the `<style scoped>` section and find the following code block:

```css
/* Used for the background blur effect when user scrolls on the Home page */
#background-blur {
  background: linear-gradient(to bottom right, rgba(0, 0, 0, 0.19) 0%, rgba(255, 255, 255, 0.21) 100%), url("../static/UWSolarBackground.png");
  background-repeat: no-repeat, repeat;
  background-size: cover;
  background-attachment: fixed;
  height: 100%;
  width: 100%;
  z-index: -10;
  position: fixed;
}
```

Find the following line of code in the code block above:

```css
  background: linear-gradient(to bottom right, rgba(0, 0, 0, 0.19) 0%, rgba(255, 255, 255, 0.21) 100%), url("../static/UWSolarBackground.png");
```

Replace `UWSolarBackground.png` with the name of the new background image and you're done!