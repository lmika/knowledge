---
title: Showing Only Changed Files in Git Log
type: tidbit
---

This technique shows only the changed files in a git log call without having to show the entire patch:

    git log --name-only ...