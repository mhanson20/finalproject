# Phylogenetic Biology - Final Project

## Guidelines - you can delete this section before submission

This repository is a stub for your final project. Fork it, develop your project, and submit it as a pull request. Edit/ delete the text in this readme as needed.

Some guidelines and tips:

- Use the stubs below to write up your final project. Alternatively, if you would like the writeup to be an executable document (with [knitr](http://yihui.name/knitr/), [jupytr](http://jupyter.org/), or other tools), you can create it as a separate file and put a link to it here in the readme.

- For information on formatting text files with markdown, see https://guides.github.com/features/mastering-markdown/ . You can use markdown to include images in this document by linking to files in the repository, eg `![GitHub Logo](/images/logo.png)`.

- The project must be entirely reproducible. In addition to the results, the repository must include all the data (or links to data) and code needed to reproduce the results.

- If you are working with unpublished data that you would prefer not to publicly share at this time, please contact me to discuss options. In most cases, the data can be anonymized in a way that putting them in a public repo does not compromise your other goals.

- Paste references (including urls) into the reference section, and cite them with the general format (Smith at al. 2003).

- Commit and push often as you work.

OK, here we go.

# A Total Evidence Tree for Palaeognathous Birds

## Introduction and Goals

In this project, I aim to answer the questions: What are the phylogenetic relationships amongst the palaeognath birds (ratites and tinamous) given the current data available from molecules and morphology? An,d how do morphological character distributions optimize within that tree.

For my methods, I will construct and analyze molecular trees from genomic and genetic data using Maximum Likelihood methods in IQtree, I will also use these trees to analyze morphologicxcal charactrer distributions, and I will construct and analyze molecular and molecular+morphological trees using Bayesian methods in RevBayes as well.

I will use data from published and publicly-available genomic and other molecular studies (most importantly, Mitchell et al. 2014 and Yonezawa et al. 2017) available on GenBank.  In the years since those studies were published, more species in this group (especially tinamous) have become available, and I will incorporate these newly released genomic data from the B10K project (recently made available on GenBank) and other smaller sequences from genetic studies (also publicly available on GenBank).
I will also incorporate morphological character data using character sets ands matrices from the morphological studies of Nesbitt and Clarke (2016), Mitchell et al. (2014), Worthy and Scofield (2012), Johnston (2011), and Bertelli et al. (2014). These matrices are generally non-overlapping in the characters used and often lack a number of key taxa covered by molecular data (particularly elephantbirds, Aepyornithiformes). In cases where characters are not coded for a particular taxon, I will preliminarily use published anatomical descriptions, though firsthand examination of specimens is ideal and will be attempted should access to museum collections become available.

## Methods

The tools I used were... See analysis files at (links to analysis files).

## Results

The tree in Figure 1...

## Discussion

These results indicate...

The biggest difficulty in implementing these analyses was...

If I did these analyses again, I would...

## References

