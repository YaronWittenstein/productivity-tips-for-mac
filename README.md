# Productivity Tips for Mac


![mac](https://bit.ly/2zYvwHy)


## Recommended Settings:

1. Authorize Mac
    * `iTunes -> Account -> Authorizations -> Authorize This Computer..`
1. System Sounds
    * Go to `System Preferences -> Sound`
    * Turn off `Play user interface sounds effects`
1. [Homebrew](https://brew.sh/) - The missing package manager for macOS
    * installation command:
    ```zsh
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```
1. [iTerm2](https://www.iterm2.com/) - A better OSX terminal
    * Shortcuts
      ```zsh
      ⌘ + ⏎  # toggle full-screen
      ⌘ + K  # clear terminal
      ⌃ + W  # delete word backwards
      ```
    * Customised Key Mappings (_Keys_)
      ```zsh
      Key Combination | Action
      -------------------------
      ⌘ h             | Send ^H Backspace
      ⌃ a             | Send Hex Codes: 0x28
      ⌃ e             | Send Hex Codes: 0x20 0x3d 0x20
      ⌘ ←             | Previous Tab
      ⌘ →             | Next Tab
      ```
    * Command (_Profiles_ -> _General_ -> _Command_)
      `zsh`
    * Working Directory (_Profiles_ -> _General_ -> _Working Directory_)
      `Reuse previous session's Directory`
    * `open .`
    * reset zsh history
      `vim ~/.zsh_history`
    * vi-mode (see later `dotfiles` and `oh-my-zsh`)
    * disable the `Last login` message
      * `touch ~/.hushlogin`
    * `Profiles -> Text`
      * Cursor
        * `Box`
        * turn-off `Blinking cursor`
      * Text Rendering
        * turn off `Draw bold text in bold font`
        * turn off `Blinking text allowed`
        * turn off `Italic text allowed`
      * Font
        * `14pt Monaco`
    * `Profiles -> Window`
      * Columns: 120
      * Rows: 20
    * Enable `View -> Show Tabs in Fullscreen (⇧ ⌘ T)`
1. [fzf](https://github.com/junegunn/fzf)
    * first install `fd` by `brew install fd` (since we have in zhrc `export FZF_DEFAULT_COMMAND='fd --type f'`)
    * ⌃+R
    * preview files
1. [ctags](https://github.com/universal-ctags/homebrew-universal-ctags)
1. [ag](https://github.com/ggreer/the_silver_searcher)
1. [rg](https://github.com/BurntSushi/ripgrep)
1. [exa](https://the.exa.website/) - A modern replacement for ls
1. [htop](https://hisham.hm/htop/) - an interactive process viewer
1. tree - list a directory
1. [diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)
  ```zsh
  brew install diff-so-fancy
  ```
1. [Tmux](https://github.com/tmux/tmux/wiki) - A Terminal multiplexer
1. Programming Languages
    * [Rust](https://www.rust-lang.org/en-US/install.html)
      * `curl https://sh.rustup.rs -sSf | sh` # all tools are installed under `~/.cargo/bin`
      * `rustc --version` # returns the installed Rust version
      * [racer](https://github.com/racer-rust/racer)
    * [Elixir](https://elixir-lang.org/install.html#mac-os-x)
      * `brew install elixir`
      * `elixir --version` # returns the installed Elixir version
    * [rbenv](https://github.com/rbenv/rbenv)
      * `brew install rbenv`
      * [rbenv-gemset](https://github.com/jf/rbenv-gemset)
        ```zsh
        brew install rbenv-gemset
        ```
      * [ruby-build](https://github.com/rbenv/ruby-build)
        ```zsh
        # Using Homebrew on macOS
        $ brew install ruby-build

        # As an rbenv plugin
        $ mkdir -p "$(rbenv root)"/plugins
        $ git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build

        # As a standalone program
        $ git clone https://github.com/rbenv/ruby-build.git
        $ PREFIX=/usr/local ./ruby-build/install.sh
        ```
    * Go
      * `brew install go`
      * `go version` # returns the installed Go version
      * [gocode](https://github.com/mdempsky/gocode)
        ```zsh
        go get -u github.com/mdempsky/gocode
        ```
    * Python
      ```zsh
      brew install readline xz
      brew install pyenv
      brew install pyenv-virtualenv
      ```
    * [JVM](https://java.com/en/download/)
1. [Adding a new SSH key to your GitHub account](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
    * This will enable us to do `git clone git@github.com:XXXXXXX`
1. [neovim](https://neovim.io/)
    * `brew install neovim`
    * install [vim-plug](https://github.com/junegunn/vim-plug/wiki/tutorial)
      ```zsh
      curl -fLo ~/.config/nvim/autoload/plug.vim --create-dirs \
      https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
      ```
    * install neovim plugins by running in neovim `:PlugInstall`
1. install dotfiles
    ```zsh
    cd ~/
    git clone git@github.com:YaronWittenstein/dotfiles.git   # will create `~/dotfiles` locally
    git clone git@github.com:YaronWittenstein/dotvim.git     # will create `~/dotvim`   locally
    git clone git@github.com:YaronWittenstein/dotemacs.git   # will create `~/dotemacs` locally
    rm ~/.zshrc
    rm ~/.gemrc
    rm ~/.ctags
    rm ~/.gitconfig
    rm ~/.vimrc
    rm ~/.config/nvim/init.vim
    rm ~/.emacs.d
    ln -s ~/dotfiles/.zshrc ~/.zshrc
    ln -s ~/dotfiles/.gemrc ~/.gemrc
    ln -s ~/dotfiles/.ctags ~/.ctags
    ln -s ~/dotfiles/.gitconfig ~/.gitconfig
    ln -s ~/dotfiles/.vimrc ~/.vimrc
    ln -s ~/dotvim/init.vim ~/.config/nvim/init.vim
    ln -s ~/dotemacs ~/.emacs.d
    ```
1. [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) - A better shell
    * installation:
    ```zsh
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
    ```
    * [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
    ```zsh
    git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions

    # add to zshrc
    source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
    ```
    * [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
    ```zsh
    brew install zsh-syntax-highlighting

    # add to zshrc
    source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
    ```

    * list of plugins:
    ```
    cargo
    rustup
    go
    ruby
    bundler
    rbenv
    gem
    mix
    rust
    brew
    osx
    gem
    git
    gitfast
    git-remote-branch
    dirhistory
    cp
    vi-mode
    last-working-dir
    zsh-autosuggestions
    zsh-syntax-highlighting
    ```
1. [Caffeine](http://lightheadsw.com/caffeine/) - Don't let your mac fall asleep
1. [evernote](https://evernote.com/download) - Note manager
1. Chrome Settings:
   * Downloads
     * go to `chrome://settings` in the address bar
     * click on `Advanced`
     * change the default `Location`
     * turn on `Ask where to save each file before downloading`
1. Chrome plugins
    * [Grammarly](https://chrome.google.com/webstore/detail/grammarly-for-chrome/kbfnbcaeplbcioakkpcpgfkobkghlhen?hl=en)
    * [JSONView](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=en)
    * [Save to Pocket](https://chrome.google.com/webstore/detail/save-to-pocket/niloccemoadcdkdjlinkgdfekeahmflj?hl=en)
    * [Evernote Web Clipper](https://chrome.google.com/webstore/detail/evernote-web-clipper/pioclpoplcdbaefihamjohnefbikjilc?hl=en)
    * [1Password](https://chrome.google.com/webstore/detail/1password-password-manage/aomjjhallfgjeglblehebfpbcfeobpgk?hl=en)
    * [Send from Gmail (by Google)](https://chrome.google.com/webstore/detail/send-from-gmail-by-google/pgphcomnlaojlmmcjmiddhdapjpbgeoc?hl=en)
    * [Octotree](https://chrome.google.com/webstore/detail/octotree/bkhaagjahfmjljalopjnoealnfndnagc)
1. Chrome shortcuts:
    ```zsh
    ⌘ + l      # Jump to the address bar
    ⌘ + n      # Open a new window
    ⌘ + ⇧ + n  # Open a new window in Incognito mode
    ⌘ + ⇧ + t  # Reopen the last closed tab, and jump to it
    ⌥ + ⌘ + j  # Open the JavaScript Console
    Esc        # Stop the page loading
    ⌘ r        # Reload your current page
    ⌘ ⇧ r      # Reload your current page, ignoring cached content
    ⌘ +        # Make everything on the page bigger
    ⌘ -        # Make everything on the page bigger
    ⌘ f        # Open the Find Bar to search the current page
    ⌘ g        # Jump to the next match to your Find Bar search
    ⌘ ⇧ g      # Jump to the previous match to your Find Bar search
    ```
    * chrome://chrome-urls/
      * chrome://settings (shortcut: `⌘ ,`)
      * chrome://extensions
1. [Github shortcuts:](https://help.github.com/articles/using-keyboard-shortcuts/)
    * find commit `t`
    * change in the commit url: `/commit` to `/tree`
    * search for a file using `t`
1. [Karabiner](https://pqrs.org/osx/karabiner/) - A powerful and stable keyboard customizer
    * open `Karabiner - Elements`
    * click on `⊕ Add item`
    * select `caps_lock` under `From key` and `escape` under `To key`

1. Git aliases (gp, gl, gmd, gmm, gsq, grhh) [note that oh-my-zsh brings most of these by default]
    ```zsh
    gp    # git push
    gl    # git pull
    gd    # git diff
    gs    # git status -sb
    gmd   # git merge develop
    gmm   # git merge master
    gac   # git add --all; git commit -m
    glg   # git log
    grhh  # git rest HEAD --hard
    gsq   # git rebase -i
    ```
1. [Tower](https://www.git-tower.com/) + [Kaleidoscope](https://www.kaleidoscopeapp.com/) - Version control with Git - made easy
1. [Github for Mac](https://desktop.github.com/)
1. [Dash](https://kapeli.com/dash)
1. Hide Spotlight
  * `System Preferences -> Spotlight -> Privacy -> Keyboard Shortcuts...`
    * turn off `Show Spotlight search`
    * turn off `Show Finder search window`
  * Important: don't Disable `Spotlight` indexing since `Alfred` relies on it
1. [Alfred](https://www.alfredapp.com/) - `Spotlight` in steroids (extreme search, hot-keys, workflows, keywords etc)
    * Make sure that Spotlight indexing is running
      `sudo mdutil -a -i on`
    * Recommended Settings
      * `General`
        * Turn on 'Launch Alfred at login'
        * Alfred Hotkey: `⌘ Space`
      * `Features`
        * `File Search`
          * Opening Files: `o` (`open` is the default)
    * Alfred Workflows
      * [Kill Process (kill _PROCESS_)](https://github.com/ngreenstein/alfred-process-killer)
      * [Flush DNS (fdns)](https://github.com/cdraeger/alfred2-flushdns-workflow)
      * [Password Generator (pwgen 10)](https://github.com/deanishe/alfred-pwgen)
      * [TimeZones (tz london)](https://github.com/zenorocha/alfred-workflows/blob/master/time-zones/time-zones.alfredworkflow)
      * [Dictionary (define _WORD_)](https://www.alfredapp.com/help/features/dictionary/)
      * [StackOverflow Search (.so ...)](http://www.packal.org/workflow/stackoverflow-search)
      * [Dash (dash ...)](https://www.alfredapp.com/blog/productivity/dash-quicker-api-documentation-search/)
        * rename `dash` to `d` under the worflow `Script Filter`
1. [FlexiGlass](https://www.nulana.com/flexiglass/) - Window Mover
    * Recommended Settings
      * Move
        * turn on `Enabled`
        * under `Start moving when pressed` mark `⌥ Option` and select the `One finger` option
      * Resize
        * turn on `Enabled`
        * under `Start resizing when pressed` mark `⌥ Option` and select the `Two fingers` option
1. [PopClip](http://pilotmoon.com/popclip/)
    * [Extensions](http://pilotmoon.com/popclip/extensions/)
    * Recommended Extensions:
        * Base64 Encode
1. [Yoink](https://eternalstorms.at/yoink/)
1. [Owl](https://itunes.apple.com/il/app/owl/id916200155?mt=12)
1. [FlyCut](https://itunes.apple.com/il/app/flycut-clipboard-manager/id442160987?mt=12)
1. [aText](http://www.trankynam.com/atext/)
    * iCloud sync (`Preferences -> Sync)`
      * Select `Sync aText data to (choose iCloud Drive)`
      * Select `Sync aText's preferences`
1. [Clear](https://itunes.apple.com/us/app/clear-todos/id493136154?mt=8)
    * iCloud sync
1. Sticky Notes
1. [Unclutter](https://unclutterapp.com/)
    * Dropbox sync
1. [Skype](https://www.skype.com/en/get-skype/skype-for-mac/)
1. [Slack](https://slack.com/downloads/osx)
1. [Telegram](https://macos.telegram.org/)
1. [Atom](https://atom.io)
1. [Kindle for Mac](https://itunes.apple.com/il/app/kindle/id405399194)
1. [Pocket](https://getpocket.com/mac/)
1. [anki](https://apps.ankiweb.net/)
    * [How to Increase Your Brain's Cache Hits?](https://www.youtube.com/watch?v=vAltVK7aMEw)
1. [Paw](https://paw.cloud/)
1. [numi](https://numi.io/)
1. Keyboard Settings
    * `Key Repeat` -> Select `Fast`
    * `Delay Until Repeat` -> Select `Short`
1. [Increasing keyboard repeat rate](https://apple.stackexchange.com/questions/10467/how-to-increase-keyboard-key-repeat-rate-on-os-x)
    ```zsh
    defaults write -g InitialKeyRepeat -int 15  # normal minimum is 15 (225 ms)
    defaults write -g KeyRepeat -int 2          # normal minimum is 2 (30 ms)
    ```
1. [emacs](https://www.gnu.org/software/emacs/)
1. [cloc](https://github.com/AlDanial/cloc) - Count Lines of Code
    * `brew install cloc`
1. [PowerPhotos – Merge Mac Photos libraries, find duplicates, and more](https://www.fatcatsoftware.com/powerphotos/)
1. [Gemini 2: The Duplicate Finder](https://itunes.apple.com/us/app/id1090488118)
1. other:
    * eyes
      * [GUNNAR](https://gunnar.com/)
      * [f.lux](https://justgetflux.com/)
    * ears
      * [QuietComfort 35](https://www.bose.com/en_us/products/headphones/over_ear_headphones/quietcomfort-35-wireless-ii.html)
    * music
      * [Classic](https://www.youtube.com/watch?v=jgpJVI3tDbY)
      * [Hot Spring](https://www.youtube.com/watch?v=QsQfJ-n90nI)
1. [Cyberduck](https://cyberduck.io/) - a cloud storage browser
