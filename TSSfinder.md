# TSSFinder

## Download 

```
wget https://github.com/tssfinder/tssfinder.github.io/releases/download/v1.0.0/tssfinder.v1.0.0.zip
unzip tssfinder.v1.0.0.zip
sudo apt install python-is-python3
pip3 install click==6.7
pip3 install pandas
pip3 install biopython
export PATH="/home/dnanexus/tssfinder:$PATH"
export PATH="/home/dnanexus/tssfinder/bin/cli:$PATH"
export PATH="/home/dnanexus/tssfinder/docker-bin:$PATH"
```

If you want to try training the models, download the training sets here.

```
wget https://github.com/tssfinder/tssfinder.github.io/releases/download/v1.0.0/training_sets.zip
unzip training_sets.zip
```

If you just want the pre-trained models for use, download the models here.

```
wget https://github.com/tssfinder/tssfinder.github.io/releases/download/v1.0.0/tssfinder-models.zip
unzip tssfinder-models.zip
```

Training syntax

```
tssfinder-train --model testing_stuff --start athaliana/athaliana.dataset1.start.bed --tata athaliana/athaliana.tata.bed --tss athaliana/athaliana.dataset1.tss.bed --genome athaliana/athaliana.tair10.fa > testing_stuff.out 2>&1 &
```

Prediction syntax

```
mkdir test_out
tssfinder.py --model models/athaliana/athaliana.1/ --start athaliana/athaliana.dataset0.start.bed --genome athaliana/athaliana.tair10.fa --output test_out > test_out.out 2>&1 &
```

## Citation

Mauro de Medeiros Oliveira, Igor Bonadio, Alicia Lie de Melo, Glaucia Mendes Souza, Alan Mitchell Durham, TSSFinder—fast and accurate ab initio prediction of the core promoter in eukaryotic genomes, Briefings in Bioinformatics, Volume 22, Issue 6, November 2021, bbab198, https://doi.org/10.1093/bib/bbab198