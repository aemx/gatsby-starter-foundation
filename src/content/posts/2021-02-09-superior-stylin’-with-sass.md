---
template: blog-post
title: Superior Stylin’ with Sass
slug: /sass
date: 2021-02-09 18:03
description: A quick rundown of some features used in Sass.
featuredImage: /assets/sass.png
---
With the backend complexity of web design becoming more apparent in the past years, it may be useful to consider an alternative to standard CSS, once you have a solid grasp on how these stylesheets work.

But how? CSS is the defined standard for every design element that appears on a website. It isn’t like we could throw in a completely new stylesheet language…unless?

Enter Sass, or “syntactically awesome style sheets”- a preprocessing language made for the simplification of CSS. In this article, we will outline some of the basics of how preprocessors work, and how you can use Sass’s variables and “mixins” to streamline stylesheet workflow.

## **Preprocessing**

Preprocessing is a way simplify and utilize code into doing more by using less actual code. Syntactically, Sass takes out the brackets and semicolons that CSS normally uses. Instead, it uses indentation to denote where blocks of code start and end. This style is similar to programming languages like Python that use whitespace and indentation to look nicer.

Sass can go further than just this, and like a programming language, you are also able to use variables and “mixins”, which have similar functionality to functions.

## **Variables**

Variables can be used in Sass just like they would in other programing languages like JavaScript, C++, or Python. You can define a variable in Sass by using a dollar sign before the variable name, followed by a colon and the value for that variable. This is incredibly useful if you want to experiment with values between certain color schemes you are testing out, or various font sizes, styles- you name it. These variables also have a great use in bigger projects. It is much easier to change out one line of code rather than scrolling through hundreds or even thousands of lines just to change a couple of style settings.

```sass
// Sass code

$my-variable: #1f1e33

.my-class
  background-color: $my-variable
```

```css
/*...processed into this CSS...*/

.my-class {
  background-color: #1f1e33;
}
```

## **Mixins**

Mixins take a similar role to that of a function would be in other programing languages. Using an at sign (@), you are able to take a set of declarations that are bundled together and stick them anywhere in a normal set of properties. This makes it easy to define common groups of declarations like borders and shadows, margins and padding, or even font options; like weight, character spacing, and line spacing. You can even use it to bundle vendor prefixes in order to support other browsers with ease.

Another great use of Mixins is the ability to pass arguments through your definitions. Not only can you add in these arguments, but you can customize them to include a default value in the situation that one is not defined by you when using it. You can override this default value just by defining what you would like to be changed to, which is a powerful tool, like variables are.

```sass
// Sass code

@mixin my-mixin($opacity: 1)
  background-color: rgba(0, 0, 0, $opacity)
  color: white
 
.my-class
  @include my-mixin

.our-class
  @include my-mixin(0.75)
```

```css
/*...processed into this CSS...*/

.my-class {
  background-color: rgba(0, 0, 0, 1);
  color: white;
}

.our-class {
  background-color: rgba(0, 0, 0, 0.75);
  color: white;
}
```

- - -

This all being said, Sass is a great resource for managing stylesheets on bigger projects, or another way of minifying your code to make it easier to read and to change.

You can go even further with Sass by reading some of the resources that were used in this article below!