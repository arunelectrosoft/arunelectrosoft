---
title: Repo Basics
layout: post
categories: DigitalLibrary
published: false
---
# Repo Tool Basics

Google created a repo tool to simplify working with several open source git repositories. 
[Android Source code tools](https://source.android.com/setup/develop)
### Source Tools used for Android. 
- [ ] Repo, Git 
- [ ] Gerrit - a web-based code review system 
- [ ] Android code search (https://cs.android.com/) 
- [ ] Android code search and Referencing system (https://developers.google.com/code-search) 

## Repo Tutorial:
Bootlin website, provided good training on yocto, android and other embedded topics. 
[Android and repo tutorial](https://bootlin.com/doc/legacy/android/android-slides.pdf)


What is Repo ?

> Repo is a python script based tool created by Google to manage 
> the complexities of so many Git repositories.


Repo Manifest XML format ?
Repo tool work with the XML Manifest input file. 
A repo manifest describes the structure of a repo client.

> repo manifest is explained in below link.
[Repo Manifest Format](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/manifest-format.md)

Using Repo Tool ?
Repo command reference is given in below android source code repository.
[Repo Command Reference](https://source.android.com/setup/develop/repo)

Repo Help Option?
Inorder to find the overall supported options, 

$repo help
> Provides supported options in the repo tool

$repo help command
> Provides supported option for current **command**