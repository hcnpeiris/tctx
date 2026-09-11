# tctx

Small Bash helper for saving target values in `.target.env` and loading them into the current shell.

## Install

```bash
mkdir -p "$HOME/.local/bin"
curl -fsSL \
  https://raw.githubusercontent.com/hcnpeiris/tctx/main/tctx \
  -o "$HOME/.local/bin/tctx"
chmod +x "$HOME/.local/bin/tctx"
echo 'tctx() { source ~/.local/bin/tctx "$@"; }' >> ~/.zshrc
source ~/.zshrc
```

The shell function lets `tctx` export and unset variables in the current shell.

## Usage

Values are stored in `.target.env` in the current directory. Value options accept one or more values and can be combined.

```text
i VALUE...      Save IPs as IP1, IP2, ...
u VALUE...      Save usernames as USER1, USER2, ...
p VALUE...      Save passwords as PASS1, PASS2, ...
U VALUE...      Save users as USERS1, USERS2, ...
c VALUE...      Save credentials as CRED1, CRED2, ...
v HOST:IP...    Save virtual hosts as VHOST1, VHOST2, ...
show TYPE       Show names and values; TYPE: i, u, p, U, c, or v
reload          Load saved variables into the current shell
reset           Unset saved variables without deleting files
addhost         Append saved virtual hosts to /etc/hosts using sudo
notes TEXT...   Append text to notes.txt
h, help         Show help
```
