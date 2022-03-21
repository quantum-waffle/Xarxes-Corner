---
description: Setting the green font
---

# Environment

{% embed url="https://www.kali.org/docs/wsl/win-kex/" %}



## Terminator + OhMyZSH

Multiplex the terminal with Terminator and add auto-completion using ZSH. This can be installed in any \*nix system, but I will be focusing with Debian-based systems. &#x20;

```bash
# Install Terminator
sudo add-apt-repository ppa:gnome-terminator
sudo apt-get update
sudo apt-get install terminator
```

```bash
# Install ZSH and OhMyZSH
sudo apt-get install zsh
cd
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
sudo apt-get install fonts-powerline
```

Change `[ZSH_THEME="robbyrussell"]` to `[ZSH_THEME="agnoster"]` in `~/.zshrc`

{% code title="~/.zshrc" %}
```bash
ZSH_THEME="agnoster"
```
{% endcode %}

Then, modify  `.oh-my-zsh/themes/agnoster.zsh-theme` in line #189, so you just keep the last three directories in your path&#x20;

{% code title=".oh-my-zsh/themes/agnoster.zsh-theme" %}
```bash
# Dir: current working directory
prompt_dir() {
  prompt_segment blue black '%(4~|.../%3~|%~)'
}
```
{% endcode %}

****[**Reference**](https://gist.github.com/renshuki/3cf3de6e7f00fa7e744a)****

## Tmux&#x20;

More multiplexers. The benefit of using Tmux is persistence. Tmux mounts a server, so we can close our terminal and the sessions will still be active. Tmux is installed by default in most Debian enviroments.&#x20;

{% tabs %}
{% tab title="Sessions" %}
Create a new session in Tmux

```bash
tmux new -s myname
```

Attach to a named session

```bash
tmux a -t myname
```

List active sessions

```bash
tmux ls
```

Kill a named session

```bash
tmux kill-session -t myname
```
{% endtab %}

{% tab title="Panes" %}
{% hint style="info" %}
In Tmux, hit the prefix`ctrl+b`and then the following.
{% endhint %}

* % : horizontal split.
* " : vertical split.
* x : kill pane.
* \[ : scroll and copy mode.
* Arrows : move to a different pane.
* d : detach.
* t : show clock.
* ? : list shortcuts.
{% endtab %}
{% endtabs %}

[**Full Tmux cheat sheet**](https://tmuxcheatsheet.com)****

## Cool commands

{% tabs %}
{% tab title="Monitor" %}
### [Glances](https://github.com/nicolargo/glances)
{% endtab %}

{% tab title="Map" %}
### ****[**Mapscii**](https://github.com/rastapasta/mapscii)****

```bash
telnet mapscii.me
```
{% endtab %}

{% tab title="Weather" %}
### [wttr.in](https://github.com/chubin/wttr.in)

```bash
curl wttr.in/Guatemala?m
```
{% endtab %}

{% tab title="Neofetch" %}
### [Neofetch](https://github.com/dylanaraps/neofetch)
{% endtab %}

{% tab title="Lolcat" %}
### [Lolcat](https://github.com/busyloop/lolcat)

```bash
wget https://github.com/busyloop/lolcat/archive/master.zip
unzip master.zip
cd lolcat-master/bin/
gem install lolcat
```

```bash
fortune | cowsay | lolcat
```
{% endtab %}
{% endtabs %}

## CommandoVM

This is a fully customizable, Windows-based security distribution for penetration testing and red teaming. Get it [here](https://github.com/fireeye/commando-vm).

### PowerShell Console

{% embed url="https://github.com/jaredhaight/PSAttack" %}

{% embed url="https://github.com/Kevin-Robertson/Inveigh" %}

{% embed url="https://github.com/codingo/Interlace" %}

{% embed url="https://github.com/maaaaz/impacket-examples-windows" %}

