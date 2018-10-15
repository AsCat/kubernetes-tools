# Kubernetes Tools

Kubernetes Tools is a set of scripts that simplifies daily Kubernetes operations.

#### Available tools
```
kctx: List contexts, switch context
kns: List namespaces, select default namespace
kpod: List pods in current namespace, describe pod
kexec: Get a shell of a selected container
kcp: Copy common cli tools to selected container
```

#### How to use
To list all the available tools, run ```ktools```

For usage of each tool, run ```[tool_name] -h```

## Installation

### Install using brew
```sh
brew tap shawnxlw/homebrew-tap
brew install kubernetes-tools
ktools init
```

### Manual installation
```sh
cd ~
git clone https://github.com/shawnxlw/kubernetes-tools
# add the follow to your .bash_profile or .zshrc
PATH=$HOME/kubernetes-tools/bin:$PATH
# set up tab completion
ktools init
```

##### BASH completion
Add the following into your `.bash_profile`:  
```sh
source $HOME/kubernetes-tools/completion/__completion`
```

##### ZSH completion
Add the following into your `.zshrc`:  
```sh
autoload -U compaudit compinit bashcompinit
compaudit && compinit && bashcompinit
source $HOME/kubernetes-tools/completion/__completion`
```

## License
This software is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Release Note
v2.0.0 - 15/10/2018
- Changed to developer workflow
- Updated kctx, kns, kpod, kcopy, kctx
- Removed kbak, kds, klogs

v1.2.0 - 08/08/2018
- Updated kexec, kns, kpod, kctx, kds
- Added kcp

v1.0.0 - 07/08/2017
- Initial release
