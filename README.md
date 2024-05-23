<h1 align="center">
    abstouch-nux
</h1>
<h3 align="center">
    An absolute touchpad input client for GNU/Linux (X11 only).
</h3>

<h5 align="center">
    <a href="https://github.com/jn-sena/abstouch-nux/blob/main/LICENSE"> <img src="https://img.shields.io/github/license/jn-sena/abstouch-nux?style=for-the-badge" alt="License" /> </a>
    <a href="https://github.com/jn-sena/abstouch-nux/commits/main"> <img src="https://img.shields.io/maintenance/yes/2021?style=for-the-badge" alt="Maintenance" /> </a>
</h5>

<h2 align="center">
  this project was discontinued in 2021 and archived in 2024. <br />
  check <a href="https://github.com/rszyma/abstouch-nux">rszyma/abstouch-nux</a> for a more accurate fork ♥ <br />
  see the <a href="https://github.com/jn-sena/abstouch-nux/tree/classic">classic</a> branch for the older version. <br />
</h2>


&nbsp;
<h2 align="center"> Installation </h2>

You can make the project from source with [CMake](https://cmake.org).

You should install the dependencies first.
- **Arch Linux**: `$ sudo pacman -Sy cmake gcc libxi libx11 xf86-input-libinput --needed`
- **Debian/Ubuntu**: `$ sudo apt-get install cmake gcc libxi-dev libx11-dev libxi6 libx11-6 xserver-xorg-input-libinput`
- **Fedora/Red Hat**: `$ sudo dnf install cmake gcc libXi-devel libX11-devel libXi libX11 xorg-x11-drv-libinput`
- **openSUSE**: `$ sudo zypper install cmake gcc libXi-devel libX11-devel libXi6 libX11-6 xf86-input-libinput`

Then you can build the package.

```bash
$ git clone https://github.com/jn-sena/abstouch-nux.git
$ cd abstouch-nux
$ cmake -B build
$ cmake --build build
$ sudo cmake --install build
```

**Make sure to add the user into the `input` group.**

```bash
$ sudo usermod -aG input $(whoami)
```

<h2 align="center"> Usage </h2>

`abstouch` binary is available after installing.

```bash
$ abstouch <command> [options] [arguments]
```

See help for more information.

```bash
$ abstouch help
```

<h2 align="center"> Examples </h2>

```bash
# Setup the abstouch-nux client first.
$ abstouch setup

# Calibrate the abstouch-nux client.
$ abstouch calibrate

# Start the abstouch-nux client on foreground.
$ abstouch start -f

# Start the abstouch-nux client as daemon.
$ abstouch start

# Stop the abstouch-nux client quietly.
$ abstouch stop --quiet

# Recalibrate the client, without the visualization.
$ abstouch calibrate --no-visual
```
