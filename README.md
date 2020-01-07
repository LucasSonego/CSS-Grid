# CSS Grid

<img src="https://raw.githubusercontent.com/LucasSonego/CSS-Grid/master/images/clean.png" />


## Grid Template Areas

>### The best way to define element positions in the grid is by using `grid-template-areas`, since that way the CSS is more readable and it also makes very simple to make changes in the grid.

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

## Grid column and Grid Row
>### Other way to define the position of the elements on the grid is by using `grid-column` and `grid-row`, this way is not very readable and is a little bit confusing, but it allows you to make the elements overlap others if it's necessary

With `grid-column` and `grid-row`, you need to define the grid line that the element starts and also the line that it ends.

Here's an example with **box1**, that starts on column 1 and ends at the column 2, and starts on the row 1 and ends at the row 3:
```css
.box1 {
  grid-column: 1/2;
  grid-row: 1/3;
}
```

```css
.container {
  height: 80%;
  width: 80%;
  display: grid;
  grid-gap: 15px;
  grid-template-columns: 2fr 2fr 1fr;
  grid-template-rows: 1fr 1fr 1fr 2fr;
}

.box1 {
  grid-column: 1/2;
  grid-row: 1/3;
}

.box2 {
  grid-column: 2/4;
  grid-row: 1/2;
}

.box3 {
  grid-column: 2/3;
  grid-row: 2/4;
}
...
```
[Click here to see the CSS file](https://github.com/LucasSonego/CSS-Grid/blob/master/grid-column-and-row.css)


>### Overlap example
```css
.box2 {
  grid-column: 2/4;
  grid-row: 1/2;
}

.box4 {
  grid-column: 3/4;
  grid-row: 1/3;
}
```
Note that **box2** starts on row 1 and ends at the row 2,
and the **box4** starts on row 1 and ends at the row 3

<img src="https://raw.githubusercontent.com/LucasSonego/CSS-Grid/master/images/overlap.png" />
