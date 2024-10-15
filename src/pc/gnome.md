# Gnome

- [Extensões](#extens%C3%B5es)
- [Keybinds](#keybinds)
- [Aparência](#aparência)
- [Flatpak](#flatpak)
    - [Configurando tema](#configurando-tema)
    - [Configurando Google Chrome Apps](#configurando-google-chrome-apps)

![](imagens/screenshot.png)

Minha configuração do [Gnome](https://www.gnome.org/) com [Wayland](https://wayland.freedesktop.org/). Atualmente usando no [EndeavourOS](https://endeavouros.com/) (base [Arch Linux](https://archlinux.org/)).

## Extensões

- [Alphabetical App Grid](https://extensions.gnome.org/extension/4269/alphabetical-app-grid/): Deixa o menu de aplicativos em ordem alfabética;
- [Arch Linux Updates Indicator](https://extensions.gnome.org/extension/1010/archlinux-updates-indicator/);
- [Caffeine](https://extensions.gnome.org/extension/517/caffeine/): Desabilita a proteção de tela e a suspensão automática;
- [Clipboard Indicator](https://extensions.gnome.org/extension/779/clipboard-indicator/): Gerenciador de área de transferência;
- [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/): Deixa a dock parecida com a do Windows, além de remover a barra superior e mover seus itens para a dock;
- [Emoji Copy](https://extensions.gnome.org/extension/6242/emoji-copy/): Menu de emojis parecido com a do Windows 10;
- [Tray Icons: Reloaded](https://extensions.gnome.org/extension/2890/tray-icons-reloaded/): Mostra os ícones de bandeja igual ao Windows;
- [User Themes](https://extensions.gnome.org/extension/19/user-themes/): Tema do shell personalizado.

## Keybinds

- `Super+a`: Abre as notificações;
- `Super+v`: Abre o clipboard;
- `Super+.`: Abre o seletor de emojis;
- `Super+Tab`: Mostra o panorama;
- `Super+Enter`: abre o terminal;
- `Super+F11`: Tela cheia;
- `Alt+Tab`: Altera entre aplicativos.

## Aparência

- Tema e ícones: Adwaita;
- Wallpaper: <a href="/pc/imagens/endeavouros-wallpaper.png" download>Clique para baixar</a>;
- Cursor: [macOS Cursor](https://www.pling.com/p/1408466);
- Icone do menu: [Circle do Icons8](https://icons8.com.br/icon/Y56BOL5zVXx6/circle).

## Flatpak

### Configurando tema

Mudar o tema dos programas [Flatpak](https://flatpak.org/):

```bash
sudo flatpak override --env=GTK_THEME=Adwaita-dark
```

Corrigir o erro dos programas [Flatpak](https://flatpak.org/) com o cursor maior que o resto do sistema:

```bash
flatpak --user override --filesystem=/home/$USER/.icons/:ro
flatpak --user override --filesystem=/usr/share/icons/:ro
```

### Configurando Google Chrome Apps

Fechar o Google Chrome totalmente:

```bash
killall chrome
```

Dar permissão para o Chrome acessar as pastas `icons` e `applications`:

```bash
flatpak override --user --filesystem=~/.local/share/applications:create --filesystem=~/.local/share/icons:create com.google.Chrome
```
