# Bash setup

Setting up bash with basic styling and commands.

## Download git-aware-prompt

[Download git-aware-prompt Here](https://github.com/jimeh/git-aware-prompt)
or simply do the following:
```
mkdir ~/.bash
cd ~/.bash
git clone git://github.com/jimeh/git-aware-prompt.git
```

## Update bash profile

Open bash profile: ```vi ~/.bash_profile``` and add
```
export GITAWAREPROMPT=~/.bash/git-aware-prompt
source "${GITAWAREPROMPT}/main.sh"
export PS1="\w\[$txtcyn\] \$git_branch\[$txtred\]\$git_dirty\[$txtrst\] \$ "
```
