---
layout: post
title: "R package Data.Table Usage Notes"
description: "from my personal experience"
category: codes
tags: [tutorial, usage, R, NGS]
---
{% include JB/setup %}

Most of those were learned from Kate Crosby's [short tutorial](https://github.com/kate-crosby/datatable_slides) in [RIL lab](http://www.rilab.org/).

## Read in data.frame rapidly with **fread**

```
## tab delimited file
data <- fread("yourfile.txt", sep="\t")
## csv file
data <- fread("yourfile.csv", sep=",")
```

## Subsetting dt
### := NULL

```
sub <- data[, c("chr", "pos") := NULL]
```
### use function of **subset**
```
sub <- subset(fulldata, select = c("chr", "pos"))
```
### .SD = "Subset of Data.table"
Select the 2nd row (SNP) for/of each chromosome!
```
dt <- dt[, .SD[2], by=chrom]
```

## Order data really quickly with setkey()


```
# Here in chr and then pos
order.dt <- setkey(dt, "chr", "pos")
```

## More information

  
