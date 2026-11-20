# Student Resume Website

A clean, ATS-friendly, one-page A4 student resume built with plain HTML, CSS and JavaScript. There are no frameworks, no libraries and no build tools. It is designed for people with zero coding knowledge: you only edit a few lines of text.

## Features

- 5 ready-made themes: Professional Blue, Modern Dark, Minimal White, Elegant Purple, Corporate Green
- Change the whole look by changing one number
- All student details are kept in one place and the resume builds itself
- Sections with no information are hidden automatically
- Supports multiple education entries, projects and certifications
- Print-ready A4 layout with one-click **Download / Save as PDF** (uses the browser's print feature)
- Warns you on screen if the resume is longer than one page
- Responsive on desktop, tablet and mobile
- Semantic HTML with selectable text, no images and no skill charts, so it is easy for resume parsers to read (compatibility with every ATS is not guaranteed)
- No external dependencies and works offline

## Files

```
resume/
├── index.html   (content, settings and JavaScript)
└── style.css    (design and themes)
```

Keep both files in the same folder.

## How to use

1. Download or clone this repository.
2. Open `index.html` in a text editor (Notepad is fine).
3. Edit only these two parts inside the `<script>` tag:
   - `SELECTED_THEME`: a number from 1 to 5
   - `student`: your personal information
4. Save the file and open `index.html` in Google Chrome.

### Editing student information

- Change only the text between the quotation marks.
- To add another skill, project, education entry or certificate, copy one complete entry (from `{` to `},`) and paste it below.
- To hide a section, leave it empty: `[]` for lists or `""` for text.

### Changing the theme

```js
const SELECTED_THEME = 1;
```

| Number | Theme |
|--------|-------|
| 1 | Professional Blue (default) |
| 2 | Modern Dark |
| 3 | Minimal White |
| 4 | Elegant Purple |
| 5 | Corporate Green |

An invalid number falls back to Theme 1.

### Saving as PDF

1. Click **Download / Save as PDF**.
2. Choose **Save as PDF** as the destination.
3. Set paper size to **A4** and margins to **Default**.
4. Click **Save**.

The Modern Dark theme automatically prints as a white, ink-friendly page.

## Adding a new theme (for example, Theme 6)

1. In `style.css`, copy the `.theme-5` block, rename it `.theme-6` and change the colour values.
2. In `index.html`, add the theme name to the list in the comment at the top of the script.
3. In `index.html`, change `const VALID_THEMES = [1, 2, 3, 4, 5];` to `[1, 2, 3, 4, 5, 6]`.

## Tips for a one-page resume

- Keep the career objective to 2 or 3 lines.
- List only your most relevant projects.
- Keep project descriptions short.
- If an orange warning appears on screen, shorten the content before printing.

## Browser support

Works best in the latest Google Chrome. It also works in Edge, Firefox and Safari.

## License

Free to use and modify for personal and educational purposes.
