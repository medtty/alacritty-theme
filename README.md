<h1> Alacritty Theme </h1>

![Alt text](https://raw.githubusercontent.com/medoxb11/alacritty-theme/main/img/screenshot.jpg)

I'm using here omz, install Oh My Zsh by running the command 

via curl (make sure you have curl or wget installed)
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

or via wget
```bash
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

If you don't like omz you can install [startship](starship.rs/) either shell or Homebrew

And you'll need a font to display the icons 

you can get from [Github](https://github.com/epk/SF-Mono-Nerd-Font)

```bash
brew tap epk/epk

# Homebrew < 2.6.0
brew cask install font-sf-mono-nerd-font

# Homebrew >= 2.6.0
brew install --cask font-sf-mono-nerd-font
```

With Shell:
```bash
curl -sS https://starship.rs/install.sh | sh
```

With [Homebrew](https://brew.sh):
```bash
brew install starship
```
Once you do that you'll need to Add the init script to your shell's config file in `~/.bashrc` or in `~/.zshrc`

Bash
```bash
eval "$(starship init bash)"
```
Zsh
```shell
eval "$(starship init zsh)"
```

Create a `~/.config` file if you don't already have 
Then create an folder and name it as `alacritty`
And finsly create a file and name it as `alacritty.yml`

Or just run this and it'll do it for you 

```bash
mkdir .conf && cd .conf && mkdir alacritty && cd alacritty && touch alacritty.yml
```

copy the following code and past it in the `alacritty.yml`

````yaml
# It makes alacritty update itself when we edit the `alacritty.yml`
live_config_reload: true

window:
  opacity: .80 # to create a transparent background
  padding: # just to make beautiful (this is optional)
    x: 10
    y: 12
  dynamic_padding: false
  decorations: buttonless # to remove the top border of the window 

font:
  normal:
    family: "SF Mono" # use this font if you're using starship
    style: Regular
  size: 13.0

# then you can add some colors to the background and the foreground 
colors:
  # Default colors
  primary:
    background: '#263238'
    foreground: '#DADADA'

  # Normal colors
  normal:
    black: '#DADADA'
    red: '#dd1f1f'
    green: '#2f9e94'
    yellow: '#e4e46d'
    blue: '#24bfb1'
    magenta: '#7d357d'
    cyan: '#38a79c'
    white: '#e5e5e5'
```
