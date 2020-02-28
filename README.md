# CSS to the Rescue

![Project](https://github.com/MarjoleinAardewijn/css-to-the-rescue-1920/blob/master/images/CSS-to-the-Rescue-Project.png "CSS to the Rescue project").

## Table of Content
- [Description](#Description)
- [Demo](#Demo)
- [Used contexts](#Used-contexts)
- [Restrictions](#Restrictions)
- [Learning process](#Learning-process)
- [Sources](#Sources)
- [Credits](#Credits)
- [Licence](#Licence)

## Description

In this three week course I create an innovative, experimental, yet pleasurable user experience for a responsive restaurant menu by using CSS and SVG. 

I had to realize this by using the Selector First Methodology.

> "You _have_ to work with the so called *Selector First* CSS Methodology. This means that you _have to_ use a wide variety of   CSS selectors. ID’s are only allowed to trigger the `:target` selector. If you really need them, you are allowed to use a     few classes. In order to differentiate between."

## Demo

You can see the final project [here](https://marjoleinaardewijn.github.io/css-to-the-rescue-1920/).

## Used contexts

The contexts that I have used for this assigment are:

- [x] prefers-reduced-motion.
- [x] animations.
- [x] input type (pointer).
- [x] hsl / hsla.
- [x] clip-path / background-clip.
- [x] skew.
- [x] border-radius.
- [x] filter -> drop-shadow().
- [x] cubic-bezier.
- [x] overflow (style).
- [x] mix-blend-mode.
- [x] background-image + background-position.

## Restrictions

For this assignment I have chosen the following two restrictions:

- [x] When SVG meets CSS: Shapes / Masks / SVG
- [x] Two colours
- [x] Responsive without media queries

## Learning process

### prefers-reduced-motion

I was looking for some contexts that I didn't know and then I came across prefers-reduction-motion. This seemed like an interesting context to learn about and experiment with. The great thing about this context is that you can adjust all animations and other styling based on a media query.

What I did is indicate in the media query that when prefers-reduction-motion has the value `reduce` all the animations must be turned off and the cursors must be set back to their original values.

```
@media (prefers-reduced-motion: reduce) {
  /*code to stop all the animations and set all the cursors to their original values.*/
}
```

### cursor

I used different images for the cursor that I show in specific places. This was a bit tricky in the beginning, since at first the images didn't show. It turned out that the image should apparently not be larger than 32x32 pixels. After I adjusted that, it worked perfectly.

I had never worked with this before and I did not know that you could actually customize the cursor.

I also tried to put SVGs in the cursor, but unfortunately this was not possible as only png and jpg are allowed.

### skew

I wasn't familiar with the skew either. I first applied this to divs and used another skew between even and odd elements by using `:nth-child (even)` and `:nth-child (odd)`.

What I also found funny was that the skew really put the whole element in that certain angle, so also the text and everything in it goes with it.

### border-radius

I wanted to use a blob in my design so I first tried to do this with an animation and SVGs, but I was unable to do this without making a lot of keyframes. Then I started looking further and found that you could give the border-radius more values. I played with that at the time and I finally came up with the blob I have now.

### animation

With this I also had never really worked, so I have studied this more. For example, I created a morphing square and a blob, animations on SVGs and on the skew.

For the morphing square I used a clip-path in an animation. And for the blob I have adjusted the border radius.

I also used the `cubic-bezier` property in an animation. With this you can indicate yourself how the animation should go. You can use this instead of `ease`, `ease-in`, `ease-out`, `alternate`, etc.

```
animation-timing-function: cubic-bezier(x1,y1,x2,y2);
```

### mix-blend-mode

mix-blend-mode was also unknown territory for me. I applied this to various elements on the site.

### overflow

I was already familiar with overflow itself, but I wanted to make the scrollbar invisible of which I did not know if this was possible. After some searching on the internet I found out that this is possible in all browsers, except Firefox, by calling the pseudo-element `::-webkit-scrollbar` and putting it on`display: none;`.

### Responsive without media queries

To get the site responsive without media queries, I used flex and used a `calc()` for the font to adjust the `font-size` depending on the size of the screen. The latter was new to me and I later applied it to adjust the `blockquote` on the page.

## Sources

- [CSS Tricks](https://css-tricks.com/).
- [MDN](https://developer.mozilla.org/).
- [YouTube](http://www.youtube.com/).
- [W3Schools](https://www.w3schools.com/).
- [CodePen](https://codepen.io/).
- [Dev](https://dev.to/).
- [JSFiddle](http://jsfiddle.net/).
- [Images / SVGs](https://www.freepik.com/).

## Credits

- [Custom Cursor](https://www.youtube.com/watch?v=nMgB-GQzEdQ).
- [prefers-reduce-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion).
- [background-position x%y%](https://www.w3schools.com/cssref/pr_background-position.asp).
- [clip-path](https://www.youtube.com/watch?v=YjnuuqVdadI).
- [Overflow (style)](https://www.w3schools.com/howto/tryit.asp?filename=tryhow_css_hide_scrollbar_keep_func).
- [Morphing Shape](https://codepen.io/hamza31/pen/rNaOrab).
- [Blob](https://codepen.io/Ninaiskel/pen/MWWgMwL).
- [border-radius](https://dev.to/equinusocio/making-a-css-blob-37nb).
- [Div as Background](http://jsfiddle.net/1fevoyze/).
- [Checkbox hack](https://css-tricks.com/the-checkbox-hack/).
- [background-clip](https://www.youtube.com/watch?v=9Kr3T4Ndl-o).
- [Responsive Font Size](https://css-tricks.com/books/fundamental-css-tactics/scale-typography-screen-size/).
- [[attribute]](https://css-tricks.com/almanac/selectors/a/attribute/).
- [mix-blend-mode](https://css-tricks.com/almanac/properties/m/mix-blend-mode/).

## Licence

[MIT License](https://github.com/MarjoleinAardewijn/css-to-the-rescue-1920/blob/master/LICENSE.txt)

Copyright (c) 2020 Marjolein Aardewijn
