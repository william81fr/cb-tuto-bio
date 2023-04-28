# cb-tuto-bio
How to build your own bio on CB

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

Open your code editor of choice, then click the File > New menu to open a new tab, and paste here the contents of your current bio. Then select the File > Save as menu, choose a file name with today's date and time, change "save as type" to "Hyper Text Markup Language (*.html)" and confirm.

Same process to backup your current wishlist:
* in your CB profile editor, find the box called Wish Lists, click inside, select all the contents with Ctrl+A, right click, copy
* in your code editor, open a new file, paste the contents, save as HTML with today's date and and time in the file name, save as type HTML, confirm save.

## How to make changes without people seeing them

You can either set a password on your profile (but don't forget to remove the password when you are ready), or you can create a fake account on the [test site provided by CB](https://www.testbed.cb.dev). The latter choice would be my recommendation. There is currently no way to preview your changes, so...

## Making your first edit

To make it easier, you will need two separate browser windows. Open one with your public profile that everyone can see, and the other is where you write your bio in.

The CB public profile can be found by searching for your nickname in the search on CB.

The CB profile editor can be found by clicking your nickname in the upper right corner, then "My Profile" in the new drop-down menu, then "Edit your bio" at the top of your bio.

In the box called "About Me", copy-paste the following code:
```html
<h1>about me test1</h1>
```

Likewise, in the box called "Wish Lists", copy-paste the following code:
```html
<h1>wish lists test1</h1>
```

Then click the button that says "Update Bio", go back to your public profile and hit refresh. You will now see "about me test1" and "wish lists test1" written in big black letters.

This is a simple HTML tag for a level-1 title.

## How to make a pretty bio

Your bio is written in HTML, so there's no way around knowing at least a little HTML.

Of course, you may prefer to use mostly images. Maybe you know how to make them yourself, or perhaps you know someone who does. Either way, these images only work if you know enough HTML to include them.

The last part you will have to learn something about is CSS. That's how we apply colors, shadows, sizes, gradients _etc._ to the document. It is also some kind of coding skill, different from HTML.

Usually on the web there is another component called JavaScript (or JS for short) but CB doesn't allow that in their bios, for security reasons.


## Basics: HTML documents

HTML is a hierarchy of what we call _tags_, also called HTML _elements_. Each tag starts with a `<` symbol and ends with a `>` symbol, for example `<img>` (image) is a tag you are likely to use a lot.

Your bio will be inserted into the global HTML docmuent made by CB, the entire bio under one tag.

HTML was made to describe documents, which means, there's a tag to describe a lot of elements of human writing. There is a tag for a paragraph of text, another tag for an image, yet another for a bullet list, _etc._

If you are curious, the entire list of HTML elements can be found at [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element). Just be aware that a lot of the elements described there, are not available for your bio on CB.

HTML elements can often have "attributes" to inform their context. The list of these attributes is given at the dedicated page in the element's documentation. For example if you want to make a link to another page (say your social profiles), you will use the `<a>` [anchor](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) tag whose most obvious attribute is `href` (to describe where the link goes to).

```html
<a href="https://chaturbate.com/apps/app_details/flexible-tip-menu/">
    My "flexible tip menu" bot on CB
</a>
```

Some HTML attributes are present in almost all of the HTML elements. The one you are most likely interested in is called `style`, which allows you to apply CSS rules (see further below).

For example, place the following in your bio, save and reload the public profile window:
```html
<a href="https://chaturbate.com/apps/app_details/flexible-tip-menu/" style="background-color: rgba(255, 42, 81, 0.19)">
    My "flexible tip menu" bot on CB
</a>
```

Okay that particular color may not necessarily be pretty, this is just an example.

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
    <p>a</p>
    <p>b</p>
</div>
```

However, CB is filtering both HTML and CSS, probably as a security measure to avoid accounts hijacking their users.


Some examples of HTML attributes for different situations are in the links at the bottom.


## Basics: CSS rules

As we've seen above, CSS can apply colors and other styling choices to elements in our page.

The example I gave previously was to style a link with a pink background:
```css
background-color: rgba(255, 42, 81, 0.19)
```

In this case, we're setting the `background-color` CSS property with `rgba` values, which is short for red, green, blue and alpha. That's what the four numbers represent, they represent how much of each color we want to mix into the background. Each of red, green and blue has a maximum of 255, while alpha (transparency) has a maximum of 1.


## More examples of HTML tags and CSS rules

You can see more examples of HTML tags to write a plain bio in [my bot's description](https://chaturbate.com/apps/app_details/flexible-tip-menu/).

The HTML code for that is available [on my github](https://raw.githubusercontent.com/william81fr/cb-flexible-tip-menu/main/description.html). If you were to copy-paste this entire file in your bio, you would get the same result.
