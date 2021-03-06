Dotfiles
========

.bash_profile and terminal settings tested with OS X **10.7+** (< 10.7 doesn't support 256 terminal colors without iTerm2).
Colors based on [ahmetsulek's Flat Terminal](https://github.com/ahmetsulek/flat-terminal)

Also includes iTerm2 scheme

![preview](preview.png)

###Installation
###### Regular
- Customise the user specific aliases and settings in .user_config
- Put the .bash_profile, .inputrc & .user_config into your home directory (`cd ~`)
- Open the .terminal or .itermcolors file and change profile preferences to set it as the default


###### Sym-linked
- First deal with your current .bash_profile and .inputrc file
- Navigate to where you've chosen to placed the files or cloned the repo and run:

```bash
ln -s $(pwd)/.bash_profile $HOME/.bash_profile
ln -s $(pwd)/.inputrc $HOME/.inputrc
ln -sf $(pwd)/.user_config.bash $HOME/.user_config.bash
```

- Open the .terminal or .itermcolors file and change profile preferences to set it as the default


###Aliases & Features
###### files
- **s** - *opens a file in sublime text*
- **o** - *short for open. 'o' opens the current directory in finder* 
- **si** *\<cmd\>* - *open the result of a command in sublime text, eg `si git diff`*
- **highlight** *\<file\>* - *syntax highlighting in terminal*
- **trash** *\<file\>* - *move file to trash*
- **l** - *list files in long format*
- **la** - *list all files including dotfiles, in long format*

###### navigation
- **z** *<search string>* - *jump to commonly used directories*
- **bk** - *go back a directory*
- **desktop** - *cd ~/Desktop*
- **..** 	- *cd ..*
- **...** 	- *cd ../..*
- **....** 	- *cd ../../..*
- **.....** - *cd ../../../..*

###### git
- **gs** - *git status*
- **ga** - *git add .*
- **gc** *\<message\>* - *git commit -m*
- **gca** *\<message\>* - *git commit -a -m*
- **gcap** *\<message\>* - *git commit -a -m \<message\> && git push*
- **push** - *git push*
- **pull** - *git pull*
- **gdiff** - *git diff*
- **gsetup** *<repo-url>* - *initialises repo with a given url*
- **gbrowser** - *opens the current remote origin url in the browser*

###### other
- **[TAB] Autocomplete is improved with single tab instead of two and case insensitivity**

- **show** / **hide** - *show/hide hidden files* 
- **sman** - *open man page with text edtior*
- **speedread** *\<file\>* - *Spritz like speed reader in terminal*
- **deleteExtraBashScripts** - *clears auto-installed bash-scripts*

###Auto-installed scripts

Additional scripts installed into ~/.bash_scripts/ on first run

- [git-completion](https://github.com/git/git/tree/master/contrib/completion) - Autocomplete for git from Github's main repository
- [z jump script](https://github.com/rupa/z) - 'Tracks your most used directories, based on frequency'
- [trash](https://github.com/morgant/tools-osx) - 'trash allows trashing of files instead of tempting fate with rm'
- [speedread](https://github.com/pasky/speedread) - 'A simple terminal-based open source Spritz-alike'

###Dependencies
- [pygmentize](http://pygments.org/) for syntax highlighting in terminal (use bash alias **highlight** *\<file\>*) can be installed with `sudo easy_install Pygments`
- git

###Key bindings iTerm2 (manual entry)
Line text-editor style line navigation  

| Combo 	| Action         	| Send 	|
|-------	|----------------	|------	|
| ⌘←    	| "HEX CODE"     	| 0x01
| ⌘→    	| "HEX CODE"     	| 0x05
| ⌥←    	| "SEND ESC SEQ" 	| b
| ⌥→    	| "SEND ESC SEQ" 	| f

