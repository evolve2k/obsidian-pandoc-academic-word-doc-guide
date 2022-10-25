# Setup Zotero with Obsidian

This guide connects Zotero with Obsidian to make automated citations, bibligraphies and literature notes.

## 1. Setup Zotero & create an account

Install Zotero [here](https://www.zotero.org)
Also create a free Zotero account to help you backup your precious research knowledge.

## 2. Install Zotero BetterBibTex Plugin

Download the [latest release](https://github.com/retorquere/zotero-better-bibtex/releases/latest)

Open Zotero -> tools -> addons -> install addon from file. Install the xpi file you downloaded.

Restart Zotero, and then setup Better BibLaTeX

Thanks to Mariana Montes for this wonderful guidance on setting up citation keys.

> Once you have installed Better BibTex, you will find a new tab in your Zotero Preferences (see Figure 1), where you can define a template for your citation keys. Mine uses, in lower case, the last name of the first author, separated by a period from the last name of the second author or, if there are more than two, etal. Then, it adds an underscore and the year.

![image](https://user-images.githubusercontent.com/114459/197723985-8714f150-1507-42ff-ba77-8a9d35fe9fce.png)

> This is a good pattern for me because it’s similar to how I’m used to thinking of the sources I cite: montes_2021 for Montes (2021); kiela.clark_2014 for Kiela & Clark (2014); heylen.etal_2015 for Heylen et al. (2015). When multiple publications have the same key, Better BibTex automatically adds an a, b, c… to the citation key. You have to remember which is which, but looking it up is not so hard either (see Figure 2).


### Export your Bibliography Library from Zotero the first time

Recommend you create a folder 'config' in your Obsidian Vault for config stuff like this.

<img width="338" alt="How to create a folder" src="https://user-images.githubusercontent.com/114459/197720840-b52105e4-c9f2-4ed3-97c0-4b1dd1d3d048.png">

In Zotero: File -> Export Library.. -> CSLJSON
Save the file in your Obsidian Vault (recommend: '/config/Library.json')

### Setup 'Citation' plugin in Obsidian


#### Create 'Literature Notes' folder
Add a new folder 'Literature Notes' to your Obsidian Vault main root directory (you can use another name here and in the config below)
(If you don't add the folder you’ll get strange ENOENT errors later)

Add a new folder in Obsidian called 'Literature Notes' (you can use a different name but make sure it's named exactly in the Citation plugin setup.)
Later Obsidian can auto create an automatic Literature Note file for any reference you have in Zotero.. and you can write your own notes on it there.

#### Configure Citation plugin

Obsidian > Preferences > Community Plugins > Browse > Search & Install 'Citation' plugin

Setup the following settings

<img width="707" alt="image" src="https://user-images.githubusercontent.com/114459/197720197-737b4ec0-cbae-43df-b41c-d00630c5bd22.png">
<img width="703" alt="image" src="https://user-images.githubusercontent.com/114459/197720264-99e5dd10-f761-4f8d-8495-665aa9d3633e.png">


More to come..

Credit to vasuagrawl for [their version of these instructions](https://notes.vasuagrawal.com/2022/04/zotero-and-obsidian-literature-notes/).

