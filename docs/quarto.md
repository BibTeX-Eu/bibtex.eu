---
title: Reference management with BibTeX, when using Quarto -- A short guide
description: "This quick tutorial will show you how to manage your references using BibTeX. BibTeX is a reference management software that allows you to store and organize your references in a simple, easy-to-use format."
sidebar_label: Using Quarto (RStudio/Posit) (Quick start)
sidebar_position: 3
---

# Reference management in Quart (RStudio/Posit) with BibTeX: A short guide

Quarto is an excellent tool for producing reproducible reports, papers, and presentations, among other things. One of the features that distinguishes Quarto is its ability to integrate with other tools and software. BibTeX, a reference management system for LaTeX documents, is one such tool. BibTeX makes it simple to cite sources and create a bibliography in your document.



## Step 1: Create a .bib-file and create some entries.

As in the previous section, we begin by creating a.bib-file called 'bibliography.bib,' which is then filled with BibTeX entries.
BibTeX entries are built in the following format and contain enough information for citation and bibliography inclusion for each literature source (book, essay, etc.).

We use the example from the previous section and quote the book "The Old Man and the Sea" by Ernest Hemingway. The result is as follows:

```latex
@book{Hemingway1952,
  title={The Old Man and the Sea},
  author={Hemingway, Ernest},
  year={1952},
  publisher={Charles Scribner's Sons}
}
```

Again, we dissect this entry's "anatomy," focusing on three components to understand how each BibTeX entry is defined:

* **Entry-type**: with `@book` we define the type according to the schema `@type` of the reference. Possible are `@article` for scientific articles and others. BibTeX likes to specify which fields are optional and which are required to indicate them correctly in the literature.
* **Entry fields**: in this case of our `@book` example, these are `title`, `author`, `year` and `publisher`. (Cf. [fields](./fields))
* **citation-key**: in our example, it is `Hemingway1952` and is used to indicate an in-text citation in LaTeX, i.e., to refer to the source. in Quarto we do this with `[@Hemingway1952]`. The citation key can be any string - often a combination of author, year, and a word from the title.



## Step 2: Create a Quarto document and connect

It is very simple to integrate BibTeX with Quarto. Simply specify the bib-file with 'bibliography: bibliography.bib' in YAML and the citation with '[@Hemingway1952]' at the location where you want the in-text citation to appear.

```md
---
title: "BibTeX references in Quarto"
author: "John Doe"
date: '2022-07-19'
bibliography: bibliography.bib
output: html_document
---


## BibTeX references in Quarto

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Praesent enim urna, dapibus et bibendum vel, consectetur et turpis.
Cras a molestie nulla. [@Hemingway1952]


```


## Reference managers

Manually formatting BibTeX files can be time-consuming, which is why it is generally recommended to use a reference manager. Here are a few that are ideal for this:

* [CiteDrive](https://www.citedrive.com/) is a bibtex-powered, collaborative, and cloud-based tool for managing project references and teams. It provides a one-click export to Overleaf ([*Cf. Overleaf Blog Post - https://www.overleaf.com/blog/citedrive... | CiteDrive-Easy Reference Management for Overleaf*](https://www.overleaf.com/blog/citedrive-easy-reference-management-for-overleaf)) along with Quarto ([*Cf. Medium post: Bibliography Management in Quarto with CiteDrive and RStudio*](https://citedrive.medium.com/bibliography-management-in-r-markdown-with-citedrive-and-rstudio-2585699dd619)), while keeping citations in sync.
* [Zotero](https://www.zotero.org/) is a free, open-source literature management tool that manages bibliographic data and related research materials (such as PDF files). The best performance for BibTeX in Zotero is achieved with **[Better BibTeX For Zotero](https://retorque.re/zotero-better-bibtex/)** by retorque.
* The free, open-source software [JabRef](https://www.jabref.org/) is a BibTeX-supported reference manager that runs on Windows, Mac, and Linux. It is based on Java and is maintained by JabRef e.V.
