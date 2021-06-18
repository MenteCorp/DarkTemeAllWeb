# Learn about dark themes

## What is a dark theme?

A dark theme is a theme that is used to make the screen appear darker. It is also called a night theme. Their counterparts are called white themes and light themes.

### Why do I need a dark theme?

Dark theme support is mainly for accessibility improvement. It is especially beneficial for people who are hypersensitive to light or who work at night.

### Common colors used in dark themes

What colors should be used in a dark theme?
- The light theme often uses black text on a white background.
- Dark themes often use white text on a black background.
- Modern dark themes use white or other less-stimulating colors on a background of a color close to black (e.g. #353535).

![Sample Image](IMG/example.png)

## Techniques for applying dark themes on the web.

## CSS
CSS extends the expression and adds color to a website.

For example, what does the DefaultCSS code look like?

```css

/*default_20210614*/
html, body, header, footer, div, article, ul, li, td, address, p, a, b, span, strong, small, h1, h2, h3, h4, h5, aside, iframe, nav, form, th, tr, blockquote
{
    background-color: black !important;
    color: white !important;
}
/*link*/
a:link, a:active, a:hover
{
    color: yellowgreen !important;
}:visited{
    color: orange !important;
}
```

- The background color of many tags is set to black, and the text color is set to white.

- The color of links is changed depending on their status. CSS, the unvisited links and those in the active and hover states are set to yellow-green, and the visited ones to orange.

- You can "override" the CSS by adding "!important" to all elements.

---

The following example shows how to set the CSS for a user.

The following example will determine whether the user is using a white or dark theme in their device settings, and display the appropriate color for that.

```css

/*Light*/
/*For devices with the light theme applied, the background color of the html tag will be white and the text color will be black. */ (prefix)
@media (prefers-color-scheme: light) {
    html {
      background-color: white;
      color: black;
    }
}
/*Dark*/
/*If the device has a dark theme applied, set the background color of the html tag to black and the color of the text to white. */ (prefix)
@media (prefers-color-scheme: dark) {
    html {
      background-color: black;
      color: black;
    }
}
```

### Extensions

With CSS, you can apply various themes to your site, but it doesn't work by itself. To make it work easily in the browser, you can override the CSS with extensions.  
Please see the [guide](guide.en.md).

## Discussion.

### Why don't web sites apply dark themes?

To apply a dark theme, you need to validate when you apply it.
For example, if the logo contains dark colors, the dark theme will bury the colors. It is rare to raise the cost to deal with it.