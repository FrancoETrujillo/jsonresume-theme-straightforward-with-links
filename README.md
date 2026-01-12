# jsonresume-theme-straightforward-fet-adapt

A straightforward [jsonresume](https://github.com/jsonresume) theme with adaptive layouts and enhanced link support.

**Note:** This is a fork of the original [jsonresume-theme-straightforward](https://github.com/slugstack/jsonresume-theme-straightforward) with modifications and enhancements.

## Preview

![Sample Resume](.img/new_straightforward_sample.png)

## Changes from Original

### Header/Basics Section

- Centered layout with name at the top
- Contact information (phone, email, social profiles) in a single centered line
- SVG icons for phone, email, LinkedIn, and GitHub
- Generic link icon (link-45deg.svg) for unrecognized networks with URLs
- Social profiles display actual URLs (e.g., `linkedin.com/in/username`) instead of platform names
- Profiles with empty or null URLs are automatically skipped
- Location only shows comma when city is present

### Work Experience Section

- Adaptive two-line layout when highlights are present:
  - Line 1: `Organization | Title`
  - Line 2: `Date range`
- Compact one-line layout when no highlights: `Organization | Title Date`

### Volunteer Section

- Same adaptive layout as Work section
- Two-line format with highlights, one-line without

### Awards Section

- Adaptive layout based on highlights presence
- Two-line format: `Award Title | Awarder` on first line, `Date` on second
- One-line format: `Award Title, Awarder Date` on single line

### Publications Section

- Adaptive layout based on highlights presence
- Two-line format: `Publication Name` on first line, `Date` on second
- One-line format: `Publication Name Date` on single line

### Education Section

- Maintains original one-line format
- Displays: `Institution | Study Type - Area, GPA Date`

### Print/PDF

- Job blocks avoid splitting when possible
- Orphan/widow control for better page breaks

### Icon Support

- Supports custom SVG icons in the `icons/` folder
- Icons are inlined for portability

## examples

- [as HTML (https://francoet.github.io/jsonresume-theme-straightforward-fet-adapt)](https://francoet.github.io/jsonresume-theme-straightforward-fet-adapt)
- [as PDF (docs/index.pdf)](docs/index.pdf)

## usage

```sh
npm install jsonresume-theme-straightforward-fet-adapt

resume export resume.pdf --format pdf --theme jsonresume-theme-straightforward-fet-adapt
resume export resume.html --format html --theme jsonresume-theme-straightforward-fet-adapt
```

## building local

```sh
npm install
npm start
npm test

npm run export:html
```

Note that running `npm run export:pdf` will result in a different binary every time it's run, even if the source hasn't changed. So it's not the most reliable indicator of differences.
