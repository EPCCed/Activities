# Converting markdown to pdf

These are some notes on how to conver the markdown sources to pdf in this
repository based on this 
[gist](https://gist.github.com/justincbagley/ec0a6334cc86e854715e459349ab1446).
I think `grip` seems to give the best output. These have only been used these on a mac. Please feel free to update for other platforms.

## pandoc

```
pandoc -V geometry:margin=2cm Readme.md -s -o sort3.pdf
```

This produces rather plain looking output.

## grip

Need to install this on to your system if it's not already there.

```
pip install grip
```

To render a markdown page:

```
grip Readme.md
```

This renders the page in a browser window under a local server:
http://localhost:6419/ which can then be printed out a pdf file.
This produces the most similar output to the rendered output.

The following is better as it puts the output directly into an html
page:


```
grip Readme.md --export output.html

```

This can then be edited and exported as a pdf from a browser.

## Markdown-pdf

Install the app

```
npm install -g markdown-pdf
```

which can be used to produce a pdf from markdown:

```
markdown-pdf -f "A4" -o outputfilename.pdf Readme.md
```

However it produces a fairly plain output.

## Other alternatives

* For mac users shift-Command-R on Safari will open the markdown in Reader. One can print from there.

<!-- Licensing and copyright stuff below -->
<br>
<a href="http://www.epcc.ed.ac.uk">
<img alt="EPCC logo" src="https://www.epcc.ed.ac.uk/sites/all/themes/epcc/images/epcc-logo.png" height="31"/>
</a>
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
<img alt="Creative Commons License" style="border-width:0" 
     src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" />
</a><br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.<br/>
&copy; Copyright EPCC, The University of Edinburgh 2017.
