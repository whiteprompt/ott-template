---
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
title: Online Tech Talks
---

<img width="300" style="margin-left:auto;margin-right:auto;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

### Online Tech Talks

<br>

# Organizing Git Commits

<br>

Please mute your mic
<br>
<br>
We will start in

<iframe src="https://free.timeanddate.com/countdown/i8dwv0lq/n541/cf100/cm0/cu4/ct0/cs0/ca0/co0/cr0/ss0/cac000/cpc000/pcfff/tcfff/fs100/szw320/szh135/iso2022-07-08T17:05:00" allowtransparency="true" frameborder="0" width="320" height="100" style="margin-left:270px;margin-top:-10px;pointer-events: none;"></iframe>

<iframe width="100" height="100" src="https://www.youtube.com/embed/07g5NFALjQs?autoplay=0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<style>
h3 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}

</style>

---

# What are the OTT (Online Tech Talks)

A space to share stuff with other TMs

<br><br>

- 🤹 **Storytime** : something that was done during the week or the week before

  - I had to do this, I did it this way, and this is the result

<br><br><br>

- 🧑‍💻 **Research/Blog Post Presentation** - theme can be shared and used with npm packages\

  - Get online to present the research or Blog Post made

<br><br><br>

- 🛠 **Technology updates** - : New features / Frameworks / Tools

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}

div.container {
  display:inline-block;
  margin-left:auto;
  margin-right:auto;
}

</style>

---

## Some disclaimers

<br><br>

### Disclaimer #1

<br>

Do not do rebase / push force in branches that other people might be using.

This will change the original reference that they were using and it would require them to rebase their own commits to the new branch.

<br>
<br>

### Disclaimer #2

<br>

Git is pretty flexible and if things get messy, probably there is a way to fix that.

A branch in Git is simply a lightweight movable pointer to one of the commits.

[Git-SCM - Git in a Nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell#:~:text=A%20branch%20in%20Git%20is,branch%20pointer%20moves%20forward%20automatically.)

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Organizing Git Commits

<br>

During this OTT, we will talk about:

- Amending an existing commit
- Rebasing a series of commits
  - Squash
  - Rename
  - Edit
  - Drop
- Adding changes from a file into separate commits
- Using reflog to identify commits without branches
- Difference between merge and rebase


<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Demo

<br>

To get familiar with the codes, I suggest creating a repository to explore these commands. During the presentation, I'll use my git-playground repository.

Some of the commands that we will use during the demo are:

- git commit --amend
- git push origin feature --force
- git rebase -i HEAD~5
- git rebase origin/master
- git add -p filename.txt
- git reflog
- git reset --hard commit_hash

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Difference between merge and rebase

<br>

Merging is nice because it’s a non-destructive operation. The existing branches are not changed in any way. This avoids all of the potential pitfalls of rebasing.

Rebasing re-writes the project history by creating brand new commits for each commit in the original branch.

<div class="container">
  <img width="400" style="float: left;" src="https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=424">

  <img width="400" style="float: right;" src="https://wac-cdn.atlassian.com/dam/jcr:3bafddf5-fd55-4320-9310-3d28f4fca3af/03%20Rebasing%20the%20feature%20branch%20into%20main.svg?cdnVersion=424">
</div>

<br><br>

[Atlassian Bitbucket Tutorials - Merging vs. Rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing#:~:text=Merging%20is%20a%20safe%20option,onto%20the%20tip%20of%20main%20.)

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Configs / shortcuts

<br>

.gitconfig file:

```markdown
[alias]
	co = checkout
	sw = switch
	ci = commit
	st = status
	br = branch
[merge]
	tool = vscode
[mergetool "vscode"]
	cmd = code --wait --diff $LOCAL $REMOTE
[diff]
	guitool = vscode
[difftool "vscode"]
	cmd = code --wait --diff $LOCAL $REMOTE
[core]
	editor = code --wait
```

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Configs / shortcuts

<br>

.bashrc file shortcuts:

```bash
alias gs='git status'
alias ga='git add'
alias gb='git branch'
alias gc='git commit'
alias gd='git diff'
alias go='git checkout'
alias gitk='gitk --all&'
alias gx='gitx --all'
alias gf='git fetch --all'
alias gfa='git fetch --all'

alias got='git'
alias get='git'

alias rmorig='find . -name '*.orig' -delete'
```

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Configs / shortcuts

<br>

.bashrc file configs to display branch name on Linux:

```bash
# Show git branch name
force_color_prompt=yes
color_prompt=yes
parse_git_branch() {
 git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
if [ "$color_prompt" = yes ]; then
 PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[01;31m\]$(parse_git_branch)\[\033[00m\]\$ '
else
 PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w$(parse_git_branch)\$ '
fi
unset color_prompt force_color_prompt
```

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>

---

# Questions / comments / suggestions?

<br>

<img width="300" style="position: absolute; bottom: 10px; left: 10px;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

---
# Thank you!

<br>

If you have any questions or you want to conduct an OTT let us know in Slack ;)

<img width="300" style="position: absolute; bottom: 10px; left: 10px;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>