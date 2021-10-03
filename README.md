# What's this?
It's an Emacs extension, using it you can just use one key to save clipboard image to disk file, and at the same time insert the file link(org-mode/markdown-mode) or file path(other mode) to current point.

Here is a usage demo:
![](./img/illustrate.gif)

Based on PasteEx, only support Windows.

# Prerequisite
- Windows: Install [PasteEx](https://github.com/huiyadanli/PasteEx/releases)
- Macoss: Install [Pngpaste](https://github.com/jcsalterego/pngpaste)

# Installation
Put `pasteex-mode.el` to your `load-path`. The `load-path` is usually `~/elisp/`. It's set in your `~/.emacs` file like this:

```emacs-lisp
(add-to-list 'load-path (expand-file-name "~/elisp"))
(require 'pasteex-mode)
```

# Basic Usage
- Windows: Add `PasteEx.exe` executable to environment PATH, or set the variable `pasteex-executable-path` in your config file, like this:

```emacs-lisp
(setq pasteex-executable-path "D:/program/PasteEx/PasteEx.exe")
```

- Bind your favorite key to function `pasteex-image`, like this:

```emacs-lisp
(global-set-key (kbd "C-x p i") 'pasteex-image)
```

- After you make a screenshot to clipboard, or copy a PNG image file to clipboard, then just press `C-x p i` shortcut, and the file link or path will be inserted to your buffer immediately, the screenshot image file is saved to `./{buffername}_imgs/` directory by default.

# Feature List
Support these functions:
- `pasteex-image`: Save clipboard image to disk file, and insert file path to current point.
- `pasteex-delete-img-link-and-file-at-line`: Delete image link at line, and delete related disk file at the same time.
- `pasteex-is-png-file`: Check a file is png file or not.

# Tips
- Only support Windows, because PasteEx only support Windows now.
- That's all, enjoy it :)


