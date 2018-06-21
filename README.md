[![Build Status](https://travis-ci.org/burden/jekyll-cards-boilerplate.svg?branch=master)](https://travis-ci.org/burden/jekyll-cards-boilerplate)

## Dependencies

1. Install bundler `gem install bundler`
2. Install bower `npm install -g bower`

## Getting Started

```
$ bundle install
$ bower install
$ jekyll serve
```

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

## Cards

Cards should be saved in the `_data` folder.

Configure cards in `_config.yml`
```
cards:
  data: films         # yaml file in _data (without .yml)
  group_by:
    name: decade      # field in yaml to group by
    caption: decades  # name of category (ex: industries)  
    icon: folder-open
```
A page for each card will automatically be generated at `/<cards.data>/<name>.html` (ex: /films/the-room.html)

In addition, all cards will be grouped into category pages located at `/<cards.categories.name>/<value>.html` (ex: /industries/consulting.html)

## Deploy to Github Pages from Travis
1. Point Travis to repository
2. Configure Travis
3. Generate a [Personal Access Token](https://github.com/settings/tokens) from Github
  - The only scope needed is repo:public_repo
4. Set `GITHUB_API=<token>` on Travis
  - Make sure `Display value in build log` toggle is set to `Off`!
