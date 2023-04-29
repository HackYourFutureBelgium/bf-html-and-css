# Development Strategy

A portfolio card to introduce Angela to her colleagues.

---

## Setup

- [ ] Boilerplate HTML file
- [ ] Page title in the HTML file
- [ ] empty CSS file
- [ ] CSS file is linked to HTML

---

## Empty Card

> As a site visitor, I can see a background and border so I know where the card
> is

Before filling in any personal information, there needs to be a card.

- [ ] _there is an empty card on the screen_
- [ ] _with a colored background_
- [ ] _and rounded corners_

### Empty Card: HTML

- an empty div with the `card-container` class

### Empty Card: CSS

- styles for the page and body to position the card
- a `card-container` class to set the card color and corners

---

## Photograph

> As an Amazon employee I can see Angela's face so that I recognize her if we
> cross in the hallways

There should be a clear photograph of the employee, this photo should be
well-sized and fit in a round border.

- [ ] _there is a clear and recognizable photo on the card_
- [ ] _the photo is fit nicely in a round border_

### Photo: HTML

- an image container div inside the main card container with class
  `img-container`
- an image inside the image container with `sub-image` class

### Photo: CSS

- a `img-container` class to position the image in the card
- a `sub-image` class to set a border around, and position the photo

### Photo: Assets

- The photo to load into the `<img>` tag

---

## Name

> As an Amazon employee I can learn Angela's name so I can call her by her name
> next time we meet.

The employee's name should be front and center under their name. The text should
be large enough that it pops out from everything else on the page.

- [ ] _the employee's name is written clearly below their photo_
- [ ] _the name is the largest text in the card_

### Name: HTML

- an element containing the name and a class `image-title`

### Name: CSS

- import the correct font
- set the font for the whole page
- an `image-title` class to style the name text

---

## Description

> As an Amazon employee I can read a description of Angela's interests so we can
> find points in common.

The person's job title should be clearly written between their name and
description.

- [ ] _there is a short introduction to the employee's personal interests_
- [ ] _the intro is under their name_

### Description: HTML

- a container for the introduction paragraph with the `image-header` class
- an introduction paragraph with the `sub-title` class

### Description: CSS

- an `image-header` class to position the description
- a `sub-title` class to style the description's text
