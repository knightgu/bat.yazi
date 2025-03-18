# bat.yazi

Plugin for `Yazi` to preview all supported files via `Bat`.

## Preview

![preview](./preview.png)


## Installation

```sh
$> ya pack -a knightgu/bat
```

## Configuration

Edit `~/.config/yazi/yazi.toml` and add `bat` as the previewer for the file types of your choice.

```toml
[plugin]
prepend_previewers = [
    { name = "*.csv", run = "bat" },
    { name = "*.md",  run = "bat" }
]

previewers = [
	{ name = "*/", run = "folder", sync = true },
	{ mime = "text/*",                 run = "bat" },
	{ mime = "*/xml",                  run = "bat" },
	{ mime = "*/cs",                   run = "bat" },
	{ mime = "*/javascript",           run = "bat" },
	{ mime = "*/x-wine-extension-ini", run = "bat" },
]
```


## References

* [Yazi - A fast terminal file manager](https://yazi-rs.github.io)
* [Bat - A cat(1) clone with wings](https://github.com/sharkdp/bat)
