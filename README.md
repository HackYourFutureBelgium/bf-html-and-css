# HTML & CSS

> ![html & css](./assets/html-css.png)

_HTML & CSS_: HTML (the Hypertext Markup Language) and CSS (Cascading Style
Sheets) are two of the core technologies for building Web pages. HTML provides
the structure of the page, CSS the (visual and aural) layout, for a variety of
devices. Along with graphics and scripting, HTML and CSS are the basis of
building Web pages and Web Applications.

- [Learning Objectives](#learning-objectives): what you will learn from this
  module
- [Suggested Study](./suggested-study.md): Helpful links for this module, useful
  but not required.
- [Deliverables](./deliverables): Projects to practice applying the learning
  objectives in context
- [Lesson Plans](./lesson-plans): A few ideas for running lessons around this
  material.
- [Study Tips](#study-tips)
- [Setting Up](#setting-up)
- [Code Quality Scripts](#code-quality-scripts)

## Learning Objectives

## [1. Developing HTML](./1-developing-html)

Practice with the skills, tools, and workflows you will need to efficiently
develop websites written with HTML.

- **VSCode**: you can ...
  - [ ] use the _LiveServer extension_ to launch an HTML page in the browser
  - [ ] use autocomplete to begin a new HTML document, create new tags, and much
        more
  - [ ] use the _HTML Support_ and IntelliSense extensions to make writing HTML
        more efficient
- **Formatting HTML**: You can ...
  - [ ] use VSCode configurations to format your code on save
  - [ ] use `npm run format` to format all the code in your repository
- [ ] **Validating HTML**: You can use the `npm run validate:html` script to
      find mistakes in your HTML, and you can fix the mistakes.
- **Browser Developer Tools**: You can ...
  - [ ] inspect the source code of a web page using the Sources tab
  - [ ] find any part of the web page in the Elements tab of your Dev Tools DOM
        inspector
  - [ ] make temporary changes in a web page from the Elements tab to see how
        they will look
- [ ] HTML elements
- [ ] HTML attributes
- [ ] HTML comments
- [ ] HTML links
- [ ] HTML tables
- [ ] HTML lists
- [ ] HTML Iframe
- [ ] HTML entities
- [ ] HTML symbols
- [ ] HTML forms
- [ ] HTML media

## [2. Developing CSS](./2-developing-css)

Practice with the skills, tools, and workflows you will need to efficiently
develop websites written with HTML and CSS.

- **VSCode**: you can ...
  - [ ] use the _HTML CSS Support_ and IntelliSense extensions to make writing
        HTML and CSS more efficient.
- **Formatting CSS**: You can ...
  - [ ] use VSCode configurations to format your code on save
  - [ ] use `npm run format` to format all the code in your repository
- [ ] **Linting CSS**: You can use the `npm run lint:css` script to find
      mistakes in your CSS, and you can fix the mistakes
- **Browser Developer Tools**: You can ...
  - [ ] inspect the source code of a web page using the Sources tab
  - [ ] find any part of the web page in the Elements tab of your Dev Tools DOM
        inspector
  - [ ] find the styles for any element in the Elements tab
  - [ ] make temporary changes in a web page from the Elements tab to see how
        they will look
- [ ] css selectors
- [ ] CSS comments
- [ ] Box model
- [ ] Display
- [ ] Position
- [ ] Z-index
- [ ] Overflow
- [ ] Combinators
- [ ] Float
- [ ] Inline-block
- [ ] pseudo class
- [ ] pseudo elements
- [ ] CSS units
- [ ] Specificity
- [ ] importance

## [3. Responsive Design](./3-respnosive-design)

Make your website respond to the user’s behavior and environment based on screen
size, platform and orientation.

- **CSS media queries** :
  - **VSCode**: you can ...
  - [ ] use the _HTML CSS Support_ and IntelliSense extensions to make writing
        HTML and CSS more efficient.
- **Browser Developer Tools**: You can ...
  - [ ] inspect the source code of a web page using the Sources tab
  - [ ] use device toolbar to view your website on different devices
  - [ ] add media queries to make sure your website respond to screen size
        changes
- [ ] View port
- [ ] Media queries

## Study Tips

<details>
<summary>expand/collapse</summary>
<br>

- Don't rush, understand! Programming is hard.
  - The examples and exercises will still be there to study later.
  - It's better to fail tests slowly and learn from your mistakes than to pass
    tests quickly and not understand why.
- Don't skip the examples! Understanding and experimenting with working code is
  a very effective way to learn programming.
- Write lots of comments in the examples and exercises. The code in this
  repository is yours to study, modify and re-use in projects.
- Practice
  [Pair Programming](https://home.hackyourfuture.be/students/study-tips/pair-programming):
  two people, one computer.
- Take a look through the
  [Learning From Code](https://home.hackyourfuture.be/students/study-tips/learning-from-code)
  guide for more study tips

### Study Board

Creating a project board on your GitHub account for tracking your study at HYF
can help you keep track of everything you're learning. You can create the board
at this link: `https://github.com/your_user_name?tab=projects`.

These 4 columns may be helpful:

- **todo**: material you have not studied yet
- **studying**: material you are currently studying
- **to review**: material you want to review again in the future
- **learned**: material you know well enough that you could help your classmates
  learn it

</details>

---

## Setting Up

> You will need
> [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
> installed on your computer to study this material

1. Clone this repository:
   - using HTTPS:
     `git clone https://github.com/HackYourFutureBelgium/bf-html-and-css.git`
2. navigate to the cloned repository
   - `cd bf-html-and-css`
3. Install dependencies:
   - `npm install`

> It's highly recommended that you use either Linux or Mac. If you have a
> Windows computer you can either dual-boot your computer or install a virtual
> machine.

---

## Code Quality Scripts

<details>
<summary>expand/collapse</summary>
<br>

This repository comes with some scripts to check the quality of this code. You
can run these scripts to check the code provided by HYF, and to check the code
you write when experiment with the examples and complete the exercises.

### `npm run format`

This script will format all of the code in this repository making sure that all
the indentations are correct, the code is easy to read, and letting you know if
there are any syntax errors.

### `npm run format:check`

Checks the formatting of all files in the repository and throws an error if any
files are not well-formatted.

### `npm run spell-check`

This script will check all of the files in your repository for spelling
mistakes. Spelling is not just a detail, is important! Good spelling helps
others read and understand your programs with less effort.

`spell-check` is not so clever though, it doesn't have _all_ possible words in
it's dictionary and it won't know if you _wanted_ to spell a word incorrectly.
If you think one of it's "Unknown word"s is not a problem, you can either ignore
the suggestion or add the word to the `"words": [ ... ],` list in
[.cspell.json](./.cspell.json).

### `npm run lint:md`

This script will [lint](https://en.wikipedia.org/wiki/Lint_%28software%29) all
the Markdown files in this repository, checking for syntax mistakes and other
bad practices. Fixing linting errors will help you learn to write better code by
pointing out your mistakes _before_ they cause problems in your program.

Some linting errors will take some practice to understand and fix, but it will
be a good use of time.

### `npm run lint:ls` & `npm run lint:css`

This script will [lint](https://en.wikipedia.org/wiki/Lint_%28software%29) the
names of all files and folders in the project to check that they follow the
project naming convention
([kebab-case](https://betterprogramming.pub/string-case-styles-camel-pascal-snake-and-kebab-case-981407998841)).

### `npm run validate:html`

This script will
[validate](https://webplatform.github.io/docs/guides/html_validation/) the HTML
in this repsitory using
[html-validate](https://gitlab.com/html-validate/html-validate).

</details>

## Class recording

<details>
<summary>expand/collapse</summary>
<br>

- [Day 1](https://www.youtube.com/watch?v=ZJnIQBMh3lo)

- [Day 5](https://youtu.be/fT0klkJPF64)

</details>
