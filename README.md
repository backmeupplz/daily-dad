# daily-dad

A terminal greeter that displays today's entry from [The Daily Dad](https://store.dailystoic.com/products/the-daily-dad) by Ryan Holiday.

![Screenshot](screenshot.png)

## Requirements

- `bash`, `unzip`, `sed`, `fold` (standard on most systems)
- Your own copy of _The Daily Dad_ epub

## Install

```bash
# Copy the script somewhere on your PATH
cp daily-dad ~/.local/bin/

# Point it at your epub (or place it at ~/the-daily-dad.epub)
export DAILY_DAD_EPUB="$HOME/path/to/the-daily-dad.epub"
```

Add to your `.bashrc` / `.zshrc` to see a quote every time you open a terminal:

```bash
export DAILY_DAD_EPUB="$HOME/path/to/the-daily-dad.epub"
daily-dad
```

## How it works

The script extracts the epub to `/tmp/daily-dad`, finds the xhtml page matching today's date, and renders the title and body text with nice formatting and centering in your terminal.

## Note

The epub is **not included** in this repository. You need to provide your own copy of the book.

## License

MIT
