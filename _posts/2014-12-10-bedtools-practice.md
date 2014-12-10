---
layout: post
title: "My usage examples of bedtools"
description: "from my personal experience"
category: genomics
tags: [tutorial, usage, bedtools, BED]
---
{% include JB/setup %}


[**Bedtools**](http://bedtools.readthedocs.org/en/latest/index.html) contain several handy utilities for genomic data analysis, especially useful for feature intersection analysis by using the function **intersect**. I like bedtools because of the simple **BED** format and speed of their algorithm. Below is my personal usage examples for my own reference.

## BED and other formats

### BED [format](http://bedtools.readthedocs.org/en/latest/content/general-usage.html)
1. BED3: A BED file where each feature is described by _chrom_, _start_, and _end_.  
For example: chr1 110 120  
Note: start is zero-based, where the first base in a chr is numbered 0. And the end is one-based. For example, a SNP at 10 should be coded as start=9, end=10.
2. BED4: _chrom_, _start_, _end_ and _name_.
### Other genomic data format can be found from UCSC Genome Browser [website](http://genome.ucsc.edu/FAQ/FAQformat#format1)

## Find SNPs in window, report SNPs and which window they belong to.

```
bedtools intersect -a window.bed -b SNP.bed -wb
```
More details see here: [**intersect**](http://bedtools.readthedocs.org/en/latest/content/tools/intersect.html)

- __-a:__ window of bed format
- __-b:__ SNPs of bed format
- __-wb:__ write the original entry in B for each overlap

  
