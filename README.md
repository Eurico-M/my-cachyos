# A diary/guide to my CachyOS

#### Or, Stuff I Learned About (Arch) Linux And Would Like To Keep Written Somewhere

## The Bin Folder

Apparently, if we want to run executables anywhere on the terminal, we need to add them to the `~/bin` folder.

Also, `~/bin` means `/home/username/bin`. But wait, I don't see that bin folder anywhere in my CachyOS installation. Better create one. But wait, does that mean my OS know to look for it?

That's what the PATH is for, it lists folders the OS looks at before running a command. Check that `/home/username/bin/` is in PATH with:

```
echo $PATH
```

I did this next step before checking if it was, but it would be pretty weird if `~/bin` was in PATH when it didn't exist.

Anyway, I went to `/home/username/.config/fish/` and opened `config.fish`. Then added this:
```
if test -d "$HOME/bin"
    fish_add_path "$HOME/bin"
end
```
## Fish (the shell, not the meaningless animal category)

The default shell of CachyOS is fish.

### Fastfetch

Fastfetch is the little program that runs everytime you start an instance of the terminal. I'm fine with this.

To customize it, go to `~/.config/fastfetch/`. If this doesn't exist, do `fastfetch --gen-config`.

The file we want to customize is `config.jsonc`. Look up what stuff does on the internet.

Notably, the following bit of code allows customization of the image:
```
"logo": {
        "source": "/home/eurico/.config/fastfetch/cachyos_logo2.png",
        "height": 28,
        "padding": {
            "top": 1
        }
    },
```
