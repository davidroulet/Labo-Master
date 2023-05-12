# Prerequisites

## Setting up/updating the git environment and git flow

[Get the installer](https://git-scm.com/downloads)

{% hint style="info" %}
Git-flow library:\
For Windows, is natively integrated.\
For Mac, [here is the procedure](https://git-scm.com/download/mac).\
Pour Linux, [here is the procedure.](https://howtoinstall.co/en/git-flow)
{% endhint %}

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* [X] Confirm the installed version

```
[INPUT]
david@pop-os:~$ git flow version

[OUTPUT]

1.12.3 (AVH Edition)

```

* [ ] What do you think about this release?

```
//TODO
Very usefull
```

## What's git-flow, branches feature.

[Source](https://nvie.com/posts/a-successful-git-branching-model/)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Source : A successful git branching model</p></figcaption></figure>

* [X] Which branches are persistent and what do they contain?

```
//TODO
Main 
et ce veux etre la branche principal (genre prod)
```

* [X] Why do we have to merge hotfix in both master and develop branches, but not into all active feature branches?

```
//TODO
Pour evité que le bug revienne à la prochaine release
```

## Initialize git flow on an existing project

* [ ] What happens when you run the "git flow init" command on an existing local repository?

```
//TODO
create develops branch
```

* [X] When do we need to make this git command?

```
//TODO
Pour avoir un bonne environment de travaille
```

## Practice the basic git commands

[Source](https://www.atlassian.com/git/glossary)

* [ ] What does this git command "git add -all" achieve (.gitignore impacts)?

```
//TODO
ajout tout et ce moque de gitignore
```

* [X] What does this git command "git status" achieve?

```
Montre ce status de la branch sur la quelle on es
```

* [X] What does this git command "git remote add upstream \<url>" achieve?

```
Ajoute une connextion a un autre depot
```
