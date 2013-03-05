Sandbox
=======

Sandbox tutorial demonstrating workflow
* fork upstream
* git clone git@github.com:user/repo.git
* git remote add upstream git@github.com:company/repo.git
* git remote add contributor1 git@github.com:contributor1/repo.git
* ...
* git checkout --track -b develop origin/develop
* git checkout --track -b feature/billing develop
* git push feature/billing
* pull request from feature/billing to upstream develop
* await merge from upstream
