# Recommendations and suggestions on reference formatting for project proposals and theses

## 1) Request: use author-year citation styles

Citation styles can be cathegorized into two groups: those that reference bibliographic resources using **the name of the first author and year of publication** ([here is an example article using this style](https://rss.onlinelibrary.wiley.com/doi/10.1111/rssc.12234)), and those that use a **sequential number** ([here is an example using this approach](https://onlinelibrary.wiley.com/doi/10.1002/sim.9178)).

Personally, as a reader I find that **author-year** citation styles make documents easier to read: if I see the name of the first author and year of publication in the text, I may already be familiar with that publication and understand what is being referenced. This is not possible with numbered referencing: in that case, for each reference I would need to scroll the document until the bibliography to find out what is being referenced.

Therefore, I would like to ask you to **use author-year citation styles in your project proposal and thesis**. You are free to choose the specific citation style you want to use among the many available author-citation styles, but if you would like a suggestion, **my recommentation is to use the APA citation style**, which was developed by the American Psychological Association. To use that in LaTex, you may use:

\usepackage{natbib}
\bibliographystyle{apalike}
\bibliography{bibliography_file}

## 2) Suggestion: use a dedicated tool to manage your bibliography and the citation style

Managing references and citation styles is a tedious task. Luckily, it can be easily automated. Here is how you can do it by using LaTeX and BibTeX:

1. Install [JabRef](https://www.jabref.org)
2. Open JabRef and create a BibTeX archive with: File -> New library
3. Use Google Scholar to identify the resource you want to cite, then click on: Cite -> BibTeX
4. Copy the BibTeX code that appears, for example:

`@article{signorelli2020model,
  title={Model-based clustering for populations of networks},
  author={Signorelli, Mirko and Wit, Ernst C},
  journal={Statistical Modelling},
  volume={20},
  number={1},
  pages={9--29},
  year={2020},
  publisher={SAGE Publications Sage India: New Delhi, India}
}`

5. Add this BibTeX-formatted citation to your JabRef file (click on the +, then in the new record click on "BibTeX source" and insert the copied text there)
6. Save the BibTeX archive
7. In your LaTeX document, include `\usepackage{natbib}` in the preamble, and:

`\bibliographystyle{apalike}`  
`\bibliography{bibtex_filename}`

 at the end of the document

8. Compile your LaTeX document with `PDFLaTeX` once, then compile the BibTeX archive with BibTeX, and then recompile the LaTeX document with PDFLaTeX **twice**.

If you have troubles doing this, let me know and I can try to help you making this procedure work. It takes some time to get used to it, but it is worth it in the long run!
