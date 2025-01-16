---
title: Managing Notes with Git
date: 2025-01-12
tags:
  - seed
---
### Github

I have spent time working with git in other projects. Mostly those projects are related to little scripts here and there to optimize my work or to backup my personal system .config files. Admittedly however, I have never really worked on any major projects or contributed to any major projects (something I would like to explore). and most of the challenges I have encountered in managing my personal notes is likely related to a general lack of knowledge of git. I am likely spoiled by non-versioned, set-it-and-forget-it sync systems like icloud and obsidian sync. 

Currently, my workflow with git and this blog looks like this:

![[git notes workflow.png]]
I have had some challenges with starting notes on one system, moving locations, then trying to continue my work on another system. 

Initially, I had a large filebase that was connected to an obsidian sync account. The requirements of [Quartz 4](https://quartz.jzhao.xyz/authoring-content) require all notes to go into the `/content` directory. This is fine, I have local copies of the repository in `~/git/quartz`. I can either just move my obsidian sync directory into the specified directory or create a symlink and forget about it.. well, actually no. My vault has directories that I don't really want to share. A big part of why I like sync is because i like to use it on my phone as well. Throughout the day, I will add notes on things that are on my mind. They are typically ephemeral but may hold relevance later on e.g. I recently switched banks (which was hugely tedious and I am not sure how an elderly person or someone who can barely run a computer could manage this in a reasonable timeframe). Herein I kept a master note with my basic account information to add to each individual item that was hitting my ledger at that bank which included autopays, mortgage, memberships that don't accept credit cards (looking at you un-named gym membership that doesn't believe in using credit cards for fear of disputes). These are obviously the types of things that one would not want to push to github and publish on a site. Fair enough, I will add them to my `.gitignore or exempt config`. I had an odd issue with quartz (again stemming from lack of git knowledge), which grabbed them anyways and began publishing them, often as blank notes, but the headings still remained. 

Instead of spending hours troubleshooting, I simply split the vault between private things and public things. In my mind this has diminished my utility in using obsidian on devices like my phone. I couldn't idly edit my posts or begin new ideas (this is lazy, I could create new ideas and move them later) from a mobile device using obsidian. 

### Sync

Quartz 4 comes with built in functionality to sync files to established git repository via `npx quartz sync`. This certainly populates my `/content` directory in my github repo, but the commits are non-verbose. I supposed this could be changed after the fact by amending the commit, but this would be an extra step instead of multiple simple notated commits. 

I have not currently reviewed the code for the sync functionality. I suppose for now, I will simply use commits. My `git remote upstream` is still connected to the original quartz repo to attempt capture of core framework updates. If update logic for the platform is contained with `npx quartz sync` then I will simply occasionally do the suggest npx sync and keep notation separate within individual commits. 