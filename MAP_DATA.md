# MAKING CHANGES TO THE MAP/DATA PAGES

Always make sure to open your Website project in Visual Studio Code before following these tutorials.

## There's a problem with the map. It's not loading/displaying properly

The map and data visualizations were developed by Christoph Strouse using [Tableau](https://www.tableau.com/). To learn more about Tableau, I recommend the following resources:

* https://www.youtube.com/watch?v=TPMlZxRRaBQ
* https://help.tableau.com/current/guides/get-started-tutorial/en-us/get-started-tutorial-home.htm

Ask UW Solar administrators to give you Christophs contact information. He will be able to assist you.

## I'd like to update the map/data visualizations

**NOTE**: This is probably one of the most difficult things to do on the website. Don't try this unless you're VERY experienced with Tableau.

You'll need to get solar array data from Jeremy Park. Ask UW Solar administrators to put you in contact with him. If he no longer is at UW, ask UW Solar administrators to contact the **UW Campus Grid Manager**. Use the resources above to learn how to make graphs/maps with Tableau and host them using Tableaus hosting service. Then click on **Share** and there should be an option to copy and paste some HTML code.

There's one adjustment you'll have to make to the HTML code Tableau gives you. You will see some code between `<noscript>` tags. An example of this is shown below:

```html
<noscript>
    <a href='#'>
        <img alt=' ' src='https://public.tableau.com/static/images/68/68G68CFX6/1_rss.png' style='border: none' />
    </a>
</noscript>
```

You'll need to change this to:

```html
<noscript inline-template>
    <a href='#'>
        <img alt=' ' src='https://public.tableau.com/static/images/68/68G68CFX6/1_rss.png' style='border: none' />
    </a>
</noscript>
```