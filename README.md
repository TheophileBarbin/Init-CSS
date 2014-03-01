init.css
========

A single CSS file that includes Eric Meyer's *Reset CSS* and a bunch of useful features for any layout architect aiming at responsiveness.

***

## What does init.css do?

`init.css` is based on Eric Meyer's famous *Reset CSS*. If you are familiar with CSS, you probably already use it in your Web projects. Almost nothing is changed in Meyer's code, so don't worry about this part.

However, `init.css` adds a few features for responsiveness:

### Box-sizing

The `box-sizing` property is set to `border-box` for every HTML element. This renders your layout easier to scale and to make it responsive. No miracles though, you will still have to code more CSS for a truly responsive Website. More information about `box-sizing` [here](http://css-tricks.com/box-sizing/).

**Code:**

```css
* {
	-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;
	-ms-box-sizing: border-box;
	-o-box-sizing: border-box;
	box-sizing: border-box;
}
```

### Viewport

The viewport's width matches the viewers's device's width.

More importantly, `init.css` supports this property for IE10+ in Modern UI mode. Basically, this means your Website will also be (finally!) responsive in snapped mode in the Modern Internet Explorer. More information [here](http://timkadlec.com/2012/10/ie10-snap-mode-and-responsive-design/).

**Code:**
```css
@viewport { width: device-width; }

@-ms-viewport { width: device-width; } /* For snapped mode in IE10+ Modern UI. */
```

### Sized HTML and Body elements

HTML's and Body's width and height are set to 100%. You won't have to think about size inheritance anymore.

**Code:**

```css
html,
body {
	width: 100%;
	height: 100%;
}
```

***

## Using init.css

Just import `init.css` in your CSS repository in any of your new projects. Then, link your HTML files to it thanks to this line:

```html
<link rel="stylesheet" type="text/css" href="<!-- Path to your CSS repository -->/init.css">
```

I don't recommend you import it in one of your existing projects: it might turn your styles upside down. Only use it to initialize the styles for a new project.
