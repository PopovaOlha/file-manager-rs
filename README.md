# File Manager CLI (Node.js)

A command-line File Manager built with Node.js (v22.14.0+) using only Node.js APIs — **no external dependencies**.

---

## ✅ Features

- CLI-based interaction
- File system navigation (`cd`, `ls`, `up`)
- File operations (`add`, `cat`, `rm`, `rn`, `cp`, `mv`, `mkdir`)
- OS info commands (`os --*`)
- Hashing files using SHA-256
- Compression & decompression via Brotli + Streams API
- Clean UX: always shows working directory, handles errors

---

## 🚀 Getting Started

### Prerequisites

- Node.js **v22.14.0 or newer**

### Install & Run

1. **Clone or download** this repo
2. Initialize project (if not done):
   ```bash
   npm init -y

Run via:

bash
npm run start -- --username=your_name

On start:
Welcome to the File Manager, your_name!
You are currently in <your_home_directory>

On exit (.exit or Ctrl+C):
Thank you for using File Manager, your_name, goodbye!

Navigation

| Command        | Description                          |
|----------------|--------------------------------------|
| `up`           | Go up one directory                  |
| `cd <path>`    | Change to directory (absolute/rel)   |
| `ls`           | List directory contents              |

File Operations

| Command                        | Description                          |
|--------------------------------|--------------------------------------|
| `cat <path>`                   | Print file content via stream        |
| `add <filename>`              | Create empty file                    |
| `mkdir <dirname>`             | Create new folder                    |
| `rn <path> <new_name>`        | Rename file                          |
| `cp <path> <dest>`            | Copy file (streams)                  |
| `mv <path> <dest>`            | Move file (copy + delete)            |
| `rm <path>`                   | Delete file                          |

OS info

| Command           | Description                         |
|-------------------|-------------------------------------|
| `os --EOL`        | Show system End-Of-Line character   |
| `os --cpus`       | Show number, model, and speed       |
| `os --homedir`    | Show home directory                 |
| `os --username`   | Show system username                |
| `os --architecture` | Show CPU architecture             |

Hashing

| Command          | Description                         |
|------------------|-------------------------------------|
| `hash <path>`    | SHA-256 hash of file content        |

Compression

| Command                              | Description                         |
|--------------------------------------|-------------------------------------|
| `compress <path> <dest>`             | Compress using Brotli (streams)     |
| `decompress <path> <dest>`           | Decompress Brotli (streams)         |

📌 Notes
You cannot go above root (e.g., C:\)

Paths can be absolute or relative

Streams used for:

cat, cp, mv

compress, decompress

 Examples:
cd ./folder/subfolder
add newFile.txt
cat ./readme.md
compress ./large.txt ./large.txt.br
decompress ./large.txt.br ./copy.txt
hash ./copy.txt
os --cpus


