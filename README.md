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

## This projet has now been changed to a simulation based on a prior published tree to observe the effects of constraining a molecular tree of palaeognaths to a morphological tree topology

## Methods

I used the intron ML tree from Cloutier et al (2019) to simulate sequences of 10000 nucleotides according to a JC model in Seq-Gen (Rambaut & Grassley 1997). These were then analyzed in IQ-TREE (Nguyen et al. 2015) both when unconstrained, and when constrained to a morphological topology from Nesbitt & Clarke (2016).

## Results

The results are as follows for the unconstrained ML tree:

MAXIMUM LIKELIHOOD TREE
-----------------------

Log-likelihood of the tree: -61326.2951 (s.e. 340.7343)
Unconstrained log-likelihood (without tree): -56010.1393
Number of free parameters (#branches + #model parameters): 27
Akaike information criterion (AIC) score: 122706.5902
Corrected Akaike information criterion (AICc) score: 122706.7418
Bayesian information criterion (BIC) score: 122901.2693

Total tree length (sum of branch lengths): 1.2028
Sum of internal branch lengths: 0.3134 (26.0592% of tree length)

NOTE: Tree is UNROOTED although outgroup taxon 'Gallus_gallus' is drawn at root
Numbers in parentheses are SH-aLRT support (%) / ultrafast bootstrap support (%)

+-----------------------------------------------------------Gallus_gallus
|
+---------Struthio_camelus
|
|               +--Rhea_americana
|  +------------| (100/100)
|  |            +--Rhea_pennata
+--| (100/100)
   |          +--Casuarius_casuarius
   |     +----| (100/100)
   |     |    +--Dromaius_novaehollandiae
   |  +--| (81.3/81)
   |  |  |       +--Apteryx_haastii
   |  |  |    +--| (100/100)
   |  |  |    |  +--Apteryx_owenii
   |  |  +----| (100/100)
   |  |       |  +--Apteryx_mantelli
   |  |       +--| (100/100)
   |  |          +--Apteryx_rowi
   +--| (84.5/80)
      |   +--------Anomalopteryx_didinus
      +---| (100/100)
          |             +--------Crypturellus_cinnamomeus
          |          +--| (100/100)
          |          |  +-------Tinamus_guttatus
          +----------| (100/100)
                     |  +-------------Eudromia_elegans
                     +--| (99.5/100)
                        +-------------Nothoprocta_perdicaria

Tree in newick format:

(Gallus_gallus:0.3996636751,Struthio_camelus:0.0703026758,((Rhea_americana:0.0072371822,Rhea_pennata:0.0070083111)100/100:0.0869384959,(((Casuarius_casuarius:0.0133319229,Dromaius_novaehollandiae:0.0185832353)100/100:0.0347051328,((Apteryx_haastii:0.0016028569,Apteryx_owenii:0.0010004477)100/100:0.0037573603,(Apteryx_mantelli:0.0009004406,Apteryx_rowi:0.0012015624)100/100:0.0043967754)100/100:0.0365914363)81.3/81:0.0005743361,(Anomalopteryx_didinus:0.0641571491,((Crypturellus_cinnamomeus:0.0608680508,Tinamus_guttatus:0.0540657611)100/100:0.0207053774,(Eudromia_elegans:0.0952888889,Nothoprocta_perdicaria:0.0941160534)99.5/100:0.0054300475)100/100:0.0741784799)100/100:0.0316185591)84.5/80:0.0009627858)100/100:0.0135704132);

The results are as follows for the morphology-constrained ML tree:

USER TREE
---------

Log-likelihood of the tree: -61813.7043 (s.e. 345.8391)
Unconstrained log-likelihood (without tree): -56010.1393
Number of free parameters (#branches + #model parameters): 28
Akaike information criterion (AIC) score: 123683.4085
Corrected Akaike information criterion (AICc) score: 123683.5714
Bayesian information criterion (BIC) score: 123885.2980

Total tree length (sum of branch lengths): 1.2617
Sum of internal branch lengths: 0.3014 (23.8902% of tree length)

WARNING: 3 near-zero internal branches (<0.0001) should be treated with caution
         Such branches are denoted by '**' in the figure below

NOTE: Tree is UNROOTED although outgroup taxon 'Gallus_gallus' is drawn at root
Numbers in parentheses are SH-aLRT support (%)

+-----------------------------------------------------------Gallus_gallus
|
|     +-----------Struthio_camelus
|  +--| (0)
|  |  |              +--Rhea_americana
|  |  |  +-----------| (100)
|  |  |  |           +--Rhea_pennata
|  |  +**| (0)
|  |     |    +--Casuarius_casuarius
|  |     +----| (100)
|  |          +--Dromaius_novaehollandiae
+**| (0)
|  |          +--Apteryx_haastii
|  |       +--| (100)
|  |       |  +--Apteryx_owenii
|  |  +----| (100)
|  |  |    |  +--Apteryx_mantelli
|  |  |    +--| (100)
|  |  |       +--Apteryx_rowi
|  +**| (0)
|     +------------Anomalopteryx_didinus
|
|                 +-------Crypturellus_cinnamomeus
|              +--| (100)
|              |  +------Tinamus_guttatus
+--------------| (100)
               |  +------------Eudromia_elegans
               +--| (98.9)
                  +------------Nothoprocta_perdicaria

Tree in newick format:

(Gallus_gallus:0.4221647939,((Struthio_camelus:0.0851130821,((Rhea_americana:0.0072530712,Rhea_pennata:0.0070002185)100:0.0883676390,(Casuarius_casuarius:0.0133575891,Dromaius_novaehollandiae:0.0185914278)100:0.0354604521)0:0.0000022861)0:0.0002301126,(((Apteryx_haastii:0.0016031245,Apteryx_owenii:0.0010005819)100:0.0037303076,(Apteryx_mantelli:0.0009005343,Apteryx_rowi:0.0012018551)100:0.0044250589)100:0.0372613989,Anomalopteryx_didinus:0.0959044535)0:0.0000025443)0:0.0000021997,((Crypturellus_cinnamomeus:0.0610900931,Tinamus_guttatus:0.0542889746)100:0.0208474801,(Eudromia_elegans:0.0958986532,Nothoprocta_perdicaria:0.0949195205)98.9:0.0051675355)100:0.1059294857);

## Discussion

These results only show preliminaarily the effects of constraining the molecular tree to a morphological topology, and further work will need to be conducted to relate this to the real-world data obtained from this group. There does seem to be less difference in likelihood and AIC scores than originally expected, though unconstrained tree values are still better. In addition, the constrained tree has many near zero-length and poorly supported branches incomparison with the unconstrained tree. Finally, tree length and sum of internal branches are also less different than initially expected, but this may be due to unconstrained having more uniform branch lengths, while those in the constrained tree are either extremely long or extremely short


## References

Bertelli S., Chiappe, L. M., Mayr, G. Phylogenetic interrelationships of living and extinct Tinamidae, volant palaeognathous birds from the New World. Zoological Journal of the Linnean Society 172 (1): 145–184.  https://doi.org/10.1111/zoj.12156
 
Cloutier et al. 2019. Whole-Genome Analyses Resolve the Phylogeny of Flightless Birds (Palaeognathae) in the Presence of an Empirical Anomaly Zone. Systematic Biology 68 (6): 937–955. https://doi.org/10.1093/sysbio/syz019
 
Johnston P. 2011. New morphological evidence supports congruent phylogenies and Gondwana vicariance for palaeognathous. Zoological Journal of the Linnean Society 163(3):959–982. https://doi.org/10.1111/j.1096-3642.2011.00730.x 
 
Mitchell K.J., Llamas B., Soubrier J., Rawlence N.J., Worthy T.H., Wood J., Lee M.S.Y., Cooper A. 2014. Ancient DNA reveals elephant birds and kiwi are sister taxa and clarifies ratite bird evolution. Science 344: 898–900. https://doi.org/10.1126/science.1251981
 
Nesbitt S.J., Clarke J. A. 2016. The anatomy and taxonomy of the exquisitely preserved Green River Formation (early Eocene) lithornithids (Aves) and the relationships of Lithornithidae. Bulletin of the American Museum of Natural History 406: 1–91. http://hdl.handle.net/2246/6664
 
L.-T. Nguyen, H.A. Schmidt, A. von Haeseler, B.Q. Minh. 2015. IQ-TREE: A fast and effective stochastic algorithm for estimating maximum likelihood phylogenies.. Mol. Biol. Evol. 32:268-274. https://doi.org/10.1093/molbev/msu300
 
Rambaut, A. and Grassly, N. C. 1997. Seq-Gen: An application for the Monte Carlo simulation of DNA sequence evolution along phylogenetic trees. Comput. Appl. Biosci. 13: 235-238. https://snoweye.github.io/phyclust/document/Seq-Gen.v.1.3.2/Seq-Gen.Manual.html
 
Worthy, T. H., Scofield, R. P. 2012. Twenty-first century advances in knowledge of the biology of moa (Aves: Dinornithiformes): a new morphological analysis and moa diagnoses revised, New Zealand Journal of Zoology 39 (2): 87–153. https://doi.org/10.1080/03014223.2012.665060
 
Yonezawa T., Segawa T., Mori H., Campos P.F., Hongoh Y., Endo H., Akiyoshi A., Kohno N., Nishida S., Wu J., Jin H., Adachi J., Kishino H., Kurokawa K., Nogi Y., Tanabe H., Mukoyama H., Yoshida K., Rasoamiaramanana A., Yamagishi S., Hayashi Y., Yoshida A., Koike H., Akishinonomiya F., Willerslev E., Hasegawa M. 2017. Phylogenomics and morphology of extinct paleognaths reveal the origin and evolution of the ratites. Current Biology 27:68–77. https://doi.org/10.1016/j.cub.2016.10.029
