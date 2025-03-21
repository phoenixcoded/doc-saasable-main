# Styles

Global styles are centralized in one place and can be added in `src/app/globals.css`. Any new global styles should be added there.

{% code title="src/app/globals.css" %}
```css
/* slick-carousel slider */
@import 'slick-carousel/slick/slick.css';
@import 'slick-carousel/slick/slick-theme.css';

/* yet-another-react-lightbox */
@import 'yet-another-react-lightbox/styles.css';
@import '../styles/yet-another-react-lightbox.css';

/* react-leaflet map */
@import 'leaflet/dist/leaflet.css';

/* to remove default browser focus-visible */
body * {
  &:focus-visible,
  &:focus {
    outline: none;
  }
}

html {
  scroll-behavior: smooth;
}

/* scrollbar */
@import '../styles/scrollbar.css';

/* Styles for RTL (right-to-left) direction */
[dir='rtl'] {
  /* Apply RTL direction to slick-slider slides */
  .slick-slider .slick-slide {
    float: left; /* Ensure slides are aligned correctly */
    direction: rtl;
  }

  /* Apply LTR (left-to-right) direction to marquee container */
  .rfm-marquee-container {
    direction: ltr;
  }

  /* Apply RTL direction to marquee container children */
  .rfm-marquee-container .rfm-child {
    direction: rtl;
  }
}

```
{% endcode %}
