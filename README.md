# Accessible Breadcrumbs  
Standard pattern for breadcrumb navigations. Use this pattern with the help of your CMS or site generator of choice, to populate the breadcrumb navigation items.


## How does it work?  
A breadcrumb navigation is different from other navigations, in that it represents the path from the index, or home page, to the current page.

```html
<nav class="breadcrumb-nav" aria-label="breadcrumb">
  <ol>
    <li>
      <a href="#">
        Index
      </a>
    </li>
    <li>
      <a href="#">
        Sub Page
      </a>
    </li>
    <li>
      <a href="#" aria-current="page">
        Current Sub Page
      </a>
    </li>
  </ol>
</nav>
```

In the markup example, the `<nav>` element has an `aria-label="breadcrumb"` to announce this as a "breadcrumb navigation" to screen readers.  

The `<ol>` is semantically appropriate, as these links are meant to be represented in a hierarchical structure.  

The `aria-current="page"`, or `aria-current="location"` should be placed on the last element in the breadcrumb navigation.  This will append "current page (or) location" to the announcement of the accessible name of the link. For example: "About, current page".  

CSS pseudo elements are used to add in dividers between the list elements, and the current page is purposefully styled differently than the links prior to it, to further visually indicate it as the current page.

You can review the [breadcrumb demo page](https://scottaohara.github.io/a11y_breadcrumbs/) for additional information and usage notes.


## License & Such
This pattern was written by Scott O'Hara ([Website](https://www.scottohara.me), [Twitter](https://twitter.com/scottohara)), referencing resources such as [Using the `aria-current` attribute](https://tink.uk/using-the-aria-current-attribute/), and verifying with the [ARIA Authoring Practices](https://w3c.github.io/aria-practices/examples/breadcrumb/index.html).

It has an [MIT](https://github.com/scottaohara/accessible-components/blob/master/LICENSE.md) license.

Use it, modify it, contribute to it to help make your project more accessible :)
