# \_marvli.scss

The \_marvli.scss is a simple but yet timesaving scss partial I use to kickstart my "classical" web-projects. I will release it step by step while I clean it up.

## How to "install"?
Installing the partial is easy.
At first, you can download the `_marvli.scss` file and put them where your project structure requires it to be.
When you downloaded the `_marvli.scss` you just need to import the file. If you have never done that before, here is how you do it:

**Importing if your main scss and the partials are saved in the same directory (small projects)**
```scss
@import 'marvli';
```

**If your partials are in a subfolder (normal projects)**
```scss
@import 'vendor/marvli'
```

Or apply your own structure. [Here is a basic guide](http://thesassway.com/beginner/how-to-structure-a-sass-project) on how to structure _scss_ projects.

## How to use \_marvli.scss?
### mediaquery
This scss is based on the "mobile first" design way and therefore everything you write is firstly applied to the smartphone and everything above it.

If you want to change specific things, like font-size or anything, you can apply the bootstrap/pure syntax like following:
```scss
html {font-size:10px;}
body {
	font-size: 1.6rem;
    @include size(md) { font-size: 1.4rem; }
    @include size(xl) { font-size: 1.8rem; }

}
```

body therefore sets a font-size of 16px while `@include size(md)` changes the font-size for **anything** with a larger width than 768px to 14px. Then `@include size(xl)` changes the size for everything wider than 1280px to 18px. As **md** sets the size to 14px you don't neeed to set it to 14px for **lg** either, as the 14px is only changed after 1280px width by the **xl**.

The waterfall is working like this:

any size > anything wider than 768px ***size(md)*** > anything wider than 1024px ***size(lg)*** > anything wider than 1280px ***size(xl)***

### branding
*coming soon*
