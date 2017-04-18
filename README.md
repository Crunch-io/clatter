# clatter: The Crunch.io Dev Blog

## Building locally

Clatter uses [Hugo](https://gohugo.io/) to build the static site from markdown. If you don't have hugo (or golang) installed, you'll need to get that. On MacOS, if you use Homebrew,

    brew update && brew install hugo

You'll also need to pull the [Kube theme](https://themes.gohugo.io/kube/). From the clatter directory, check out the kube repository into the "themes" subdirectory like this:

    git clone https://github.com/jeblister/kube.git ./themes/kube

You should only need to do this the first time you set up your local environment. Do not make any changes inside the theme directory--that directory is `.gitignore`d. See below on how to override styles and templates.

Once you have hugo and the kube theme, run

    hugo server

to build and serve locally. Hugo will be watching the file system and will automatically update if you make changes.

## How to add a new post

To create a new blog post, you can use hugo's templating tool ("archetypes") and create the file like:

    hugo new --kind blog blog/my-new-post.md

You can probably copy an existing post and edit it appropriately, too, but I'm not sure what side effects calling `hugo new` might have.

In the metadata (called [front matter](https://gohugo.io/tutorials/creating-a-new-theme/#front-matter) in Hugo-speak), there are some fields you should edit:

* **title** and **description**: you'll see those featured prominently on the site, and they also go into the link preview meta tags.
* **categories**: Use this to distinguish between feature announcements ("features") and other streams of dev blogging (TBD).
* **tags**: Use these for specific topics, e.g. the names of features affected by the feature announcement.
* **weight**: For blog posts, you probably don't want to touch this, but if you want to pin some post to the top of the list (and not have it sort by date), you can give it a higher weight.
* **draft**: Looks like you can write a post and flag it not to appear until you set this to `false`.

## Customizing the theme

The [Kube theme](https://themes.gohugo.io/kube/) has decent docs, so check them out for more info on what it is designed to do. The main [Hugo docs](https://gohugo.io/overview/introduction/) are pretty thorough too.

To override anything in the theme, don't edit the theme files--Git isn't tracking them. Instead, make a copy of the file from the theme into `clatter` and edit it. For example, if I wanted to edit the "docs/single.html" layout file,

    cp themes/kube/layouts/docs/single.html layouts/docs/single.html

and edit that copy. Hugo layers our copies on top of the theme's resources when it builds the site.

## Deployment

Deploying the site happens automatically when you push to the master branch. Travis-CI runs hugo and pushes the generated website to where we host it. No further action required on your part.
