# Command Design

```
git topwork stocks [path/to/specific/submodule]

git topwork graft --all --recursive --force [path/to/specific/submodule] [commit-ish]

git topwork tie --recursive [path/to/specific/submodule]
git topwork untie --recursive [path/to/specific/submodule]

git topwork growth --all --recursive [path/to/specific/submodule]

git topwork prune --all --recursive [path/to/specific/submodule]
```

# Configuration

```
[graft "rootstock-name"]
	scion = /path/to/another/git-repos
```

# Terminology

-- topworking: 嫁接的通俗說法
-- grafting/graftage: 嫁接的專有名詞
-- scion: 組合植物的上部稱為接穗
-- rootstock: 組合植物的下部稱為砧木

# Misc

```
$ git config --name-only --get-regexp graft
git config --name-only --get-regexp graft
```

```
$ git config --get-regexp graft
graft.hal_g6/mac.remote origin
graft.hal_g6/mac.merge refs/heads/master
```

```
$ git config --show-scope --get-regexp graft
local   graft.hal_g6/mac.remote origin
local   graft.hal_g6/mac.merge refs/heads/master
```

```
$ git config --name-only --get-regexp graft
$ git config get --show-names --name-only --all --regexp graft

graft.hal_g6/mac.remote
graft.hal_g6/mac.merge
```

```
git config --list
git config --list --show-scope
```

# Reference
* [git-config - Get and set repository or global options](https://git-scm.com/docs/git-config)
* [How do I show my global Git configuration?](https://stackoverflow.com/questions/12254076/how-do-i-show-my-global-git-configuration)
* [LeGEC/git-wip](https://gist.github.com/LeGEC/a75473eb5575a5c6814efafcace80957)
* [Git grafts - merge history of multiple repos](https://til.juliusgamanyi.com/posts/git-graft-combine-multiple-repos-history/)
