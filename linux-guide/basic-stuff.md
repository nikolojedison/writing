# Basic Introduction
Some quick things before we get started that Linux does differently:
* the command line in Linux is called the *shell*; in almost every version of Linux you'll be using a shell called `bash` (*B*ourne *A*gain *Sh*ell). Shell scripts (collections of command-line commands saved into an editable file) normally end with the extension `.sh` - you'll pretty much never see .exe files work with Linux.
* Linux comes in a variety of kinds, called *distributions* or more commonly *distros*. Distros based off of a kind called Debian are normally the most common, and the most stable/least amount of breaking.
* forward slash ( / ) instead of back slash ( \ ) in file paths - this one's especially important as the back slash is used to provide special characters, like the newline, or in other situations.
* *directories* instead of *folders* - This is mostly just a change in terminology. There might be some more complex stuff behind the scenes to differentiate the two, but I haven't learned that yet.
* `Tab` when typing a command, filename, or command option to auto-complete the command, filename, or command option in question. Depending on what you're using, if there's multiple options (`filename.png` and `filename2.png`), repeated presses of `Tab` will reveal the options for you. 

## Common Terminal Tools
### Navigation/Maintenance
* `man` - command-line reference manual. Normal usage is `man [program name]`, and a page will appear with the name of the command, a synopsis, a description, some examples, a general overview, the default options, some explanations of the command's options, related commands, and other information. This page can be navigated with the arrow keys, Page Up/Page Down, or j/k.
* `cd` - stands for *c*hange *d*irectory. Strangely, there isn't a `man` page for `cd`, but you can get a general idea of it by googling some examples. Do `cd` to return to your home directory, `cd [directory name]` to change to a directory (so long as it's directly inside your current directory - for example, `/home/nik/` has the directories `Documents/ Downloads/ Music/ Pictures/ Videos/`, so you either have to type `cd /home/nik/Documents/` to get to nik's Documents/ direrctory, or you have to be in the `/home/nik` directory and type `cd Documents/`). 
In order to move a directory back (`/home/nik/Documents/` to `/home/nik/`), type `cd ..`. This works for nearly every directory except the root directory ( `/` ).
* `ls` - one of the simplest commands, ls lists the files in your current directory. You can use `ls` similarly to `cd`, in the sense that you can type a directory after `ls` (`ls /home/nik/Downloads/` or `ls /etc/`) and the contents of that directory will be listed. If you want to see hidden files (basically any file with a dot as the start of the filename in Linux is a hidden file; for example, `.tmux.config`), do `ls -a` (`-a` for all, in this case). 
`ls -ls` or `ls -la` shows additional information about the files, including the permissions (Read/Write/Execute), owner, size (in bytes), and time of creation alongside each file or directory's name. `ls -ls` functions similarly to the standard `ls` command, while `ls -la` functions similarly to `ls -a`.
* `sudo` - stands for *s*uper *u*ser *do*. Essentially the command-line version of administrator privileges in Linux, you'll need to do `sudo` before some commands in order for them to work. Some examples of these programs would be `apt-get` (used to update and install new software from the command line, will be explained later), or when you're editing files that are restricted by the system (mostly system files that Linux needs to run).

### Editing

### Web Browsing

---
## Common GUI Tools
### Navigation

### Editing 

### Web Browsing

