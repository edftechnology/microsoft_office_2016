# PlayOnLinux Wine builds (linux-x86)

These are the four 32-bit Wine runners copied from `~/.PlayOnLinux/wine/linux-x86/`:

- `3.4/`
- `3.14/`
- `4.15/`
- `5.8/`

To restore them into a PlayOnLinux user profile, copy the version directories into:

```bash
cp -a 'docs/PlayOnLinux wine/linux-x86/'* "$HOME/.PlayOnLinux/wine/linux-x86/"
```

Wine 5.8 was obtained from WineHQ's Ubuntu Focal i386 packages and unpacked into the PlayOnLinux runner layout. Its principal package was checked against WineHQ's official package index (SHA-256 `ca937330c706d3388959dc06ef65729a40c86b94e29cfaddc81d10423575a49c`). The WineHQ build identifies itself as `wine-5.8` and successfully initialized a 32-bit prefix.
