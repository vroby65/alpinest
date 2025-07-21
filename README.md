# 🏔️ alpinest

**alpinest** is a rootless userland Alpine Linux environment, inspired by [junest](https://github.com/fsquillace/junest), but based on Alpine instead of Arch.  
It lets you run a full Alpine Linux environment from any Linux distribution, with no root privileges required.

## ✨ Features

- No installation required: works from a regular user directory.
- Based on `proot`: no root permissions needed.
- Fully isolated Alpine Linux environment.
- Use `apk` to install packages inside the Alpine root.
- Supports multiple independent versions side-by-side.
- Automatically uses your current working directory when launched.

## 🚀 Quick Start

```bash
sudo apt install curl tar proot
git clone https://github.com/vroby65/alpinest.git
cd alpinest
./alpinest
```

(Optional) Add it to your PATH:

```bash
sudo ln -s "$(pwd)/alpinest" /usr/local/bin/alpinest
```

Make sure `/usr/local/bin` is in your `$PATH`.

## 🧰 Requirements

- Linux
- `proot`
- `curl` or `wget`
- `tar`

## 📦 Usage

Start the Alpine environment:

```bash
./alpinest
```

Install packages using `apk`:

```sh
apk add git build-base
```

Exit the environment:

```sh
exit
```

## 🔒 Security

`alpinest` is fully rootless — everything runs with your current user permissions. No changes are made outside the Alpine folder.

## 📁 Directory Structure

- `alpinest` — main launcher script
- `alpine/` — contains the downloaded Alpine Linux system
- `etc/`, `tmp/` — optional local customizations

## 🧪 Use Cases

- Quickly test scripts or binaries in a clean Alpine environment
- Build `.apk` packages without Docker or VMs
- Try Alpine without affecting your main OS

## 📄 License

[MIT License](LICENSE)

---

**alpinest** is an independent project and is not affiliated with Alpine Linux or junest.
