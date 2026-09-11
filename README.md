# tctx

Small Bash helper for saving target values in `.target.env` and loading them into the current shell.

## Install


```bash
mkdir -p ~/.local/bin && curl -fsSL https://raw.githubusercontent.com/hcnpeiris/tctx/main/tctx -o ~/.local/bin/tctx && chmod +x ~/.local/bin/tctx
```

Make sure `~/.local/bin` is in your `PATH`.

## Usage

Use `source` so variables load into the current shell:

```bash
source tctx -i 192.168.1.8 192.168.1.9
source tctx -u admin -p 'Password123!'
source tctx -c 'admin:Password123!'
source tctx -v example.local:192.168.1.5
```

Show saved values:

```bash
source tctx -show i
source tctx -show u
source tctx -show p
source tctx -show c
source tctx -show v
```

Other commands:

```bash
source tctx -reload
source tctx -addhost
source tctx -notes "Found anonymous FTP access"
source tctx -h
```
