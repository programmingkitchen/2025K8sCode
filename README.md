# BASIC CHEATS



## This Repo

- Clone

- Git config settings before commit. 

```
~/.gitconfig

git config --global user.name "Randall Alta3" 
git config --global user.email "rgranier@gmail.com"

```
- Clone
```
git clone git@github.com:programmingkitchen/2025K8sCode.git
```

- Setting up the repo from scratch (no clone)
```
echo "# 2025K8sCode" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:programmingkitchen/2025K8sCode.git
git push -u origin main
```


## SSH Keys
- Create new keys at the CLI on the Alta 3 node
- Name:  id_rsa_github

```
ssh-keygen
```

- Add public key to github. 

## Command completion
- Kubectl command completion. Add to .bashrc

```
echo 'source <(kubectl completion bash)' >> ~/.bashrc
```



# Port forwarding

kubectl port-forward simpleservice 2224:9876 --address=0.0.0.0
curl http://127.0.0.1:2224/env

- Quick pod

```
kubectl run portforwardpod --image=nginx:1.19.6
```
- Do the port forward from the 2224 port (set up for web browsing) to 80, the port
that the container is running on.

student@bchd:~/2025K8sCode$ kubectl port-forward portforwardpod 2224:80 --address=0.0.0.0
Forwarding from 0.0.0.0:2224 -> 80
Handling connection for 2224



# Git Prompt for Linux 

## Set up prompt in command lineThis seems to display (main) even when not in a git repo
curl -o ~/.git-prompt.sh https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh


source ~/.git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
export PS1='\u@\h:\w$(__git_ps1 " (%s)")\$ '

source ~/.bashrc

