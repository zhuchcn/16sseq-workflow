## Description

This is a 16S amplicon sequencing data processing workflow. The fastq_multx is used for demultiplexing and dada2 is used for ASV picking. This workflow takes about 2-3 hours to run on a Macbook pro with i7 and 16GB memory.

## Setting up

Make sure conda and R is installed in your computer.

+ Create conda enrironment

```
conda env create -f environment.yml
```

+ Activate enviroment

```
conda activate 16sseq-workflow
```

+ Add bash_kernel
```
python -m bash_kernel.install
```

## workflow

This workflow has two parts. The demutiplexing is done in jupyter notebook with a bash kernel, and dada2 is ran in R. We chose jupyter notebook becuase it is an excellent interactive environment for reproducible research with a variety of programming languages. And here we used the base kernel to run different tools and bash scripts/commands.

Type the following command to start the demultiplex workflow.

```
jupyter notebook demultiplex.ipynb
```

After demultiplex, open the dada2_workflow.Rmd to run dada2 for ASV picking.