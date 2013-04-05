---
layout: layout
title: Git Tips
---

Git Tips
========

### Remove a specific commit:

Here is a command to non-interactively remove a specific commit-id, knowing only the commit-id you would like to remove:

```
git rebase --onto <commit-id>^ <commit-id> HEAD
```

(from http://stackoverflow.com/a/3705310)
