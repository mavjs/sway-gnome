# sway-gnome
Create a more pleasant [sway](https://swaywm.org/) - a tiling Wayland compositor, experience with GNOME Shell's ecosystem.

There are many like it[^0], but this one is mine...

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
