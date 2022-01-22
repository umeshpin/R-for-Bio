# seqinR
The seqinR package contains bundle of utilities to retrieve and analyse biological sequences. Also using sequinr, we can access nucleotide / protein sequence data present in GenBank and in EMBL. 
As always, first you need to download and install the package. Then load the package into the R environment.

```R
install.packages("seqinr") 
library("seqinr")
```

Now let us first download the sequence of your interest by using R environment. Let us try to download human hemoglobin sequence from Swissprot. For this you have to choose the database as - swissprot and make sure that you are connected to internet. Before you start you need to find the Accession number of your sequence. In the example, the accession number of the gene is P69891  Now try the following codes.

```R
choosebank("swissprot")
hemo=query("hemoglo", "AC=P69891")
```

This will create a list with name hemo and having details of human hemoglobin inside it.  To get the sequence of the protein, following code can be used.

```R
seq_hemo<-getSequence(hemo$req[1])
```
Let us write this fasta file.
```R
write.fasta(sequences = seq_hemo, names = names(seq_hemo), nbchar = 147, file.out = "NewfileHemo")
```
In the similar way you can download data from any sequence database , or even search data using R environment. 
You can also do manipulations of your sequence by using seqinr. A sequence file from your desktop can be opened in R environment by using simple command (if you don't have a sequence file,
click here to get one) 
To read your fasta sequence, try 

```R
myseq=read.fasta(file="insulin.fasta", seqtype="DNA")
```

Now try 
```R
length(myseq$seq1) 
count(myseq$seq1, wordsize=2)
count(myseq$seq1, wordsize=3)
translate(myseq$seq1) 
GC(myseq$seq1) 
c2s(myseq$seq1)
```


## BLAST using Annotate Package

```R
library(annotate)
MyBlast <- blastSequences("acttcttggg cttagaacaa ctagaacatc tggatttcca gcattccaat ttgaaacaaa")
```


