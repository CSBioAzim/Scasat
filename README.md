# ScAsAT (Single cell ATAC-seq analysis tool)
ScAsAT (single cell ATAC-seq analysis tool) is a complete pipeline to process scATAC-seq data with simple steps. The pipeline is developed in a Jupyter notebook environment that holds the executable code along with the necessary description and results. For the initial sequence processing steps, the pipeline uses a number of well-known tools which it executes from a python environment for each of the fastq files. While functions for the data analysis part are mostly written in R.

## Prerequisites:

You have to have the following tools installed in the machine where you are running ScAsAT
1. [samtools](http://www.htslib.org)
2. [bedtools](http://bedtools.readthedocs.io/en/latest/)
3. [macs2](https://github.com/taoliu/MACS)

If you are using jupyter from anaconda installation then you can install the tools with the following command
* samtools: conda install -c bioconda samtools
* bedtools: conda install -c bioconda bedtools 
* macs2: conda install -c bioconda macs2 (please note that macs2 only runs on python2.7 so you have to create a python2.7 environment if you are using python3

## Application:##
Two notebooks to process two different datasets are provided here. 

### Deconvolute cell types ###

The objective of this experiment was to deconvolute the different cells from a complex mixture of cells.

__Experimental design:__

Two classic oesophageal adenocarcinoma (OAC) cell lines, OE19, OE33 and one non-neoplastic HET1A cell line were mixed together to create the complex mixture of population. These three cell lines were mixed at equal proportion to create this mixture. Single cell ATAC-seq was then performed on those two replicates by loading on two separate C1 fluidigm chips using a $96$ well plate integrated fluidic circuit (IFC) and sequenced on an Illumina NextSeq. This experimental figure is shown in the figure below

<img src="ExperimentalDesign.png" alt="Experimental Desing" style="width: 500px;"/>

### Public datatset: ###
ScAsAT is then applied to process and analyze the public dataset by [_Buenrostro et. al._](https://www.nature.com/articles/nature14590)
