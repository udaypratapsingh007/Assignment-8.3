# Assignment 8.3 - Magazine Layout Using Grid Areas

## Grid Container

The .magazine container uses display: grid with two columns and four rows. The columns are 3fr and 1fr, so the main article gets three times as much width as the sidebar.

## grid-template-areas

The layout is written as a visual map:

"header  header"
"nav     nav"
"article sidebar"
"footer  footer"

- header, nav and footer each span both columns.
- article and sidebar sit side by side in the third row.

## Named Areas

Each section is placed on the grid with the grid-area property:

- .mag-header uses grid-area: header
- .mag-nav uses grid-area: nav
- .mag-article uses grid-area: article
- .mag-sidebar uses grid-area: sidebar
- .mag-footer uses grid-area: footer

## Sizes and Alignment

The article column is wider than the sidebar (3fr and 1fr). The sidebar uses align-self: start so it keeps its own height at the top of its area instead of stretching to the full height. On screens narrower than 700px, a media query changes the areas into a single column, with the sidebar below the article.
