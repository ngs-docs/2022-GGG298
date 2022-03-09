---
tags: ggg, ggg2022, ggg298
---
# GGG 298, Mar 2 2022 - Week 9 - sourmash again: github and HPC practice!

[![hackmd-github-sync-badge](https://hackmd.io/w_PK0JzzTtGPRJGd7MrLRg/badge)](https://hackmd.io/w_PK0JzzTtGPRJGd7MrLRg)

[(Permanent link)](https://github.com/ngs-docs/2022-GGG298/tree/main/lab-9-sourmash-2/README.md)

[toc]

## Overview and Goals

In week 6, we [learned how to use git and github to put our code under version control](https://hackmd.io/kJX0JtN0RtWwaJj8QfvTgw?view) and make it available to others. In week 7, we [learned how to run analyses on the farm HPC cluster](https://hackmd.io/7wL_dBfPRM-csn2V0CQgCA?view).

Our goals for today are to take the sourmash project from [week 5](https://hackmd.io/qvTaFZjpRTqLkjMxKHBqqw?view) and do the following:

1. create a git repo for it.
2. make that git repo available to others on github.
3. create slurm sbatch scripts so that we can run the sourmash workflow on farm's compute nodes.

By the end of today, everyone will have run someone else's sourmash snakemake workflow on farm!

Our stretch goal will be to make this into a binder so that anyone, anywhere can run it, even without access to farm :).

## Up front details

right conda environment
where the source Snakefile is
where the genomes are (?)

## Step: Create a git repository on farm

* make a new directory for this project
* change directory into it
* download the Snakefile like so: `curl -L -O https://raw.githubusercontent.com/ngs-docs/2022-GGG298/main/lab-9-sourmash-2/Snakefile`
* run `git init` to create a git repository
* set the default branch name to main with `git branch -m main`

At the end of this, `git status` should show output similar to the following:
```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Snakefile

nothing added to commit but untracked files present (use "git add" to track)
```

## Step: Add/commit files to the git repository

* add the Snakefile into the git tracking system
* commit the new file

At the end of this, `git status` should show:
```
On branch main
nothing to commit, working tree clean
```
and `ls Snakefile` should show that you have Snakefile in the current directory.

## Step: Create a github repository and link it to the git repo on farm

* Go to [github.com/new](https://github.com/new) and create a new repository with no files created in it. Be sure to make it public.
* Read the instructions for pushing an existing repository from the command line, and execute them on farm.

`git status` should look like this:
```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
and you should see `Snakefile` in your github view when you reload.

## Step: verify github with a new clone

* clone your repo to a new directory on farm. Note that you can use `git clone <url> ~/new-dir-name` so that it uses a non-default directory name.
* change to that directory and run snakemake

The workflow should complete successfully.

## Step: have someone else clone the github repo and run the workflow

Have someone else clone your github repo and do the above!

## Step: create a slurm sbatch script to run your workflow

Clean out your directory of generated files with `snakemake --delete-all-output`.

Create a slurm sbatch script based on [this example](https://hackmd.io/7wL_dBfPRM-csn2V0CQgCA?view#A-stock-sbatch-script-that-includes-activating-a-conda-environment)

Edit it to activate the right conda environment and run snakemake with `-n`.
Test it at the command line with `bash <script name>`.
Edit out the `-n`, and run it with sbatch.
Verify that it worked by looking at the logs and/or looking for the output files.

## Step: update your github repo with your script

Add the script to your git repo, commit the changes, and push to github.

## Step: have someone else use the new sbatch script

Have someone else `git clone` your repo (if they haven't before) or `git pull` the updates from your repo (if they already have a copy).

Look over the script to make sure it should work with this user's settings.

Edit the script to run`snakemake -n` and see if it works with `bash <scriptname>`.

Edit the script to remove `-n` and run it via sbatch.

Verify the results.

Declare victory!
