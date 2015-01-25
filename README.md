## All online color converters suck

They are covered in ads and inflexible in their input and output.  

Some of them even moronically post data off to a server and do a page refresh to show you the result.

Like it's 1997 or something.

## This one doesn't.

Here, it's a single input box where you type commands like


    rgb2hsl #432123

    hex2rgb #ab3s34

    hsv2hex 34 53 12

And bam, it's done.

Here's what it looks like:<br>
<img src=http://i.imgur.com/PwYJ2ys.png>
<br>

<h3><a href="http://9ol.es/quick-color.html">Live version</a></h3>

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

 * a hex color in the form of #aabbcc
 * 3 numbers between 0 and 256
 * 3 floating point numbers between 0 and 1
 * a percentage expressed like "90%"
 * an equation with no spaces, such as "0.5/2".

If the LHS is col, such as "col2rgb", then the input can be an html color name ... the valid names are in the index.html file. Scroll down and a huge table should be obvious.


## Examples

### Syntax

We're going to take an input expressed in a mixed form of percentages, floating point numbers, and a value that is [0..256].

Our test case will be the mid-point of each of these expressions.

    > rgb2hex 50% 0.5 128 

The answer we are given here is:

    #808080

### Complex

Let's say I have an html color, goldenrod, and I want to find a darker version of it.

    > col2hsl goldenrod
    42.903 0.744 0.488

Now I can click on the triplet number above and it will become part of the input.  The type of the input is remembered, as you see, the input box now becomes:

    > hsl2xxx 42.903 0.744 0.488

With the xxx selected.  Let's put in rgb 

    > hsl2rgb 42.903 0.744 0.488

And now we want the luminance (last number) multiplied by 0.75

    > hsl2rgb 42.903 0.744 0.488*0.75 
    163 124 24

As you can see from the little boxes, it looks like we are successful.  But how do we use that number.

Hover over the little box and you'll see the hex code to use for html.

Click on it and you'll see the color appended to the input box and selected.  

Now you can do a Ctrl+x (or equivalent cut) on your platform and get the color into the clipboard.
