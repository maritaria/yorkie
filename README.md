# yorkie

> Git hooks made easy

This is a fork of [husky](https://github.com/typicode/husky) with a few changes:

- Prioritizes `package.json` located next to `.git` directory, instead of hard-coded upward search. This avoids the problem when a root package in a lerna monorepo and a sub package both depends on husky, it gets confused and double-updates the root git hooks with wrong paths.

- Changed where hooks are read from in `package.json`:

  **Before**

  ``` json
  {
    "scripts": {
      "precommit": "foo"
    }
  }
  ```

  **After**

  ``` json
  {
    "gitHooks": {
      "pre-commit": "foo"
    }
  }
  ```

# Hooks

The following githooks are available for scripting:

- [applypatch-msg](https://git-scm.com/docs/githooks#_applypatch_msg)
- [pre-applypatch](https://git-scm.com/docs/githooks#_pre_applypatch)
- [post-applypatch](https://git-scm.com/docs/githooks#_post_applypatch)
- [pre-commit](https://git-scm.com/docs/githooks#_pre_commit)
- [prepare-commit-msg](https://git-scm.com/docs/githooks#_prepare_commit_msg)
- [commit-msg](https://git-scm.com/docs/githooks#_commit_msg)
- [post-commit](https://git-scm.com/docs/githooks#_post_commit)
- [pre-rebase](https://git-scm.com/docs/githooks#_pre_rebase)
- [post-checkout](https://git-scm.com/docs/githooks#_post_checkout)
- [post-merge](https://git-scm.com/docs/githooks#_post_merge)
- [pre-push](https://git-scm.com/docs/githooks#_pre_push)
- [pre-receive](https://git-scm.com/docs/githooks#pre-receive)
- [update](https://git-scm.com/docs/githooks#update)
- [post-receive](https://git-scm.com/docs/githooks#post-receive)
- [post-update](https://git-scm.com/docs/githooks#post-update)
- [push-to-checkout](https://git-scm.com/docs/githooks#_push_to_checkout)
- [pre-auto-gc](https://git-scm.com/docs/githooks#_pre_auto_gc)
- [post-rewrite](https://git-scm.com/docs/githooks#_post_rewrite)
- [sendemail-validate](https://git-scm.com/docs/githooks#_sendemail_validate)
