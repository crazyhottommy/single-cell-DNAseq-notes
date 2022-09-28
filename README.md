# single-cell-DNAseq-notes

Single-cell DNAseq has its own challenges including elevated error rates, allelic drop-out, and uneven coverage.
Analysis of single cell DNA sequencing data remains challenging due to bias and artifacts that arise during DNA extraction and whole-genome amplification, including allelic imbalance and dropout.

>in the human genome a genes copy number may fluctuate in **cancer cells** that have lost the ability to correct errors. In some instances all chromosomes are duplicated to produce tetraploids which may appear to be diploid unless you provide a read reference.

Sequencing libraries suitable for genotyping require whole genome amplification, which introduces allelic bias and copy errors.

DNA amplification methods:

* [multiple displacement amplified (MDA) single cell DNA sequencing](https://www.qiagen.com/us/knowledge-and-support/knowledge-hub/bench-guide/wga/multiple-displacement-amplification-wga/multiple-displacement-amplification-wga)

>Multiple displacement amplification (MDA) involves the binding of random hexamers to denatured DNA followed by strand displacement synthesis at a constant temperature using the enzyme Phi29 polymerase. Additional priming events can occur on each displaced strand leading to a network of branched DNA structures (see figure Schematic representation of MDA).

![image](https://user-images.githubusercontent.com/4106146/192796968-236390e8-0a80-4e29-bc42-11451641b89f.png)


* To reduce this artifact burden, an improved amplification technique, primary template-directed amplification (PTA) is introduced in Gonzalez-Pena, V. et al. [Accurate genomic variant detection in single cells with primary template-directed amplification](https://www.pnas.org/doi/10.1073/pnas.2024176118). Proc. Natl Acad. Sci. USA 118, e2024176118 (2021).

>Here, we present primary template-directed amplification (PTA), an isothermal WGA method that reproducibly captures >95% of the genomes of single cells in a more uniform and accurate manner than existing approaches, resulting in significantly improved variant calling sensitivity and precision.

![image](https://user-images.githubusercontent.com/4106146/192797536-f2e108b3-a1c2-449f-9c0a-32c6277c634d.png)


### mutation calling

* [Single-cell mutation identification via phylogenetic inference](https://www.nature.com/articles/s41467-018-07627-7)
* [Single-cell mutation calling and phylogenetic tree reconstruction with loss and recurrence](https://www.biorxiv.org/content/10.1101/2022.01.28.478229v1)

Simona:
>these two papers that I shared are relevant especially for cancer, where the observed mutations come from clonal evolution, i.e. they didn’t arise independently.hence logic is that one estimates these variants best if taking the tree into account;most optimal if inferred together

* [SCAN2](https://github.com/parklab/SCAN2) from Peter Park's group. used for mutation calling in this Paper https://www.nature.com/articles/s41588-022-01180-2
* [Accurate and scalable variant calling from single cell DNA sequencing data with ProSolo](https://www.nature.com/articles/s41467-021-26938-w)
