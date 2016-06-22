---
layout: post
title: Using bundle config to work with local git gems
---
After an agonizing day of trying to get my local gem working as a
local and remote git repository, I think I finally figured it out.

In my `Gemfile` now, I have `gem 'gem_name', git: 'https://TOKEN:x-oauth-basic@github.com/org_name/repo_name.git'`
where TOKEN is a personal access token to read my private repos. However,
for this to work locally, I had to modify my bundle config so that it
uses my local path to the repository. A simple `bundle config local.GEM_NAME /path/to/gem`
makes sure it uses the local repository. You can later remove this config
with `bundle config --delete local.GEM_NAME` so you can test how it works
using the remote repo.

The most annoying thing for me at this point is that I cannot get it to
let me simply use uncommited changes. Each time I edit something, I have
to commit it, bundle install and restart everything for the changes to
show up. Alas.
