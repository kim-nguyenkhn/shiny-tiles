# Shiny Tiles ✨

Make your buttons (or any row element) shiny ✨✨✨

Shiny Tiles is:
* is a lightweight (?KB) CSS file
* plug-and-play
* customizble in any color!


## How to Use

```html
<!-- STYLESHEET -->
<link rel="stylesheet" href="css/shiny-tile.css">

<!-- HTML -->
<div class="shiny-tile">
    <!-- Put your content here -->
</div>
```


## Behind the Scenes: CSS

```css
.shiny-tile {
    position: relative;

    /* Keep the style inside the container */
    overflow: hidden;

    transition: all 0.4s ease;
}

.shiny-tile:hover {
    /* Give the tile a "pop-out" effect */
    box-shadow: 0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.shiny-tile:after {
    position: absolute;
    /* Set :after as invisible element */
    content: '';
    width: 0;

    /* Flush with the container */
    left: 0;
    bottom: 0;

    /* Don't let it cover the content */
    z-index: -1;

    /* Choose any color */
    background: #f5f5f5;

    /* Angle the transition */
    transform: skewX(-45deg);

    transition: 0.4s;
}

.shiny-tile:hover:after {
    /* Expand the styling */
    left: -10%;
    width: 130%;
    height: 120%;
}
```
