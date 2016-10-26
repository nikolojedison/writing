# Basic Introduction
I won't go over how to get to GUI programs as much; I figure you can play around with Ubuntu on your own and get the gist of opening the terminal, using Firefox, the Ubuntu Software Centre, and other such tools on your own -- I trust you're intelligent. You can use LibreOffice to open any Word or Office files you'd normally use Office for in Windows, in case you wanna try homework, and you can either use Firefox (if I recall correctly, it comes built-in) or install Chromium (Google Chrome's open-source version for Linux. There's normal Chrome for Linux too, but it's normally easier to use Chromium due to its speed and other reasons.). 
Some quick things before we get started that Linux does differently:
* the command line in Linux is called the *shell*; in almost every version of Linux you'll be using a shell called `bash` (**B**ourne **A**gain **Sh**ell). Shell scripts (collections of command-line commands saved into an editable file) normally end with the extension `.sh` - you'll pretty much never see .exe files work with Linux.
* Linux comes in a variety of kinds, called *distributions* or more commonly *distros*. Distros based off of a kind called Debian are normally the most common, and the most stable/least amount of breaking.
* forward slash ( / ) instead of back slash ( \ ) in file paths - this one's especially important as the back slash is used to provide special characters, like the newline, or in other situations.
* *directories* instead of *folders* - This is mostly just a change in terminology. There might be some more complex stuff behind the scenes to differentiate the two, but I haven't learned that yet.
* `Tab` when typing a command, filename, or command option to auto-complete the command, filename, or command option in question. Depending on what you're using, if there's multiple options (`filename.png` and `filename2.png`), repeated presses of `Tab` will reveal the options for you. 
* If for any reason you need to stop a program and it isn't responding, `Ctrl+c` will stop it for you. You probably shouldn't use `Ctrl+c` otherwise, though.

## Common Terminal Tools
### Navigation/Maintenance
* `man` - command-line reference manual. Normal usage is `man [program name]`, and a page will appear with the name of the command, a synopsis, a description, some examples, a general overview, the default options, some explanations of the command's options, related commands, and other information. This page can be navigated with the arrow keys, Page Up/Page Down, or j/k.
* `cd` - stands for **c**hange **d**irectory. Strangely, there isn't a `man` page for `cd`, but you can get a general idea of it by googling some examples. Do `cd` to return to your home directory, `cd [directory name]` to change to a directory (so long as it's directly inside your current directory - for example, `/home/nik/` has the directories `Documents/ Downloads/ Music/ Pictures/ Videos/`, so you either have to type `cd /home/nik/Documents/` to get to nik's Documents/ direrctory, or you have to be in the `/home/nik` directory and type `cd Documents/`). 
In order to move a directory back (`/home/nik/Documents/` to `/home/nik/`), type `cd ..`. This works for nearly every directory except the root directory ( `/` ).
* `ls` - one of the simplest commands, ls lists the files in your current directory. You can use `ls` similarly to `cd`, in the sense that you can type a directory after `ls` (`ls /home/nik/Downloads/` or `ls /etc/`) and the contents of that directory will be listed. If you want to see hidden files (basically any file with a dot as the start of the filename in Linux is a hidden file; for example, `.tmux.config`), do `ls -a` (`-a` for all, in this case). 
`ls -ls` or `ls -la` shows additional information about the files, including the permissions (Read/Write/Execute), owner, size (in bytes), and time of creation alongside each file or directory's name. `ls -ls` functions similarly to the standard `ls` command, while `ls -la` functions similarly to `ls -a`.
* `sudo` - stands for **s**uper **u**ser **do**. Essentially the command-line version of administrator privileges in Linux, you'll need to do `sudo` before some commands in order for them to work. Some examples of these programs would be `apt-get` (used to update and install new software from the command line, will be explained later), or when you're editing files that are restricted by the system (mostly system files that Linux needs to run).
* `tmux` - stands for **t**erminal **mu**ltiple**x**er. Essentially takes one terminal window and allows you to have multiple terminals inside it, in a variety of arrangements. If you wanna learn more about it, I would recommend googling it as it's too complex to go in depth with here. 
`tmux` uses a special shortcut for you to tell it that it's time to run a command - by default, `Ctrl+b` (when I describe `tmux` commands from here forward, I'll assume that you're entering `Ctrl+b` quickly & with a little delay before executing the shortcut that I describe) . 
Basic commands (after starting `tmux` by typing `tmux` at the command line) include `Shift+'` to split the terminal window in half vertically and open a new pane, `%` to split the terminal window in half horizontally and open a new pane, `exit` to completely close `tmux`, `tmux detach` to "detach" from a tmux session (and leave it for later - doesn't stay if you reboot your computer entirely), and `tmux attach` to attach to an already existing session.

### Editing
To edit a file with these programs, type `[program name] [filename]` at the command prompt.
* `nano` - `nano` is a lighweight and simple programmer's/sysadmin's editor, and it has most of the keyboard shortcuts you'll need right on the bottom of the screen for you. `^` stands for `Ctrl` (`^X` == `Ctrl+x`), and instead of "saving" in `nano` you "write out" (`Ctrl+o`).
* `vim` - `vim` is love, `vim` is life, `vim` will eat your children. `vim` is a simple yet powerful programmer's editor that can be used to edit a wide variety of files (for full scope, I would suggest googling). Most of `vim`'s power centers around the ability to use combinations of keys to insert or manipulate text, and its remarkable ability to be configured through its `.vimrc` configuration file.
A very spartan yet functional and 'suck it up, champ'-style tutorial for `vim` is available by running `vimtutor`.
A solid chunk of the electronic notes that I'm keeping for my classes (as well as this guide) was/were written using `vim`, `tmux`, and a language called Markdown (which is really fun and kinda like a note-taking style or shorthand... of sorts.).

### Web Browsing
In progress still. I *technically* know how to browse the Web from the command line but it's weird and hard to describe so I'll just fill this out later. There's also command line email clients available but I just figured out how to use mine so I'll hold off on that too.

---
## Common GUI Tools
### Navigation
Most Linux distributions come with a built-in file manager/navigation tool, and it's pretty self-explanatory.

### Editing 
Libreoffice is useful for editing Microsoft file formats or more complex files, but basic text files can be opened in a program called `gedit` (essentially Notepad++ for Linux - tabs, a working "File" bar, support for more file types, etc).

### Web Browsing
Like I mentioned, use Chromium, Chrome, or Firefox. There's other web browsers available (Opera, Midori, etc) but they kinda suck.
