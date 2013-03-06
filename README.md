Sandbox
=======

Sandbox tutorial demonstrating workflow
[contributor]
* github-fork> fork upstream
* workspace> git clone git@github.com:user/repo.git
* workspace> git remote add upstream git@github.com:company/repo.git
* workspace> git remote add contributor1 git@github.com:contributor1/repo.git
* workspace> git checkout --track -b develop origin/develop
* workspace> git checkout --track -b feature/billing develop
* workspace> [development tasks]
* workspace> git add [files,...]
* workspace> git commit -m 'add ability to take money'
* workspace> git push origin feature/billing
* github-fork> pull request from feature/billing to upstream develop
* workspace> git checkout develop
* workspace> git pull
* workspace> git checkout --track -b feature/security
* ... rinse repeat ...
* ... pull request rejected ...
* workspace> git pull
* workspace> [apply review comments]
* workspace> git add [files,...]
* workspace> git commit -m 'applying review comments'
* workspace> git push origin feature/security

[release-master]
* github> merge/close pull requests into develop
* workspace> [follow the clone/remote/checkout setup from contributor]
* workspace> git checkout --track -b release/v1.22 upstream/develop
* workspace> [collaborate release tasks]
* workspace> [optional: git push upstream release/v1.22]
* workspace> git pull
* workspace> git checkout develop
* workspace> git merge release/v1.22
* workspace> git checkout master
* workspace> git merge develop
* workspace> git tag -s v1.22 -m 'my signed 1.22 tag'
* workspace> git push --tags upstream
* workspace> git push upstream

[continuous-integration]
* ...
