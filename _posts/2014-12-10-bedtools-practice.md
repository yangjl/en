---
layout: post
title: "My usage examples of bedtools"
description: "from my personal experience"
category: bedtools
tags: [tutorial, usage, bedtools, BED, VCF]
---
{% include JB/setup %}


[**Bedtools**](http://bedtools.readthedocs.org/en/latest/index.html) is a very handy utilities for genomic data analysis, especially useful of the function **intersect** for feature intersection analysis. I like it because of the simple **BED** format and speed of their algorithm. Below is my personal usage examples for my own reference.

## BED and other formats

- BED [format](http://bedtools.readthedocs.org/en/latest/content/general-usage.html)
- Other genomic data format can be found from UCSC Genome Browser [website](http://genome.ucsc.edu/FAQ/FAQformat#format1)


## Find SNPs in window, report SNPs and which window they belong to.

```
bedtools intersect -a window.bed -b SNP.bed -wb
```
More details see here: [**intersect**](http://bedtools.readthedocs.org/en/latest/content/tools/intersect.html)

- __-a__ window of bed format
- **-b** SNPs of bed format
- **-wb** write the original entry in B for each overlap

  
