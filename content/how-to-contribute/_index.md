---
title: How to contribute
linkTitle: "How to contribute"
weight: 100
type: docs

tags: [meta, Git]
---

This page explains how to contribute to the OESA Knowledge Collection
via feedback or edits.

### Feedback

To give feedback on the site, use the <a class="">Give feedback</a> link at the top of the right navigation bar of the page under consideration.
This will start a GitLab issue with a link to the page.
Add your feedback below the link and press "Create issue" at the very bottom.

### Editing

The website is powered by [Hugo](https://gohugo.io/), a Static Site Generator (SSG).
Source files are written in Markdown.     


#### In the browser: Edit existing pages

The easiest way to edit existing pages is to use the <a class="">Edit</a> link at the top of the respective page.
This will open the file for editing in GitLab in your browser.

Change the "Target branch" field to a branch name different from `main` and leave the "Start a new merge request with these changes" ticked.
Then, press "Commit changes" at the bottom.
A new merge request page will appear. Optionally, add a description.
Then, press "Create merge request" at the bottom.


#### Locally: 

To edit the site locally, potentially with [Local preview](#local-preview), clone the repository 

```
git clone https://git.ufz.de/oesa/knowledge.git
```

and create a branch and switch to it, e.g. 
```
git checkout -b newbranchname
```

Markdown for the individual pages can be found in folder [`content`](https://git.ufz.de/oesa/knowledge/-/tree/main/content).

Make your edits and create a Merge Request when done.

VSCode is recommended for editing (gives a nice markdown preview) - but any other editor will do. 

##### Edit a page: 
Open the page in an editor and edit it. 

##### Add a page
- copy the page template file from the template folder to the folder you want your new page to reside in.
- Edit the copied file and change according to your needs.
- With the weight fied in the header you can determine page ordering. 

##### Add a folder

- add a folder
- copy _index.md from the template folder to the new folder
- edit _index.md according to your needs.

The new folder is shown in the menue with the link title specified in _index.md. When this link is choosen _index.md gets displayed. 
 

### Local preview

For local preview, [Hugo](https://gohugo.io/) (extended) is required. On oesa151w it is already installed.      
Otherwise get Hugo from the [GitHub releases](https://github.com/gohugoio/hugo/releases/) or follow the [installation instructions](https://gohugo.io/installation/).

{{% alert title="Important!" color="warning" %}}
`hugo-extended` is required!
{{% /alert %}}

With Hugo installed, run the following in the site repository's root directory:

```
hugo serve
```

Then, open the address shown at the bottom of the console output in a web browser.
Usually, it is:

```
http://localhost:1313/knowledge/
```

The page will update automatically when source files are changed.

On oesa151w the local preview it still looks ugly and not usable. 
