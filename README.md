### Installation dependencies

#### Install `flameshot`

```
# Download official flameshot
curl --remote-name \
    --remote-header-name \
    --location $(curl -s https://api.github.com/repos/flameshot-org/flameshot/releases/latest \
                | grep -Po 'https://github.com/flameshot-org/flameshot/releases/download/[^}]*\.AppImage' \
                | uniq)
```

Set it to executable
```
chmod +x Flameshot-*.x86_64.AppImage
```

Move Flameshot to other bins
```
mv ./Flameshot-*.x86_64.AppImage /usr/local/bin/flameshot
```

#### Install `xclip`

Fedora
```
sudo dnf update
sudo dnf -y install xclip
```

Ubuntu/Debian
```
sudo apt-get update
sudo apt-get install -y xclip
```

#### Install flameshit script

Clone repo
```
git clone https://github.com/hzswdef/Flameshit.git
cd flameshit
```

Set it to executable
```
chmod +x ./flameshit
```

Move script to **/usr/local/bin/**
```
sudo mv ./flameshit /usr/local/bin/
```

Set path to save screenshots, specified path must be absolute
```
export FLAMESHIT_SCREENSHOTS_SAVE_PATH="/home/$USER/Pictures/Screenshots/"
```

And, then you may specify the hotkey to make screenshots. Command to execute -
```
/usr/local/bin/flameshit
```
