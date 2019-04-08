# Bash setup

Setting up bash with basic styling and commands.

## Install brew
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Download git-aware-prompt

[Download git-aware-prompt Here](https://github.com/jimeh/git-aware-prompt)
or simply do the following at the time of writing:
```
mkdir ~/.bash
cd ~/.bash
git clone git://github.com/jimeh/git-aware-prompt.git
```

Open bash profile: ```vi ~/.bash_profile``` and add
```
export GITAWAREPROMPT=~/.bash/git-aware-prompt
source "${GITAWAREPROMPT}/main.sh"
export PS1="\w\[$txtcyn\] \$git_branch\[$txtred\]\$git_dirty\[$txtrst\] \$ "
```

## Download git completion
[Download git completion here](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
or simply do the following at the time of writing:
```
brew install git bash-completion
```

Open bash profile: ```vi ~/.bash_profile``` and add
```
[ -f /usr/local/etc/bash_completion ] && . /usr/local/etc/bash_completion || {
    # if not found in /usr/local/etc, try the brew --prefix location
    [ -f "$(brew --prefix)/etc/bash_completion.d/git-completion.bash" ] && \
        . $(brew --prefix)/etc/bash_completion.d/git-completion.bash
}
```
