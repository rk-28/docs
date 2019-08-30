# Map design

Regardless of what you're mapping in Kumu, **design** plays a key role in making sure you and your audience can read the visualization and draw insight from it.

This includes both graphic design and user experience design:
- **Graphic design**—making sure your audience can easily read the map
- **User experience design**—making sure your audience can easily interact with the map, even if they have never used Kumu or seen a system/network map before

This guide covers the basics of effective graphic design and user experience design in Kumu. _Don't_ read this guide as if it were a set of rigid rules you need to follow on every project, but _do_ interpret it as a set of tactics and guidelines that will help you and your audience make sense of complexity.


## Graphic design

**Graphic design** includes all of the actions you will take to represent your information visually. Colors, sizes, shapes, and layouts are


### Color

Color is one of the most common and most effective ways to visually represent your data in Kumu.

You can color-code qualitative data—for example, assign colors to factors in a system based on what section or sub-system they belong to:

![Color coding a map based on qualitative data](/images/qualitative-color-coding.png)

And you can also color-code quantitative data—for example, assign lighter colors to weaker connections and darker colors to stronger connections:

![Color coding a map based on quantitative data](/images/quantitative-color-coding.png)



### Size

Size is a go-to visual tool for representing any numbers stored in your elements and connections.

You can scale the size of elements and connections based on numbers like net worth, total grants received/awarded, or any of our [system and network analysis metrics](/guides/metrics.html).

You can also assign fixed sizes to groups of elements to make them stand out a bit more—for example, you might want

### Shape

Using different shapes can be a great way to distinguish between different types of elements.

Note that Kumu only supports circles and squares by default, but you can check our our FAQ on changing element shape

### Layout




## User experience design


### Describe the map with simple language

When we're talking about Kumu with other Kumu users or here in the documentation, we tend to use terms like "element", "connection", "network map", "system map", etc. But, when you're introducing a map, it's best to eschew technical terms as much as possible and just keep it simple.

For audiences that may not have ever seen a system or network map before, start by defining those terms. Here are some examples to get you started:

| Map type | Example definitions |
| --- | --- |
| Network map | <ul><li>"A visual representation of people and the relationships between them."</li><li>"Similar to a spiderweb, but each corner of the web is a person, and each thread in the web is a relationship between two people. You can trace each thread to figure out who is connected to whom."</li><li>(If you're not mapping people, replace "people" in the definitions above with something more accurate.)</li></ul> |
| System map | <ul><li>"A visual representation of cause-and-effect relationships."</li><li>"Similar to a flow chart, but without a defined starting and ending point. Arrows can point back to other areas of the chart, creating complex flows that sometimes catch you in feedback loops."</li></ul>  |

Next, clearly explain what each "circle" represents (or "square", if you're using them), and explain what each "line" represents. If your map is color-coded, clearly explain how to interpret the color scheme, too.

![Describe the map with simple language](/images/describe-the-map-with-simple-language.png)


### Teach the basics of using Kumu

Many of Kumu's interactive features are intuitive. For example, **scrolling** will zoom in and out of the map, and **clicking** on items will bring up their profiles, where you can see more information. Those behaviors are exactly what you would expect if you're accustomed to popular mapping tools like Google Maps or Waze.

That said, there are plenty of Kumu features that people might not be immediately familiar with, like **clicking and holding** on any item to apply [focus](/guides/focus.html). To that end, it's always a good idea to make a short video or write a short description to teach your audience the basics of interacting with a Kumu map.

![Teach the basics of using Kumu](/images/teach-the-basics-of-using-Kumu.png)

Here's a sample description that we like to use, written in [Markdown](/guides/markdown.html) so that you can copy/paste it right into your project:

```
# Interacting with the map

<kbd>Click and drag</kbd> to move around the map.

Use the toolbar in the top right to zoom in, zoom out, and zoom fit. Or, <kbd>scroll</kbd> to zoom in and out, and press <kbd>\</kbd> on your keyboard to fit your zoom to the map.

Press <kbd>Tab</kbd> on your keyboard to hide/show the sidebar.

<kbd>Hover your cursor</kbd> over circles and lines to showcase anything nearby.

<kbd>Click</kbd> on a circle or line to see detailed information. <kbd>Click</kbd> on the background of the map to clear your selection.

<kbd>Click and hold</kbd> on a circle to focus on its connections, then use the focus toolbar on the right to expand and contract the focus.

Press <kbd>spacebar</kbd> to stop circles from floating around,  then <kbd>click and drag</kbd> circles to move them to a different position. Press <kbd>spacebar</kbd> again to bring back the floating behavior.

Looking for something in particular? Click on the search bar in the upper left of the map, or press <kbd>S</kbd> on your keyboard.

And just for fun, press <kbd>B</kbd> to bump the map!
```


### Explain your controls

![Explain your controls](/images/explain-your-controls.png)


### Define SNA metrics

![Define SNA metrics](/images/define-sna-metrics.png)
