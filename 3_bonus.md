## bonus

Some additional information on config, best practices, resources etc.

### config

manage sensible defaults & tweaks in `~/.gitconfig`

#### » color example

    diff = auto
    status = auto
    branch = auto
    interactive = auto
    ui = auto

#### » color "diff" example

    meta = yellow bold
    frag = magenta
    plain = white bold
    old = red bold
    new = green bold
    commit = yellow bold
    func = green dim

#### » color "status" example

    added = yellow
    changed = green
    untracked = cyan

#### » core example

`excludesfile = /Users/sjugge/.gitignore`

#### » push example

`default = current`

### gitignore

manage global and user specific .gitignore rules on your machine in `~/.gitignore`

#### » example

    # OS specific files
    *.DS_Store
    *.Spotlight-V100
    *.Trashes
    # app specific files
    *bbprojectd
    *nbproject
    *.sublime*

### resources

- official homepage: [http://git-scm.com/]
- official documentation: [http://git-scm.com/documentation]
- git pro book online: [http://git-scm.com]
- git reference site: [http://gitref.org]
- learn git online with GitHub Code School: [http://try.github.io]
