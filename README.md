## Features

- bulma 0.7.1
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
