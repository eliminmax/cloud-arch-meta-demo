# Cloud Architecture

This is the directory for the Hugo site that I slapped together as part of a presentation on cloud architecture.

## IMPORTANT:

This git repository includes a submodule - another git repository included within it. Unless you clone it with the `--recurse-submodules` flag, **it will not work as-is**. To get it to work, run the following commands:

```bash
git submodule init
git submodule update
```

The `hugo-shell` executable runs a single command: `docker run --rm -it -p 1313:1313 --user "$(id -u):$(id -g)" -v $(pwd):/src klakegg/hugo:ext-alpine shell`. It requires Docker, and gives you access to the `hugo` command. I did this because it was the easiest way to get hugo up and running in a pinch.
