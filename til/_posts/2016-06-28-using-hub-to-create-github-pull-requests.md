---
layout: post
title: Using hub to Create GitHub Pull Requests
---
I install `hub` for the first time today to assist in sharing my code
with my interns more often. At first, using it was confusing because
I couldn't find in the documentation how to create a pull request (the
entire reason I installed it).

Magic `hub pull-request -b merge_onto_branch`.

By default `hub pull-request` uses master, but our process has pull
requests going against a different branch.

After that, it's _amazing_.
