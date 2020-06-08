# Demo of metagenome Atlas

Metagenome-Atlas is a easy-to-use metagenomic pipeline based on snakemake

It handels all steps from QC, Assembly, Binning, to Annotation.

![scheme of workflow](images/ATLAS_scheme.jpg?raw=true)



# Quick Start Demo

Three commands to start analysing your metagenome data:
```
    conda install -y -c bioconda -c conda-forge metagenome-atlas
    atlas init --db-dir databases path/to/fastq/files
    atlas run all
```
All databases and dependencies are installed on the fly. Atlas is based on snakemake which allows to sheddule parts of the workflow to a cluster. 

Have a Look
[![asciicast](https://asciinema.org/a/337467.svg)](https://asciinema.org/a/337467)


You want to run these three commands on the [example data](https://github.com/metagenome-atlas/atlas/exmple_data).

Atlas should be run on a _linux_ sytem, with enough memory (min ~50GB but assembly usually requires 250GB).
The only dependency is the _conda package manager_, which can easy be installed with [anaconda](http://anaconda.org/).






# Get Started
If you have more time, then we recommend you to create a conda environment for atlas to avoid any conflicts of versions.

```
    conda create -y -n atlasenv
    source activate atlasenv
    conda install -y -c bioconda -c conda-forge metagenome-atlas
```

And you can run atlas. All other dependencies are installed in specific environments during the run of the pipeline.

We recommend you configure atlas according to your needs.
  - check the `samples.tsv`
  - edit the `config.yaml`
  - run atlas on any [cluster system](https://metagenome-atlas.readthedocs.io/en/latest/usage/cluster.html)


For local execution we have also a [docker container](https://metagenome-atlas.readthedocs.io/en/latest/usage/getting_started.html#c-use-docker-container)

[Tweet about it](https://twitter.com/intent/tweet?text=%23metagenomeAtlas%20%3A%20Three%20commands%20to%20start%20analyzing%20your%20data%2C%20from%20%40SilasKieser%20at%20%23SIBDays20%20https%3A%2F%2Fdoi.org%2F10.1101%2F737528%20)

# Cite

We have a BioRxiv preprint please cite:

ATLAS: a Snakemake workflow for assembly, annotation, and genomic binning of metagenome sequence data
Silas Kieser, Joseph Brown, Evgeny M Zdobnov, Mirko Trajkovski, Lee Ann McCue
bioRxiv 737528; doi: https://doi.org/10.1101/737528
