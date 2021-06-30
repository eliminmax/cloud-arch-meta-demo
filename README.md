# Cloud Architecture

This is the directory for the Hugo site that I slapped together as part of a presentation on cloud architecture.
**NOTE: Now that the website has been presented, this repository is no longer mainained, and the referenced sites will shut down by midnight July 1st, 2021, Eastern Daylight Time.**
## IMPORTANT:

This git repository includes a submodule - another git repository included within it. Unless you clone it with the `--recurse-submodules` flag, **it will not work as-is**. To get it to work, run the following commands:

```bash
git submodule init
git submodule update
```

The `hugo-shell` executable runs a single command: `docker run --rm -it -p 1313:1313 --user "$(id -u):$(id -g)" -v $(pwd):/src klakegg/hugo:ext-alpine shell`. It requires Docker, and gives you access to the `hugo` command. I did this because it was the easiest way to get hugo up and running in a pinch.

### TO USE

0. Launch the `hugo-shell` Docker container with the `docker run` command from above, or `./hugo-shell`.
1. Within the `hugo-shell` container, run the command `hugo -D`
2. Copy the contents of *data/public* to your server's web root directory.

