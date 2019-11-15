# Contributing to the blog
Create a pull request with the content of the blog post placed in the `drafts` folder using the following file naming scheme: `YYYY-MM-DD-post-title.adoc`.  Blogs are written in [AsciiDoc](https://asciidoctor.org/docs/asciidoc-writers-guide/) format with a file extension of `.adoc`. In the blog post file the following front matter variables must be set:
- layout: post
- title: `title of the blog post`
- categories: blog
- author_picture: `secure url to author picture`
     - If a picture cannot be found, the kabanero.io logo can be used instead https://avatars3.githubusercontent.com/u/50876789
- author_github: `secure url to author github`
- blog_description: `Description of blog post used in the preview card on kabanero.io/blog`
     - Please keep your `blog_description` to around 60 words
- seo-title: `Blog Title used in search results and on social media - Kabanero.io`
     - Please ensure that your `seo-title` ends with ` - Kabanero.io`
- seo-description: `Blog Description used in search results and on social media`
     - Please keep your `seo-description` between 50-300 characters

`drafts` folder contains blog posts that are still in draft and are not ready to be published

`publish` folder contains blog posts that are ready to be published

`img` folder contains images used in the blog `adoc` files. These images are copied over to the website's `/img/blog` dir during build.

### Viewing your blog post on a local development environment
 1. Setup a local development environment by following [the local setup](https://github.com/kabanero-io/kabanero-website/blob/master/CONTRIBUTING.md#local-development-setup)
 1. Put your `.adoc` file in `src/main/content/_posts` and refresh the site

### Contributing a third party blog post

If you would like to add a blog post that is actually a link to an existing third party blog post, you can follow the normal steps described above for creating a blog post. You simply need to add the following attributes to the liquid front matter: 
- redirect_link: 'link'
- permalink: /blog/redirected.html
