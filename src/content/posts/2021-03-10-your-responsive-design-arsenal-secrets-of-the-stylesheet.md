---
template: blog-post
title: "Your Responsive Design Arsenal: Secrets of the Stylesheet"
slug: /responsive-design
date: 2021-03-09 23:43
description: Some helpful considerations and pointers for beginners interested
  in utilizing responsive web design.
featuredImage: /assets/arsenal-on-ice-idmx.png
---
As the world is continuously driven to surf the web on a plethora of on-the-go devices, this raises an important question for web developers: How do we accommodate for these users? There are a growing number of types of mobile devices, and without set standards (and continued use of old technology), there’s no saying if a user will be viewing a webpage on a brand new 4K monitor or an iPhone 4. It is our job to make a user experience streamline, simple, and free from hassle, but…again, how exactly do we do that?

In this article, let’s go over some key basics of what we call “responsive design”- the design philosophy that makes it easy to accommodate all types of devices on the market. We’ll go through how to utilize special “viewport” CSS units, Media Queries, and what you can do with the flex and grid CSS properties.

## **Viewport Units**

You may be familiar with some of the various units you are able to use in CSS, like pixels (px), ems, and percent (%). Those last two units are relative units, as are the units vw, vh, vmin, and vmax. Like how ems are relative to font size of an element, and percent is relative to the parent element, these “v” units are relative to the size of a user’s browser (or viewport).

Wow! That sounds pretty great- right? You can just replace all of your units with these and make a responsive webpage…right?

*Yeah, if only it were that easy…!*

These viewport units can do a bit of heavy lifting with certain elements you want to keep sized consistently with the browser window. A great example of using a viewport unit is when dealing with pictures.

```css
 /*Make .some-image 50% of viewport width, if it larger than 500px!*/
.some-image { 
  min-width: 500px;
  width: 50vw;
}
```

The CSS snippet above will keep a picture at a minimum width of 500 pixels, but if the user grows the viewport large enough, the picture will grow in tandem with the browser window. You can go even further with this, using the calc() function allows for an incredible number of options when considering how you need to scale things against the viewport.

## **Media Queries**

One of the earlier forms of maintaining a responsive design philosophy is though @media queries. Introduced in CSS2, these are similar to “if” statements for your stylesheet, which makes them great for defining different layouts at different viewport widths. We can set various “breakpoints” to change the style of our CSS, styles that will function better on mobile devices versus desktop devices.

Of course, there are a few things to keep in mind if you’re going to use this in your journey towards a responsive website.

If you don’t already have a meta viewport tag in your HTML (like below), you absolutely should. This ensures that the content on your page can match with various types of devices.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

The other key takeaway from using @media queries is that it is best to design for the devices with the smallest width first and move up to more typical desktop viewport widths later in development. This way, refactoring your CSS will be leagues easier, and you will have already gotten most of the hard work out of the way. You’d be surprised at how much mobile viewport and desktop viewport-oriented CSS overlap!

## **Flex and Grid**

One last helpful tip to speed up your responsive design process are the flex and grid properties in CSS. These properties were created to help make responsive design a much easier process. Flex, or “Flexbox”, is meant for one-dimensional layouts, while the grid property is meant for two-dimensional layouts.

Flexbox works great for aligning items in a row or column, as well as smaller scale designs as well. While you are more limited in how you can change the position of objects that use flex, it is still incredibly robust in what it does.

![An example of a Flexbox layout](/assets/chrome_21-03-09_23-54-35.png "An example of a Flexbox layout")

The grid property is for larger-scale designs that require more intricate layouts. It can easily be combined with the @media queries mentioned above to change its general layout with just a few extra lines of code.

![An example of a Grid layout](/assets/chrome_21-03-09_23-57-26.png "An example of a Grid layout")

- - -

This is just the tip of the iceberg in the glacier of responsive design. I encourage you to go out and explore the wonders of special CSS properties, media queries, and viewport units. Of course, with the world gaining more and more types of devices every day, you’ll still be at the forefront of those unique designs- so keep learning!

Check out some of the articles below for additional information on responsive design!

## **Resources**

* [Nirazan Basnet on viewport units](https://dev.to/nirazanbasnet/viewport-units-in-css-1bdj)
* [Responsive design basics from web.dev](https://web.dev/responsive-web-design-basics/)
* [Leonardo Maldonado's Flexbox vs. Grid](https://blog.logrocket.com/flexbox-vs-css-grid/)