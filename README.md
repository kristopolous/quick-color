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

## Syntax

We break it down as follows:


    (LHS) 2 (RHS) (Arguments)

Where LHS and RHS is one of

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

For instance:

    rgb2hex 50% 0.5 128 

would yield:

    #808080

And that's it.

## Examples

Let's say I have an html color, goldenrod, and I want to find a darker version of it.

    > col2hsl goldenrod
    42.903 0.744 0.488

Now I can click on the triplet number above and it will become part of the input.  The type of the input is remembered, as you see, the input box now becomes:

    > hsl2xxx 42.903 0.744 0.488

With the xxx selected.  Let's put in rgb and then take the luminance (last number) and multiply it by 0.75

    > hsl2rgb 42.903 0.744 0.488*0.75 
    163 124 24

As you can see from the little boxes, it looks like we are successful.

Hover over the little box and you'll see the hex code to use for html.

Click on it and you'll see the color appended to the input box and selected.  Now you can do a Ctrl+x (or equivalent cut) on your platform and get the color into the clipboard.
