# git contribution workflow

We develop using [triangular workflows](https://github.blog/2015-07-29-git-2-5-including-multiple-worktrees-and-triangular-workflows/#improved-support-for-triangular-workflows) on git.

For local deployment please create a fork of the [Offseter SDK repo](https://github.com/kargakis/offseter-sdk).

Clone your fork:

```bash
git clone git@github.com:YOURUSERNAME/offseter-sdk.git
git config remote.pushdefault origin
git config push.default current
```

next add the root repository as `upstream`:

```bash
git remote add upstream git@github.com:kargakis/offseter-sdk.git
git fetch upstream
```

Run:

```bash
git remote -v
```

and you should see something like:

```bash
origin	git@github.com:YOURUSERNAME/offseter-sdk.git (fetch)
origin	git@github.com:YOURUSERNAME/offseter-sdk.git (push)
upstream	git@github.com:kargakis/offseter-sdk.git (fetch)
upstream	git@github.com:kargakis/offseter-sdk.git (push)
```

Feature flow:

```bash
git checkout main && git pull --ff-only upstream main
```

Cmd+shift+. to copy your issue number from linear, and use it as your branch name:

```bash
git checkout -b co2-190-small-edits-on-the-home-page
```

To open a PR push to your fork and open your PR to `kargakis/offseter-sdk`.