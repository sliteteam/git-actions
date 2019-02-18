# GitHub Action for running git commands

You can run any `git` commands you need. For example, you could run `git status` like this.

```hcl
workflow "My build" {
  resolves = [
    "git command",
  ]
  on = "push"
}

action "git command" {
  uses = "srt32/git-actions@v0.0.3"
  args = ["status"]
}
```

You can also run multiple git commands like so:

```hcl
workflow "My build" {
  resolves = [
    "git command",
  ]
  on = "push"
}

action "git command" {
  uses = "srt32/git-actions@v0.0.3"
  args = ["status", "show"]
}
```
