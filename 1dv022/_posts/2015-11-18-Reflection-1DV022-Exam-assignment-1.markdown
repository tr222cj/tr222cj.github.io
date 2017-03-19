---
layout: post
comments: true
title:  "Reflection 1DV022 Exam assignment 1"
date:   2015-11-18 07:55:00
categories: 1dv022 jekyll vagrant css html reflection exam-1
---
* TOC
{:toc}

This exam assignment has taught me a lot. Not so much about html or css - or javascript even - but about technologies I've never used before. Static site generators, CSS Preprocessors, Open Graph and humans.txt are all new concepts that I've either haven't worked with or - in some cases - never even heard of before.

## CSS preprocessors
I've heard about this concept before: Use CSS files with a special syntax that can contain variables, functions, loops and much more. Write them in a syntax that then will be compiled into regular css files.

I would say that scss is what css should have been from the beginning. The syntax in scss is very similar but a bit more complex to regular css. You quickly learn to love setting a color once and instead of specifying the same color in 100 places, you assign it to a variable. You then use this variable instead of the color and when you want to change that color, you change it in one place: the variable.

In this project I mostly used variables or functions on variables, example: $base-color is one variable and $base-color-dark: $darken($base-color, 25%) is another but uses a darker variant of the main color. In this example I can use a color specified in ONE place in the code on several variants of that color. Very powerful!

### Pros
DRY DRY DRY: "Do not Repeat Yourself". The concept is worth repeating... :) In scss you can avoid repeating yourself by using the many options that are available.

### Cons
The learning curve is a bit steeper. Everyone can css but to be able to scss properly you should know at least a little programming.

## Static site generators
The concept appeals to me a lot, especially in the format of a blog. The content in a blog is almost always static. The posts are posted once and they never changed. For this reason alone a blog is a perfect candidate for a static site generator. Add the possibility to adapt it to your specific needs and the deal is made.

### Pros
Speed! Since there are no database queries to run. The site is also precompiled so very little processing is needed for each request.

### Cons
A con but not really? No user input :( The site is static so how can you let visitors comment you post when the site only contains static html? The solution is third-party services as Disqus. There are several alternatives for many specific needs.

## robots.txt
The robots.txt is a simple text file placed in the root of your site that tells search engines, webcrawlers and the like how and if they are allowed to process your site. You can allow/disallow specific parts or pages on your site or even the entire site. I've chosen not to allow any agents on this site. Perhaps I will open it up in the future but for now it's only semi-public.

## humans.txt
Just like the robots.txt this sits in the root of your site. It's only purpose is to tell others about who the author of the website are. The file lets you specify - in a none-intrusive way - many things about you and/or the team responsible for the site.

## Posts
As previously mentioned a static site is just that: static. There is no builtin method of letting users comment the posts. To solve that I implemented a third-party solution named Disqus. This adds the comment-function but as a plugin to my site and separated from it. To the user it works seamlessly but for the developer it's a matter of adding a few lines of code.

## Open Graph
Open Graph is a set of meta tags that you can add to your site. It's a way for social media and others to make sure linked pages are presented similar to other linked pages. It also gives me some control over what data is presented in these links.

## Extras
I did mention this in an earlier post but here it comes again: This is a list of some of the additions I made that was not specified in the assignment:

* Post preview - See the first 40 words of each post. If there is more than 40 words in the post you'll also see a Read more link.
* Pagination - One page only contains max 4 blog posts. In the bottom of the page there is a navigation to Older posts.
* Font Awesome - Less images and more text. Less Images makes for less requests. This is used in the footer to display contact alternatives.

