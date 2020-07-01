# Ancient bacterial genomes reveal a high diversity of _Treponema pallidum_ strains in early modern Europe**Kerttu Majander**, **Saskia Pfrengle**, Judith Neukamm, Arthur Kocher, Louis du Plessis, Marta Pla-Díaz, Natasha Arora, Gülfirde Akgül, Kati Salo, Rachel Schats, Sarah Inskip, Markku Oinonen, Heiki Valk, Martin Malve, Aivar Kriiska, Päivi Onkamo, Fernando González-Candelas, Denise Kühnert, **Johannes Krause**, **Verena J. Schuenemann**

---

This repository contains the data files, configuration files, log files, tree files and scripts necessary to reproduce the molecular clock dating analyses and figures presented in Majander et al. [https://doi.org/10.1101/2020.06.09.142547](https://doi.org/10.1101/2020.06.09.142547). Some of the scripts may need some adjustment depending on the local setup.

---

## Abstract

_Syphilis is a globally re-emerging disease, which has marked European history with a devastating epidemic at the end of the 15th century. Together with non-venereal treponemal diseases, like bejel and yaws, which are found in subtropical and tropical regions, it currently poses a substantial health threat worldwide. The origins and spread of treponemal diseases remain unresolved, including syphilis’ potential introduction into Europe from the Americas. Here, we present the first genetic data from archaeological human remains reflecting a high diversity of Treponema pallidum in early modern Europe. Our study demonstrates that a variety of strains related to both venereal syphilis and yaws-causing T. pallidum subspecies were already present in Northern Europe in the early modern period. We also discovered a previously unknown T. pallidum lineage recovered as a sister group to yaws and bejel-causing lineages. These findings imply a more complex pattern of geographical distribution and etiology of early treponemal epidemics than previously understood._


## Dependencies

- Biopython, numpy
- snp-sites
- RAxML
- BEAST v2.6
- ggplot2, ggtree, treeio, ggsci, ggpubr, coda, cowplot, phytools, phangorn, ape
- [beastio](https://github.com/laduplessis/beastio): Commit #b18caa6


## Data

Input data for the molecular clock dating analyses are in [`data/`](https://github.com/laduplessis/Treponema_pallidum_in_early_modern_Europe/tree/master/data).


## Workflow

The workflow and results are only given for the alignment with genomes mapped to the TPA (Nichols) reference sequence, with recombining and hypervariable genes removed, as well as all sites with >25% missing data. To use a different dataset simply change the input dataset in the workflow (and to avoid confusion all output filenames and directories). 



Define the following datasets for downstream analyses:

- **Dataset A:** Full dataset _(33 genomes)_
- **Dataset B:** Remove genomes without stable placement for finding recombining loci: `KM14-7` (Kampen) _(32 genomes)_
- **Dataset C:** Remove genomes problematic for clock-dating due to passaging: `KM14-7,NIC2,Nichols` _(30 genomes)_
- **Dataset D:** Remove genomes problematic for clock-dating due to unique SNPs: `KM14-7,NIC2,Nichols,94A,94B` _(28 genomes)_
- **Dataset E:** Remove genomes problematic for clock-dating due to underrepresentation: `KKM14-7,NIC2,Nichols,94A,94B,BosniaA` _(27 genomes)_
- **Dataset F:** Remove genomes that could also be problematic for clock-dating due to passaging: `KKM14-7,NIC2,Nichols,94A,94B,BosniaA,Fribourg` _(26 genomes)_


### Create alignments

- Add metadata to alignment files and subsample to create datasets A-F. 
- Use `snp-sites` to get the constant site breakdown for each dataset.

```bash
mkdir results/alignments/

# Dataset A
python scripts/processdata.py -i data/treponema_metadata.csv -a data/Nichols_reference/norecomb_nohypervariable/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -s "name,accession,clade,date_lower,date_upper,date" -o results/alignments/A/ -p fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25

# Dataset B
python scripts/processdata.py -i data/treponema_metadata.csv -a data/Nichols_reference/norecomb_nohypervariable/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -s "name,accession,clade,date_lower,date_upper,date" -o results/alignments/B/ -p fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25 -e KM14-7

# Dataset C
python scripts/processdata.py -i data/treponema_metadata.csv -a data/Nichols_reference/norecomb_nohypervariable/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -s "name,accession,clade,date_lower,date_upper,date" -o results/alignments/C/ -p fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25 -e KM14-7,NIC2,Nichols

# Dataset D
python scripts/processdata.py -i data/treponema_metadata.csv -a data/Nichols_reference/norecomb_nohypervariable/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -s "name,accession,clade,date_lower,date_upper,date" -o results/alignments/D/ -p fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25 -e KM14-7,NIC2,Nichols,94A,94B

# Dataset E
python scripts/processdata.py -i data/treponema_metadata.csv -a data/Nichols_reference/norecomb_nohypervariable/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -s "name,accession,clade,date_lower,date_upper,date" -o results/alignments/E/ -p fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25 -e KM14-7,NIC2,Nichols,94A,94B,BosniaA

# Dataset F
python scripts/processdata.py -i data/treponema_metadata.csv -a data/Nichols_reference/norecomb_nohypervariable/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -s "name,accession,clade,date_lower,date_upper,date" -o results/alignments/F/ -p fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25 -e KM14-7,NIC2,Nichols,94A,94B,BosniaA,Fribourg

# Extract SNP alignments and constant sites
for DATASET in A B C D E F
do 
	snp-sites -o results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas results/alignments/${DATASET}/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas
	snp-sites -C -o results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25_constantsites.csv results/alignments/${DATASET}/fullAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas
	tr ',' ' ' < results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25_constantsites.csv > results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25_constantsites.txt
done

```

- Only use trimmed SNP alignments for subsequent analyses.



### Partition files for RAxML

- Create partition and constant sites files by hand and save in the directory where RAxML will be run, e.g. `results/RAxML/A/` for dataset A. 

Partition file contents for Dataset A:

```
[asc~../../alignments/A/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25_constantsites.txt],ASC_DNA, p1=1-1631

```

Partition files for other datasets only differ in the filename and the number of sites.


### Build trees in RAxML

- Use RAxML to build genetic distance trees (run from the directory where RAxML output should be stored, e.g. `results/RAxML/A/`).
- After RAxML finishes midpoint root trees in FigTree and export as displayed with NEXUS block. 

```bash

# Dataset A
raxmlHPC-PTHREADS-AVX -T 2 -m ASC_GTRGAMMA -f a -x 12345 -p 12345 -N autoMRE -s ../../alignments/A/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas --asc-corr=stamatakis -q partition_snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.txt -n snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.tree

# Dataset B
raxmlHPC-PTHREADS-AVX -T 2 -m ASC_GTRGAMMA -f a -x 12345 -p 12345 -N autoMRE -s ../../alignments/B/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas --asc-corr=stamatakis -q partition_snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.txt -n snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.tree

# Dataset C
raxmlHPC-PTHREADS-AVX -T 2 -m ASC_GTRGAMMA -f a -x 12345 -p 12345 -N autoMRE -s ../../alignments/C/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas --asc-corr=stamatakis -q partition_snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.txt -n snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.tree

# Dataset D
raxmlHPC-PTHREADS-AVX -T 2 -m ASC_GTRGAMMA -f a -x 12345 -p 12345 -N autoMRE -s ../../alignments/D/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas --asc-corr=stamatakis -q partition_snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.txt -n snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.tree

# Dataset E 
raxmlHPC-PTHREADS-AVX -T 2 -m ASC_GTRGAMMA -f a -x 12345 -p 12345 -N autoMRE -s ../../alignments/E/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas --asc-corr=stamatakis -q partition_snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.txt -n snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.tree

# Dataset F
raxmlHPC-PTHREADS-AVX -T 2 -m ASC_GTRGAMMA -f a -x 12345 -p 12345 -N autoMRE -s ../../alignments/F/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas --asc-corr=stamatakis -q partition_snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.txt -n snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.tree

```

---



### BEAST2 analyses

- Create NEXUS files with SNP sequences, sampling dates and tip date priors.

```bash
for DATASET in B C D E F
do 

	# Narrow uniform priors
	python scripts/fasta2nexus.py -i results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -o results/alignments/${DATASET}/narrow -d 5 -l 3 -u 4

	# Normally distributed priors
	python scripts/fasta2nexus.py -i results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -o results/alignments/${DATASET}/normal -d 5 -l 3 -u 4 -n

	# Wide uniform priors 
	python scripts/fasta2nexus.py -i results/alignments/${DATASET}/snpAlignment_cov2_cleaned_excluded_real_noRecomb_genesTrimmed_trimmed_0.25.fas -o results/alignments/${DATASET}/wide -d 5 -l 3 -u 4 -L 1000 -U 2016 -w

done

```

- The NEXUS files above can be dragged into BEAUti v2.6 to immediately load the alignment and set tip date priors. 
- Create the XML files in BEAUti v2.6 and adjust by hand (only the XML files for dataset D are provided on the repository).
- Run on remote server using commands below (from the directory where XML files are stored, e.g. `results/beast/D/`).
- Build MCC trees.

```bash 
# On remote server (from directory with XML files)
mkdir output 

ls *.xml | parallel --delay 1 --jobs 30% --results outdir -I% --max-args 1 ~/BEASTv2.6.0/bin/beast -overwrite -seed 127 % & 		

cd output
mkdir mcctrees

for i in `ls *.trees | cut -f 1,2,3,4 -d "."`; do ~/BEASTv2.6.0/bin/treeannotator -burnin 30 ${i}.trees mcctrees/${i}.MCC.tree; done

```


### Bayesian Date Randomisation Test

- Create config files in `results/beast/shuffleddates/config/` by hand. 
- Run Python scripts to produce XML files (only the XML files for dataset D are provided on the repository). 
- Run on remote server using commands below (from the directory where XML files are stored, e.g. `results/beast/shuffleddates/D/`).

```
# On local (from project root)
python scripts/MakeBEASTXML.py -i results/beast/shuffleddates/config/D/


# On remote server (from directory with XML files)
mkdir output

ls *R{0..50}.xml | parallel --delay 1 --jobs 75% --results outdir -I% --max-args 1 ~/BEASTv2.6.0/bin/beast -overwrite -seed 127 % & 		

```

---

## Reports

### Temporal signal by root-to-tip vs sampling date regression

Follow `reports/TemporalSignal.Rmd`


### Manuscript figures











