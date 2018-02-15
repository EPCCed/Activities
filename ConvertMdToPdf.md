# Converting markdown to pdf

Thee are some notes on how to conver the markdown sources to pdf in this
repository based on this 
[gist](https://gist.github.com/justincbagley/ec0a6334cc86e854715e459349ab1446).
I think `grip` seems to give the best output. Have only used these on a mac though. Please feel free to update for other platforms.

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
