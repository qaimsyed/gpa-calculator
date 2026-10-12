# GPA Calculator

A simple, fast web app that calculates your semester GPA from your subjects, credit hours, and grades. It runs entirely in the browser, so there is nothing to install and no data leaves your device.

## Features

- Add as many subjects as you need, and remove any you don't
- Choose a letter grade (A to F) for each subject
- Calculates GPA using the credit-hour weighted formula
- Checks your input and shows a clear message if something is missing or wrong
- Saves your result as a PDF report (`GPA_Report.pdf`)
- Works on both desktop and mobile screens

## How it works

Each grade is converted to grade points, multiplied by the subject's credit hours, and then divided by the total credit hours:

```
GPA = (sum of grade points × credit hours) / (total credit hours)
```

**Grade scale used:**

| Grade | Points | Grade | Points |
|-------|--------|-------|--------|
| A     | 4.0    | C+    | 2.3    |
| A-    | 3.7    | C     | 2.0    |
| B+    | 3.3    | C-    | 1.7    |
| B     | 3.0    | D     | 1.0    |
| B-    | 2.7    | F     | 0.0    |

Universities use slightly different scales (for example, 3.67 instead of 3.7 for A-). To match yours, edit the `gradeMap` values near the top of the `<script>` section in `index.html`.

## How to use

1. Download or clone this repository
2. Double-click `index.html` to open it in your browser
3. Enter the subject name, credit hours, and grade
4. Click **+ Add Subject** for more subjects
5. Click **Calculate GPA** to see your result
6. Click **Save as PDF** to download a report

An internet connection is needed only for the PDF feature, because it loads the html2pdf.js library online.

## Built with

- HTML
- CSS
- JavaScript (no frameworks)
- [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) for PDF export

## Project structure

```
gpa-calculator/
├── index.html   # the whole app (page, styling, and logic)
└── README.md
```

## Possible future improvements

- Calculate overall CGPA across multiple semesters
- Support different grading scales chosen from a dropdown
- Save entered subjects so they are still there after a refresh


