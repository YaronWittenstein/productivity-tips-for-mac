### Productivity on Mac
<br>

#### Recommended Settings:

1. System Sounds
  turn off `Play user interface sounds effects`

1. [Homebrew](https://brew.sh/) - The missing package manager for macOS
  * installation command:
    ```zsh
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

1. [iTerm2](https://www.iterm2.com/) - A better OSX terminal
    * Shortcuts
      ```
      ⌘ + ⏎  # toggle full-screen
      ⌘ + K  # clear terminal
      ⌃ + W  # delete word backwards
      ```
    * Customised Key Mappings (_Keys_)
      ```
      Key Combination | Action
      -------------------------
      ⌘ h             | Send ^H Backspace
      ⌃ a             | Send Hex Codes: 0x28
      ⌃ e             | Send Hex Codes: 0x20 0x3d 0x20
      ⌘ ←             | Previous Tab
      ⌘ →             | Next Tab
      ```
   * Working Directory (_Profiles_ -> _Working Directory_ -> _Directory_ )
   * `open .`
   * reset zsh history
    `vim ~/.zsh_history`
   * vi-mode
1. [Tmux](https://github.com/tmux/tmux/wiki) - A Terminal multiplexer
1. [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) - A better shell
    * installation:
    ```zsh
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
    ```

    * [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
    * [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
    * gem
    * bundler
    * rvm
    * brew
    * mix
    * git
    * vi-mode

1. [Caffeine](http://lightheadsw.com/caffeine/) - Don't let your mac fall asleep
1. [evernote](https://evernote.com/download) - Note manager
1. Chrome Settings:
   * Downloads
     * go to `chrome://settings` in the address bar
     * click on `Advanced`
     * change the default `Location`
     * turn on `Ask where to save each file before downloading`

1. Chrome plugins
    * [JSONView](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=en)
    * [Save to Pocket](https://chrome.google.com/webstore/detail/save-to-pocket/niloccemoadcdkdjlinkgdfekeahmflj?hl=en)
    * [Evernote Web Clipper](https://chrome.google.com/webstore/detail/evernote-web-clipper/pioclpoplcdbaefihamjohnefbikjilc?hl=en)
    * [1Password](https://chrome.google.com/webstore/detail/1password-password-manage/aomjjhallfgjeglblehebfpbcfeobpgk?hl=en)
    * [Send from Gmail (by Google)](https://chrome.google.com/webstore/detail/send-from-gmail-by-google/pgphcomnlaojlmmcjmiddhdapjpbgeoc?hl=en)
    * [Octotree](https://chrome.google.com/webstore/detail/octotree/bkhaagjahfmjljalopjnoealnfndnagc)
1. Chrome shortcuts:
    ```
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
    * remap ⇪ to _Esc_
1. Git aliases (gp, gl, gmd, gmm, gsq, grhh) [note that oh-my-zsh brings most of these by default]
    ```
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
1. [Alfred](https://www.alfredapp.com/) - Spotlight in steroids (extreme search, hot-keys, workflows, keywords etc)
    * [Kill Process (kill _PROCESS_)](https://github.com/ngreenstein/alfred-process-killer)
    * [Flush DNS (fdns)](https://github.com/cdraeger/alfred2-flushdns-workflow)
    * [Password Generator (pwgen 10)](https://github.com/deanishe/alfred-pwgen)
    * [TimeZones (tz london)](https://github.com/zenorocha/alfred-workflows/blob/master/time-zones/time-zones.alfredworkflow)
    * [Dictionary (define _WORD_)](https://www.alfredapp.com/help/features/dictionary/)
    * [StackOverflow Search (.so ...)](http://www.packal.org/workflow/stackoverflow-search)
    * [Dash (dash ...)](https://www.alfredapp.com/blog/productivity/dash-quicker-api-documentation-search/)
1. [Dash](https://kapeli.com/dash)
1. [FlexiGlass](https://www.nulana.com/flexiglass/)
1. [PopClip](http://pilotmoon.com/popclip/)
    * [Extensions](http://pilotmoon.com/popclip/extensions/)
1. [Yoink](https://eternalstorms.at/yoink/)
1. [Owl](https://itunes.apple.com/il/app/owl/id916200155?mt=12)
1. [FlyCut](https://itunes.apple.com/il/app/flycut-clipboard-manager/id442160987?mt=12)
1. [aText](http://www.trankynam.com/atext/)
    * iCloud sync
1. [Clear](https://itunes.apple.com/us/app/clear-todos/id493136154?mt=8)
    * iCloud sync
1. Sticky Notes
1. [Unclutter](https://unclutterapp.com/)
    * Dropbox sync
1. [anki](https://apps.ankiweb.net/)
    * [How to Increase Your Brain's Cache Hits?](https://www.youtube.com/watch?v=vAltVK7aMEw)
1. [Paw](https://paw.cloud/)
1. [fzf](https://github.com/junegunn/fzf)
    * ⌃+R
    * preview files
1. [numi](https://numi.io/)
1. [ctags](https://github.com/universal-ctags/homebrew-universal-ctags)
1. [ag](https://github.com/ggreer/the_silver_searcher)
1. [rg](https://github.com/BurntSushi/ripgrep)
1. [htop](https://hisham.hm/htop/)
1. tree
1. [diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)
1. [increasing keyboard repeat rate](https://apple.stackexchange.com/questions/10467/how-to-increase-keyboard-key-repeat-rate-on-os-x)
    ```
    defaults write -g InitialKeyRepeat -int 10  # normal minimum is 15 (225 ms)
    defaults write -g KeyRepeat -int 1          # normal minimum is 2 (30 ms)
    ```
1. [vim](http://www.vim.org/)/[neovim](https://neovim.io/)
1. [emacs](https://www.gnu.org/software/emacs/)
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
