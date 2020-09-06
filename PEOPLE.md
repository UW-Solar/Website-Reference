# MAKING CHANGES TO THE PEOPLE PAGE

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

The skeleton of the `people.vue` page is shown below:

```html
<template>
  <div class="data-container">
    <!-- The following div adds spacing between page title and navbar. -->
    <div class="data"></div>
    <div>
      <h1>People</h1>
      <br />
      <br />
      <br />
      <br />
      <h2>Faculty</h2>
      <br />
      <section>
        LIST OF PEOPLE
      </section>
      <br />
      <br />
      <h2>Students</h2>
      <br />
      <div class="column">
        <section>
          LIST OF PEOPLE
        </section>
      </div>
      <br />
      <br />
      <h2>Alumni</h2>
      <br />
      <div class="column">
        <section>
          LIST OF PEOPLE
        </section>
      </div>
      <br />
      <br />
      <h2>Friends</h2>
      <br />
      <div class="column">
        <section>
            LIST OF PEOPLE
        </section>
      </div>
      <br />
      <br />
      <h2>Partners</h2>
      <br />
      <section>
        LIST OF PARTNERS
      </section>
      <br />
      <br />
      <br />
      <section>
        MESSAGE AT BOTTOM OF PAGE
      </section>
    </div>
  </div>
</template>

<script>
// JavaScript for People Page
</script>

<style scoped>
/* Styles for the People page */
</style>
```

## I want to add/remove Faculty, Students, Alumni or Partners

If you'd like to add someone to Faculty, Students or Alumni, figure out if they belong in the Faculty, Student or Alumni Category. You'll find a list of people in each category. Go to the bottom of the list of the category you want. You'll see that the last person has no `<br />` after their name. This is simply a line break which puts the persons name on a different line. Otherwise all the names would be displayed one after another. Add the `<br />` to the last person of the list, and directly underneath that, add the new persons name.

If you'd like to remove someone from Faculty, Students or Alumni, figure out if they belong in the Faculty, Student or Alumni Category. Simply remove their name from the list. If the person you're removing happens to be the last person in the list, make sure to remove the `<br />` from the now last person in the updated list. The last person in each list should not have a `<br />` after their name.

If you add someone to Faculty, remember to add a vertical bar and their position at the club. An example might be: `John Doe | Research Advisor`.

If you'd like to move someone from one category to another, follow the steps outlined in the paragraphs above.

If you'd like to add a Partner, use the following template to add a new Parter link to the bottom of the Partners section:

```html
<a href="URL" target="_blank">PARTNER NAME</a><br />
```

Replace `URL` with the website of the partner, and `PARTNER NAME` with the name of the partner. Simply add this to the bottom of the list of partners.

## I want to add a new section

Figure out where you want to add the new section on the page. In between Alumni and Friends? Between Faculty and Students? Once you figure this out, continue.

A "section" of the People page looks like this. Each section always has two `<br />` at the bottom. The `<div class="column">` makes the long list of students be split into 3 columns on a wide enough screen, and when the screen size shrinks enough, it reverts to a single column. The Partners section does not have this, so make sure you decide whether it would make sense to include this feature in your section.

```html
<h2>SECTION NAME</h2>
<br />
<div class="column">
    <section>
        LIST OF PEOPLE
    </section>
</div>
<br />
<br />
```

Simply copy and paste this block in between any sections on the People page, and you'll be good to go.