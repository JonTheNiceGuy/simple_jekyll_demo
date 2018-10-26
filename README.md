# Hello bold traveller!

This is a demo project to show how you'd build a bearbones Jekyll site - no formatting as such, just a simple loop over data and an index file.

Give it a whirl, see what you can do with it. Oh, and if you want to see which files you need to touch, here's the directory structure...

```
+- _config.yml       | The site config file. This is where you set site-wide variables, and define which files are excluded from the build
+- index.md          | Our single-page web site. It has "jinja2" content parsing using the _data directory in it.
\                    |
|+- _data            | The directory for all the content which populates the index.md file separated into categories.
| \                  |
|  +- CLI            | Like Command Line tools:
|  |\                |
|  | +-Sample.yml    |     In this file we have a single CLI tool
|  +- Desktop        | Or Desktop GUI tools:
|  |\                |
|  | +- Demo.yml     |     Where we have
|  | +- Example.yml  |     three separate
|  | +- Sample.yml   |     Apps!
|  +- Mobile         | Or Mobile apps:
|   \                |
|    +- Bar.yml      |     Like this one
|    +- Foo.yml      |     And this one
+- _layouts          | And then here's where the actual HTML is generated from
 \                   |
  +- default.html    |     This is the "default" file. Others can be defined in the header block for _posts and pages as "layout:"
```

Talking of header blocks, this is what you'll probably need to define if you create any other pages:

```
---
title: <your page title>
layout: <your _layout file, e.g. for _layouts/mypage.html, enter "mypage" here>
---
Your Content Goes here
```

In your _layouts files, add this line if you want to inject the block below the header into your page:

```
{{ content }}
```

There are *LOTS* more examples than this. But this works.

Oh, and if you're struggling to make `bundle install && bundle exec jekyll serve -H 0.0.0.0` work, try installing virtualbox and vagrant, and then entering this directory, and running `vagrant up` (and then browsing to http://your_machine:4000 or http://localhost:4000)
