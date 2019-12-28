# Markdown

This is a guide that list the most commonly used (almost all) features of markdown used to build the DevNotes Repo.

I am primarily using GFM (GitHub Flavored Markdown), which is Github's custom version of Markdown that is built on top of the Sundown parser.

I love working on [VSCode](https://code.visualstudio.com/) and it is my editor of choice. I highly recommend using the '[Markdown All In One Plugin (Markdown AIO)](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)' which has made writing markdown much more simpler for me. It has many powerful features such as keyboard shortcuts, supports GFM, HTML previews and much more.

Note: **All keyboard shortcuts** mentioned on this repo page are for the Markdown AIO plugin. Also, I will not be elaborating a lot about features particular to the plugin until they are relevant to writing/editing markdown.

## Text Formatting

### Headings

Heading lines start with #, ##, ... ###### to represent H1 - H6 respectively.

# This is a h1

## This is a h2

### This is a h3

#### This is a h4

##### This is a h5

###### This is a h6

```markdown
# This is a h1
## This is a h2
### This is a h3
#### This is a h4
##### This is a h5
###### This is a h6
```

Alternatively, you can underline with ==== and ---- for h1 and h2 respectively.

This is a h1 level heading
====

This is a h2 level heading
----

```markdown
This is a h1 level heading
====

This is a h2 level heading
----
```

### Styling text

#### Bold

We can make text **bold** by enclosing them in `**`'s. We can also use **`Ctrl + B`** to make a selection bold if you are using '[Markdown All In One Plugin](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)' on VSCode (which I highly recommend).

```markdown
We can make text **bold** by enclosing them in **'s.
```

#### Italics

We can make text *italics* by enclosing them in `*`'s. We can also use **`Ctrl + I`** to make a selection bold if you are using '[Markdown All In One Plugin](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)' on VSCode (which I highly recommend).

```markdown
We can make text *italics* by enclosing them in *'s.
```

#### Strikethrough

~~Strikethrough~~ text is created by enclosing text in \~\~'s.

```markdown
~~Strikethrough~~ text is created by enclosing text in ~~'s.
```

#### Italics nested within bold text

We can emphasize text with italics **in a _bold_ statement**

```markdown
We can emphasize text with italics **in a _bold_ statement**
```

#### Bold + Italic text

Statements enclosed in \*\*\* will be both bold and italicizes.

We can make text ***both bold and italic*** with three `***`'s.

```markdown
We can make text ***both bold and italic*** with three `***`'s.
```

### Quoting

A statement or a part of a statement that you do not want to apply markdown to can be `quoted` by enclosing them within \`'s.

If you want to apply the quotation functionality to a block, you should enclose the block in \`\`\`'s.

```markdown
These block of lines
is quoted...
```

The code for the above snippet is:
\`\`\`
These block of lines
is quoted...
\`\`\`

### Links

To create a [link](#), we use the following syntax.

```markdown
[Link text](https://url.address/)
```

Note: Github automatically creates links for **valid** url's. You can create links to Github users/issues/pull-requests etc. by using this feature. Learn more about this feature [here](https://help.github.com/en/github/writing-on-github/autolinked-references-and-urls).

Markdown allows linking withing the folder structure using relative links.

*Github Flavoured Markdown(GFM) automatically **transforms** the relative address to the absolute address* when it is rendered and you can be assured that the relative links will always work.

1. Relative Links:

Relative links and image paths can be reached by specifying the destination relative to the current location.

For the uninitiated, here is a quick refresher to relative links:

- File in same folder - `/file.ext`
- File in sub folder - `/sub/location/file.ext`
- Root location - `../`

For example, if I wanted to [link to the main page](../README.md) of this repo, I would use the following code: `[link to the main page](../README.md)`.

If I wanted to link to a sister section on the same level, say for example the [python section](/Python/README.md), I would use the following code: `[python section](/Python/README.md)`.

The same address can be accessed by using an absolute address. We would access the [python section](../Python/README.md) by using this markdown: `../Python/README.md`.

2. Section Links:

You can link to a section on the page by copying the link from the *rendered file*. You will have to hover over the section to view the required link.

### Images

Markdown on Github can be used to place an image along with the alt-text describing it as shown below.

![Programmers can relate...](https://i.imgur.com/I6RpztMl.jpg)

```markdown
![Programmers can relate...](https://i.imgur.com/I6RpztMl.jpg)
Format: ![Alt Text](url)
```

#### Links placed on images

There is no functionality built in to markdown that allows us to link images to urls, but there are a few workarounds listed below.

1. Image with link to a url.

[![Visit YouTube.com](https://i.imgur.com/SrQXBqG.gif)](https://www.youtube.com/ "Image Title on Hover Here")

```markdown
[![IMAGE ALT TEXT HERE](https://image-url.here)](https://www.url.here "Title on Hover Here")
```

The markdown basically comprises of two parts:

- an image (the-link-text) `![IMAGE ALT TEXT HERE](https://image-url.here)`
- wrapped in a link `[the-link-text](https://www.url.here "Title on Hover Here")`

2. Image with link to a video.

Please note that this is ***not*** *a different method* than the one listed above.  what I personally do link my videos on my Github repos.

The syntax is the same as the above but we will perform a the extra step of making a custom thumbnail for the video, uploading it to an online service (like Imgur) and using that image in the markdown.

[![YouTube video on making custom thumbnail](https://i.imgur.com/SrQXBqG.gif)](https://www.youtube.com/watch?v=8YbZuaBP9B8 "WATCH Video - How to Make a YouTube Custom Thumbnail Tutorial")

```markdown
[![YouTube video on making custom thumbnail](https://i.imgur.com/SrQXBqG.gif)](https://www.youtube.com/watch?v=8YbZuaBP9B8 "WATCH Video - How to Make a YouTube Custom Thumbnail Tutorial")
```

### Lists

Preceding a line with `-` or `*` will begin an unordered list.

- This
- is a
- list

```markdown
- This
- is a
- list
```

Using a `*` will have the same effect.

* Here is
* another
* list

```markdown
* Here is
* another
* list
```

Preceding a line with a number will start a numbered list starting at the number specified.

1. This is
2. an ordered
3. list

```markdown
1. This is
2. an ordered
3. list
```

7. This list
8. starts with
9. number 7

```markdown
7. This list
8. starts with
9. number 7
```

#### Nested Lists

If any line in a list is indented, it is rendered as a sub list.

1. Main list item 1
2. Main list item 2
   1. Sub list item 1
3. Main list item 3
   - Sub list item 2
4. Main list item 4

```
1. Main list item 1
2. Main list item 2
   1. Sub list item 1
3. Main list item 3
   - Sub list item 2
4. Main list item 4
```

### Escaping\Ignoring Markdown

Using a `\` before a character which has a special meaning in markdown is used to ignore\escape it from being formatted in markdown.

For example, if I wanted to render a \*, \` or a \\ as normal text, we will need to escape it.

```markdown
For example, if I wanted to render a \*, \` or a \\ as normal text, we will need to escape it.
```

### Task Lists

Task lists are easy to create with markdown.

- Create a list of items using `- Task details`
- Preface the item with a space and `[ ]`
- If an item is complete mark the item with `[x]`

Here is an example list:

- [x] Create Github repo to maintain notes
- [x] Add your notes to repo
- [x] Add lots more useful stuff
- [ ] Get Github stars ;-)

```
- [x] Create Github repo to maintain notes
- [x] Add your notes to repo
- [x] Add lots more useful stuff
- [ ] Get Github stars ;-)
```
