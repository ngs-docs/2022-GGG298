---
tags: ggg, ggg2022, ggg298
---


# Syllabus for GGG 298: Tools to support data-intensive research (Winter 2021/2022)

[![hackmd-github-sync-badge](https://hackmd.io/PpgYFrY3SMuGsDsB6VMoMw/badge)](https://hackmd.io/PpgYFrY3SMuGsDsB6VMoMw)


UC Davis

[toc]

## Code of Conduct

Please abide by [my lab's Code of Conduct](http://ivory.idyll.org/lab/coc.html) in this course.

In particular, this is not an intellectual contest, and please realize that we all have plenty of things to learn.

## Course sessions

<!--
[GitHub site for class](https://github.com/ngs-docs/2022-GGG298) - redundant with links below, but more permanent!
-->

### Lab

What: hands-on computational work
When: Wed 9am-noon
Where: Zoom on Canvas

Lab 1 - January 5th, 2022 - [An RNAseq workflow as an starting point](https://hackmd.io/0GPKdxPnQ7KFPoyI_v5Eag?view)

### Discussion

What: read & discuss a paper.
When: Fri 12-1pm
Where: Zoom on Canvas

## Homework

There will be 9 paragraph-length homeworks due, one each week on the reading; they'll be assigned a week in advance and due on Thursday at midnight.

Each week several (1-2) students will be asked to take a lead in preparing for the paper discussion on Fridays. Each student will only be asked to do this once. This counts as 3 homeworks instead of 1, for a total of 10.

## Grading

The course is S/U, and only graded on homework; you need to hand in 7 of the 9 homeworks to pass.

## Office hours

Please sign up here in advance: https://calendly.com/ctitusbrown/30min?back=1&month=2022-01, or contact him via e-mail at ctbrown@ucdavis.edu. The calendly link will provide zoom rooms.

## Instructors

C. Titus Brown (IOR) (<ctbrown@ucdavis.edu>)

## Course description

This course will provide a practical introduction to common tools used in data-intensive research, including the UNIX shell, version control with git, RMarkdown, JupyterLab, and workflows with snakemake. The associated discussion section will connect the lab practicals to foundational concepts in data science, including repeatability/reproducibility, statistics, and publication ethics.

This course is open to all graduate students. No prior computational experience is required or assumed. There will be some minimal overlap with GGG 201(b) topics. All materials will be open to the community and freely available online.

## Attendance and recordings

Lab sessions (on Wednesday) will be recorded and saved for a month, in Canvas. Please ask if you can't find one!

Discussion sessions (on Friday) will not be recorded.

Attendance is expected for both Wednesday and Friday. Please let Dr. Brown know if you can't attend.

## In-class chat via Slack

We'll use Slack for sharing links and commands on both days. Please visit ucdavis.slack.com to create an account, and then join the slack channel `#2022-ggg298`.

## Schedule of lab topics

Wednesdays, 9-noon

These will be lab practicals where we take a solid look at a given piece of technology and work through using it together.

From week 2 onwards, there will be ~20 minutes of videos to watch before we get together. Please watch them by 9:30am. At 9:30, Titus will join the zoom. Class will go 'til noon (with a 10 minute biobreak at 10:30). During this period we'll work through the day's lesson interactively.

<!--
You can view the lab topics here:

https://github.com/ngs-docs/2022-GGG298
-->

Lab 2 - [Introduction to UNIX for Remote Computing](https://hackmd.io/4RgZmv_2QsSLutdHdndKSQ?view).

## Paper discussions

Fridays, noon-1pm.

These will be discussion periods where we explore the concepts and questions introduced by various papers, articles, and blog posts. The topics will mostly be on data science and the practice of science.

### First reading: due Thursday, Jan 6th.

---

Our first paper is [Trust but Verify: How to Leverage Policies, Workflows, and Infrastructure to Ensure Computational Reproducibility in Publication](https://hdsr.mitpress.mit.edu/pub/f0obb31j/release/1), by Willis and Stodden.

Please use [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) to answer the following question by noon on Thursday, January 6th: **Who decides if a paper is sufficiently reproducible?**

In class on Friday we may discuss this question as well: **How do you think "transparency" (as defined in the paper) differs for the experimental and the computational components of biology research? (and what are the implications for reproducibility and/or replicability)?**

---

### Second reading: due Thursday, Jan 13th.

["How does science really work?"](https://www.newyorker.com/magazine/2020/10/05/how-does-science-really-work) - this is a long read, beware, but it's pretty interesting. Feel free to skim it! 

Question for second reading:

What does it mean for how *you* (or *we*) do research that "science was born when philosophical talk was exiled to the pub?" Please be as concrete and practical as you can be in your answer, and provide it to [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, January 13th.

---

### Third reading: due Thursday, Jan 20th.

[Draft blog post: I found a sizeable bug in our published software. Now what?](https://hackmd.io/@ctb/HJNK-2yk_)

Question for third reading: Who should have found this bug, and how would that have worked (e.g. authors, reviewers, journal editors, random Internet people, senior authors' mothers, etc)? Feel free to refer back to your answer in week 1 ;).

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, January 20th.

---

### Fourth reading: due Thursday, Jan 27th.

Please read [Principles of Data Analysis, Stoudt et al., 2021](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008770).

Question for fourth reading: what role does hypothesis testing play in data analysis projects, according to Stoudt et al? And/or what is the proportion of time in a project that is to be spent on hypothesis testing (either your opinion or theirs :)?

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, Jan 27th.


---

### Fifth reading: due Thursday, Feb 3rd.

Read [5-HTTLPR: A pointed review](https://slatestarcodex.com/2019/05/07/5-httlpr-a-pointed-review/).

What reasons (if any) might we have to doubt the conclusions from Border et al? Dig as deep as you wish :). And/or what's the right way to move forward in this area?

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, Feb 3rd.

----

### Sixth reading: due Thursday, Feb 10th.

please read EITHER [The preregistration revolution](https://www.pnas.org/content/115/11/2600) OR [Prediction, pre-specification, and transparency](https://featuredcontent.psychonomic.org/prediction-pre-specification-and-transparency/), and then answer the following question:

What good practices does preregistration support, what good practices does preregistration prevent, and/or what bad practices does preregistration encourage, drawing from your own personal experience and/or preconceptions?

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, February 10th.

(Yes, you can read both papers if you like. :)

----

### Seventh reading: due Thursday, Feb 17th.

Please skim [Functionally Enigmatic Genes: A Case Study of the Brain Ignorome](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0088889), and then answer the following question:

Suppose that you were a program manager for a funding agency with $100m to spend in 5 years, and you wanted to fund ignorome studies (in a field of your choice - doesn't have to be human/neuro). What would your directions to applicants be, and/or how would you set up your granting program?

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, February 17th.

---

### Eighth reading: due Thursday, Feb 24th.

Please read [There is a reproducibility crisis in psychology and we need to act on it](http://deevybee.blogspot.com/2016/03/there-is-reproducibility-crisis-in.html), and then answer the following question:

How might one (or more) of the problems discussed for psychology map onto reproducibility challenges in biology/biomedicine? Are there challenges that are unique to biology as well, or challenges that are in psych but not in bio/biomed?

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, February 24th.

---

### Ninth reading: due Thursday, March 2nd.

Please read [Bring back the bodies](https://mitpressonpubpub.mitpress.mit.edu/pub/zrlj0jqb/release/6) by D'Ignazio and Klein, and then answer the following question:

What is an example of the kind of systems-level "oppression" or "bias" discussed in the article, in the biological/biomedical data science field? Feel free to take inspiration from your personal research or observations, and/or the article itself.

Please provide your answer in [this form](https://docs.google.com/forms/d/e/1FAIpQLSegaKpzD2IaMVQ-dMRQpkw7wb0huhJLtf774O6jkR7GSWFhfg/viewform) by midnight on Thursday, March 2nd.

### Tenth reading: due Thursday, March 9th.

TBD; Probably one of Abeba Birhane's thesis chapters :).
