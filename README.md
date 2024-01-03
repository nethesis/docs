# NETHIPEDIA

Documentation scheme of all nethesis products.

## Development

- Install a full [Ruby development environment](https://jekyllrb.com/docs/installation/)
- Install Jekyll and bundler gems 
```
gem install jekyll bundler
```
- Clone repository
```
git clone 
cd docs-nethesis
```
- Install gems
```
bundle install
```
- Install [Yarn](https://yarnpkg.com/lang/en/docs/install/#centos-stable)
- Install npm modules
```
yarn install
```
- Build the site and make it available on a local server
```
bundle exec jekyll serve
```
- Now browse to http://localhost:4000

## Build and deploy

Execute:
```
rm -rf _site/*
JEKYLL_ENV=production bundle exec jekyll build
lftp -u docs@nethesis.it,PASSWORD c110061.sgvps.net -e "set ftp:ssl-allow no ; mirror -v -e -R -p ./_site . ; quit"
```

Ask for `PASSWORD` to the admin of the site.

### Note
Check [here](https://jekyllrb.com/docs/themes/#overriding-theme-defaults) to learn how the Jekyll theme works.
