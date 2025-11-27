# Hyprland Dots

Screenshots:

<img src="/assets/github_repo/images/screenshot-1.png" alt="screenshot-1">
<img src="/assets/github_repo/images/screenshot-2.png" alt="screenshot-2">

## Documentation
1. [Prerequisites](docs/prerequisites.md)
2. [Core Installation](docs/installation_Hypr.md)
3. [Basic Configuration](docs/basic_configuration.md)
4. [Useful Utilities](docs/useful_utilities.md)
5. [Theming](docs/theming.md)
6. [Summary](docs/final.md)

Installation:

Clone the repository:
```
git clone https://github.com/c4rt3z/hyprland-dots
```

Enter the installer path and run the installer:
```
cd ~/hyprland-dots/scripts/installer
sudo ./install.sh
```

(Optional) Install zsh + oh-my-zsh + Pure:
```
sudo pacman -S zsh npm #Install dependencies
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" #Install oh-my-zsh
sudo npm install --global pure-prompt #Install pure theme
```

Install theme + plugins (Find the required lines in .zshrc and replace them):
```
#In .zshrc (sudo nano .zshrc):
ZSH_THEME=""
autoload -U promptinit; promptinit
prompt pure # (setting theme)

#NOT in .zshrc:
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting #Install zsh-syntax-highlighting (plugin)
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions #Install zsh-autosuggestions (plugin)
pip install pygments # or sudo pacman -S python-pygments (Install pygments, plugin)
npm install --global trash-cli #Install trash-cli (plugin)

#IN .zshrc:
plugins=(
  git
  brew
  common-aliases
  node
  npm
  rand-quote
  sudo
  yarn
  z
  colored-man-pages
  colorize
  cp
  zsh-syntax-highlighting
  zsh-autosuggestions
) #Set plugins

#NOT in .zshrc:
source .zshrc #Apply changes
```
Important Notes:

- This script is user-centric and allows you to choose which components to install (Everything is asked, even for the core).
- While the script offers flexibility, it is recommend to installing all components for the best experience, as this is already a minimal setup.
- The installation process follows the same flow as the documentation, ensuring a structured and educational approach.
- Although designed for Arch Linux/EndeavourOS, users of Arch-based distributions may also find this script helpful.

> Note for Newcomers: Although this script enables rapid setup, it's highly recommended to read through the documentation for those new to Hyprland. Understanding each step will greatly enhance your ability to customize and troubleshoot your environment.


Keybinds:

After installation, you'll want to familiarize yourself with the default key bindings. Here are some essential shortcuts to get you started:

General
- `Super + RETURN (Shift)`: Open the terminal (`$terminal`).
- `Super + B`: Open the browser (`$browser`).
- `Super + O`: Open notes application (`$notes`).
- `Super + C`: Open the primary editor (`$editor`).
- `Super + S`: Open the alternative editor (`$editor-alt`).
- `Super + F`: Open the file manager (`$fileManager`).
- `Super + A`: Open the application menu (`$menu`).
- `Super + M`: Exit Hyprland.

Window Management & Workspace Navigation
- `Super + Q`: Close the active window.
- `Super + W`: Toggle floating mode for the active window.
- `Super + J`: Toggle split mode in the Dwindle layout.
- `SUPER + [Arrow Keys]`: Move focus between windows
- `SUPER + SHIFT + [Arrow Keys]`: Move active window
- `SUPER + CTRL + [Arrow Keys]`: Resize active window
- `SUPER + [1-9]`: Switch to workspace 1-9
- `SUPER + SHIFT + [1-9]`: Move active window to workspace 1-9

Screen Brightness, Volume and Media Control
- `Brightness Up`: Increase the screen brightness by 5%.
- `Brightness Down`: Decrease the screen brightness by 5%.
- `Volume Up`: Increase the volume by 5%.
- `Volume Down`: Decrease the volume by 5%.
- `Mic Mute`: Mute the microphone.
- `Audio Mute`: Mute the audio.
- `Play/Pause`: Toggle play/pause for media.
- `Next Track`: Skip to the next track.
- `Previous Track`: Go back to the previous track.

Miscellaneous
- `Super + V`: Open the clipboard history and paste the selected item.
- `Super + P`: Open the color picker and copy the selected color to the clipboard.
- `Super + L`: Lock the screen.
- `Super + Escape`: Open the logout menu.
- `Ctrl + Escape`: Toggle the Waybar (kill if running, start if not).
- `Print Screen`: Take a screenshot of the entire screen and copy it to the clipboard.
- `Super + Print Screen`: Take a screenshot of the active window and copy it to the clipboard.
- `Super + Alt + Print Screen`: Select an area to take a screenshot and copy it to the clipboard.

Make sure to have applications installed corresponding to the binds. Feel free to customize these keybindings to better suit your needs. You can customize these and add more in your Hyprland configuration file (`~/.config/hypr/hyprland.conf`).

Credits
Many configuration parts, themes, and scripts in this guide are sourced from the community. I extend my thanks to all contributors, especially the [Hyprland project](https://github.com/hyprwm/Hyprland) and other cool repositories like [hyprdots](https://github.com/prasanthrangan/hyprdots). If you find that credit has not been given where due, please feel free to open a Pull Request (PR). Thanks for pure theme [iTerm2 + oh-my-zsh + Pure + plugins](https://gist.github.com/ganapativs/e571d9287cb74121d41bfe75a0c864d7). Also, thanks to [oh-my-zsh](https://ohmyz.sh).

References
* [Hyprland Wiki](https://wiki.hyprland.org/)
* [Hyprdots Repo](https://github.com/prasanthrangan/hyprdots)
* [Hyprland-titus Repo](https://github.com/ChrisTitusTech/hyprland-titus) and more.

Feel free to explore the documentation and contribute to this guide if you find any improvements or have suggestions.
