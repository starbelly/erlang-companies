[![Build Status](https://travis-ci.org/burden/jekyll-cards-boilerplate.svg?branch=master)](https://travis-ci.org/burden/jekyll-cards-boilerplate)
## Cards

Cards can be added to the `_data` folder.

Configure cards in `_config.yml`
```
cards:
  data: cards    # yaml file in _data (without .yml)
  categories:
    name: decades    # name of category (ex: industries)
    group_by: decade # field in yaml to group by
    icon: folder-open

```
## Features

- bulma 0.6.2
- jquery 3.2.1
- Google Analytics
- jekyll-assets
- compress.html
- html-proofer

## Dependencies

1. Install bundler `gem install bundler`
2. Install bower `npm install -g bower`

## Getting Started

```
$ bundle install
$ bower install
$ jekyll serve
```

## Deploy to Github Pages from Travis
1. Point Travis to repository
2. Configure Travis
3. Generate a [Personal Access Token](https://github.com/settings/tokens) from Github
  - The only scope needed is repo:public_repo
4. Set `GITHUB_API=<token>` on Travis
  - Make sure `Display value in build log` toggle is set to `Off`!
