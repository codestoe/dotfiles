# dotfiles
> Setup and sync your Mac system in the quickest way possible.

## Overview
This dotfiles project is a combination of some shell scripts and configuration files. The shell scripts automate setup and installation of dev tools, apps, symlinks, and other things. The "dotfiles" are simply local configuration files that we're moving to Dropbox in order to sync multiple systems to the same configuration.

### Why?
New computers are hard to setup without automation and keeping all of your machines in sync is painful. A system like this solves it all.

### How It Works
It's pretty straightforward. This system:

* Runs a shell script that automates the installations of command line tools, package managers, and Mac applications.
* Runs a shell script that automates your MacOS preferences.
* Symlinks your shell configurations, git configs and any other configs to Dropbox, allowing all of your machines to sync up to the same configuration.
* Symlinks application configurations using Mackup.
* Allows you to separate your personal and work configurations to keep things organized.

** Note: Mackup can automate your entire system for you, but I chose not to use that because it's hard to keep track of what Mackup is doing. Instead, I only use Mackup to sync apps that do not support native Dropbox sync.

### Folder Structure
I store this repo in icloud, in a folder named `.config`.

### Setup scripts

* [bootstrap](/dotfiles/scripts/bootstrap) - Install and configure packages managed by Homebrew, Yarn/NPM, Homebrew Cask, Mac App Store.
* [setup_mac](/dotfiles/scripts/setup_mac) - Set your macOS defaults. Reboot required.
* [setup_symlinks](/dotfiles/scripts/setup_symlinks) - Symlinks local config files to your Dropbox config folder.