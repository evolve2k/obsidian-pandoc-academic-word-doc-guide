# Obsidian Pandoc Academic Word Doc Guide

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

Setup 'citation' plugin to integrate with your reference manager.
Setup 'pandoc plugin' to export to desired 

## 2. Embeds your images

Current the default Images markup used by Obsidian is not understood by Pandoc.

WORKAROUND: Install 'Wikilinks to MDLinks' plugin and convert the image markdown for each image
1. Install (& Enable) Plugin '[Wikilinks to MDLinks](https://github.com/agathauy/wikilinks-to-mdlinks-obsidian)'
2. Click on each image link, press 'Cmd/Ctrl + Shift + L' to swap the Link format.
3. Generate the document and the images should be there :)

NOTE: Converting from md to docs DOES NOT require `--extract-media` 
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
--bibliography=/Users/richiekhoo/Zotero/Library.json 
--csl=/Users/richiekhoo/Zotero/styles/apa.csl

