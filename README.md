ssh-askpass
===========

ssh-askpass for macOS X. Works in (at least) 10.7+ (including Mojave and Big Sur)

Used to accept (or deny) the use of the private key(s) added to the SSH authentication agent with `ssh-add -c`.

![Screenshot](https://github.com/gaelicWizard/ssh-askpass/raw/main/sample/ssh-askpass.png)

**If you’re having trouble with ssh-askpass after OS upgrade, please follow the installation steps again.**

## Installation

### [Homebrew](http://brew.sh/)
* Run:

    ```
    $ brew install gaelicWizard/Tools/ssh-askpass
    ```
* Follow caveats

### Without Homebrew

* Run:
```
$ cp ssh-askpass /usr/local/bin/
$ cp ssh-askpass.plist ~/Library/LaunchAgents/
$ launchctl load -w ~/Library/LaunchAgents/ssh-askpass.plist
```
* No need to log out; you can add keys to the agent with `ssh-add -c`

## Enabling keyboard navigation
For security reasons ssh-askpass defaults to cancel since it's too easy to
press spacebar and accept a connection or other actions which might use
ssh-keys. To make it easier to press `OK`:

* Go to `System Preferences` and then `Keyboard`.

#### Pre 10.11
* Under the `Keyboard` tab, click on `All controls`.

#### 10.11+
* Under the `Shortcuts` tab, click on `All controls`.

Now you can press ⇥+spacebar to press `OK`.

## License
ISC license

## Contributors
* [theseal](https://github.com/theseal)
* [simmel](https://github.com/simmel)
