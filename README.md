# Package Cheatsheet

A curated cheat sheet to hands on all kinds of package manager

|                                | **apt**                             | **🍺 Homebrew**                    | **🐍 Python**                               | **npm**                   | **💎 Ruby**                                   |
| ------------------------------ | ----------------------------------- | ---------------------------------- | ------------------------------------------- | ------------------------- | --------------------------------------------- |
| Search                         | `apt search [query]`                | `brew search [query]`              | `pip search [query]`                        | `npm search [query]`      | `gem serach [query]`                          |
| Install                        | `apt install [package]`             | `brew install [formula/cask]`      | `pip install [package]`                     | `npm install [package]`   | `gem install [gem]`                           |
| Install from list              | `xargs -a list.txt apt install`     |                                    | `pip install -r requirements.txt`           |                           |                                               |
| Install for project            | -                                   | -                                  |                                             | `npm install`             | `bundle install`                              |
| Uninstall                      | `apt remove [package]`              | `brew uninstall [formula/cask]`    | `pip uninstall [package]`                   | `npm uninstall [package]` | `gem uninstall [gem]`                         |
| Uninstall all                  |                                     | `brew remove --force $(brew list)` | `pip uninstall -y -r <(pip freeze)`         | `npm uninstall *`         | `gem uninstall -aIx`                          |
| Upgrade                        | `apt upgrade [package]`             | `brew upgrade [formula/cask]`      | `pip install --upgrade [package]`           |                           | `gem update [gem]`                            |
| Upgrade all                    | `apt upgrade`                       | `brew upgrade`                     | <sup>[1](#pip-upgrade-all)</sup>            |                           |                                               |
| List installed (System)        | `apt list`                          | `brew list`                        | `pip list`                                  | `npm list -g`             | `gem list`                                    |
| List installed (Project)       | -                                   | -                                  | `pip freeze`                                | `npm list`                | `bundle list`                                 |
| List upgradable                | `apt list --upgradable`             | `brew outdated`                    | `pip list --outdated`                       | `npm outdated`            | `gem outdated`, `bundle outdated`             |
| List undepend                  |                                     | `brew leaves`                      | `pip list --not-required`                   |                           |                                               |
| Information                    | `apt show [package]`                | `brew info [formula/cask]`         | `pip show [package]`                        | `npm view [package]`      | `gem info [gem]`                              |
| Depend on (dependency)         | `apt depends [package]`             | `brew deps [formula/cask]`         | `pipdeptree --packages [package]`           |                           | `gem dependency [gem]`                        |
| Depend by (reverse dependency) | `apt rdepends [package]`            | `brew uses [formula/cask]`         | `pipdeptree --reverse --packages [package]` |                           | `gem dependency [gem] --reverse-dependencies` |
| List source                    | `apt policy`                        | `brew tap`                         | -                                           |                           | `gem sources --list`                          |
| Add source                     | `add-apt-repository [ppa]`          | `brew tap [repo/url]`              | -                                           |                           | `gem sources --add [uri]`                     |
| Remove source                  | `add-apt-repository --remove [ppa]` | `brew untap [repo/url]`            | -                                           |                           | `gem sources --remove [uri]`                  |
| Update from source             | `apt update`                        | `brew update`                      | -                                           |                           | `gem sources --update`                        |
| Cleanup all cache              | `apt clean`                         | `brew cleanup --prune=all`         | `pip cache purge`                           |                           | `gem sources --clear-all`                     |
| Cleanup useless cache          | `apt autoclean`                     | `brew cleanup`                     | -                                           |                           |                                               |
| Uninstall useless              | `apt autoremove`                    | `brew autoremove`                  |                                             |                           |                                               |
| Healthcheck                    |                                     | `brew doctor`                      |                                             |                           |                                               |

<a name="pip-upgrade-all">1</a>: `pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip install -U`

## TODO

Turn this into a frontend website with copy-to-clipboard function.
