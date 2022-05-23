<h1 align="center">HTML Picture Element</h1>

[![Netlify Status](https://api.netlify.com/api/v1/badges/3f059b5f-657b-42a0-b835-b717355d5a58/deploy-status)](https://app.netlify.com/sites/picture-element/deploys)

The picture element is an HTML element for declaring images based on different screen sizes or viewport without the need of writing CSS media queries. It takes in two properties, the —`<source>` tag which makes use of the `srcset` property to specify different images based on different screen sizes and a compulsory `<img>` tag that acts as a fallback image in case the browser doesn't support the picture element.

There are a few use-case scenarios in which the picture tag can be very useful, below are three examples of these cases.

- Image type support
- Image width
- Saving Bandwidth

```html
<picture>
   <source media="(min-width: 800px)" srcset="desktop-image.gif" />
   <source media="(min-width: 500px)" srcset="tablet-image.png" />
   <img src="mobile-image.png" alt="Banner image" />
</picture>
```

## Browser Compatibility

![picture-tag-support.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653076517086/7XbrEluqY.png)

Source: [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)
