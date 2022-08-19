---
title: "Getting Started With Hugo"
date: 2022-08-01T12:39:45-05:00
draft: true
---

# Getting familiar with Hugo

## Introduction

As part of the learning path, you will need to have hands-on experiencie with Git/Github.
Hugo is a popular site generator and we plan to use it to learn some `git` operations and real-world 
use cases.


### Day 1. Installation

1. Install hugo following the proper documentation https://gohugo.io/getting-started/installing/
2. Start a hugo server locally

    ```
    git clone https://github.com/gohugoio/hugoDocs.git
    cd hugoDocs
    hugo server
    ```
3. Read the documentation and get familiar with basic commands, e.g., create a new post, add content and build static files.

### Day 2. Add a new post and create a Pull Request

0. Clone this public repo `git clone https://github.com/dennysreg/datumbucle.git`
1. `cd datumbucle`
2. Create a new branch `git checkout -b dev/day-2-create-my-first-post-<your-name>`
3. Create a new post `hugo new post/my-first-post-<your-name>`
4. Edit the `content/post/my-first-post-<your-name>.md`
5. Start hugo server including the drafts `hugo server -D` and verify everything looks as expected.
6. Stage your changes `git add .`
7. Create a commit `git commit -m 'my first post'`
8. Push your branch to origin `git push --set-upstream origin dev/day-2-create-my-first-post-<your-name>`
9. Go to [github](https://github.com/dennysreg/datumbucle) and create a Pull Request
