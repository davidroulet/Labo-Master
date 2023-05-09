# Fork process

[Source](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Git-flow scenario to master</p></figcaption></figure>

* [ ] Fork the "upstream" repository in your github organisation

```
//TODO
![image](https://user-images.githubusercontent.com/47849716/237053339-3187e0f2-db3d-4baf-aa5e-7077ddbcbc1b.png)
```

* [ ] Clone "teacher" repo in your local machine

```
[INPUT]
git clone https://github.com/davidroulet/Labo-Master.git


[OUTPUT]
Cloning into 'Labo-Master'...
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 16 (delta 1), reused 14 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), 4.71 KiB | 4.71 MiB/s, done.
Resolving deltas: 100% (1/1), done.

```

* [ ] Init Git flow (with standard settings)

```
[INPUT]
 git flow init


[OUTPUT]

Which branch should be used for bringing forth production releases?
   - main
Branch name for production releases: [main] 
Branch name for "next release" development: [develop] 

How to name your supporting branch prefixes?
Feature branches? [feature/] 
Bugfix branches? [bugfix/] 
Release branches? [release/] 
Hotfix branches? [hotfix/] 
Support branches? [support/] 
Version tag prefix? [] 
Hooks and filters directory? [/home/david/Documents/mon/Labo-Master/.git/hooks] 

```

* [ ] Update your develop branch directly to the upstream (main branch)

```
[INPUT]
git remote add upstream https://github.com/CPNV-MON1/Labo-Master
git push --set-upstream origin develop
git pull upstream main 

[OUTPUT]
From https://github.com/CPNV-MON1/Labo-Master
 * branch            main       -> FETCH_HEAD
Already up to date.

```

* [ ] Create a branch feature called "terraformBasicScript"

```
[INPUT]
git branch "terraformBasicScript"
git switch terraformBasicScript 


[OUTPUT]

```

* [ ] Add this code and commit it (feat:add basic terraform script")

```
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.16"
    }
  }

  required_version = ">= 1.2.0"
}

provider "aws" {
  region  = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}
```

```
[INPUT]
git add .
git commit -m "feat:add basic terraform script"


[OUTPUT]
[terraformBasicScript 061b567] feat:add basic terraform script
 1 file changed, 23 insertions(+)
 create mode 100644 terraformBasicScript

```

* [ ] Finish the feature

```
[INPUT]
git flow feature finish terraformBasicScript


[OUTPUT]
Branches 'develop' and 'origin/develop' have diverged.
And local branch 'develop' is ahead of 'origin/develop'.
Switched to branch 'develop'
Your branch is ahead of 'origin/develop' by 1 commit.
  (use "git push" to publish your local commits)
Updating 0388bff..061b567
Fast-forward
 terraformBasicScript => script | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename terraformBasicScript => script (100%)
Deleted branch feature/terraformBasicScript (was 061b567).

Summary of actions:
- The feature branch 'feature/terraformBasicScript' was merged into 'develop'
- Feature branch 'feature/terraformBasicScript' has been locally deleted
- You are now on branch 'develop'

```

* Push this modification on your repository

```
[INPUT]
git push

[OUTPUT]
Username for 'https://github.com': davidroulet
Password for 'https://davidroulet@github.com': 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 754 bytes | 754.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/davidroulet/Labo-Master.git
   cf09931..061b567  develop -> develop

```

* What happens to the feature/branch ?

```
//TODO
 git reflog show 

061b567 (HEAD -> develop, origin/develop) HEAD@{0}: merge feature/terraformBasicScript: Fast-forward

```

* Open a pull request comparing your develop branch to your main
* Assign the pull request to your partner

```
//TODO
Screenshot pull request on github
```

* Notify him using a issue "Could you please review my pull request ?"

```
//TODO
Screenshot issue on github
```
