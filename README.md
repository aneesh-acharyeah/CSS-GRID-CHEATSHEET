# 📖 CSS Grid Cheatsheet

A complete **CSS Grid Cheatsheet** to help you master two-dimensional layouts with ease. Covers all properties, visual diagrams, and examples. Perfect for beginners and pros!

---

## 📦 Grid Container Properties

| Property            | Values                                                                                               | Description                                                     |
|---------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| **display**         | `grid` \| `inline-grid`                                                                             | Defines a grid container.                                       |
| **grid-template-rows** | `<track-size>` \| `repeat()` \| `minmax()`                                                         | Defines row sizes.                                              |
| **grid-template-columns** | `<track-size>` \| `repeat()` \| `minmax()`                                                     | Defines column sizes.                                           |
| **grid-template-areas** | `"header header"`<br>`"main sidebar"`<br>`"footer footer"`                                        | Defines named grid areas.                                       |
| **grid-template**   | `<rows> / <columns>`                                                                                | Shorthand for defining rows and columns.                        |
| **grid-auto-rows**  | `<track-size>`                                                                                      | Size of implicitly created rows.                                |
| **grid-auto-columns** | `<track-size>`                                                                                    | Size of implicitly created columns.                             |
| **grid-auto-flow**  | `row` \| `column` \| `dense` \| `row dense` \| `column dense`                                        | Controls how auto-placed items flow.                            |
| **gap** (or `grid-gap`) | `<length>` \| `<row-gap> <column-gap>`                                                          | Sets the space between rows and columns.                        |
| **row-gap**         | `<length>`                                                                                          | Sets space between rows.                                        |
| **column-gap**      | `<length>`                                                                                          | Sets space between columns.                                     |

---

## 📦 Grid Item Properties

| Property            | Values                                                                                 | Description                                            |
|---------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| **grid-column-start** | `<number>` \| `span <number>` \| `<name>` \| `auto`                                   | Start line for the item’s column.                      |
| **grid-column-end**   | `<number>` \| `span <number>` \| `<name>` \| `auto`                                   | End line for the item’s column.                        |
| **grid-column**       | `<start> / <end>`                                                                     | Shorthand for `grid-column-start` and `grid-column-end`.|
| **grid-row-start**    | `<number>` \| `span <number>` \| `<name>` \| `auto`                                   | Start line for the item’s row.                         |
| **grid-row-end**      | `<number>` \| `span <number>` \| `<name>` \| `auto`                                   | End line for the item’s row.                           |
| **grid-row**          | `<start> / <end>`                                                                     | Shorthand for `grid-row-start` and `grid-row-end`.      |
| **grid-area**         | `<name>` \| `<row-start> / <column-start> / <row-end> / <column-end>`                 | Assigns the item to a named grid area or specific lines.|
| **justify-self**      | `start` \| `end` \| `center` \| `stretch`                                             | Aligns item horizontally within its grid area.         |
| **align-self**        | `start` \| `end` \| `center` \| `stretch`                                             | Aligns item vertically within its grid area.           |
| **place-self**        | `<align-self> <justify-self>`                                                         | Shorthand for `align-self` and `justify-self`.          |

---

## 🖼 Grid Diagram

```
Grid Container (3x3)
+---------+---------+---------+
| header  | header  | header  |
+---------+---------+---------+
| sidebar |  main   | sidebar |
+---------+---------+---------+
| footer  | footer  | footer  |
+---------+---------+---------+
```

---

## 💻 Example: Basic Grid Layout

```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr 200px;
  grid-template-rows: auto 1fr auto;
  grid-gap: 10px;
}
```

```html
<div class="container">
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="main">Main</div>
  <div class="footer">Footer</div>
</div>
```

---

## 🎨 Example: Responsive Grid with `repeat()` and `minmax()`

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}
```

```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
</div>
```

---

## 📝 Quick Tips

✅ Use `repeat()` for cleaner grid definitions.  
✅ `minmax()` helps create responsive columns.  
✅ Use `grid-template-areas` for semantic layouts.  
✅ `gap` replaces `grid-gap` (legacy).  

---

## 📚 Resources

- [CSS-Tricks Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [MDN CSS Grid Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Grid Garden Game](https://cssgridgarden.com)

