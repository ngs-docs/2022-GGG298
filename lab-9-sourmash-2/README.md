---
tags: ggg, ggg2022, ggg298
---
# GGG 298, Feb 2022 - Week 9 - sourmash again: github and HPC practice!

[(Permanent link)](https://github.com/ngs-docs/2022-GGG298/tree/main/lab-9-sourmash-2/README.md)

## Overview and Goals

In week 6, we [learned how to use git and github to put our code under version control](https://hackmd.io/kJX0JtN0RtWwaJj8QfvTgw?view) and make it available to others. In week 7, we [learned how to run analyses on the farm HPC cluster](https://hackmd.io/7wL_dBfPRM-csn2V0CQgCA?view).

Our goals for today are to take the sourmash project from [week 5](https://hackmd.io/qvTaFZjpRTqLkjMxKHBqqw?view) and do the following:

1. create a git repo for it.
2. make that git repo available to others on github.
3. create slurm sbatch scripts so that we can run the sourmash workflow on farm's compute nodes.

By the end of today, everyone will have run someone else's sourmash snakemake workflow on farm!

Our stretch goal will be to make this into a binder so that anyone, anywhere can run it, even without access to farm :).

## CTB TODO

put a copy of the final Snakefile from week 5 on farm somewhere
break down the steps that we need to do, and link into the appropriate week 6 and 7 materials.
look at week 8 to see if there's anything there we should do.
create a public github repo that contains the right stuff so that everyone can succeed at running, even if their group doesn't finish.
