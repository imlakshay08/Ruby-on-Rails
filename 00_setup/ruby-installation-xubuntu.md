# 🐧 Install Ruby on Xubuntu (Linux) — Step-by-Step Beginner's Guide

This guide walks you through installing **Ruby** on **Xubuntu** (or any Ubuntu-based Linux distro).

If you’re planning to learn Ruby on Rails, this is your first step!

---

## 🧰 Step 1: Update Your System
Open your terminal with **Ctrl + Alt + T** and run:

```bash
sudo apt update
sudo apt upgrade
(Enter your password and press Y when prompted.)
```

🧩 Step 2: Install Required Libraries

```bash
sudo apt install gcc make libssl-dev libreadline-dev zlib1g-dev libsqlite3-dev libyaml-dev
```

These are essential packages Ruby needs to compile properly.

🧱 Step 3: Install rbenv and ruby-build

```bash
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
~/.rbenv/bin/rbenv init
```

Close and reopen the terminal.

Then install ruby-build:

```bash
mkdir -p "$(rbenv root)"/plugins
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
```

Verify installation:

```bash
rbenv -v
```

💎 Step 4: Install Ruby
```bash
rbenv install 3.3.5 --verbose
rbenv global 3.3.5
ruby -v
```

If you see output like ruby 3.3.5, congratulations — Ruby is installed! 🎉

📽 Watch the full video walkthrough:
[Install Ruby on Xubuntu (YouTube)](https://www.youtube.com/watch?v=L0275goPFYc)
