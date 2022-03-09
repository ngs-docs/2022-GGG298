---
tags: ggg, ggg2022, ggg298
---
# GGG 298, Mar 9, 2022 - Week 10 - a smorgasbord of miscellany (R and RMarkdown)

[![hackmd-github-sync-badge](https://hackmd.io/SJxLcVlTTRuY43gB7j_CIw/badge)](https://hackmd.io/SJxLcVlTTRuY43gB7j_CIw)

[(Permanent location)](https://github.com/ngs-docs/2022-GGG298/blob/main/lab-10-rmarkdown/README.md)


## sourmash

We'll run through the solution to [week 9](https://hackmd.io/w_PK0JzzTtGPRJGd7MrLRg?view)! but maybe on my laptop, since farm is slow today.

## RMarkdown 

### Open an environment in binder

Note: this requires github login.

[![Binder](https://aws-uswest2-binder.pangeo.io/badge_logo.svg)](https://aws-uswest2-binder.pangeo.io/v2/gh/nih-cfde/rnaseq-in-the-cloud/stable?urlpath=rstudio)

(If it tells you you already have a server running, you can go to `https://hub.aws-uswest2-binder.pangeo.io/hub/` and click 'stop server'.)

### Work with an existing RMarkdown file

Open `rnaseq-workflow.Rmd`

Go up to the 'Knit' pulldown and select "Knit to HTML". Say "yes" when it asks to install stuff.

Now wait a bit :).

Let's explore the HTML, and then also the Rmd file.

### Creating your own Rmd file.

Go to 'File...' and then 'New file...' and then 'R Markdown file'.

Name it 'class'.

Save it, and name it 'class.Rmd'.

Now, knit it! And let's look at the underlying source etc.

### What is Markdown?

Markdown is a [lightweight markup language](https://en.wikipedia.org/wiki/Markdown), which basically means it's a way of writing nicely formatted text that can include bold, italic, and links, while also being readable by humans without that formatting.

I've used it for all of my teaching this year (and many previous years!); both GitHub and hackmd.io let me edit and display it.

**(Here will be a brief hackmd.io demonstration)**

### How do 'snakemake' and R interact in workflows?

Generally I use snakemake to compute a bunch of stuff, and then use R or Python to analyze the results.

RStudio and Jupyter Notebook/JupyterLab are two different visual analysis environments that support interactive data exploration as well as interactive construction of reports.

The way we used RMarkdown in the rnaseq workflow binder is pretty typical:
* use snakemake to run a big pipeline on your raw data; produce summary files (CSV, TSV)
* use a graphical Python or R environment to explore the results
* "save" your results from interactive exploration into one or more notebooks or R Markdown documents.

The only confusing thing in this particular is that we saved the necessary output files from the snakemake workflow in the binder, so you don't _have_ to run snakemake in order to knit. But in most cases you would do them in order.

**(Here will be a brief demo of Jupyter Notebook from [this repo](https://github.com/ctb/2022-ggg-201b-assembly-collapse) from GGG 201(b)'s assembly collapse project)**

(See a final notebook from GGG 201(b) [here](https://github.com/ngs-docs/2022-GGG201b-lab/blob/main/lab-9-assembly-collapse.ipynb).)

## R and RMarkdown on farm via command-line


(This may not happen today, since farm is being really slow!)

As long as you don't want care about both:

(a) being able to install your own software with conda

(b) having interactive access to RStudio

on farm, you can use farm to install all your R packages in conda and run RMarkdown etc.

To try it out with the RNAseq workflow, first you'll need the repository:

```
cd ~/
git clone https://github.com/nih-cfde/rnaseq-in-the-cloud/
cd rnaseq-in-the-cloud
```

(optional) At this point you could run:
```
snakemake -j 2 --use-conda
```

To install all the R packages needed for RMarkdown, you need to do:
```
mamba env create -f binder/environment.yml -n rmd
conda activate rmd
```

and then
[here](https://github.com/ngs-docs/2020-ggg-201b-rnaseq/blob/latest/knit-Rmd.R) is an R script that you can run at the command line to do the knit. 
```
curl -L -O https://raw.githubusercontent.com/ngs-docs/2020-ggg-201b-rnaseq/latest/knit-Rmd.R
Rscript knit-Rmd.R
```

**(CTB will demo on his laptop)**

The problem with this is that you don't have convenient access to your data along with a viz environment. There are some technically tricky ways to make that work... read on.

## RStudio and JupyterLab on farm via ssh tunnelling

(This may not happen today, since farm is being really slow!)

Log into farm, then run:
```
srun --nodes=1 -p high2 -t 1:00:00 -c 4 --mem 6GB --pty /bin/bash
```
and now execute:
```
module load rstudio-server
```
and then
```
rserver-farm
```

It will then direct you to execute some more instructions that are Linux/Mac OS X specific. More in person.

## More R and R Markdown resources

An old lesson from GGG 298 last year is [here](https://github.com/ngs-docs/2021-GGG298/tree/latest/Week11-Rmarkdown_for_reports_documentation_and_beyond).

The [Software Carpentry tutorial](https://swcarpentry.github.io/r-novice-gapminder/15-knitr-markdown/) is pretty good!