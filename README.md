[![Build Status](https://travis-ci.org/burden/jekyll-cards-boilerplate.svg?branch=master)](https://travis-ci.org/burden/jekyll-cards-boilerplate)
# Jekyll Cards Boilerplate

## Features

- [Bulma 0.6.2](https://github.com/jgthms/bulma/tree/0.6.2)
- [jQuery 3.2.1](https://github.com/jquery/jquery/tree/3.2.1)
- Dependency management: [bower](https://bower.io)
- Asset pipeline: [jekyll-assets](https://rubygems.org/gems/jekyll-assets)
  - [JS uglifier](https://rubygems.org/gems/uglifier/versions/3.2.0)
- HTML compression: [compress.html](http://jch.penibelst.de/)
- Testing: [html-proofer](https://github.com/gjtorikian/html-proofer)
- Analytics: [Google Analytics](https://www.google.com/analytics/)
- Search: [simple-jekyll-search](https://github.com/christian-fei/Simple-Jekyll-Search/tree/v1.7.0)
- Comments: [disqus](https://disqus.com)


## Dependencies

1. Install bundler `gem install bundler`
2. Install bower `npm install -g bower`

## Getting Started

```
$ bundle install
$ bower install
$ jekyll serve
```


## Cards

Cards should be saved as a yaml file in the `_data` folder.

Feel free to add whatever metadata applies to your card. If present, the `description` field will be shown below your metadata.
```
Title
  - meta1: 1
  - meta2: two
  - description: "A short description"
```


Configure cards in `_config.yml`.

```
cards:
  data: films         # yaml file in _data (without .yml)
  comments: true      # toggle global comments on pages
  group_by:
    name: decade      # field in yaml to group by
    caption: decades  # name of category (ex: industries)  
    fa-icon: folder-open
    fa-style: far     # valid: fas (solid), far (regular), fal (light), fab (brand)
  meta:
  - name: year        # field in yaml to map
    caption: year
    fa-icon: calendar
    fa-style: far
  - name: url
    caption: www
    fa-icon: globe
    fa-style: fas

```

A page for each card will be automatically generated at `/<cards.data>/<card.name>.html` (ex: /films/the-room.html)

When you use the `group_by` section (currently required), all cards will be grouped into category pages located at `/<cards.categories.name>/<value>.html` (ex: /decades/1930s.html)

If you wish to override the comment configuration on a specific card, you may add a `comments` field to your cards entry (ex: `comments: false`)

## Deploy to Github Pages from Travis
1. Point Travis to repository
2. Configure Travis
3. Generate a [Personal Access Token](https://github.com/settings/tokens) from Github
  - The only scope needed is repo:public_repo
4. Set `GITHUB_API=<token>` on Travis
  - Make sure `Display value in build log` toggle is set to `Off`!
