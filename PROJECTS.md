# MAKING CHANGES TO THE PROJECTS PAGE

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

## I want to add a new Project to "Current" or "Completed"

Locate the "Current" and "Completed" headers by looking for the comment that says `<!--Current Projects-->` or `<!--Completed Projects-->`. Once you've done that, follow the steps below:

1. Go to the `components` folder and add a new file called `<Project-Name>.vue`. Make the `<Project-Name>` be a 1-3 word description of the project, done in camel-case. This means that the first letter of every word is capitalized. For example, if your project was the **Burke Museum Rooftop Solar Array**, the file you would create in the `components` folder might be called: `BurkeRooftop.vue`. Whatever you name this file, keep track of it, you'll need the name later.
2. Inside of this file, copy and paste the **HTML Template** below. Note that this template includes an image carousel. If you don't want to include the image carousel, it is clearly marked in the HTML block shown below. Once you copied the block, simply delete the carousel if you don't want it. You will notice that there are several `XXXXXXXXXXXXX` preceded by a number. These are all the locations in this HTML that need to be customized for the page. Once you've copied and pasted this template, begin filling in the number followed by `XXXXXXXXXXXXX` according to the outline below:

### Project Template Fill-in Code Descriptions

Code | Description
--- | ---
1 | This part serves as an identifier for the drop down menu. If you look at other project files in the `components` folder, you'll see that this value is either: "one", "two", "three", etc. Count the number of projects in the `components` folder and then add 1 to this number. Write out the full name of this number in place of `1XXXXXXXXXXXXX`. As of writing this documentation, there are 7 projects. **Keep in mind that this value is surrounded by single quotes ('), they need to be there!**
2 | Each project has an icon describing it's system type. Currently there are four options for Icons: **Roof Mounted**, **Ground Mounted**, **Pole Mounted**, and **Carport**. Look at the table below under the **Project Type Icon Table** section to know what to put for `2XXXXXXXXXXXXX` and `3XXXXXXXXXXXXX`.
3 | Reference the table below under the **Project Type Icon Table** section.
4 | This will be the same value as `1XXXXXXXXXXXXX` without the single quotes (').
5 | This is where you will write the project description. You're not limited to text, any HTML will work here. This means you can add lists, break text into paragraph, or do other cool things. To keep things simple though, we recommend that you only write one paragraph to keep things concise.
6 | This is ID for the image carousel. If you do not want to include an image carousel, delete the section surrounded by the comments: `<!-- ############### IMAGE CAROUSEL STARTS HERE ############### -->` and `<!-- ############### IMAGE CAROUSEL ENDS HERE ############### -->`. Use the number version you got in **Code 1**. For example, if the number you found in Code 1 was "eight", then the ID you'd use here is "8". In the code, that would look like: `id="carousel-8"`.
7 | If you've decided that you'd like to include an image carousel with the project, then continue reading. First, navigate to the `static` folder. Inside of this folder, create a new folder with the name of your project as its name. Name the folder the name of the file you're working on (from step 1 above). In this example, the name of the file is `BurkeRooftop.vue`, so your folder name might be `BurkeRooftop`. Inside of this folder, put all the images associated with your project. You'll notice that each image in the carousel is given by the following line of code: `<b-carousel-slide img-src="~/static/7XXXXXXXXXXXXX"></b-carousel-slide>`. Copy and paste this line for every image you have, and replace the `7XXXXXXXXXXXXX` with the file path to each image. In this case that might look like: `~/static/BurkeRooftop/Image1.png`. If you have any other questions, please consult the **I want to add/remove an image carousel to a project** and **I want to add/remove images from an image carousel** sections below.
8 | This will be the same name as the name you came up with in step 1 above with `Proj` appended to the end. In this example, the thing you'd replace `8XXXXXXXXXXXXX` with here is `BurkeRooftopProj`.

### Project Type Icon Table

Icon File Name | `alt` (`2XXXXXXXXXXXXX`) | `src` (`3XXXXXXXXXXXXX`)
--- | --- | ---
`carpotPV.svg` | Car Port Solar Array | `~/static/carportPV.svg`
`groundPV.svg` | Ground Mounted Solar Array | `~/static/groundPV.svg`
`polePV.svg` | Pole Mounted Solar Array | `~/static/polePV.svg`
`roofPV.svg` | Roof Mounted Solar Array | `~/static/roofPV.svg`

### HTML Template for New Project

```html
<template>
  <div>
    <!-- The toggler for the dropdown. -->
    <div v-b-toggle="'1XXXXXXXXXXXXX'" id="project" class="card-header">
      <h3>UW Campus Plan</h3>
      <!-- This image is the black icon for the project. -->
      <img class="project-icon" alt="2XXXXXXXXXXXXX" src="3XXXXXXXXXXXXX">
    </div>
    <!-- This content appears when the accordian menu drops down. -->
    <b-collapse id="4XXXXXXXXXXXXX">
      <br />
      <section>
        5XXXXXXXXXXXXX
      </section>
      <br />
      <!-- ############### IMAGE CAROUSEL STARTS HERE ############### -->
      <!-- THIS ID MUST BE UNIQUE!!! DO NOT FORGET TO CHANGE IF YOU COPY AND PASTE. -->
      <!-- The rest of the elements should be copy and pasted. -->
      <b-carousel
        id="carousel-6XXXXXXXXXXXXX"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <!-- Images. -->
        <b-carousel-slide img-src="~/static/7XXXXXXXXXXXXX"></b-carousel-slide>
      </b-carousel>
      <br />
      <!-- ############### IMAGE CAROUSEL ENDS HERE ############### -->
    </b-collapse>
  </div>
</template>

<script>
export default {
  name: '8XXXXXXXXXXXXX',  // This should be different for each project.
  // The rest of this code should be the same for each project. DO NOT MODIFY.
  data () {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    }
  }
}
</script>
```

3. Navigate back to the `projects.vue` page inside the `pages` directory. If you want to add a project to "Current", find the `<!--Current Projects-->` comment. Otherwise, find the `<!--Completed Projects-->` comment. Once you've found the section you want, paste the following code block wherever you'd like to place the project. The example shown below is an example for the hypothetical Burke Museum Project used in this example. Make adjustments as necessary.

```html
<!-- Burke Museum Project (PUT PROJECT NAME HERE) -->
<div class="project-wrapper">
    <burke-rooftop-proj />
</div>
```

For the `<burke-rooftop-proj />` line, you'll want to replace this with your project. The way you do this is you split the name by captial letters and then add a dash in between the words. This is because this is the code used in Code 8 in the **Project Template Fill-in Code Descriptions**. Examples are shown below to give you an idea of what to put in the `<burke-rooftop-proj />` line.

Additionally, all the project blocks (shown in the code block above) should come one after another in the `project.vue` file in their section in either "Current" or "Completed" projects. Look at the existing entries to see how to do it right.

* BurkeMuseumProj -> `<burke-museum-proj />`
* UWProj -> `<u-w-proj />`
* ABCDEFProj -> `<a-b-c-d-e-f-proj />`

4. Now, in the `projects.vue` file, go to the `<script>` section. Find the block of code that looks like this:

```js
import ManastashProj from '~/components/Manastash.vue';
import CampusPlanProj from '~/components/CampusPlan.vue';
import UWTransportationProj from '~/components/UWTrasportation.vue';
import MercerProj from '~/components/Mercer.vue';
import GridTestbedProj from '~/components/GridTestbed.vue';
import LSBRooftopProj from '~/components/LSBRooftop.vue';
import PortSeattleProj from '~/components/PortSeattle.vue';
```

You'll want to add your project to this list. For this example, using the Burke Museum, the `import` statement would look something like: `import BurkeRooftopProj from '~/components/BurkeRooftop.vue';`. You'll want to add this import statement to the bottom of the list of import statements.

5. Next, you'll want to locate the following block of code that is right below the list of import statements: 

```js
export default {
  name: "Projects",  // Name of the page.
  layout: "secondary",  // The layout used (from layouts folder).
  // This, combined with the import statements, lets us use each individual
  // project component.
  components: {
    ManastashProj,
    CampusPlanProj,
    UWTransportationProj,
    MercerProj,
    GridTestbedProj,
    LSBRooftopProj,
    PortSeattleProj
  },
  head () {  // The name of the page displayed on the browser tab.
    return {
      title: 'Projects | UW Solar'
    }
  },
};
```

You'll see something called `components:`. You'll want to add your project to the end of the list of projects inside of `components:`. In the code block shown above, the `PortSeattleProj` is the last project. You'd add your project (the Burke Museum Project example in this case) to the end of this list. Keep in mind that you'll need to add a comma after `PortSeattleProj`. In the end, the `components:` should look something like this:

```js
  components: {
    ManastashProj,
    CampusPlanProj,
    UWTransportationProj,
    MercerProj,
    GridTestbedProj,
    LSBRooftopProj,
    PortSeattleProj, // <-- Added a comma to second to last item
    BurkeRooftopProj // <-- New Project added down here
  },
```

## I want to update the description of a project

This is really simple. Navigate to the `components` folder and click on the file containing your project. Navigate to the `<section>` tags. This is where the project description is. Simply change the content here to change the project description.

## I want to add/remove an image carousel to a project

Navigate to the `components` folder and click on the file containing your project. If you want to add an image carousel to a project, find the `<section>` tags with the project description. Right underneath the `</section>` tag you'll see a `<br />`. Right underneath that, copy and paste the code block below. If you want to remove an image carousel, navigate to the section of the file that looks like the code block shown below and delete it.

For adding images, consult the **I want to add/remove images from an image carousel** section below.

```html
<b-carousel
id="carousel-X"
v-model="slide"
:interval="4000"
controls
indicators
@sliding-start="onSlideStart"
@sliding-end="onSlideEnd"
>
  <!-- Image Carousel. -->
  <b-carousel-slide img-src="~/static/PROJECT NAME/IMAGE.png"></b-carousel-slide>
</b-carousel>
<br />
```

## I want to add/remove images from an image carousel

Inside of the image carousel (example shown in code block above), you'll see lines of code that look like: `<b-carousel-slide img-src="~/static/PROJECT NAME/IMAGE.png"></b-carousel-slide>`. If you want to add images, make sure that your images are stored in a folder with your project name in the `static` folder as shown by the file path in the line of code: `<b-carousel-slide img-src="~/static/PROJECT NAME/IMAGE.png"></b-carousel-slide>`. Copy and paste this line for every image you have for the project. That's all there is to add images to an image carousel.

## I want to move a project from "Current" to "Completed"

Look at the Projects Page skeleton above. Locate your project. Locate the "Current" and "Completed" headers by looking for the comment that says `<!--Current Projects-->` or `<!--Completed Projects-->`. Simply copy and paste the project into either section to move it. A project "section" example is shown below:

```html
<!--Life Sciences Building Rooftop/BIPV-->
<div class="project-wrapper">
    <l-s-b-rooftop-proj />
</div>
```