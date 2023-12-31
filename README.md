# About the course

Today it is possible to obtain genome-wide transcriptome data from single cells using high-throughput sequencing (scRNA-seq). The main advantage of scRNA-seq is that the cellular resolution and the genome wide scope makes it possible to address issues that are intractable using other methods, e.g. bulk RNA-seq or single-cell RT-qPCR. However, to analyze scRNA-seq data, novel methods are required and some of the underlying assumptions for the methods developed for bulk RNA-seq experiments are no longer valid.

In this course we will discuss some of the questions that can be addressed using scRNA-seq as well as the available computational and statistical methods avialable. The course is taught through the University of Cambridge <a href="http://training.csx.cam.ac.uk/bioinformatics/" target="blank">Bioinformatics training unit</a>, but the material found on these pages is meant to be used for anyone interested in learning about computational analysis of scRNA-seq data. The course is taught twice per year and the material here is updated prior to each event.

The number of computational tools is increasing rapidly and we are doing our best to keep up to date with what is available. One of the main constraints for this course is that we would like to use tools that are implemented in R and that run reasonably fast. Moreover, we will also confess to being somewhat biased towards methods that have been developed either by us or by our friends and colleagues. 

**:information_source: Note that currently (first half of 2022) the course is being actively updated, and the content will change significantly without further notice.**

## Web page

| HOMEPAGE | DATA |
| ------------- | ------------- |
| https://www.singlecellcourse.org  | https://singlecellcourse.cog.sanger.ac.uk/index.html?shared=data/  |

## Video

This video was recorded during the course (2 days) in May 2019. **The content will not match the updates that happened in 2021. New videos will be uploaded when available.**

| Day | Link | Description |
| ------------- | ------------- | ------------- |
| **#1** | [https://www.youtube.com/watch?v=thHgPqQpkE4](https://www.youtube.com/watch?v=thHgPqQpkE4&t=2738s) | The lecture **starts at 45:38** of video. Topics: About the course, Introduction to Single-Cell RNA-seq, Processing Raw scRNA-Seq Sequencing Data, Introduction to R/Bioconductor, scRNA-seq Analysis with Bioconductor, Basic Quality Control (QC) and Exploration of scRNA-seq Datasets. |
| **#2** | [https://www.youtube.com/watch?v=7dQ_pleDO2Y](https://www.youtube.com/watch?v=7dQ_pleDO2Y&t=3436s) | The lecture **starts at 57:16** of video. Topics: Biological Analysis, Single cell RNA-seq analysis using Seurat, scRNA-seq Dataset Integration, Resources |


## Registration  

Please follow this link and register for the __"Analysis of single cell RNA-seq data"__ course:
<a href="http://training.csx.cam.ac.uk/bioinformatics/search" target="blank">http://training.csx.cam.ac.uk/bioinformatics/search</a>

## GitHub :octocat:

- Updated repository: https://github.com/cellgeni/scRNA.seq.course
- Original course (outdated) https://github.com/hemberg-lab/scRNA.seq.course


## Docker image

[![Docker Repository on Quay](https://img.shields.io/badge/container-quay.io-brightgreen)](https://quay.io/repository/cellgeni/scrna-seq-course?tab=tags)

The course can be reproduced without any package installation by running the course docker image which contains all the required packages.

### Run the image
Make sure Docker is installed on your system. If not, please follow [these instructions](https://docs.docker.com/engine/installation/). To run the course docker image use [the `latest` version](https://quay.io/repository/cellgeni/scrna-seq-course?tab=tags). 

You can pass the environment variable `JUPYTER_TOKEN` to the container to set a specific password or you can let jupyter generate a random access token:

```
docker run -p 8888:8888 -e JUPYTER_TOKEN=password quay.io/cellgeni/scrna-seq-course:latest
```

Then follow the instructions provided, e.g.:
```
To access the notebook, open this file in a browser:
    file:///home/jovyan/.local/share/jupyter/runtime/nbserver-6-open.html
Or copy and paste one of these URLs:
    http://(a9ee1aad5398 or 127.0.0.1):8888/?token=22debff49d9aae3c50e6b0b5241b47eefb1b8f883fcb7e6d
```

A Jupyter session will be open in a web browser (we recommend Chrome).

#### Windows users

On Windows operating system the IP address of the container can be different from `127.0.0.1` (`localhost`). To find the IP address please run:
```
docker-machine ip default
```

### Download data/other files

Please click on `New -> Terminal`. In the new terminal window please run:
```
source <(curl -s https://raw.githubusercontent.com/cellgeni/scRNA.seq.course/master/setup.sh)
```

If you want to download data files outside of Docker image you can still use the `poststart.sh` script from this repository but you will need to install [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-bundle.html) on your computer.

Alternatively, you can browse and download the files in you web-browser by visiting [this link](https://singlecellcourse.cog.sanger.ac.uk/index.html?shared=data/).

### RStudio

Now go back to Jupyter browser tab and change word `tree` in the url to `rstudio`. RStudio server will open with all of the course files, software and the data folder available.


### Container's base software
```bash
$ lsb_release -d
Description:    Ubuntu 20.04.2 LTS

$ R --version
R version 4.2.1 (2022-06-23) -- "Funny-Looking Kid"

$ rstudio-server version
2022.07.0+548 (Spotted Wakerobin) for Ubuntu Bionic
```

## Manual installation 

If you are not using the docker version of the course, then to be able to run all code chunks of the course you need to clone or download the [course GitHub repository](https://github.com/cellgeni/scRNA.seq.course) and start an R session in the `course_files` folder. The course files can also be retrieved using the `setup.sh` from this repository if you're working on Unix/Mac. You will also need to install all required R/python packages manually. Alternatively, you can just install packages listed in a chapter of interest.

## License
All of the course material is licensed under <b>GPL-3</b>. Anyone is welcome to go through the material in order to learn about analysis of scRNA-seq data. If you plan to use the material for your own teaching, we would appreciate if you tell us about it in addition to providing a suitable citation.

## Prerequisites

The course is intended for those who have basic familiarity with Unix and the R scripting language.

We will also assume that you are familiar with mapping and analysing bulk RNA-seq data as well as with the commonly available computational tools.

We recommend attending the [Introduction to RNA-seq and ChIP-seq data analysis](http://training.csx.cam.ac.uk/bioinformatics/search) or the [Analysis of high-throughput sequencing data with Bioconductor](http://training.csx.cam.ac.uk/bioinformatics/search) before attending this course.

## Citation

Please cite [Tutorial: guidelines for the computational analysis of single-cell RNA sequencing data](https://www.nature.com/articles/s41596-020-00409-w)
> Andrews, T.S., Kiselev, V.Y., McCarthy, D. et al. Tutorial: guidelines for the computational analysis of single-cell RNA sequencing data. Nat Protoc 16, 1–9 (2021). https://doi.org/10.1038/s41596-020-00409-w

## Contact

If you have any __comments__, __questions__ or __suggestions__ about the material, please contact <a href="mailto:predeus@gmail.com">Alexander Predeus</a> or <a href="mailto:hm533@cam.ac.uk">Hugo Tavares</a>.
