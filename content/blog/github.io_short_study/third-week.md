---
title: a short review of the third week
date: 2021-12-22 01:12:21
category: github.io short study
thumbnail: { thumbnailSrc }
draft: false
---
### This week's goal

- [x]  [add a workflow script](https://saltysalt77.github.io/github.io%20short%20study/short-review-of-the-third-week/#adding-a-workflow-script)
- [x]  [start studying React](https://saltysalt77.github.io/github.io%20short%20study/short-review-of-the-third-week/#start-studying-react)
- [x]  [add comments feature in the blog](https://saltysalt77.github.io/github.io%20short%20study/short-review-of-the-third-week/#adding-comment-feature-on-the-blog)
- [x]  [translate Gatsby Official Tutorial Part 3](https://saltysalt77.github.io/github.io%20short%20study/short-review-of-the-third-week/#translating-gatsby-official-tutorial-part-3)

### Adding a workflow script

Thanks to Hyojekim, I finally added a working workflow script to my repository. The reason why it didn’t work on my GitHub pages was because of the branch name. Yes, the branch name was the main reason.

I recreated the repository and pushed it to branch main. And it did work!

You can find the workflow script on [my GitHub page](https://github.com/SaltySalt77/SaltySalt77.github.io).

### Start studying React

> **React**: A code library (built with JavaScript) for building user interfaces. It’s the framework that Gatsby uses to build pages and structure content.
> 
> 
>  *- from. Gatsby Official Tutorial Part: 0[(here)](https://www.gatsbyjs.com/docs/tutorial/part-0/)*
> 

I’ve started studying React on [42seoul.groom.io](https://42seoul.goorm.io/). But as you see from above, it’s a code library built with JavaScript. So I decided to learn Javascript basics.

### Adding comment feature on the blog

The initial restoring repo of blog comments is the theme creator’s repo. So, I had to update the `gatsby-meta-config.js` file.
I changed the repo in gatsby-meta-config.js file and deployed it. And then, ***BOOM!*** All of the comments were gone, like this.
![image](https://user-images.githubusercontent.com/91731260/146970342-1f645be4-4502-4278-af1c-c8a3dd1dcbaa.png)

I was in a panic. I’ve tried everything, but the comment didn’t come back. The next day, I was going to start from the beginning. Before deleting the repository of my blog, I compared the gatsby-meta-config.js file from others. And found out the difference.

```jsx
//wrong one
comment: {
	disqusShortName: '', // Your disqus-short-name. check disqus.com.
	utterances: 'SaltySalt77/blog_comments.git', // Your repository for archive comment
}
//right one
comment: {
	disqusShortName: '', // Your disqus-short-name. check disqus.com.
	utterances: 'SaltySalt77/blog_comments', // Your repository for archive comment
}
```


Did you find it? Yes, I had to add the repository name, not the link of the repository. After correcting the code, the comments feature came back. Like this.

![image](https://user-images.githubusercontent.com/91731260/146970456-a0cd39c1-3ec8-41d6-ac49-c9899ecd5268.png)

### Translating Gatsby Official Tutorial Part 3

As you know, I’m Korean, so I participated in translating Gatsby Official Tutorial. While translating, I learned about how to install and use plugins.

You can find Gatsby Official Tutorial Part 3 in [*here*](https://www.gatsbyjs.com/docs/tutorial/part-3/).
