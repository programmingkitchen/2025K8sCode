



# This Repo

- Git config settings before commit. 

```
git config --global user.name "Randall Alta3" 
git config --global user.email "rgranier@gmail.com"

```

```
echo "# 2025K8sCode" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:programmingkitchen/2025K8sCode.git
git push -u origin main
```


# SSH Keys
- Create new keys at the CLI
- Name:  id_rsa_github

```
ssh-keygen
```

- Add public key to github. 

# Added some stuff
- Kubectl command completion. Add to .bashrc

```
echo 'source <(kubectl completion bash)' >> ~/.bashrc

```

# Git Prompt for Linux 

## Set up prompt in command lineThis seems to display (main) even when not in a git repo
curl -o ~/.git-prompt.sh https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh


source ~/.git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
export PS1='\u@\h:\w$(__git_ps1 " (%s)")\$ '

source ~/.bashrc

