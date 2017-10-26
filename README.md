# Accessible BreadCrumbs  

Standard pattern for breadcrumb navigations. Use this pattern with help CMS/framework of choice to populate the navigation items.


## How does it work?  
What sets a breadcrumb navigation apart from other navigations, primarily revolves around the labeling of the navigation, and the type of list element that is used.

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

In the above markup example, the ```<nav>``` element has an ```aria-label="breadcrumb"``` to announce this as a 'breadcrumb navigation' to assistive technologies.  

The ```<ol>``` is semantically appropriate, as these links are meant to be represented in an ordered, hierarchical, manner.  

The ```aria-current="page"``` will give additional context to assistive technologies that understand this attribute, that it represents the current page, adding additional context to it's placement in the list/link ordering.  

CSS pseudo elements are used to add in dividers between the list elements, and the current page is purposefully styled differently than the links prior to it, to further visually indicate it as the current page.


## License & Such  
This script was written by [Scott O'Hara](https://twitter.com/scottohara).

It has an [MIT license](https://github.com/scottaohara/accessible-components/blob/master/LICENSE.md).

Do with it what you will :)
