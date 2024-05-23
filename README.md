<p align="center">
  <h1 align="center">abstouch-nux</h1>
  <h4 align="center">An absolute touchpad input client for GNU/Linux (X11 only).</h4>
  <h5 align="center">Inspired by <a href="https://github.com/apsun/AbsoluteTouchEx">apsun/AbsoluteTouchEx</a>. Make sure to check his repository, especially if you use Windows!</h5>

  <h6 align="center">
    <a href="https://github.com/jn-sena/abstouch-nux" alt="License">
      <img src="https://img.shields.io/github/license/jn-sena/abstouch-nux?style=for-the-badge"></a>
    <a href="https://github.com/jn-sena/abstouch-nux/commits/classic">
      <img src="https://img.shields.io/maintenance/yes/2021?style=for-the-badge" alt="Maintenance"></a>
  </h6>

  <h2 align="center">
    this project was discontinued in 2021 and archived in 2024. <br />
    this is the old branch. see <a href="https://github.com/jn-sena/abstouch-nux/tree/main">main</a> for the newer one.
  </h2>
</p>


## Installation

Only available for **GNU/Linux** and **X11**.

**See the *[installing](doc/installing.md)* documentation for better guide.**

### Building From Source

* You can use ***autotools*** and ***make*** to make it.
* Make sure you have `gcc`, `automake`, `autoconf` and `libx11-dev (libx11 or libX11-devel for some systems)` installed.
* Don't forget to add user to `input` group.

```bash
$ git clone -b classic https://github.com/jn-sena/abstouch-nux.git
$ cd abstouch-nux
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
$ sudo usermod -aG input $(whoami)
```

You can replace `install` with `uninstall` if you want to uninstall.

## Important

* Make sure the user is in the `input` group, or else you'll have to run it using `sudo`.
* If the input system doesn't work, make sure you use **X11 / X.org *instead of* Wayland** to run the desktop environment on.

## Usage
* Make sure the user is in `input` group.

* **See *[usage](doc/usage.md)* documentation for more information.**

* **See *[examples](examples)* directory for some examples.**

You can start the client right away.

```bash
$ abstouch start
```

You can calibrate the input to match your touchpad.

```bash
$ abstouch calibrate
```

You can select the display and screen to match your setup.

```bash
$ abstouch setdisplay
```

You can run it on background if you use `--daemon` flag.

```bash
$ abstouch start -d
```

See the help or the man page for more information.

```bash
$ abstouch help
$ man abstouch
```
