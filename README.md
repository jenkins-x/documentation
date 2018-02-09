# Jenkins X Documentation

## Develop

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Editing

Edition is already optimised for adding, updating and removing documentation pages in CloudCannon.

### Documentation pages

* Add, update or remove a documentation page in the *Documentation* collection.
* Change the category of a documentation page to move it to another section in the navigation.
* Documentation pages are organised in the navigation by category, with URLs based on the path inside the `_docs` folder.

### Search

* Add `excluded_in_search: true` to any documentation page's front matter to exclude that page in the search results.

### Table of contents

* Add `toc: true` to any documentation page's to include a table of contents for the page

### Navigation

* Change `site.show_full_navigation` to control all or only the current navigation group being open.

# Docker

The Dockerfile provided captures the static website generated in `/_site` and serves it using Nginx.

To build the container:

    bundle exec jekyll build
    docker build -t jenkinsx/docs .

To run the container:

    docker run -itd --name jenkinsxdocs --publish 8080:80 jenkinsx/docs

# Credits

Thank you to CloudCannon for [the template](https://github.com/CloudCannon/edition-jekyll-template) we are using for the Jenkins X documentation. You are awesome!
