# Third-party notices

AS SubCalc is distributed under the terms in [LICENSE](LICENSE). The components
below are **not** mine and are not covered by that licence — each is used
under its own terms, set by its own authors, and nothing in my licence
restricts the rights those terms give you.

| Component | Used for | Licence |
|---|---|---|
| [PySide6 / Qt 6](https://doc.qt.io/qtforpython/) | The entire user interface | **LGPL v3** (see below) |
| [NumPy](https://numpy.org/) | Image arrays and all the maths | BSD 3-Clause |
| [python-lz4](https://github.com/python-lz4/python-lz4) | LZ4-compressed XISF files | BSD 3-Clause |
| [zstandard](https://github.com/indygreg/python-zstandard) | Zstd-compressed XISF files | BSD 3-Clause |

`python-lz4` and `zstandard` are optional at runtime — the app only needs them for compressed XISF files — but they are listed because a build that has them installed will ship them.

## Qt / PySide6 and the LGPL

Qt is used under the **LGPL v3**, which is what allows it inside a closed
freeware application — but it comes with two conditions I have to meet, and
both are met by how this app is built and shipped:

1. **This notice.** You are told that Qt is used, under which licence, and
   where to get it. Qt's own source is at
   [code.qt.io](https://code.qt.io/cgit/) and
   [download.qt.io](https://download.qt.io/official_releases/QtForPython/);
   the version in a release is named in that release's notes.

2. **You must be able to replace Qt with your own build of it.** The release
   is a **onedir** build, not onefile: the Qt libraries sit as separate `.dll`
   and `.pyd` files inside the `_internal` folder next to the executable, so
   you can swap in a different build of the same Qt version yourself. That is
   what the LGPL calls relinking, and it is the reason the releases are not
   packaged as a single `.exe`.

If you ever want to do that and hit a problem, email me and I will help.

---

If you believe something here is wrong or missing, please tell me and I will
correct it: **stewart@astroshed.co.uk**
