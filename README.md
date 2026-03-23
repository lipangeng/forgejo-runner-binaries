# forgejo-runner-binaries

Prebuilt multi-platform binaries for Forgejo Runner.

## 📖 Overview

This repository provides **prebuilt binaries of Forgejo Runner** for multiple platforms and architectures.

The goal is to make it easy to:

* Download and run without building from source
* Use in offline or restricted environments
* Integrate into automation pipelines
* Ensure reproducible and consistent runtime environments

---

## ✨ Features

* ✅ Cross-platform builds

  * Linux (amd64, arm64)
  * Windows (amd64)
  * (Optional) macOS (amd64, arm64)
* ✅ Fully static binaries (no external dependencies)
* ✅ Built with `CGO_ENABLED=0` for maximum portability
* ✅ Ready-to-use, no compilation required
* ✅ Suitable for air-gapped environments

---

## 📦 Available Artifacts

Each release includes binaries named as:

```
forgejo-runner-<os>-<arch>
forgejo-runner-<os>-<arch>.exe  (Windows)
```

Examples:

* `forgejo-runner-linux-amd64`
* `forgejo-runner-linux-arm64`
* `forgejo-runner-windows-amd64.exe`

---

## 🚀 Quick Start

### Download

Go to the [Releases](../../releases) page and download the binary for your platform.

### Run

#### Linux / macOS

```bash
chmod +x forgejo-runner-*
./forgejo-runner-linux-amd64 --help
```

#### Windows

```powershell
.\forgejo-runner-windows-amd64.exe --help
```

---

## 🔧 Usage

Example:

```bash
# Generate config
./forgejo-runner generate-config

# Register runner
./forgejo-runner register

# Run as daemon
./forgejo-runner daemon
```

For full usage:

```bash
./forgejo-runner --help
```

---

## 🏗 Build Information

Binaries are built from:

* Source: [https://code.forgejo.org/forgejo/runner](https://code.forgejo.org/forgejo/runner)
* Go version: (fill your version, e.g. go1.26)
* Build flags:

  * `CGO_ENABLED=0`
  * `-tags netgo osusergo`
  * `-ldflags "-s -w"`

---

## ⚠️ Disclaimer

This repository provides **unofficial builds** of Forgejo Runner.

* Not affiliated with the Forgejo project
* No guarantee of full feature parity on all platforms
* Use at your own risk in production environments

---

## 🔐 Security

* Consider verifying checksums before use
* Prefer running in controlled environments
* For production, review upstream source code

---

## 🤝 Contributing

Issues and pull requests are welcome.

---

## 📜 License

Same as upstream Forgejo Runner.

---

## ⭐ Why this repo?

Because sometimes you just want:

> **Download → Run → Done**
