# Swayidle user scripts

## Using:

* Make directories:
  * `~/.config/swayidle/timeout-$TIME.d` for scripts running on timeout where `$TIME` is timeout
  * `~/.config/swayidle/timeout-$TIME-resume.d` for scripts running on resume after timeout where `$TIME` is timeout
  * `~/.config/swayidle/before-sleep.d` for scripts running before sleep
  * `~/.config/swayidle/after-resume.d` for scripts running after resume from sleep
  * `~/.config/swayidle/lock.d` for scripts running on locking session
  * `~/.config/swayidle/unlock.d` for scripts running on unlocking session

* Start systemd service:
  `systemctl --user start swayidle.service`

Example:

```bash
mkdir -d ~/.config/swayidle/timeout-120.d
cat <<EOF > ~/.config/swayidle/timeout-120.d/20-write-to-file.sh
echo "120 seconds elapsed" >> /tmp/file.txt
EOF
```
Will write "120 seconds elapsed" to `/tmp/file.txt` after 120 seconds from last user activity.

## Install:

* Archlinux:
  ```bash
  git clone https://github.com/x1b6e6/swayidle-users.pkgbuild.git
  cd swayidle-users.pkgbuild
  makepkg -si
  ```
