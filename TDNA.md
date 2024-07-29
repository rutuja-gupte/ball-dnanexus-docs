#TDNAscan

Author: Rutuja Gupte  

These are the important bits from their guides. The complete guide is linked at the bottom.

## Downloads

### Dependencies

#### BWA
```
git clone https://github.com/lh3/bwa.git
cd bwa; make
export PATH="/home/dnanexus/bwa:$PATH"
cd ..
```

#### Samtools
```
sudo apt install samtools
```

#### Python

This should already be installed but we just need an extra package to make the code work
```
sudo apt install python-is-python3
```


### Actual software

```
git clone "https://github.com/BCH-RC/TDNAscan"
```

## Test it!
```
cd TDNAscan/
python tdnascan.py -1 example/mt4_chr1_20x_mut_tdna_1.fq -2 example/mt4_chr1_20x_mut_tdna_2.fq -t example/t-dna_elison.fa -g example/mt4_chr1_2Mb.fa -p tdna
```

## Use it!

```
python tdnascan.py -1 R1.fastq.gz -2 R2.fastq.gz -t plasmid.fasta -g ref.fasta -p tdna_folder -@ 16 > file.out 2>&1 &
```

-@ for threads

## Citation

Sun, Liang, et al. ["TDNAscan: A Software to Identify Complete and Truncated T-DNA Insertions."](https://www.frontiersin.org/journals/genetics/articles/10.3389/fgene.2019.00685/full) Frontiers in Genetics (2019),doi: 10.3389/fgene.2019.00685

[GitHub and instructions](https://github.com/BCH-RC/TDNAscan)