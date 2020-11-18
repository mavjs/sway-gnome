# sway-gnome
Create a more pleasant [sway](https://swaywm.org/) - a tiling Wayland compositor, experience with GNOME Shell's ecosystem.

There are many like it[^0], but this one is mine...

## Notes
I started out looking at [Drakulix's sway-gnome](https://github.com/Drakulix/sway-gnome/network) fork and ended up on using [iH8c0ff33's sway-gnome](https://github.com/iH8c0ff33/sway-gnome) fork. However, that results in sway systemd serivce failsures and I couldn't get it to work.

There is an extensive discussion on [sway#5160](https://github.com/swaywm/sway/issues/5160) why it's a bad idea to try starting sway as a systemd service, which I only saw after troubleshooting the above for several hours. :stuck_out_tongue_closed_eyes:

At the end of the day, I'm a much simpler man and my use case was mainly around getting things like `gnome-keyring` and `swayidle` to work, so I opted for this simple version from [swaywm's wiki](https://github.com/swaywm/sway/wiki/Systemd-integration), however, your mileage may vary.


[^0]: https://github.com/Drakulix/sway-gnome/network

## Installing
### Get dependency
* [meson](https://mesonbuild.com/index.html)

#### Fedora
```bash
sudo dnf install meson -y
```

### Steps
Clone the repository:
```bash
git clone https://github.com/mavjs/sway-gnome.git
```

Create meson build directory:
```bash
meson builddir
```

Install the service files:
```bash
sudo meson install
```
