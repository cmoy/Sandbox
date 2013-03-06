Sandbox
=======

Sandbox tutorial demonstrating workflow
[contributor]
* github-fork> fork upstream
* workspace> git clone git@github.com:user/repo.git
* workspace> git remote add upstream git@github.com:company/repo.git
* workspace> git remote add contributor1 git@github.com:contributor1/repo.git
* workspace> ...
* workspace> git checkout --track -b develop origin/develop
* workspace> git checkout --track -b feature/billing develop
* workspace> git push origin feature/billing
* github-fork> pull request from feature/billing to upstream develop

[release-master]
* github> merge/close pull requests into develop
* workspace> [follow the clone/remote/checkout setup from contributor]
* workspace> git checkout --track -b release/v1.22 upstream/develop
* workspace> ...
* workspace> [optional: git push upstream release/v1.22]
* workspace> git checkout develop
* workspace> git merge release/v1.22
* workspace> git checkout master
* workspace> git merge develop
* workspace> git tag -s v1.22 -m 'my signed 1.22 tag'
* workspace> git push --tags upstream

[continuous-integration]
* ...
