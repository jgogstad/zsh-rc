# zsh-rc

## What

ZSH plugin for working with RC branches. Typically useful in the following workflow

* Work is done on feature branches
* A branch suffix of "-rc" signals to CI that it should produce an artifact for the branch

```
 git checkout -b feature/foo
Switched to a new branch 'feature/foo'

# Easily switch back and forth, RC branch will be created if it doesn't exists
 rc
Switched to a new branch 'feature/foo-rc'

 rc
Switched to branch 'feature/foo'

# RC branch will always be hard reset to non-rc branch
 git commit --allow-empty -m "Foo"
[feature/foo bf6d376] Foo

 rc
Switched to branch 'feature/foo-rc'
HEAD is now at bf6d376 Foo
```

## Installation

*****Antibody**

```
antibody bundle jgogstad/zsh-rc
```

**Antigen**

```
antigen bundle jgogstad/zsh-rc
```

**Zplug**

```
zplug "jgogstad/zsh-rc"
```

**Plain zsh**

Add to `.zshrc`

```
. /path/to/zsh-rc.plugin.zsh
```
