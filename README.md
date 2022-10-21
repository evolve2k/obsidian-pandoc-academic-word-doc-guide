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


## 2. Embeds your images (IN PROGRESS)

BUG. Currently there are known issues setting up Obsidian Pandoc to export images.
This issues references most of them as a state of play: https://github.com/OliverBalfour/obsidian-pandoc/pull/128

## 3. Automatic Table of Contents drawn from your Markdown headers

The 'Dynamic Table of Contents' plugin adds a table of contents within an Obsidian file.
No idea how to do this currently.

Closest workaround is to Manually paste what 'Dynamic Table of Contents' creates into the word document afterwards, but this comes with formatting issues.

## 4. Has reasonable styling so headings and document is readable without formatting work

This can be achieved by adding a reference document to pandoc.
Not yet explored. 
