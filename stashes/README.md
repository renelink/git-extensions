# git stashes

The git stashes extensions help you to push your stashes to a remote and fetch them from there. They provide you a way to backup your stashes.


## git stashes-push

Pushs all stashes to the origin remote repository using the current user's name as its context.

     git stashes-push

You can change the remote repository as well as the context. E.g.

    git stashes-push anotherRemoteRepo myContext

The context is used to separate stashes on the remote. The stashes will be pushed to

    refs/stashes/<CONTEXT>/*

on the remote.

By separating the stashes on the remote each team member can push their own stashes. 

---
**NOTE**

The context is the current user's name per default. If multiple users have the same username on their machine they will override their stashes.

---

## git stashes-fetch

Fetches stashes from a remote repository (default origin) using the current user's name as its context.

     git stashes-fetch

You can change the remote repository as well as the context. E.g.

    git stashes-fetch anotherRemoteRepo myContext
