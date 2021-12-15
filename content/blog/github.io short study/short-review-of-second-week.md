---
title: short review of second week
date: 2021-12-15 14:12:10
category: github.io short study
thumbnail: { thumbnailSrc }
draft: false
---
##### This weeks goal

- [x] write a workflow for auto-deploying -> changed to write a shell script for auto-deploying.
- [ ] study markdown syntax
- [ ] analyze blog features

#### Writing a workflow for auto-deploying  
##### ~ Monday  
I've tried many of them which came up while searching. But errors occurred while installing npm(`npm install`). So I changed the way for auto-deploying. I wrote a shell script! And this is it.
```shell
#!/bin/bash
git add .
git commit -m "$(date)"
git push origin master
npm run deploy
git checkout gh-pages
git pull origin gh-pages
git add .
git commit -m "$(date)"
git push origin gh-pages
git checkout master
npm install
```
It pushes source codes to branch master with commit message(date) and pushes deployed files to branch gh-pages.  

##### Tuesday
I peeped in Hyojekim\_space and saw `nodejs version occurred errors`. So I simply added code of setting nodejs version in a workflow. And it did work!  
It worked but it pushed the deployed files not on branch gh-pages, on master. So I went to Github pages, read readme files, and found that it pushes the deployed files on branch master in default.  

#### Changed profile images and site tab images.
I've changed profile images and site tab images.  
These images are found in the `content/assets` directory. 

file name | before | after
--------- | ------- | -----
profile.png |![image](https://user-images.githubusercontent.com/91731260/146139180-9bc2fcf3-e51c-49a9-85dc-b2f4c5168f19.png)|![profile](https://user-images.githubusercontent.com/91731260/146138849-00c2af82-4f44-4f42-8bdc-b2216e16913c.png)  
felog.png|![image](https://user-images.githubusercontent.com/91731260/146139265-bed16bcb-5292-41dd-9a07-701d0690c468.png)|![felog](https://user-images.githubusercontent.com/91731260/146138918-5a580bf4-1466-4919-b858-7669330b80db.png)

Thank you.
