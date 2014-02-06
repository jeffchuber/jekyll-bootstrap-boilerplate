jekyll-bootstrap-boilerplate
============================

A quick and easy way to prototype ideas using [Twitter Bootstrap](http://getbootstrap.com/) and [Jekyll](http://jekyllrb.com/).

### What's included?

1. [Twitter Bootstrap 3](http://getbootstrap.com/) - you have access to all the CSS and JS
2. [Underscore.js](http://underscorejs.org/)
3. [Handlebars.js](http://handlebarsjs.com/)
4. [Jquery 1.9.1](http://jquery.com/)
5. [Bootstrap datepicker](http://www.eyecon.ro/bootstrap-datepicker/) JS and CSS
6. [jekyll](http://jekyllrb.com/)

### How to set up

1. Open up terminal, or I suggest [iTerm2](http://www.iterm2.com/#/section/home)
2. Clone repo `git clone git@github.com:jeffchuber/jekyll-bootstrap-boilerplate.git`
3. Enter repo `cd jekyll-bootstrap-boilerplate`
4. Make sure you have jekyll installed `gem install jekyll`
5. Run `jekyll serve --watch`.
6. In your browser go to [localhost:4000](localhost:4000)
7. Make edits, refresh your browser, and see things happen!

### Recommended workflow

1. `_layouts/default.html` is where you edit the base styles of your app. This is where you can put your header and footer that are standard across all page. This is also where you can and should include javascript, fonts, CSS, etc that you want to add to the page. (basically anything in the `<head>` element) `{{content}}` is where sub pages will put their content. For example for your landing page, the contents of `index.html` will be placed in the default layout and replace `{{content}}`
2. `index.html` is your landing page
3. `_posts/2013-10-10-example.html` is your first page. You can access it by going to [localhost:4000/example](localhost:4000/example). To create a new page, use the same naming as you see for the example page. So if you about a page called `about`, create `2013-10-10-about.html`. Now you can go to `[localhost:4000/about](localhost:4000/about)` or link to it from another view by typing `<a href="/about">About</a>` Make sure to include the block at the top that you see in the example.

```ruby
---
layout: default
title:  "Example"
date:   2013-10-21 12:06:36
---
```

For more learning check out the [Jekyll Documentation](http://jekyllrb.com/docs/templates/)

### Easily host your mockups
If you want to easily put your mockups up on the internet, there is a super simple way to do this using [s3_website](https://github.com/laurilehmijoki/s3_website)
The basic instructions are (copied from Readme.md):

Here's how you can get started:

- Create API credentials that have sufficient permissions to S3. More info here.
- Go to your website directory
- Run s3_website cfg create. This generates a configuration file called s3_website.yml.
- Put your AWS credentials and the S3 bucket name into the file
- Run s3_website cfg apply. This will configure your bucket to function as an S3 website. If the bucket does not exist, the command will create it for you.
- Run s3_website push to push your website to S3. Congratulations! You are live.
