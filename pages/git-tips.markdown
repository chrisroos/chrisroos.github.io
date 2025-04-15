---
layout: page
title: Git tips
permalink: /git-tips
---

```
# Add a new file so that it can then be partially staged with `git add -p`
git add -N file

#  -N, --intent-to-add
#    Record only the fact that the path will be added later. An entry for the path is placed in the index with no content. This is useful for, among other things, showing the unstaged content of such files with git diff and committing them
#    with git commit -a.
```
