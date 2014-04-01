# What do we want from our writing tools?
+ human readable
	- what does "¬Kÿò∫CËÂ€ÒV•êæ~§ˇk≤¢Á]ÎB∆∏›PF»6}"h8áºÔ" mean? 
+ sustainable
	- no format is forever. except plaintext.
+ separate form from content
	- it's inefficient to spend time or effort formatting
+ support the academic apparatus
	- i need tables, bibliographies, footnotes, easily
+ platform independence
	- needs to work on my palm pilot or my pebble watch
	
## An example of a markdown doc
	
```
---
title: Baby's First Pandoc-Markdown document
author: Amrita Maz
date: March 4th, 2014
---

# Section 1
## Subsection 1.1
Some brilliatn thoughts here in a paragraph

## Subsection 1.2
Some other not so smart things here.[^1]

## Subsection 1.3
Whatever. How about a list?
- Thing 1
- Thing 2

# Section 2
Some more text here. Emphasis is *this* or **this**.[^1]


[^1]: All these lines are verbatim from [Dennis Y. Tenen](www.dennistenen.com)
```

## How to convert from markdown to pdf
+ prereqs: have pandoc and latex installed
+ step one: write your file! preferably in vim.
+ step two: execute `pandoc -o first_pandoc.pdf first_pandoc.md`
+ step three: profit! execute `open first_pandoc.md` if you're on a mac, where things are pleasant.