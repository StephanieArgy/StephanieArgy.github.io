---
layout: page
title: Advanced Web Dev Tools, Week Four
permalink: /pcsnotes_c3_w4/
---

* [More Command Line details](#commandLineDetails)
* [Backend as a Service](#BaaS)
* [Style Guides](styleGuides)

<a name="commandLineDetails"></a>
##Command Line Details

(These are very random and I need to learn more about the command line to really understand my notes.)

$ cd
$ pwd
$ ls -al

.bashrc

Aliases
Bash command shortcuts

```
alias glo = 'git log --graph --oneline --decorate --tags
```

Environment variable called PATH

```
export PATH = $PATH:/Applications/Postgres.app/Contents/Versions/9.3/bin
```

Makes computer follow that path. Can force it into another path:

```
export PATH = "/usr/local/bin:$PATH"
```

###Ruby on Rails stuff

(Can store keys for API's etc. 

[Mandrill](http://blog.mandrill.com/) gives you "whitelisting" for MailChimp: spammer's dream.

Node Version Manager

```
function parse_git_branch {
  git branch --no-color 2>dev/null (etc. -- INCOMPLETE)
}
```

PS1 = "${TITLE}" (Can change to put in other details, such as date, user, machine, path)


<a name="BaaS"></a>
##Backend as a Service

* The Why of Servers
* Architecture and components
* Installfest
* Simple verification of functionality
* Refactor glossary and kitten site



<a name="styleGuides"></a>
##Style Guides

