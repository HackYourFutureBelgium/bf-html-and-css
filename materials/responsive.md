# Responsive website

> What is responsive design?

Responsive Web design is the approach that suggests that design and development
should respond to the user’s behavior and environment based on screen size,
platform and orientation.

```css
/* =========== Desktop first ======== */

/* 4K screen */
@media (max-width: 2560px) {
  .showcase {
    width: 100%;
  }
}

/* Desktop */
@media (max-width: 1440px) {
  .showcase {
    width: 90%;
  }
}

/* Laptop */
@media (max-width: 1024px) {
  .showcase {
    width: 80%;
  }
}

/* Tablet */
@media (max-width: 768px) {
  .showcase {
    width: 70%;
  }
}

/* Mobile L */
@media (max-width: 425px) {
  .showcase {
    width: 65%;
  }
}

/* Mobile M */
@media (max-width: 375px) {
  .showcase {
    width: 60%;
  }
}

/* Mobile S */
@media (max-width: 320px) {
  .showcase {
    width: 50%;
  }
}

/* =========== Mobile first ======== */
/* Mobile S */
@media (max-width: 320px) {
  .showcase {
    width: 50%;
  }
}
/* Mobile M */
@media (max-width: 375px) {
  .showcase {
    width: 60%;
  }
}
/* Mobile L */
@media (max-width: 425px) {
  .showcase {
    width: 65%;
  }
}

/* Tablet */
@media (max-width: 768px) {
  .showcase {
    width: 70%;
  }
}

/* Laptop */
@media (max-width: 1024px) {
  .showcase {
    width: 80%;
  }
}

/* Desktop */
@media (max-width: 1440px) {
  .showcase {
    width: 90%;
  }
}

/* 4K screen */
@media (max-width: 2560px) {
  .showcase {
    width: 100%;
  }
}
```
