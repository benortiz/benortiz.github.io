---
layout: post
title: Finding Lost Commits
---
In the process of rebasing with preserving a merge commit (`git rebase -i -p base_branch`),
I somehow managed to lose two commits I was trying to squash together.

To find the lost commits, I tried to use a combination of git commands.
First, I tried using `git fsck --lost-found` which returned a list of
commits that were "dangling". I have no idea how these specific commits
got lost to time, but now they were found. I also checked `git reflog`
which keeps a log of each action and--it seems--its id.

Unfortunately for me, I couldn't find the specific commit I was looking
to reset everything to in either of these. What I ended up doing was looking
through my terminal history for a previous time when I had run `git log`
and grabbed the commit id from there.

After that, it was a simple `git merge --ff-only commit_id` and all my
changes were back.

*wipes sweat from brow*
