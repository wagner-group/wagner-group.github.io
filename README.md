# Wagner group page

This is the repository for the [Wagner Research Group](https://wagner-group.github.io), which runs on Jekyll and Github pages.

## Run the page locally using Jekyll

To run locally, follow instruction [here](https://jekyllrb.com/) to install Jekyll then run `jekyll serve` to see in `localhost:4000`. Here is a brief install guidelines.

```bash
sudo gem install jekyll
sudo gem install rouge
jekyll serve
```

## Adding content

The website can either be edited directly on Github using the `Add file` button from the web client, or by cloning the repository and editing locally.

### Blog posts

Blog posts should be saved under the `_posts` folder and written in markdown (or HTML). The filename should be in the format `YYYY-MM-DD-title.md`. The header of the file should be in the following format:

``` markdown
---
title: My title
description: My description
---
```

The `description` field will be shown as a preview when shared on social media. See the official Jekyll docs for more details: [https://jekyllrb.com/docs/posts/](https://jekyllrb.com/docs/posts/).

### Project pages

Project pages function similarly to blog posts. Create and add your project page under the `_projects` folder. The header should include the following information:

``` markdown
---
title: My project
description: My project description
---
```

### Group members

You can add a new person under the `_people` folder by creating a new file with the name `<firstname>_<lastname>.md` in the folder. The header should include the following information:

``` markdown
---
name: First Last
position: grad
avatar: firstname_lastname.jpg
joined: 2020
---
```

And the rest of the file defines the content shown on their personal page, e.g. an About Me and Research Interests sections.

The `avatar` field should refer to a file within the `images/people` folder, where you should upload the person's picture. 
Position should be one of: `pi`, `postdoc`, `grad`, `ugrad`, or `alum` (which will hide the person from the main page but keep their personal page).
