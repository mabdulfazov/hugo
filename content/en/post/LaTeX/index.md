---
title: LaTeX
subtitle: Software system for document preparation

# Summary for listings and search engines
summary: LaTeX  is a software system for document preparation.
# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Logo**](https://en.wikipedia.org/wiki/File:LaTeX_project_logo_bird.svg)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---


## Overview

<hr>

**LaTeX**  is a software system for document preparation. When writing, the writer uses plain text as opposed to the formatted text found in "What You See Is What You Get" word processors like Microsoft Word, LibreOffice Writer and Apple Pages. The writer uses markup tagging conventions to define the general structure of a document to stylise text throughout a document (such as bold and italics), and to add citations and cross-references. A TeX distribution such as TeX Live or MiKTeX is used to produce an output file (such as PDF or DVI) suitable for printing or digital distribution.

LaTeX is widely used in academia for the communication and publication of scientific documents in many fields, including mathematics, computer science, engineering, physics, chemistry, economics, linguistics, quantitative psychology, philosophy, and political science. It also has a prominent role in the preparation and publication of books and articles that contain complex multilingual materials, such as Sanskrit and Greek. LaTeX uses the TeX typesetting program for formatting its output, and is itself written in the TeX macro language.

LaTeX can be used as a standalone document preparation system, or as an intermediate format. In the latter role, for example, it is sometimes used as part of a pipeline for translating DocBook and other XML-based formats to PDF. The typesetting system offers programmable desktop publishing features and extensive facilities for automating most aspects of typesetting and desktop publishing, including numbering and cross-referencing of tables and figures, chapter and section headings, the inclusion of graphics, page layout, indexing and bibliographies.

Like TeX, LaTeX started as a writing tool for mathematicians and computer scientists, but even from early in its development, it has also been taken up by scholars who needed to write documents that include complex math expressions or non-Latin scripts, such as Arabic, Devanagari and Chinese.

LaTeX is intended to provide a high-level, descriptive markup language that accesses the power of TeX in an easier way for writers. In essence, TeX handles the layout side, while LaTeX handles the content side for document processing. LaTeX comprises a collection of TeX macros and a program to process LaTeX documents, and because the plain TeX formatting commands are elementary, it provides authors with ready-made commands for formatting and layout requirements such as chapter headings, footnotes, cross-references and bibliographies.

LaTeX was originally written in the early 1980s by Leslie Lamport at SRI International. The current version is LaTeX2e (stylised as LATEX2ε), released in 1994, but updated in 2020. LaTeX3 (LATEX3) has been under long-term development since the early 1990s. LaTeX is free software and is distributed under the LaTeX Project Public License (LPPL).


## Typesetting system

<hr>

LaTeX attempts to follow the design philosophy of separating presentation from content, so that authors can focus on the content of what they are writing without attending simultaneously to its visual appearance. In preparing a LaTeX document, the author specifies the logical structure using simple, familiar concepts such as _chapter_, _section_, _table_, _figure_, etc., and lets the LaTeX system handle the formatting and layout of these structures. As a result, it encourages the separation of the layout from the content — while still allowing manual typesetting adjustments whenever needed. This concept is similar to the mechanism by which many word processors allow styles to be defined globally for an entire document, or the use of Cascading Style Sheets in styling HTML documents.

The LaTeX system is a markup language that handles typesetting and rendering, and can be arbitrarily extended by using the underlying macro language to develop custom macros such as new environments and commands. Such macros are often collected into _packages,_which could then be made available to address some specific typesetting needs such as the formatting of complex mathematical expressions or graphics (e.g., the use of the `align`environment provided by the `amsmath` package to produce aligned equations).

In order to create a document in LaTeX, you first write a file, say `document.tex`, using your preferred text editor. Then you give your `document.tex` file as input to the TeX program (with the LaTeX macros loaded), which prompts TeX to write out a file suitable for onscreen viewing or printing. This write-format-preview cycle is one of the chief ways in which working with LaTeX differs from the What-You-See-Is-What-You-Get (WYSIWYG) style of document editing. It is similar to the code-compile-execute cycle known to computer programmers. Today, many LaTeX-aware editing programs make this cycle a simple matter through the pressing of a single key, while showing the output preview on the screen beside the input window. Some online LaTeX editors even automatically refresh the preview, while other online tools provide incremental editing in-place, mixed in with the preview in a streamlined single window.


## Pronouncing and writing "LaTeX"

<hr>

The characters 'T', 'E', and 'X' in the name come from the Greek capital letters tau, epsilon, and chi, as the name of TeX derives from the Ancient Greek: τέχνη ('skill', 'art', 'technique'); for this reason, TeX's creator Donald Knuth promotes its pronunciation as /tɛx/ (_tekh_) (that is, with a voiceless velar fricative as in Modern Greek, similar to the ch in loch). Lamport remarks that "TeX is usually pronounced _tech_, making _lah_-tech, lah-_tech_, and _lay_-tech the logical choices; but language is not always logical, so _lay-tecks_ is also possible."

The name is traditionally printed in running text with a special typographical logo: LATEX. In media where the logo cannot be precisely reproduced in running text, the word is typically given the unique capitalization _LaTeX_. Alternatively, the TeX, LaTeX and XeTeX logos can also be rendered via pure CSS and XHTML for use in graphical web browsers — by following the specifications of the internal `\LaTeX` macro.


## Related software

<hr>

As a macro package, LaTeX provides a set of macros for TeX to interpret. There are many other macro packages for TeX, including Plain TeX, GNU Texinfo, AMSTeX, and ConTeXt.

When TeX "compiles" a document, it follows (from the user's point of view) the following processing sequence: Macros → TeX → Driver → Output. Different implementations of each of these steps are typically available in TeX distributions. Traditional TeX will output a DVIfile, which is usually converted to a PostScript file. More recently, Hàn Thế Thành and others have written a new implementation of TeX called pdfTeX, which also outputs to PDF and takes advantage of features available in that format. The XeTeX engine developed by Jonathan Kew, on the other hand, merges modern font technologies and Unicode with TeX.

The default font for LaTeX is Knuth's Computer Modern, which gives default documents created with LaTeX the same distinctive look as those created with plain TeX. XeTeX allows the use of OpenType and TrueType (that is, outlined) fonts for output files.

There are also many editors for LaTeX, some of which are offline, source-code-based while others are online, partial-WYSIWYG-based. For more, see Comparison of TeX editors.


## History

<hr>

LaTeX was created in the early 1980s by Leslie Lamport, when he was working at SRI. He needed to write TeX macros for his own use, and thought that with a little extra effort he could make a general package usable by others. Peter Gordon, an editor at Addison-Wesley, convinced him to write a LaTeX user's manual for publication (Lamport was initially skeptical that anyone would pay money for it); it came out in 1986 and sold hundreds of thousands of copies. Meanwhile, Lamport released versions of his LaTeX macros in 1984 and 1985. On 21 August 1989, at a TeX Users Group (TUG) meeting at Stanford, Lamport agreed to turn over maintenance and development of LaTeX to Frank Mittelbach. Mittelbach, along with Chris Rowley and Rainer Schöpf, formed the LaTeX3 team; in 1994, they released LaTeX2e, the current standard version. LaTeX3 itself has since been cancelled with version features intended for that version being back-ported to LaTeX 2e since 2018.

