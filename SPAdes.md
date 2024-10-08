# SPAdes documentation

Author: Rutuja Gupte  

This is the important stuff from the SPAdes guide. The complete guide is linked at the bottom.

## Installation

```
wget https://github.com/ablab/spades/releases/download/v4.0.0/SPAdes-4.0.0-Linux.tar.gz
tar -xzf SPAdes-4.0.0-Linux.tar.gz
cd SPAdes-4.0.0-Linux/bin/
ls
export PATH="/home/dnanexus/SPAdes-4.0.0-Linux/bin:$PATH"
cd ..
cd ..
```

## Test it!

This will dump a lot of text but it will do something.

```
spades.py --test
```

## Run it

```
spades.py -1 fastq_1.fq.gz -2 fastq_2.fq.gz --isolate -o fname
```

--isolate flag recommended for multi-cell Illumina reads.

## k-mer values

"read length 100bp the default k values are 21, 33, 55; for 150bp reads SPAdes uses k-mer sizes 21, 33, 55, 77; and for 250bp reads six iterations are used by default: 21, 33, 55, 77, 99, 127"

- Substring of length k
- (Think N-grams for NLP)
- Mammals have multimodal distribution
- Illumina NGS will have 100mers
- assumption: k mer must overlap the adjoining one  by k-1
### k-mer size

#### Small
- easy too make de bruijn graph
- more likely to overlap
- information loss
- info about repeats lsot
#### Large
- more memory
- more small contigs

## Citation

Prjibelski, A., Antipov, D., Meleshko, D., Lapidus, A., & Korobeynikov, A. (2020). Using SPAdes de novo assembler. Current protocols in bioinformatics, 70(1), e102.

[GitHub](https://github.com/ablab/spades)

[User manual](https://ablab.github.io/spades/)
