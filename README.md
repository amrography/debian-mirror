# Debian Mirror (GitHub-hosted)

This repository hosts a Debian APT repository with selected `.deb` packages such as **Ghostty** and **TopTracker**.
It is built automatically using GitHub Actions and published via GitHub Pages.

---

## 🔹 Client Setup (one-time)

1. Import the GPG key:
```bash
curl -fsSL https://amrography.github.io/debian-mirror/amrography-debian.gpg \
   | sudo gpg --dearmor -o /usr/share/keyrings/amrography-debian.gpg
```

2. Add the repository to APT sources:
```bash
echo "deb [signed-by=/usr/share/keyrings/amrography-debian.gpg] https://amrography.github.io/debian-mirror stable main" \
   | sudo tee /etc/apt/sources.list.d/amrography-debian.list
```

3. Update APT:
```bash
sudo apt update
```

---

## 🔹 Usage

Install packages directly from this mirror:

```bash
sudo apt install ghostty
sudo apt install toptracker
```

---

## 🔹 Updating

Whenever this repo is updated (new `.deb` files added or rebuilt), just run on your client:

```bash
sudo apt update
```

Packages will then be available via normal `apt install`.
