# command-line
# What Is the Command Line?
The command line is the ultimate seat of power on your computer. Using the command line, you can perform amazing feats of wizardry and speed, taming your computer and getting it to do precisely what you want. Unfortunately, the price of this power is complexity: nobody ever said that ruling your computer would be easy.
The command line is, at its heart, simply a place where you type commands to the computer. The computer is your obedient servant, and will attempt to carry out any command that it understands. Unfortunately, the computer does not speak English, or any other language spoken by humans (although it has recognizable elements). In order to give it commands, we must first start learning the language of the computer.
NOTE: The command line, as with all power, has its risks. You have the capability to instruct the computer to do anything it has the capability of doing. If you instruct the computer to erase all of your data, it will cheerfully proceed to do so. Do not run a command just to see what it does. Make sure you understand what the command is supposed to do first, especially if the command involves changing or removing files.

## customizing your command line:

The more you operate on the command line, the more you will find that the majority of the commands you use are a very small subset of the available commands. While the makers of many of the most common command utilities have attempted to eliminate extraneous typing by using shortened names (think of how many keystrokes you save daily by typing "ls" instead of "list" and "cd" instead of "change-directory"), these are not ubiquitous. Additionally, many people always run commands with the same few options enabled every time.
Luckily, bash allows us to create our own shortcuts and time-savers through the use of aliases and shell functions.

## How To Declare a Bash Alias

 **alias alias_name="command_to_run"**

ex: alias gp="git pull"

in order to save all the aliases in one file 
**atom ~/.profile**
**"source ~/.profile"**


## removing a declarated alias name

 **unalias alias_name**

ex: unalias gp

## list all of your configared aliases
 
 **alias**

##to find a file in the current directory 

alias fthere="find. -name"


##Save on typing

Up Arrow or Ctrl + P

Scrolls through the commands you've entered previously.

Down Arrow or Ctrl + N

Takes you back to a more recent command.

Enter

When you have the command you want.

tab

A very useful feature. It autocompletes any commands or filenames, if there's only one option, or else gives you a list of options.

Ctrl + R

Searches for commands you've already typed. When you have entered a very long, complex command and need to repeat it, using this key combination and then typing a portion of the command will search through your command history. When you find it, simply press Enter.

History

The history command shows a very long list of commands that you have typed. Each command is displayed next to a number. You can type !x to execute a previously typed command from the list (replace the X with a number). If you history output is too long, then use history | less for a scrollable list.

##to search for a specific used command 

**ctrol+R**


##Some Useful and Interesting Bash Prompts

**Show a Happy face upon successful execution**

code:
PS1="\`if [ \$? = 0 ]; then echo \[\e[33m\]^_^\[\e[0m\]; else echo \[\e[31m\]O_O\[\e[0m\]; fi\`[\u@\h:\w]\\$ "



**Change color on bad command**

code:
PROMPT_COMMAND='PS1="\[\033[0;33m\][\!]\`if [[ \$? = "0" ]]; then echo "\\[\\033[32m\\]"; else echo "\\[\\033[31m\\]"; fi\`[\u.\h: \`if [[ `pwd|wc -c|tr -d " "` > 18 ]]; then echo "\\W"; else echo "\\w"; fi\`]\$\[\033[0m\] "; echo -ne "\033]0;`hostname -s`:`pwd`\007"'


##installation using a package manager

 package management tools keep track of updates and upgrades so that the user doesn’t have to hunt down information about bug and security fixes.

package management system, based on a tool called dpkg with the very popular apt system

Advanced Packaging Tool (APT)
You may already be familiar with apt-get, a command which uses the advanced packaging tool to interact with the operating system’s package system. The most relevant and useful commands are (to be run with root privileges):

apt-get install package-name(s) - Installs the package(s) specified, along with any dependencies.
apt-get remove package-name(s) - Removes the package(s) specified, but does not remove dependencies.
apt-get autoremove - Removes any orphaned dependencies, meaning those that remain installed but are no longer required.
apt-get clean - Removes downloaded package files (.deb) for software that is already installed.
apt-get purge package-name(s) - Combines the functions of remove and clean for a specific package, as well as configuration files.
apt-get update - Reads the /etc/apt/sources.list file and updates the system’s database of packages available for installation. Run this after changing sources.list.
apt-get upgrade - Upgrades all packages if there are updates available. Run this after running apt-get update.

**lists of packages for ubuntu:**

trusty (14.04LTS)
trusty-updates
trusty-backports
xenial (16.04LTS)
xenial-updates
xenial-backports
yakkety (16.10)
yakkety-updates
yakkety-backports
zesty (17.04)
zesty-updates
zesty-backports
artful





