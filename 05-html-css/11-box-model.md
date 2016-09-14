# Box Model


## Learning Goals 📚
-
-

## What is the Box Model

**Every** element on a page is a rectangular box.

In a document, each element is represented as a rectangular box. Understanding the structure of an elements box is essential in setting it's size and the position.

In CSS, each of these rectangular boxes are described using the standard box model. This model describes the content of the space taken by an element.

Each box has four edges:
- Margin edge
- Border edge
- Padding edge
- content edge.

![Box Model Diagram](imgs/css-box-model.jpg)
*[Image source](http://www.slideshare.net/niciuzza/css-box-model-25142045)*


With a site you have already created, add the following:
```css
  * {
    border: black 1px solid;
  }
```
Adding a border to every element will show you it's box and the space it actually takes up.

## Altering an Element's Box Model

There are several properties that determine the size of that box. The core of the box is defined by the width and height of an element, which may be determined by the display property, by the contents of the element, or by specified width and height properties.

By adding margin, border or padding, you are adding on to the block's width.

### It all Adds Up!

According to the box model, the total width of an element can be calculated using the following formula:
margin-right + border-right + padding-right + width + padding-left + border-left + margin-left

And this formula for the height:
margin-top + border-top + padding-top + height + padding-bottom + border-bottom + margin-bottom

This is important to consider when setting an element's width. Even if you have two elements with a width of 50%, they will not show up side by side if there is any padding, margin or border adding to the widths.

** Note ** A lot of front-end developers prefer to set the width or height to *include* the padding and border along with the content, but not the margin. [This article](http://www.paulirish.com/2012/box-sizing-border-box-ftw/), written by a google chrome developer, demonstrates how to do so!


## Measurements

You site may be viewed on a wide range of devices, from mobile phones to 50" smart TV's. It is a best practice to keep your site as 'fluid' as possible. That means using measurements that adjust to screen size and are not absolute.

### Absolute Measurements
**Example: Pixels**

Pixels will not adjust based on screen size. If you were to set an element's width to 500px, it may look perfect on your laptop computer but may be too big on a mobile and too small on a 50" monitor.

### Relative Measurements

**Example: Percentages**

When using a percentage, that element will always take up that percent of the screen. For example, if I set an element to be 50% width, it would *always* take up 50% of a screen regardless of it's size.

**Note** 100% *is* the width of the screen you are using. If any elements inline with each other have widths that add up to be more that 100% , elements may move below the other elements. Example: If had 3 elements I wanted to be inline with each other, but each had a width of 40%, one element would end up below.

**em or rem**
Ems and Rems are used for font-sizing

Both em and rem are flexible, scalable units which are translated by the browser into pixel values, depending on the font size settings in your design. If you use a value of 1em or 1rem, it could translate in the browser as anything from 16px to 160px or any other value.

Em is relative to the font-size of its direct or nearest parent, rem is only relative to the html (root) font-size.

[This article](http://webdesign.tutsplus.com/tutorials/comprehensive-guide-when-to-use-em-vs-rem--cms-23984) is a comprehensive read on the differences between em and rem

## Use DevTools to View an Element's Box-Model
The best way to be aware of your element's box model is to constantly check it in DevTools!

## Vocab ✅
- margin
- border
- padding
- relative measurements
- absolute measurements

## 🔑 Key Takeaway
Understanding an elements box-model is essential to positioning elements in more complex layouts.

### Additional Resources
- [DevTools Documentation](https://developers.google.com/web/tools/chrome-devtools/iterate/inspect-styles/?utm_source=dcc&utm_medium=redirect&utm_campaign=2016q3)
- [Opening the Box Model Lesson](http://learn.shayhowe.com/html-css/opening-the-box-model/)
