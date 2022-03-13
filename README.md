<!-- ⚠️ This README has been generated from the file(s) "README.md" ⚠️--><!-- ⚠️ This README has been generated from the file(s) "README.md" ⚠️-->
[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#renovate-purge-deps-reproduction)


[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#-renovate-purge-deps-reproduction)

# ➤ ➤ Renovate Purge Deps Reproduction

Currently renovate purges indirect dependencies from other (not only root) package-lock files inside a lerna monorepo if a direct dependency is being updated by renovate.
This causes the dependency graph for those packages to be broken.

Example below:

![caseinpoint](https://user-images.githubusercontent.com/4698322/158016439-339b65d0-8fc1-4960-8fb5-451cd3897e65.PNG)

This causes commander to be missing from the root package.json and not available

See: [Discussion](https://github.com/renovatebot/renovate/discussions/14618)
