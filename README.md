# grab — grab your latest screenshots

You have all your screenshots saved automatically to a directory, but you often want to move the last few somewhere specific? Just `grab` them.

```
┌───=[ me :: x1 ]-( 0 )-[ ~/Downloads ]
└──( grab -2 web
moving /home/user/Downloads/screenshots/screenshot-2026-05-13-18:53:16.png → ./web-1.png
moving /home/user/Downloads/screenshots/screenshot-2026-05-11-10:39:17.png → ./web-2.png
```

`grab` is a tiny, portable Bash tool that:

- Finds the **latest N screenshots**
- Moves or copies them into your working directory (or a target directory)
- Optionally renames them (`name.png`, `name-1.png`, …)
- Works on **Bash 3+**, **Arch**, **Debian**, **macOS**, **Nix**, **BusyBox**, etc.
- Has zero dependencies and is safe under `set -euo pipefail`

## Usage

```
Usage:
  grab [options] [name]

Options:
  -n, --dry-run          Show what would be done without moving/copying
  -c, --copy             Copy instead of move
  -q, --quiet            Suppress non-error output
  -s, --source <dir>     Source directory (default: ~/Downloads/screenshots)
  -p, --pattern <glob>   Filename pattern (default: screenshot-*.png)
  -t, --target <dir>     Target directory (default: .)
  -h, --help             Show this help and exit
      --version          Show version and exit

Examples:
  grab               # move last screenshot into .
  grab web           # rename last screenshot to web.png
  grab -3 web        # rename last 3 screenshots to web-1.png, web-2.png...
  grab -c -t ~/tmp   # copy last screenshot into ~/tmp
```

## Installation

Drop `grab` anywhere in your `$PATH`.

## License

ISC
