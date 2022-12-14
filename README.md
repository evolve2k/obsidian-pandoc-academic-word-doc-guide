# Obsidian Pandoc Academic Workflow Guide

This guide has been created to be a community resource providing guidance on how to setup Obsidian to generate word documents for academic purposes.
This guide is explictly concerned with generating documents from pandoc.

# Objectives

Pressing a shortcut key combo within a document in Obsidian, auto-generates a Word/Libre Office Document.

The document contains:

1. Automatic inline citations and a reference list (based on your desired reference style).
2. Embeds your images 
2. An automatic Table of Contents drawn from your Markdown headers.
4. Has reasonable styling so headings and document is readable without formatting work

# Getting setup

## 1. Automatic inline citations and a reference list 

Pandoc provides support for various academic referencing styles. This makes using pandoc for document conversion the necessary tool to use.

Instructions to Setup Obsidian with Zotero [are here](setup-zotero-obsidian.md).


### How to add page numbers in a citation

When you add a citation (eg I press Ctrl + Shift + M) it drops in a citation link (I have mine set to use APA).

    [@gwilt_2022] becomes (Gwilt, 2022) # for me as I'm using APA.

To add page numbers to a reference; add the the page number(s) after a comma inside the brackets

    [@gwilt_2022,5] becomes (Gwilt, 2022, p. 5)
    [@gwilt_2022,17-19] becomes (Gwilt, 2022, pp. 17-19)
    
| Markdown | Example Pandoc Output |
| ------------- | ------------- |
| [@gwilt_2022,5]  | (Gwilt, 2022, p. 5)  |
| [@gwilt_2022,17-19] | (Gwilt, 2022, pp. 17-19)  |
| [@gwilt_2010 updated 2020]  | (Gwilt, 2010 updated 2020) |


## 2. Embeds your images

Generally there are two issues at play
- The defauly image markup used by Obsidian when you drag images in, is not understood by Pandoc.
- The file path has issues, either not pointing to the same place or also it has spaces in it.

Here's my personal workaround, to 'get it images working' to begin with.

1. Update where images are stored in Obsidian Preferences

 > Files & Links > Default location for new attachments

(I've used a folder called 'media', but you can use a different name)

![image](https://user-images.githubusercontent.com/114459/197368985-1ec874f5-b5e4-458c-baa9-89a6038111cf.png)

2. Use links in this format

```![](media/filename.png)```

*Test this yourself: Drag a new image into your document, check that it was added to /media within the same folder as your document and then hand adjust the markdown match the format above.*

3. Making this *more* efficient

WORKAROUND: Install 'Wikilinks to MDLinks' plugin and convert the image markdown for each image
1. Install (& Enable) Plugin '[Wikilinks to MDLinks](https://github.com/agathauy/wikilinks-to-mdlinks-obsidian)'
2. Click on an image link, press 'Cmd/Ctrl + Shift + L' to swap the Link format.
3. Manually delete extra path details from the image path so you only have '/media/filename.png'
4. Generate the document and the images should be there :)

NOTE: Converting from md to docs [DOES NOT require `--extract-media`](https://groups.google.com/g/pandoc-discuss/c/NSAeHu0YTE8/m/7_7tmW4sCQAJ) 
This is needed when converting from docx > md BUT NOT for md > docx.

This issues references most of them as a state of play: https://github.com/OliverBalfour/obsidian-pandoc/pull/128

## 3. Automatic Table of Contents drawn from your Markdown headers

The 'Dynamic Table of Contents' plugin adds a table of contents within an Obsidian file.

Add `--toc` paramater to your "Extra Pandoc Arguments" within the `pandoc plugin`.

## 4. Has reasonable styling so headings and document is readable without formatting work

This can be achieved by adding a reference document to pandoc.
Not yet explored. This seems to be the best guide I've found so far: https://stackoverflow.com/questions/70513062/how-do-i-add-custom-formatting-to-docx-files-generated-in-pandoc

## Extra Pandoc Arguments Example

--toc
--citeproc 
--bibliography=/Users/username/Zotero/Library.json 
--csl=/Users/username/Zotero/styles/apa.csl

Contributions, questions, isssues, PR's welcome :)

## 5. Refinements to address annoyances that affect personal flow

### When switching between notes in Obsidian, when you return to a note you are taken back to the top of the document.

This interupts flow and thought process as every time you switch between notes you loose your place.

Best discussion is this forum post: [Restore last document position](https://forum.obsidian.md/t/restore-last-document-position/962/59), accessed Nov 2022

As of 2022, Install the community plugin: [obsidian-remember-cursor-position](https://github.com/dy-sh/obsidian-remember-cursor-position)
