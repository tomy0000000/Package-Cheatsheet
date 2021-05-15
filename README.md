# Package Cheatsheet

A curated cheat sheet to hands on all kinds of package manager

|                       | **apt**                             | **homebrew**                    | **pip**                                     | **npm**                   | **gem**                |
| --------------------- | ----------------------------------- | ------------------------------- | ------------------------------------------- | ------------------------- | ---------------------- |
| Search                | `apt search [query]`                | `brew search [query]`           | `pip search [query]`                        | `npm search [query]`      |                        |
| Install               | `apt install [package]`             | `brew install [formula/cask]`   | `pip install [package]`                     | `npm install [package]`   |                        |
| Uninstall             | `apt remove [package]`              | `brew uninstall [formula/cask]` | `pip uninstall [package]`                   | `npm uninstall [package]` |                        |
| Upgrade               | `apt upgrade [package]`             | `brew upgrade [formula/cask]`   | `pip install --upgrade [package]`           |                           |                        |
| List                  | `apt list`                          | `brew list`                     | `pip list`                                  | `npm list`                | `gem list`             |
| List upgradable       | `apt list --upgradable`             | `brew outdated`                 | `pip list --outdated`                       | `npm outdated`            |                        |
| List undepend         |                                     | `brew leaves`                   | `pip list --not-required`                   |                           |                        |
| Information           | `apt show [package]`                | `brew info [formula/cask]`      | `pip show [package]`                        | `npm view [package]`      | `gem info [gem]`       |
| Depend on             | `apt depends [package]`             | `brew deps [formula/cask]`      | `pipdeptree --packages [package]`           |                           | `gem dependency [gem]` |
| Depend by             | `apt rdepends [package]`            | `brew uses [formula/cask]`      | `pipdeptree --reverse --packages [package]` |                           |                        |
| List source           | `apt policy`                        | `brew tap`                      |                                             |                           |                        |
| Add source            | `add-apt-repository [ppa]`          | `brew tap [repo/url]`           |                                             |                           |                        |
| Remove source         | `add-apt-repository --remove [ppa]` | `brew untap [repo/url]`         |                                             |                           |                        |
| Update from source    | `apt update`                        | `brew update`                   | -                                           |                           |                        |
| Cleanup all cache     | `apt clean`                         | `brew cleanup --prune=all`      | `pip cache purge`                           |                           |                        |
| Cleanup useless cache | `apt autoclean`                     | `brew cleanup`                  | -                                           |                           |                        |
| Uninstall useless     | `apt autoremove`                    | `brew autoremove`               |                                             |                           |                        |
| Healthcheck           |                                     | `brew doctor`                   |                                             |                           |                        |

## TODO

Turn this into a frontend website with copy-to-clipboard function.