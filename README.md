## All online color converters suck

They are covered in ads and inflexible in their input and output.  

Some of them even moronically post data off to a server and do a page refresh to show you the result.

We can do better.

## A clean open-source hacker-friendly color converter.

<img src=http://i.imgur.com/PwYJ2ys.png>
<br>

<h3> Click <a href="http://9ol.es/quick-color.html">Here for a Live version</a>!</h3>

## Syntax

We break it down as follows:


    (LHS) 2 (RHS) (Arguments)

Where LHS and RHS is one of

    col* (see note)
    rgb
    hex
    hsv
    hsl

and arguments are either one of

 * a hex color in the form of #aabbcc or the short syntax of #abc
 * a numbers between 0 and 255 (or 0 to 360 when appropriate in hsl/hsv space).
 * a floating point numbers between 0 and 1.
 * a percentage expressed like "90%"
 * an equation with no spaces, such as "0.5/2".

> Note: If the LHS is "col", such as "col2rgb", then the input can be an html color name ... the valid names are in the index.html file. Scroll down and a huge table should be obvious.

## Examples

### Syntax

We're going to take an input expressed in a mixed form of percentages, floating point numbers, and a value that is [0..255].

Our test case will be the mid-point of each of these expressions.

    > rgb2hex 50% 0.5 128 

The answer we are given here is:

    #808080

#### Helpers

There's two 'replacement' charaters that immediately get replaced with a contextual answer from the last query.

**?** - If your first character is a `?` then you get the RHS value of the last query ... that is to say the format of the output.  For instance, if the last command was `rgb2hex 50% 0.5 128` and you put in a `?` then the `?` will get replaced with `hex2`.

**!** - If you put an exclamation point after your function name, such as `rgb2hsl !` then the `!` gets replaced with the output of the last command.

These shortcuts help quickly chain a process such as the one below.

### Complex

Let's say I have an html color, goldenrod, and I want to find a darker version of it.

    > col2hsl goldenrod
    42.903 0.744 0.488

Now I can click on the triplet number above and it will become part of the input.  The type of the input is remembered, as you see, the input box now becomes:

    > hsl2xxx 42.903 0.744 0.488

With the xxx selected.
<br>
<img src=http://i.imgur.com/sh5Gzol.png>

Let's put in the text "rgb"

    > hsl2rgb 42.903 0.744 0.488

And now we want the luminance (last number) multiplied by 0.75

    > hsl2rgb 42.903 0.744 0.488*0.75 
    163 124 24

As you can see from the little boxes, it looks like we are successful.  But how do we use that number.

Hover over the little box and you'll see the hex code to use for html.

<img src=http://i.imgur.com/xoOeLzF.png><br>

Click on it and you'll see the color appended to the input box and selected.  

<img src=http://i.imgur.com/jOnkOgX.png><br>

Now you can do a Ctrl+X (or equivalent cut) on your platform and get the color into the clipboard.




