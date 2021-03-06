# ssh-agent_fish

ssh-agent automatic startup for fish

## Installation

#### Using fisherman (recommended)

1. Install fisherman [https://github.com/fisherman/fisherman](https://github.com/fisherman/fisherman)
2. Run:

    fisher install https://github.com/virtualxdriver/ssh-agent.fish.git

#### Classic

Copy-paste the contents of the `conf.d/ssh-agent.fish` into your `.config/fish/config.fish` file.

## Usage

If a previous instance cannot be found, `ssh-agent` will be launched on shell startup automatically.

#### Multiple identities

By default, ssh-agent_fish only loads the default identity.

You can load multiple identities with the `__ssh_agent__identities` variable, for example:

    set -U __ssh_agent__identities id_rsa id_rsa2

#### Lifetime

By default, identities stay in memory forever.

You can adjust the maximum lifetime of the identities with the `__ssh_agent__lifetime` variable, for example:

    set -U __ssh_agent__lifetime 4h

## Thanks

* oh-my-zsh ssh-agent plugin authors
  * https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/ssh-agent/ssh-agent.plugin.zsh
* Joseph M. Reagle
  * http://www.cygwin.com/ml/cygwin/2001-06/msg00537.html
