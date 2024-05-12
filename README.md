# Arch WSL Setup
- Install Arch WSL from [Microsoft Store](https://apps.microsoft.com/detail/9mznmnksm73x)
- **Create default user and set it as default**

  - add user & password:
  ```
    sudo useradd -m <username>
    sudo passwd <username>
  ```
  - checking if sudo installed:
  ```
    sudo pacman -Sy sudo
  ```
  - edit the sudoers file:
  ```
    sudo usermod -aG wheel <username>
    sudo EDITOR=<editor> visudo
    add %wheel ALL=(ALL) ALL
    su - <username>
  ```
  - test sudo: (should say "root")
  ```
  sudo whoami
  ```
- **Add the user as default Windows Terminal profile using PowerShell**
  ```
  arch config --default-user <username>
  ```
# Theming
  **Font:** [Iosevka](https://github.com/be5invis/Iosevka)
  
  **Themes:** [Tsoding Emacs Gruber Minimal for VSCode](https://github.com/AnksioXD/Tsoding-Gruber-Minimal-For-VSCode)
