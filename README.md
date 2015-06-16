# How I setup my new system (manually)

- Adjust Trackpad Settings (System Preferences > Trackpad)
  - Tap to click
  - Secondary click

- Enable right click (System Preferences > Mouse)
- Adjust Keyboard settings (System Preferences > Keyboard)
  - Set CAPSLOCK to CTRL, because caps lock sucks. (> modifier keys)
  - Increase key repeat to very high

- Install [homebrew](http://brew.sh)
- Get some taps

  ```
  brew install caskroom/cask/brew-cask
  brew tap homebrew/services
  brew tap domt4/autoupdate
  brew autoupdate --start
  ```
- Start installing some stuff

  ```
  brew install vim tree mercurial bazaar wget z libyaml
  brew install chruby ruby-install mongodb mysql postgresql redis node
  brew install syncthing
  brew cask install iterm2 sublime-text flux slack hosts launchrocket sequel-pro unrarx 1password dropbox
  ```

- Rename system vim

  ```
  which vim
  mv /usr/bin/vim /usr/bin/vim72
  ```

- Log into Apple App store
  - install divvy
  - cloud.app
  - fantastical
- Install [Oh My Zsh](http://ohmyz.sh)
- Install [Solarized](http://ethanschoonover.com/solarized)
  - Then set it to be the theme for iTerm2
- Install [powerline patched fonts](https://github.com/powerline/fonts)
  - Then set it to be the non-standard unicode font
- Install [PragmatoPro font](http://www.fsd.it/fonts/pragmatapro.htm)
  - Then set it to be the standard character font
- Install [maximum awesome by square](https://github.com/square/maximum-awesome)
- Install [golang "manually"](http://golang.org/doc/install#osx)
- Customize zsh
- Set default search engine to DuckDuckGo

- Customize some low level stuff

  ```
  # Disable the sound effects on boot
  sudo nvram SystemAudioVolume=" "

  # Expand save panel by default
  defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true
  defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode2 -bool true

  # Expand print panel by default
  defaults write NSGlobalDomain PMPrintingExpandedStateForPrint -bool true
  defaults write NSGlobalDomain PMPrintingExpandedStateForPrint2 -bool true

  # Automatically quit printer app once the print jobs complete
  defaults write com.apple.print.PrintingPrefs "Quit When Finished" -bool true

  # Finder: show all filename extensions
  defaults write NSGlobalDomain AppleShowAllExtensions -bool true

  # Finder: show status bar
  defaults write com.apple.finder ShowStatusBar -bool true

  # Avoid creating .DS_Store files on network volumes
  defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool true

  # Disable Dashboard
  defaults write com.apple.dashboard mcx-disabled -bool true

  # Don’t show Dashboard as a Space
  defaults write com.apple.dock dashboard-in-overlay -bool true

  # Automatically hide and show the Dock
  defaults write com.apple.dock autohide -bool true

  # Prevent Safari from opening ‘safe’ files automatically after downloading
  defaults write com.apple.Safari AutoOpenSafeDownloads -bool false

  # Hide Safari’s bookmarks bar by default
  defaults write com.apple.Safari ShowFavoritesBar -bool false

  # Enable Safari’s debug menu
  defaults write com.apple.Safari IncludeInternalDebugMenu -bool true


  # Enable the Develop menu and the Web Inspector in Safari
  defaults write com.apple.Safari IncludeDevelopMenu -bool true
  defaults write com.apple.Safari WebKitDeveloperExtrasEnabledPreferenceKey -bool true
  defaults write com.apple.Safari com.apple.Safari.ContentPageGroupIdentifier.WebKit2DeveloperExtrasEnabled -bool true


  # Don’t display the annoying prompt when quitting iTerm
  defaults write com.googlecode.iterm2 PromptOnQuit -bool false
  ```

- Create new SSH key (https://help.github.com/articles/generating-ssh-keys/) or sometimes copy existing key
- Add key to github/stash/etc
- Make some standard dirs
  - `~/repos`
  - `~/go`
  - `~/sync` (if using syncthing)
