# MAKING CHANGES TO THE HOME PAGE

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

The basic skeleton of the Home Page looks something like this:

```html
<template>
  <div class="data-container">
    <div class="occupy-solo">
      <img id="header-img" class="mx-auto animated fadeIn" src="../static/uwsolar.png" alt="UW Solar Logo" title="UW Solar Logo">
    </div>
    <h2>About</h2>
    <br />
    <section>
      "ABOUT" CONTENT HERE
    </section>
    <br />
    <h2>Meeting Details</h2>
    <br />
    <section>
      "MEETING DETAILS" CONTENT HERE
    </section>
    <br />
    <h2>Contact</h2>
    <br />
    <section>
      "CONTACT" CONTENT HERE
    </section>
  </div>
</template>

<script>
export default {
  name: "Home",  // Name of the page.
  layout: "default",  // The layout used (from layouts folder).
}
</script>

<style scoped>
/* All styles for the Home Page here */
</style>
```

## I want to change the content in the "About" section

Navigate to the `Pages` folder. Click on `index.vue`. This is the Home page file. Shown below is the part of the `index.vue` file that contains all the content in the **About** section of the home page:

```html
<h2>About</h2>
<br />
<!-- Main content. Notice how you can put links in it with a tags. target="_blank" opens in new tab. -->
<section>
UW Solar is a <a href="https://vip.uw.edu/about" target="_blank">Vertically Integrated Project</a>
and Registered Student Organization that is part of the
<a href="http://uil.be.uw.edu/" target="_blank">Urban Infrastructure Lab</a> at the University of
Washington. We participate in the planning, design, and development of solar and related electrification 
(e.g., electric vehicles, charging, energy storage) projects and information systems on campus, and 
advise public organizations off-campus (e.g., other colleges, schools, and large public organizations) 
in this subject matter. Students from various disciplines and class standings (Freshman to PhD) work 
together on a diverse set of projects spanning (but not limited to) engineering, architecture, 
construction management, public policy and administration, business and urban planning. Below is a list
of services we provide in Project Development and Advising.
<br />
<br />
<!-- Uses bootstrap row and column classes to make two even columns. -->
<div class="row">
    <div class="column">
        <h3>Project Development</h3>
        <ul>
            <li>Site Evaluations and Shading Analysis</li>
            <li>Photovoltaic (PV) System Preliminary Design</li>
            <li>Cost Estimation and Financial Modeling of Solar Arrays</li>
            <li>Creating and reviewing policy documents with sections for Industry Trends, Federal Regulations, State Law, City Code and UW Policy</li>
            <li>Procurement of Funding</li>
            <li>Request for Proposal (RFP) Drafting</li>
            <li>Contractor Selection</li>
            <li>Reviewing of Installation and Comissioning</li>
        </ul>
    </div>
    <div class="column">
        <h3>Research & Advising</h3>
        <ul>
            <li>Research and Evaluation of Photovoltaic (PV) and Electrical Vehicle (EV) Technologies</li>
            <li>Compile Databases of Available Technologies</li>
            <li>Financial Modeling for implementation of PV/EV Technologies</li>
            <li>Decision Making Models</li>
            <li>Strategic and Spatial Planning</li>
        </ul>
    </div>
</div>
<br />
UW Solar is also offered as a 1-2 credit course in the College of Engineering
(<a href="https://myplan.uw.edu/course/#/courses/ENGR%20297?id=5511afbb-18e5-4b6c-940f-95b14f046817&states=N4Ig7gDgziBcLADrgJYDsAmB7MAJApigOYAWALsrAIxUCsAbADTJjrZgAKWUKZKWaSgCYAHAAYAviAlA" target="_blank">ENGR 297/497</a>)
and in the Department of Urban Design and Planning of the College of Built Environments
(<a href="https://myplan.uw.edu/course/#/courses/URBDP%20498?id=68500d39-af14-4837-ad0e-d20fd202f96c&states=N4Ig7gDgziBcLADrgJYDsAmB7MAJApigOYAWALsrAIxUCcA7ADTJjrZgAKWUKZKWaSgAYAviBFA" target="_blank">URBDP 498/598</a>).
If you decide to take UW Solar for credit, you must take any of the courses listed for two
consecutive quarters. Add codes are available at meetings.
<br />
<br />
UW Solar is an active participant in the <a href="https://green.uw.edu/sustainability-plan" target="_blank">UW Sustainability Action Plan</a>,
and a proud recipient of the <a href="https://green.uw.edu/hga17" target="_blank">Husky Green Award</a>.
</section>
```

Making changes to the text is actually really easy. Just change the text! Make sure all text is in between the `<section>` tags. These tags style the text to be a certain font and size. Anywhere where you see a `<br />` is a line break. This adds space in between paragraphs. Keep this in mind when adding new paragraphs.

To add links, the way to do it is shown below. Look at the links in the code block above as well for reference. `target="_blank"` opens the link in a new tab, and you should add this to every link you add in order for all links to act the same on this website.

```html
<a href="URL" target="_blank">Linked Text</a>
```

If you want to make changes to the "Project Development" or "Research & Advising" sections, look for either `<h3>Project Development</h3>` or `<h3>Research & Advising</h3>`. Right below these headers you'll see something called `<ul>`. This stands for **unordered list** and makes up the bullet points. Each bullet point is encapsulated in a `<li>` tag, this stands for **list item**. Simply follow the pattern to add new items to either list. Make sure to format everything nicely and maintain the good style of the code!

## I want to change the content in the "Meeting Details" or the "Contact" sections

Navigate to the `Pages` folder. Click on `index.vue`. This is the Home page file. Shown below is the part of the `index.vue` file that contains all the content in the **Meeting Details** and **Contact** sections of the home page:

```html
<h2>Meeting Details</h2>
<br />
<section>
    <b>Who: </b>Students of all majors and every class standing. No experience or application is necessary.<br />
    <b>Where: </b>We currently meet on <a href="https://washington.zoom.us/j/99108117155" target="_blank">Zoom Meetings</a>.
    Once UW reopens we will resume our normal meeting space at <a href="http://be.uw.edu/spaces/facilities/gould-hall/" target="_blank">Gould Hall</a> room <b>012C</b>.<br />        
    <b>When: </b>We currently meet every two weeks on Mondays from 6:00 - 8:00 pm. Once UW reopens we will resume our normal meeting times of Mondays and Wednesdays from 6:00 - 8:00 pm.<br />
</section>
<br />
<h2>Contact</h2>
<br />
<!-- Mailto opens the user's mail client. -->
<section>
    If you have any questions, feel free to contact us at <a href="mailto:solaruw@uw.edu">solaruw@uw.edu</a>
</section>
```

As with the **About** section explained above, editing the content of each section is extremely simple. Just change the text as you see fit. Always look for `<h2>SECTION NAME</h2>` (the section name surrounded by `<h2>`) and then look for the `<section>` tags associated with that section. Make any and all content changes inside of the `section` tags.

## I want to add a new section to the UW Solar Home page

The UW Solar home page has 3 sections (as of the completion of this documentation): About, Meeting Details, and Contact. If you'd like to add another section, it's simple, but there are some rules to follow.

Navigate to the `Pages` folder. Click on `index.vue`. This is the Home page file. Shown below is the part of the `index.vue`. This is the file with all the information for the Home page.

The structure of the content on this page is roughly as follows:

```html
<h2>About</h2>
<br />
<section>
    CONTENT HERE
</section>
<br />
<h2>Meeting Details</h2>
<br />
<section>
    CONTENT HERE
</section>
<br />
<h2>Contact</h2>
<br />
<section>
    CONTENT HERE
</section>
<br />
<h2>NEW HEADER</h2>
<br />
<section>
    CONTENT HERE
</section>
<br />
```

The fourth `<h2>` header shows an example of how to integrate a new section header. You can insert this in between any other sections as well. Also note that each header is surrounded by `<br />` break tags to create space between sections. Just follow the template shown above for adding a section and make sure everything works fine when you run `npm run dev` and check out the website on the localhost.