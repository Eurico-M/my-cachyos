# A diary/guide to my CachyOS

#### Or, Stuff I Learned About (Arch) Linux And Would Like To Keep Written Somewhere

## The Bin Folder

Apparently, if we want to run executables anywhere on the terminal, we need to add them to the `~/bin` folder.

Also, `~/bin` means `/home/username/bin`. But wait, I don't see that bin folder anywhere in my CachyOS installation. Better create one. But wait, does that mean my OS know to look for it?

That's what the PATH is for, it lists folders the OS looks at before running a command. Check that `/home/username/bin/` is in PATH with:

```
echo $PATH
```

It is! Great!
