# cb-tuto-bio
How to build your own bio on Chaturbate

# Tools

The following are recommendations of tools to write your bio in. You could write it directly in the box on your profile, but that's not ideal. If you've tried it, you understand what I mean.

So instead of modifying directly on CB, what I recommend is having a file on your computer that you can make changes in, using a better editing tool, and then you can just replace the entire bio with a good old copy-paste.

_NB: Avoid using a writing tool like Notepad, MSWord, Google Docs and such, these will wreak havoc with your code. They'll follow writing styles made for humans, not computers._

Either one of these tools is decent for our purpose here, and both are free of charge.

Remember that you don't need either of these tools, but they'll make your work much easier.

## Notepad++

This is the easiest to use, very straightforward. This editor won't interfere with what you write, but it also won't offer help in improving your code.

[Download and install](https://notepad-plus-plus.org/downloads/)

## Visual Studio Code

If you don't mind the tool nudging you every now and then towards better code, this is the best editor for you. Just know that it can be a little annoying at times. Has a wide variety of plugins.

[Download and install](https://code.visualstudio.com/)

Two settings that I tend to change when I install vscode are:
* Trim Final Newlines: disabled
* Trim Trailing Whitespace: enable


# First steps

## Make a backup of your current bio

The profile editor on CB can be found by clicking your nickname in the upper right corner, then "My Profile" in the new drop-down menu, then "Edit your bio" at the top of your bio.

Click inside the box called "About Me", then hit Ctrl+A to make sure the entire box contents are highlighted, then right-click and copy.

Open your code editor of choice, then click the `File > New` menu to open a new tab, and paste there the contents of your current bio. Then select the `File > Save as` menu, choose a file name with today's date and time as well as the word "bio", change "save as type" to `Hyper Text Markup Language (*.html)` and confirm.

Same process to backup your current wishlist:
* in your CB profile editor, find the box called Wish Lists, click inside, select all the contents with Ctrl+A, right click, copy
* in your code editor, open a new file, paste the contents, write today's date and and time in the file name as well as the word "wishlists", save as type HTML, confirm save.

I would suggest repeating this process every day you make a change, so that you can easily restore a previous backup at any time.

## How to make changes without people seeing them

You can either set a password on your profile (but don't forget to remove the password when you are ready), or you can create a fake account on the [test site provided by CB](https://www.testbed.cb.dev). The latter choice would be my recommendation. There is currently no way to preview your changes, so...

## Making your first edit

To make it easier, you will need two separate browser windows. Open one with your public profile that everyone can see, and the other is where you write your bio in.

The CB public profile can be found by searching for your nickname in the search on CB. This is the only one where changes matter.

The CB profile editor can be found by clicking your nickname in the upper right corner, then "My Profile" in the new drop-down menu, then "Edit your bio" at the top of your bio.

In the box called "About Me", copy-paste the following code:
```html
<h1>about me test1</h1>
```

This is a simple HTML tag for a level-1 title.

Likewise, in the box called "Wish Lists", copy-paste the following code:
```html
<h1>wish lists test1</h1>
```

Then click the button that says "Update Bio", go back to your public profile and hit refresh. You will now see "about me test1" and "wish lists test1" written in big black letters.

NB: CB may show the changes directly in the profile editor window but be careful about two things:
* this is not a preview (changes are always final);
* what it looks like here may be slightly different on the public profile;
* => Be sure to refresh the public profile often.

## How to make a pretty bio

Your bio is written in HTML, so there's no way around knowing at least a little HTML.

Of course, you may prefer to use mostly images. Maybe you know how to make them yourself, or perhaps you know someone who does. Either way, these images only work if you know enough HTML to include them.

The last part you will have to learn something about is CSS. That's how we apply colors, shadows, sizes, gradients _etc._ to the document. It is also some kind of coding skill, different from HTML.

Usually on the web there is another component called JavaScript (or JS for short) but CB doesn't allow that in their bios, for security reasons.


## The basics: HTML documents

HTML is a hierarchy of what we call _tags_, also called HTML _elements_. Each tag starts with a `<` symbol and ends with a `>` symbol, for example `<img>` (image) is a tag you are likely to use a lot.

Technically, your bio will be inserted into the global HTML document made by CB, the entire bio under one tag.

HTML was made to describe documents, which means that there is a tag to describe a lot of elements of human writing. There is a tag for a paragraph of text, another tag for an image, yet another for a bullet list, _etc._

If you are curious, the entire list of HTML elements can be found at [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element). Just be aware that a lot of the elements described there, are not available for your bio on CB.

### The HTML elements allowed by CB

CB themselves explain in the very profile page which HTML elements they allow.

Bio box:
> a p i strong b u ul ol li h1 h2 h3 img font br span

Whishlit box:
> a p i strong b u ul ol li h1 h2 h3 img font br

Let's got over them:
* [`a`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) is a link (the technical name being an anchor)
* [`img`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) for an image
* [`p`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p) is a paragraph
* [`strong`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong) is used for strong emphasis on text, by default it is often "bold"
* [`ul`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul) is a grouping element for a list of items; `ul` should have only `li` elements directly inside
* [`ol`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) is a grouping element for an ordered (numbered) list of items; `ol` should have only `li` elements directly inside
* [`li`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li) is a bullet list point, they are always placed directly inside either `ul` or `ol`
* [`h1`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h1) is a level-1 title, by default it is big
* [`h2`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h2) is a level-2 title, by default it is smaller
* [`h3`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h3) is a level-3 title, by default is the smallest (but still bigger than regular text)
* [`br`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br) is a line break in a text paragraph
* [`span`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span) is a grouping element to apply some CSS on individual words for example

Be aware that a few of these are really old and have been deprecated, which means that web browsers can remove them at any point and your bio will look broken. These elements are `b`, `i`, `u` and `font`. There are CSS equivalents for each, so it's no big deal.
* [`b`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b) was the old way to make text appear with bold styling. Now deprecated. Replace with CSS `<span style="font-weight: bold">...</span>`
* [`i`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i) was the old way to make some words appear with italic styling. Now deprecated. Replace with CSS `<span style="font-style: italic">...</span>`
* [`u`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u) was the old way to underline some text. Now deprecated. Replace with CSS `<span style="text-decoration: underline">...</span>`
* [`font`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/font) to change the styling of text (size, color etc). Now deprecated. Replace with CSS on a `span` tag.


### How to combine HTML elements

HTML was meant as a hierarchy. There's the global document created by CB, and inside that there are a bunch of layers until we arrive at the layer with our bio.

Inside our bio and wishlist, we probably want things to make sense to the audience.

For example to have a link to our social media or whatever, we can make a simple link with text:
```html
<a href="...">this is the anchor text</a>
```

Or perhaps the link would make more sense with an image that people can identify easily:
```html
<a href="..."><img src="..."></a>
```

The same happens with `ul/li` and `ol/li`, which are the only elements that CB allows to structure our content.
```html
<ul>
    <li>something</li>
    <li>something else</li>
    <li>yet another thing</li>
</ul>
```

```html
<ul>
    <li style="list-style-type: none"><h1>title section 1</h1></li>
    <li style="list-style-type: none">
        <ul>
            <li>something 1</li>
            <li>something else 1</li>
            <li>yet another thing 1</li>
        </ul>
    </li>
    <li style="list-style-type: none"><h1>title section 2</h1></li>
    <li style="list-style-type: none">
        <ul>
            <li>something 2</li>
            <li>something else 2</li>
            <li>yet another thing 2</li>
        </ul>
    </li>
</ul>
```

The example above has the same effect as this next one, except when you try to apply a background on the entire bio:
```html
<h1>title section 1</h1>
<ul>
    <li>something 1</li>
    <li>something else 1</li>
    <li>yet another thing 1</li>
</ul>

<h1>title section 2</h1>
<ul>
    <li>something 2</li>
    <li>something else 2</li>
    <li>yet another thing 2</li>
</ul>
```


### How to write HTML attributes

HTML elements can often have "attributes" to inform their context, like the `style` we've been seeing here. The list of these attributes is given at the dedicated page in the element's documentation. For example if you want to make a link to another page (say your social profiles), you will use the [`<a>` anchor element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) whose most obvious attribute is `href` (to describe where the link points to).

```html
<a href="https://chaturbate.com/apps/app_details/flexible-tip-menu/">My "flexible tip menu" bot on CB</a>
```

The way to write these attributes is to write their name immediately followed by a `=` symbol and two double quotes `"`. Then you write the attribute's value inbetween these double quotes. Be careful not to leave extra spaces (especially for `<a href` and `<img src`, not so much for `style`), because it would likely break your links. There can be extra spaces around the attribute as a whole (like in `<a href="..." >`) but not elsewhere (for example `<a href = "...">` is wrong).

Some HTML attributes are present in almost all of the HTML elements. The one you are most likely interested in is called [`style`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style), which allows you to apply CSS rules (see further below) separated by a `;`.

For example, place the following in your bio, save and reload the public profile window:
```html
<h1 style="background-color: rgba(255, 42, 81, 0.19); font-size: 2.5em; font-weight: 900; text-align: center; line-height: 49px;">My awesome bio v1</h1>
```

Okay that particular color may not necessarily be pretty, this is just an example.

Explanation of this `style` value:
* `background-color` defines how to paint the background color, here with a very specific color code (deep red with some green and a little more blue)
* `font-size` changes the font size to 2.5 times what it should be
* `font-weight` how thick the letters are
* `text-align` to center the text horizontally on the line
* `line-height` to make sure the background covers the entirety of the letters (vertically)


## The basics: CSS rules

As we've seen above, CSS can apply colors and other styling choices to elements in our page.

The example I gave previously was to style a link with a pink background:
```css
background-color: rgba(255, 42, 81, 0.19)
```

In this case, we're setting the `background-color` CSS property with `rgba` values, which is short for red, green, blue and alpha. That's what the four numbers represent, they measure how much of each color we want to mix into the background. Each of red, green and blue is a non-decimal number between 0 and 255, while alpha (transparency) is a decimal number between 0 and 1.

When choosing colors, perhaps a good idea is to use a tool [like this one](https://mdn.github.io/css-examples/tools/color-picker/).


## Examples of HTML tags and CSS rules

_Limitations:_
* Unfortunately, unless the code is on a single line, CB will add `br` elements that break the design, so I will always provide both versions.
* Be aware that nothing from your bio and wishlist can break out of the Bio tab. CB made sure that anything trying to break out, would be hidden. For example, you can't have the social media links floating next to your streaming window. Some people have tried re-styling the entire page, and sometimes people find clever tricks that can change the orange color or their logo, but it is also very likely to get you in trouble with CB. Recommended to stay within the defined constraints. The only exception is `position: fixed` but that makes the element move with the scroll, and is not always ideal.
* CSS can apply some rudimentary visual filters on any HTML element (for example shadows and geometric skewing) but it's unlikely to really WOW you as a model. Any visually appealing filter you may want, like the ones you are used to with social media, are out of reach here. For those, you're better off hiring someone to make an image file that you can include in your bio.


### How to make it work on CB specifically

The point is, once you figure out what you aim to do, you can look up the ways that elements & attributes should be combined for this goal. For example if you want to display your tip menu, you'll probably want to use a plain paragraph (`<p>`) or perhaps a bullet list (one `<ul>` element with a bunch of `<li>` inside).

Normally, if you want to group elements together so that you can apply styling to them as a whole, you can place them in a `<div>` element like this:
```html
<div style="background-color: rgba(42, 255, 81, 0.19)">
    <h1>My bio part1</h1>
    <p>a</p>
    <p>b</p>
</div>
<div style="background-color: rgba(255, 42, 81, 0.19)">
    <h1>My bio part2</h1>
    <p>c</p>
    <p>d</p>
</div>
```

However, CB is filtering both HTML and CSS, probably as a security measure to avoid accounts hijacking their users. There is no `div` element available on CB but no matter, we can use `ul` & `li` to the same effect. It's a little more complicated to write, but it works...

Readable version:
```html
<ul style="padding: 0; margin: 0; width: 100%">
    <li style="list-style-type: none;">top (outer)</li>
    <li style="list-style-type: none">
        <ul style="padding: 0; margin: 0">
            <li style="list-style-type: none">top (inner)</li>
            <li style="list-style-type: none; text-align: center">middle (inner)</li>
            <li style="list-style-type: none">bottom (inner)</li>
        </ul>
    </li>
    <li style="list-style-type: none">bottom (outer)</li>
</ul>
```

Copy-pasteable version:
```html
<ul style="padding: 0; margin: 0; width: 100%"><li style="list-style-type: none">top (outer)</li><li style="list-style-type: none"><ul style="padding: 0; margin: 0"><li style="list-style-type: none">top (inner)</li><li style="list-style-type: none; text-align: center">middle (inner)</li><li style="list-style-type: none">bottom (inner)</li></ul></li><li style="list-style-type: none">bottom (outer)</li></ul>
```

Or the same thing with a gradient background:

Readable version:
```html
<ul style="background: linear-gradient(blue, 10%, pink); padding: 0; margin: 0; width: 100%">
    <li style="list-style-type: none; mix-blend-mode: difference; color: grey; padding-top: 10px; padding-bottom: 5px">top (outer)</li>
    <li style="list-style-type: none; mix-blend-mode: difference; color: grey; padding-top: 5px; padding-bottom: 5px">
        <ul style="padding: 0; margin: 0; mix-blend-mode: difference; color: grey">
            <li style="list-style-type: none">top (inner)</li>
            <li style="list-style-type: none; text-align: center">middle (inner)</li>
            <li style="list-style-type: none">bottom (inner)</li>
        </ul>
    </li>
    <li style="list-style-type: none; mix-blend-mode: difference; color: grey; padding-top: 5px; padding-bottom: 10px">bottom (outer)</li>
</ul>
```

Copy-pasteable version:
```html
<ul style="background: linear-gradient(blue, 10%, pink); padding: 0; margin: 0; width: 100%"><li style="list-style-type: none; mix-blend-mode: difference; color: grey; padding-top: 10px; padding-bottom: 5px">top (outer)</li><li style="list-style-type: none; mix-blend-mode: difference; color: grey; padding-top: 5px; padding-bottom: 5px"><ul style="padding: 0; margin: 0; mix-blend-mode: difference; color: grey"><li style="list-style-type: none">top (inner)</li><li style="list-style-type: none; text-align: center">middle (inner)</li><li style="list-style-type: none">bottom (inner)</li></ul></li><li style="list-style-type: none; mix-blend-mode: difference; color: grey; padding-top: 5px; padding-bottom: 10px">bottom (outer)</li></ul>
```

### Social media links, pinned in a row at the top, centered and spaced by 10px

Readable version, remember to change the `a href` and `img src` to your liking:
```html
<ul style="position: absolute; z-index: 99; top: 0px; left: 0px; padding: 0; margin: 0; width: 100%; text-align: center;">
    <li style="list-style-type: none; display: inline; margin-right: 10px;">
        <a href="https://www.testbed.cb.dev/william81fr_2/"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a>
    </li>
    <li style="list-style-type: none; display: inline; margin-right: 10px;">
        <a href="https://www.testbed.cb.dev/p/william81fr_2/?tab=bio"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a>
    </li>
</ul>
```

Explanations
* `position: absolute` moves the entire list "out of flow" from the document, so that we can specify the exact position on the screen (within the Bio tab)
* changing to `position: fixed` would make the list stick to the browser scroll (breaking out of the Bio tab) but it isn't allowed
* `z-index: 99` ensure that thos block stays over the other layers on the page
* `top: 0px; left: 0px;` the position where we want the box to stay, in this case the top left
* `padding: 0; margin: 0;` cancelling default browser padding & margins for this element
* `width: 100%` making sure the list can span the entire width of the page
* `text-align: center` aligning our elements to the center of the page (horizontally)
* `list-style-type: none` removes the big dot that goes in front of each `<li>` by default
* `display: inline` moves the images next to one another, rather than each on a new line
* `margin-right: 10px` spaces the bimages by 10 pixels

Copy-pasteable version:
```html
<ul style="position: absolute; z-index: 99; top: 0px; left: 0px; padding: 0; margin: 0; width: 100%; text-align: center;"><li style="list-style-type: none; display: inline; margin-right: 10px;"><a href="https://www.testbed.cb.dev/william81fr_2/"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a></li><li style="list-style-type: none; display: inline; margin-right: 10px;"><a href="https://www.testbed.cb.dev/p/william81fr_2/?tab=bio"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a></li></ul>
```

### Social media links, pinned in a column in the top left

Readable version:
```html
<ul style="position: absolute; z-index: 99; top: 0px; left: 0px; padding: 0; margin: 0;">
    <li style="list-style-type: none">
        <a href="https://www.testbed.cb.dev/william81fr_2/"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a>
    </li>
    <li style="list-style-type: none">
        <a href="https://www.testbed.cb.dev/p/william81fr_2/?tab=bio"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a>
    </li>
</ul>
```

Explanations:
* no need for `width: 100%` or `text-align: center` on the list
* no need for `display: inline` or `margin-right: 10px` on the cells

Copy-pasteable version:
```html
<ul style="position: absolute; z-index: 99; top: 0px; left: 0px; bottom:100px; padding: 0; margin: 0;"><li style="list-style-type: none"><a href="https://www.testbed.cb.dev/william81fr_2/"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a></li><li style="list-style-type: none; display"><a href="https://www.testbed.cb.dev/p/william81fr_2/?tab=bio"><img src="https://www.testbed.cb.dev/static/images/socials/snapchat.svg" style="height:40px"></a></li></ul>
```


### Some quick CSS tricks

Text with color that stays readable over any background, use [`mix-blend-mode`](https://developer.mozilla.org/en-US/docs/Web/CSS/mix-blend-mode) in the `style` tag:
```css
mix-blend-mode: difference;
color: white;
```

Text with shadows, use [`text-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow) in the `style` tag:
```css
text-shadow: 5px 5px #558ABB;
```
```css
text-shadow: #FC0 1px 0 10px;
```

Element with a border around it, use [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) in the `style` tag:
```css
border: solid;
```
```css
border: thick double #32a1ce;
```

Perhaps you'll want to look into some other basic effects like [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) and [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform).


### A background image that stays fixed regardless of the scroll

Readable version:
```html
<ul style="padding: 0; margin: 0; background-image: url(https://www.testbed.cb.dev/static/images/socials/snapchat.svg); background-repeat: no-repeat; background-size: cover; background-attachment: fixed; width: 100%">
    <li style="list-style-type: none; mix-blend-mode: difference; color: white">azerty1</li>
    <li style="list-style-type: none; mix-blend-mode: difference; color: white; text-align: center">azerty2</li>
    <li style="list-style-type: none; mix-blend-mode: difference; color: white">azerty3</li>
</ul>
```

Copy-pasteable version:
```html
<ul style="padding: 0; margin: 0; background-image: url(https://www.testbed.cb.dev/static/images/socials/snapchat.svg); background-repeat: no-repeat; background-size: cover; background-attachment: fixed; width: 100%"><li style="list-style-type: none; mix-blend-mode: difference; color: white">azerty1</li><li style="list-style-type: none; mix-blend-mode: difference; color: white; text-align: center">azerty2</li><li style="list-style-type: none; mix-blend-mode: difference; color: white">azerty3</li></ul>
```
