# CSS Grid

<img src="https://raw.githubusercontent.com/LucasSonego/CSS-Grid/master/images/clean.png" />


## Grid Template Areas
```css
.container {
  display: grid;
  grid-gap: 15px;
  grid-template-columns: 2fr 2fr 1fr;
  grid-template-rows: 1fr 1fr 1fr 2fr;
  grid-template-areas:
    "b1 b2 b2"
    "b1 b3 b4"
    "b5 b3 b6"
    "b7 b7 b6";
}
```
```css
.box1 {
  grid-area: b1;
}

.box2 {
  grid-area: b2;
}
...
```
[Click here to see the CSS file](https://github.com/LucasSonego/CSS-Grid/blob/master/grid-template-areas.css)



<img src="https://raw.githubusercontent.com/LucasSonego/CSS-Grid/master/images/grid.png" />
