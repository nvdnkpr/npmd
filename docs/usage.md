npmd [cmd] {options}

npmd --sync --verbose?                  # sync registry.

npmd install [module(@version)?,...]    # install modules
  --global?                             #   install globally
  --greedy?                             #   install deduped by default

npmd link [module(@version)?,...]       # install by symlink (fast)
  --global?                             #   install globally

(`install` and `link` both also take thes options)

  --path      # directory that the node_modules folder lives in.
  --bin       # place to install bin commands, if there any any.
  --global    # sets --path to npm.config.prefix/lib,
              # and --bin to npm.config.prefix/bin

npmd resolve [module(@version)?,...]    # output dependency tree for install
  --greedy?

npmd lresolve [module(@version)?,...]   # output dependency tree for link

npmd packages prefix?                   # output modules starting with prefix

npmd versions modulename                # output versions of modulesname

npmd dependencies [$modulename1,...]    # output modules that depend on modules
  
