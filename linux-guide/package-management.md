# Package Management & Updates

## apt/apt-get
`apt-get`is a versatile tool for handling the installation and updating of packages and programs in some versions of Linux (mostly distros based off of Debian or Ubuntu). Recently, there's been a push to start using `apt` instead of `apt-get`, since `apt` manages packages in a way that's more end-user-friendly & can deal with the *apt cache*. 

### Managing packages with apt
Please note that whether you use `apt` or `apt-get` (and for do-release-upgrade), you have to put `sudo` in front in order for the tool to install or upgrade packages - otherwise, it won't have the proper permissions needed. 
Additionally, unless otherwise noted here, `apt` commands work with `apt-get`, and vice versa.
* `apt install [package name]` - installs the package requested
* `apt update` - updates the list of packages' locations on the internet, should almost always be run before `apt upgrade` to prevent "not found" errors
* `apt upgrade` - upgrades most packages that have a new release to their latest version
* `apt dist-upgrade` - upgrades more important packages that aren't touched by `apt upgrade` due to stability reasons
* `do-release-upgrade` - upgrades the operating system to the next system update

> As a sidenote, this is a great time to explain Ubuntu's release/upgrade structure.
> Major releases of Ubuntu occur twice a year - once in April (the x.04 release), and once in October (the x.10 release). Every two years, a **L**ong **T**erm **R**elease (LTS) will be released in April as a x.04 LTS release. These versions have support for 5 years from their release date, and are designed to be the most stable versions of Ubuntu.

## apropos
`apropos` is a tool for searching the `man` pages, and is often useful for finding common packages or programs to install with `apt`. Usage is similar to `apt`; that is, `apropos [package name]` to find a package.

