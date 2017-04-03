# Accessible BreadCrumbs

Standard pattern for breadcrumb navigations. Use this pattern with help CMS/framework of choice to populate the navigation items.


## How does it work?

What sets the breadcrumb navigation apart from other navigations on the page, primarily revolves around the labeling and the list element that is used.

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
        Second Page
      </a>
    </li>
    <li>
      <a href="#" aria-current="page">
        Current Page
      </a>
    </li>
  </ol>
</nav>
```  

As noted in the above markup example, the ```<nav>``` element has an ```aria-label="breadcrumb"``` to announce this as a 'breadcrumb navigation' to assistive technology.  

The ```<ol>``` is semantically appropriate, as these links are meant to be represented in an ordered, hierarchical, manner.  

The ```aria-current="page"``` will give additional context to assistive technologies that understand this attribute, that it represents the current page, which is why it is last in the link order.  

CSS is used to add in dividers between the list elements, and the current page is purposefully styled differently than the links prior to it, to further visually indicate it as the current page.


### License & Such

This script was written by [Scott O'Hara](https://twitter.com/scottohara).

It has an [MIT](https://github.com/scottaohara/accessible-components/blob/master/LICENSE.md) license.

Do with it what you will :)
