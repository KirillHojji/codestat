# 📦 codestat

<div align="center">

**Simple, fast source code line counter**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-0.3-brightgreen.svg)](#)
[![Python 3.6+](https://img.shields.io/badge/python-3.6+-blue.svg)](https://www.python.org/downloads/)

`codestat` is a command-line tool to count lines of code in your projects.  
It filters comments, blank lines, and supports many languages out of the box.

</div>

---

## 📋 Package Info

```

Package: codestat
Version: 0.3
Author: KirillHojji
License: MIT
Repository: https://github.com/KirillHojji/codestat
Dependencies: Python 3.6+

```

## ✨ Features

- **Multi-language support** – TypeScript, Python, JavaScript, YAML, JSON, CSS, HTML, and more
- **Comment & blank line filtering** – Shows real code size, not just total lines
- **Docstring handling** – Properly counts Python docstrings as comments, not code
- **Timeout protection** – Skips files that take too long (no more stuck counters)
- **Exclude directories** – Ignore `node_modules`, `.git`, `__pycache__`, and custom folders

## 🚀 Installation

### Quick install (Linux / macOS / Termux)

```bash
wget https://raw.githubusercontent.com/KirillHojji/codestat/refs/heads/master/codestat -O ~/.local/bin/codestat && chmod +x ~/.local/bin/codestat
```

Or if you have root/sudo:

```bash
sudo wget https://raw.githubusercontent.com/KirillHojji/codestat/refs/heads/master/codestat -O /usr/local/bin/codestat && sudo chmod +x /usr/local/bin/codestat
```

Manual download

Just download the script and make it executable:

```bash
wget https://raw.githubusercontent.com/KirillHojji/codestat/refs/heads/master/codestat
chmod +x codestat
./codestat /path/to/project
```

🛠 Usage

```
codestat [OPTIONS] <directory>
```

Options

Option Description
--help Show this help message
--version Show version information
--info Show author, license, and package info
--timeout N Set timeout in seconds for each file (default: 0 = no timeout)
--exclude DIR Exclude a directory (can be used multiple times)
--verbose Show detailed processing information

Examples

Basic usage

```bash
codestat /path/
```

Exclude common folders

```bash
codestat --exclude file ./my-project
```

Set timeout for huge files

```bash
codestat --timeout 5 --verbose ~/large-project
```

📊 Output Example

```
     150 text files.
Unique:      150 files                                     0 unique files.
      0 files ignored.

------------------------------------------------------------------------------------------
Language                Files      Total       Code    Comment      Blank
------------------------------------------------------------------------------------------
TypeScript                112      32000      29500        600       1900
Python                      2       8500       7500         70        930
YAML                        2       7200       5800          1       1399
JSON                        8       1000        990          5          5
CSS                         1        500        400         50         50
HTML                        1        100         80          5         15
------------------------------------------------------------------------------------------
SUM                       126      49300      44270        731       4299
```

🤝 Contributing

Found a bug or want to add a new language?

1. Fork the repository
2. Create a feature branch (git checkout -b feature/amazing-feature)
3. Commit your changes (git commit -m 'Add amazing feature')
4. Push to the branch (git push origin feature/amazing-feature)
5. Open a Pull Request

📜 License

Distributed under the MIT License. See the [LICENSE](https://github.com/KirillHojji/codestat/blob/master/LICENSE) file for more information.

---

Author: [KirillHojji](https://github.com/KirillHojji)
