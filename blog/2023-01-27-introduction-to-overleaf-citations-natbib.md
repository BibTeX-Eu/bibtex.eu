---
slug: "using-overleaf-for-writing-papers-with-citations-and-natbib"
title: "Using Overleaf for Writing Papers with Citations and natbib"
authors:
  name: BibTeX FAQ
  title: https://www.CiteDrive.com/
  mail: hello@citedrive.com
  url: https://www.CiteDrive.com/
  image_url: https://avatars.githubusercontent.com/u/65911387?s=200&v=4
tags: [AcademicWriting, natbib, LaTeX, CitationManagement, Overleaf, BibTeX, BibLaTeX, natbib, Zotero, Mendeley, Research, WritingTips, Academia, ScholarlyWriting, References]
---


# Using Overleaf for Writing Papers with Citations and natbib

Overleaf is a popular online LaTeX editor that allows users to collaborate on documents in real-time. One of the great features of Overleaf is the ability to easily add citations and bibliographies to your documents using the natbib package. In this post, we will go over the basics of using natbib with Overleaf to add citations and bibliographies to your papers.

## Adding Citations

To add citations in Overleaf, you first need to add the natbib package to your document. This can be done by adding the following line to the preamble of your document:

`\usepackage[numbers]{natbib}`

This will allow you to use the `\citep` and `\cite` commands to add citations to your document. The `\citep` command is used for in-text citations and will display the citation as a number in parentheses, while the `\cite` command is used for in-text citations and will display the citation as a number.

For example, to cite a paper by Smith et al. (2020) in-text, you would use the following command:

`According to \citep{Smith2020}, this is an important finding.`

This will display the citation as:

> According to (Smith et al., 2020), this is an important finding.

## Adding a Bibliography

To add a bibliography to your document in Overleaf, you first need to create a `.bib` file that contains the information for all of the references that you will be citing. The `.bib` file should be saved in the same directory as your main `.tex` file. One of the easiest ways to create this `.bib` file is by using [CiteDrive](https://citedrive.com/), a tool that connects to Overleaf and generates the bib file for you. More information can be found in the [blog post on Overleaf.com](https://www.overleaf.com/blog/better-bibliography-management-with-overleaf-citedrive-and-bibtex-biblatex).

Once you have created your `.bib` file, you can add a bibliography to your document by adding the following command to your document:

`\bibliography{mybibfile}`

where `mybibfile` is the name of your `.bib` file.

You can also specify the style of your bibliography by adding the following command to your document:


`\bibliographystyle{plainnat}`

This will format your bibliography in a plain style. There are many different bibliography styles available, and you can find a list of them [here](https://www.overleaf.com/learn/latex/Bibliography_styles).

## Conclusion

In this post, we have gone over the basics of using natbib with Overleaf to add citations and bibliographies to your papers. With Overleaf's easy-to-use interface and natbib's powerful citation and bibliography management capabilities, you can easily keep track of your references and format your bibliography in the style that is required by your publication. Additionally, using CiteDrive to generate the bib file for you can save a lot of time and effort.
