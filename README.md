These are my Terminal's settings:

- Modded `Galaxy` Theme (original [here](https://github.com/lysyi3m/osx-terminal-themes))
- Font: `Akkurat Mono` 10pt.
- `~/.bash_profile`:

```shell
cd ~/Desktop

# Set up the Terminal colors
red=$(tput setaf 1)
green=$(tput setaf 2)
yellow=$(tput setaf 3)
blue=$(tput setaf 4)
magenta=$(tput setaf 5)
cyan=$(tput setaf 6)
reset=$(tput sgr0)

export CLICOLOR=1
export LSCOLORS=GxFxCxDxBxegedabagaced
# and the prompt
ttynumber=$(echo "`tty`" | sed 's/\/dev\/ttys00//g')
if [[ "$ttynumber" == "0"  ]]; then
  ttynumber=" "
else
  rightparentheses=")"
  ttynumber=" ($ttynumber$rightparentheses "
fi

export PS1="\[$red\]\w \[$yellow\]>\[$green\]$ttynumber\[$reset\]"
``` 