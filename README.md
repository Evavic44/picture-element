<h1 align="center">HTML Picture Element</h1>

The picture element is an HTML element for declaring images based on different screen sizes or viewport without the need of writing CSS media queries. It takes in two properties, the —`<source>` tag which makes use of the `srcset` property to specify different images based on different screen sizes and a compulsory `<img>` tag that acts as a fallback image in case the browser doesn't support the picture element.

## Use Cases
There are a few use-case scenarios in which the picture tag can be very useful, below are three examples of these cases.

### Image type support
Images have a variety of formats like AVIF, and WEBP, which have many advantages but might not be supported by all browsers. The picture tag is great in this case for offering alternative formats using the `<source>` tag. Source: [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)

### Image width
Decide what image to show based on different screen sizes. This can be especially important if you want to preview a large image on desktop screens and a smaller image on mobile or tablet screens.

### Saving Bandwidth
The picture tag can be great for saving bandwidth which in turn speeds up page load time by loading the most appropriate image for the viewer's display.

## How it works
I'll be demonstrating how the picture tag works by building a simple webpage that shows a **6MB** large `gif` image on desktop, a **200kb** `PNG` image on tablet, and finally a **60kb** `PNG` image on mobile. This is how images are optimized in some websites, it helps create a wonderful experience for mobile users and positively improves SEO and performance.

```html
<picture>
   <source media="(min-width: 800px)" srcset="desktop-image.gif" />
   <source media="(min-width: 500px)" srcset="tablet-image.png" />
   <img src="mobile-image.png" alt="Banner image" />
</picture>
```

We specified the desktop image and gave it a min-width of 768px which means on tablet screens(768px) and higher, we want to show the desktop image and on less than tablet screens(mobile screens and below), we want to load the mobile image. 

*Here’s a codepen example, you can resize the screen to see the effect.*

## Browser Compatibility

The picture tag is supported on most browsers except good old "Internet Explorer" but I wouldn't bother about that because Microsoft announced they will discontinue IE on [June 15 2022](https://docs.microsoft.com/en-us/lifecycle/announcements/internet-explorer-11-end-of-support). So it's safe to say all major browsers will support the picture tag from next month. 😅

![picture-tag-support.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653076517086/7XbrEluqY.png)

Source: [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)

## Finally

