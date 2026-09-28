# Classroom Python IDE

A complete Python editor and runner in a single HTML file. It runs entirely in the browser: students write code, press Run, and see the output straight away. There is nothing to install, no logins, and no student code is ever sent to a server.

## Why use it in the classroom?

- **Zero setup:** works on any device with a modern browser, including Chromebooks, iPads and locked-down school laptops.
- **Private by design:** Python runs locally in the student's own browser tab via WebAssembly.
- **Instantly shareable:** the whole program is stored in the link itself. Send a URL and the recipient sees exactly the same code.

## Features

- **Real Python 3.12** using [Pyodide](https://pyodide.org/), with output and errors shown in a colour-coded console
- **Code editor** with syntax highlighting, multi-cursor editing (Ctrl/Cmd-D), block comment/uncomment with `#`, and block indent with Tab / Shift-Tab
- **Turtle graphics:** `import turtle` draws to an on-page canvas
- **p5.js sketches:** write `setup()` and `draw()` for creative coding
- **Parsons puzzles:** turn any program into a drag-and-drop line-ordering puzzle with a Check button, shareable as a standalone link
- **File handling:** paste text into the "Program input file" box and read it with `open("filename")`. Files your program writes appear as downloads
- **Download / upload** `.py` files
- **Tidy:** auto-format code to PEP 8 style using autopep8
- **Share by URL:** code is compressed into the link, with no backend required

## Getting started

**Option 1: GitHub Pages (recommended)**
1. Go to **Settings → Pages**.
2. Set the source to your main branch and save.
3. Share the published link with your class.

**Option 2: Run locally**
Open `index.html` in a browser. If Python fails to load, serve the folder instead:

```bash
python3 -m http.server
```

then visit `http://localhost:8000`.

## Notes for teachers

- **Internet needed on first load.** Pyodide, CodeMirror, p5.js and LZ-String are loaded from public CDNs (jsDelivr and cdnjs). The Tidy button also downloads autopep8 from PyPI the first time it's used.
- **School filtering:** if the IDE won't load, ask your network team to allow `cdn.jsdelivr.net`, `cdnjs.cloudflare.com`, `pypi.org` and `files.pythonhosted.org`.
- **Turtle is a lightweight reimplementation** that draws to a canvas, because the standard library version needs Tkinter. Common commands work, but less usual methods may be missing.
- **Browser limitations:** `time.sleep`, threading and network sockets don't behave as they do on a desktop.
- **Long programs and links:** very large programs may exceed practical URL length when shared.

## Built with

[Pyodide](https://pyodide.org/) · [CodeMirror 5](https://codemirror.net/5/) · [LZ-String](https://pieroxy.net/blog/pages/lz-string/index.html) · [p5.js](https://p5js.org/) · [autopep8](https://github.com/hhatch/autopep8)

## Licence

MIT applies ☺️
