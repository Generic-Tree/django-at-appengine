# Django Project at AppEngine
> This intends to be an [readme-documented][-0], [open-source-licensed][-1], [semantic-versioned][-2],
[conventional-committed][-3] and [changelogged][-4] git repository starting point
for the development of a brand-new [twelve-factor][-5] Django project

A straightforward beginning for an open-source Django project repository

Beside brings GAE's expected file system structure, generic-named powered-up Django project base
and useful Makefile targets to help development process, it also provides deploy-on-push automation 
through the use of [Google's official deploy-appengine][>5] Github action.

[-0]: https://www.makeareadme.com/ "Make a README"
[-1]: https://choosealicense.com/licenses/ "Choose a License"
[-2]: https://semver.org/ "Semantic Versioning"
[-3]: https://www.conventionalcommits.org/en/v1.0.0/ "Conventional Commits"
[-4]: https://keepachangelog.com/en/1.0.0/ "Keep a Changelog"
[-5]: https://12factor.com/ "Twelve Factor"

[>1]: https://github.com/RichardLitt/standard-readme/blob/master/spec.md "Standard readme specification"
[>2]: https://www.repostatus.org "Repo maintenance status"
[>3]: https://choosealicense.com/licenses/gpl-3.0/ "GPL 3.0 License description"
[>4]: https://docs.djangoproject.com/en/3.2/intro/tutorial01/ "Django tutorial"
[>5]: https://github.com/google-github-actions/deploy-appengine "Github action: Deploy App Engine"
[>6]: https://console.developers.google.com/apis/api/appengine.googleapis.com "Google Cloud Console: App Engine Admin API"
[>7]: https://console.cloud.google.com/iam-admin/serviceaccounts "Google Cloud Console: Service Accounts"
[>8]: https://docs.github.com/en/free-pro-team@latest/actions/reference/encrypted-secrets "GitHub Docs: Secrets"

[!1]: https://github.com/generic-tree/root/generate "Github repository's template generation URL"

[B1]: https://img.shields.io/static/v1?label=create%20a%20new%20repository&message=%20&style=social "Create new repository"
[B2]: https://www.repostatus.org/badges/latest/active.svg "Repostatus active badge"
[B3]: https://img.shields.io/github/license/artu-hnrq/Django_GoogleAppEngine_Template?color=green "License badge"

### Table of Contents
<details>
  <summary>See all</summary>

  * [Getting started](#getting-started)
    * [Development environment](#development-environment)
    * [Repo publication](#repo-publication)
  * [Project specifications](#project-specifications)
    * [Features](#features)
    * [Folder structure](#folder-structure)
  * [Maintenance](#maintenance-)
  * [License](#license-)

</details>


## Getting started
First of all, [![create a new repository][B1]][!1] from this template, \
Name it accordingly and place where it best fits for your team.

### Development environment
Make sure you have `Git`, `Make` and `Python` installed:
```bash
$ git --version
git version 2.25.1
$ make --version
GNU Make 4.2.1
$ python3 --version
Python 3.9.0+
```

Thus, clone the recent-created repository locally,
and set up its development environment:

```bash
$ make init
$ . venv/bin/activate
```

Finally, you are ready to create [your Django's first app][>4]
and proceed developing your application.

### Continuos deployment setup
You will need to have a *Google Cloud Project* configured.
So, through its console, enable the [App Engine Admin API][>6]
and also set up a [Service Account][>7] to your project,
registering its key into your fresh-repo [secrets][>8]
as `GCP_SA_KEY`.

For more details, check [deploy appengine][>5] action description. 

### Repo publication
After all, you should make this project your own: \
Write a good README to present it to the world. \
And also ensure to tailor the project license to your needs.


## Project specifications
Here some descriptions about this template project:

### Features
This project shortens a repository start setup, considering:
* Inclusion of a mature README document, inspired by [Standard Readme][>1]
* Inclusion of an open-source LICENSE file
* Inclusion of a structured, yet raw, CHANGELOG file
* Compliance with widely-used version control conventions, such as:
    * [Semantic Versioning][-2]
    * [Conventional Commit][-3]
    * [Keep a Changelog][-4]

It also powers up development workflow by:
* Inclusion of an appropriate .gitignore and .gcloudignore files
* Inclusion of a minimal requirements file
* Inclusion of a proficient Makefile that improve development management
* Inclusion of preconfigured Django project settings functionalities
* Inclusion of a structed app.yaml (App Engine service settings) file

And configures continuous delivery workflow to:
* Deploy application on Google App Engine

### Folder structure
```
.
????????? .git/                       Version control system folder
????????? .github                     Github repo's configuration directory
???   ????????? workflows               Continuous integration settings
???       ????????? deploy.yml          Deploy-on-push automation descriptor
????????? .gcloudignore               GCP ignored files manifest
????????? .gitignore                  VCS ignored files manifest
????????? app.yml                     App Engine service settings
????????? CHANGELOG.md                Release notes description
????????? LICENSE                     License file
????????? Makefile                    Development management facilities
????????? README.md                   Repo readme document
????????? requirements.txt            Python dependency descriptor
????????? src
    ????????? __project__             Django project root folder
    ????????? manage.py               Django's command-line utility
```


## Maintenance [![][B2]][>2]
This project is maintained by the author, [@artu-hnrq](https://github.com/artu-hnrq). \
It has reached a stable, usable state and is being **actively developed**.


## License [![][B3]][>3]
This project is published under the permissions established by [GNU General Public License v3.0][>3].

