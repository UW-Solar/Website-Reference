# MAKING CHANGES TO THE PROJECTS PAGE

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

## I want to add a new Project to "Current" or "Completed"

Locate the "Current" and "Completed" headers by looking for the comment that says `<!--Current Projects-->` or `<!--Completed Projects-->`.

```html
<template>
  <div>
    <!-- The toggler for the dropdown. -->
    <div v-b-toggle="'two'" id="project" class="card-header">
      <h3>UW Campus Plan</h3>
      <!-- This image is the black icon for the project. -->
      <img class="project-icon" alt="Roof Mounted Solar Array" src="~/static/roofPV.svg">
    </div>
    <!-- This content appears when the accordian menu drops down. -->
    <b-collapse id="two">
      <br />
      <section>
        PROJECT DESCRIPTION
      </section>
      <br />
      <!-- THIS ID MUST BE UNIQUE!!! DO NOT FORGET TO CHANGE IF YOU COPY AND PASTE. -->
      <!-- The rest of the elements should be copy and pasted. -->
      <b-carousel
        id="carousel-2"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <!-- Image Carousel. -->
        <b-carousel-slide img-src="~/static/Campus Plan/CP1.png"></b-carousel-slide>
        <b-carousel-slide img-src="~/static/Campus Plan/CP2.png"></b-carousel-slide>
        <b-carousel-slide img-src="~/static/Campus Plan/CP3.png"></b-carousel-slide>
        <b-carousel-slide img-src="~/static/Campus Plan/CP4.png"></b-carousel-slide>
      </b-carousel>
      <br />
    </b-collapse>
  </div>
</template>

<script>
export default {
  name: 'CampusPlanProj',  // This should be different for each project.
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

## I want to update the description of a project

## I want to add/remove an image carousel to a project

## I want to add/remove images from an image carousel

## I want to move a project from "Current" to "Completed"

Look at the Projects Page skeleton above. Locate your project. Locate the "Current" and "Completed" headers by looking for the comment that says `<!--Current Projects-->` or `<!--Completed Projects-->`. Simply copy and paste the project into either section to move it. A project "section" example is shown below:

```html
<!--Life Sciences Building Rooftop/BIPV-->
<div class="project-wrapper">
    <l-s-b-rooftop-proj />
</div>
```