# Computer Setup and Management

This is how I set up a new computer/manage my current computer.

As I change what I have installed, tools I use, configurations I set, etc., I immediately update this repo. This keeps my environment organized and deterministic. Well, most of the time at least.

Since I always try to avoid reinventing the wheel and instead like to find best-in-breed resources, this setup relies heavily on other tried-and-true setups, configurations, and conventions, with my tools and small configurations added on.

These steps set up a brand new mac out of the box.

# The Steps

- Map caps lock key to escape.
- Install used applications from the Mac App store, including xcode.
- Open/setup xcode
- Run the Thoughtbot setup script from [here](https://github.com/thoughtbot/laptop).
- Clone this repo to `~/`
- Symlink `.zshrc`, `.vimrc`, `.gitconfig`, and `.default-npm-packages` to `~/`.
- Install user apps and etc. by running `install_user.sh`.
- Install dev apps and etc. by running `install_dev.sh`.
- Configure iTerm so new tabs open in same directory as last session.
- Sync 1Password vault.
- Add Google account to computer.
- Symlink VeraCrypt (`ln -s /Applications/VeraCrypt.app/Contents/MacOS/VeraCrypt /usr/local/bin/veracrypt`)
- Create ssh key, instructions [here](https://help.github.com/articles/generating-ssh-keys/).
- Add ssh key to Github, Heroku, and so on.
- Set Mac defaults by running `update_mac_settings.sh`.
- Install favorited applications from Setapp.
- Setup Alfred, Google Drive, Bartender.
- Change computer name.
- Setup personal secure backup scheme. Further details in Block.

# Misc

## Setup Postgres
```shell
createdb
createuser -s postgres
```

## Setup NeoVim
`~/.config/nvim/init.vim`
```shell
set runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath=&runtimepath
source ~/.vimrc
```
`:checkhealth`
