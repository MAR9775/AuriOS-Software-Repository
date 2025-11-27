
# 📦 AurIOS Software Repository

> Official software package distribution repository for [AurIOS](https://github.com/MAR9775/FYP-AurIOS) - Automated Software Installation & Configuration System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Releases](https://img.shields.io/github/v/release/MAR9775/AurIOS-Software-Repository)](https://github.com/MAR9775/AurIOS-Software-Repository/releases)
[![Software Count](https://img.shields.io/badge/Software_Packages-3+-blue.svg)](https://github.com/MAR9775/AurIOS-Software-Repository/releases)

---

## 🎯 Purpose

This repository serves as the central distribution hub for software packages managed by **AurIOS**. Each software release contains:
- Pre-validated installers (`.exe`, `.msi`)
- Installation metadata
- Verification checksums
- Version compatibility information

## 📋 Available Software

### 🛠️ Developer Toolkit

| Software | Version | Type | Status |
|----------|---------|------|--------|
| **Git for Windows** | 2.43.0+ | `.exe` | ✅ Available |
| **Visual Studio Code** | 1.85.0+ | `.exe` | ✅ Available |
| **Node.js** | 20.x LTS | `.msi` | ✅ Available |
| GitHub Desktop | Latest | `.exe` | 🔄 Coming Soon |
| Postman | Latest | `.exe` | 🔄 Coming Soon |

### 🐳 Backend & Containers

| Software | Version | Type | Status |
|----------|---------|------|--------|
| Docker Desktop | Latest | `.exe` | 📋 Planned |
| MySQL Server | 8.0+ | `.msi` | 📋 Planned |
| MySQL Workbench | 8.0+ | `.msi` | 📋 Planned |

### 📊 Data Science & AI

| Software | Version | Type | Status |
|----------|---------|------|--------|
| Python | 3.11+ | `.exe` | 📋 Planned |
| JupyterLab | Latest | `.whl` | 📋 Planned |
| R-Studio Desktop | Latest | `.exe` | 📋 Planned |

### 🌐 General Software

| Software | Version | Type | Status |
|----------|---------|------|--------|
| VLC Media Player | Latest | `.exe` | 📋 Planned |
| Notepad++ | Latest | `.exe` | 📋 Planned |
| Google Chrome | Latest | `.exe` | 📋 Planned |

---

## 🚀 How AurIOS Uses This Repository

### Installation Workflow

```python
# AurIOS Install Agent fetches from this repository
from src.agents.install_agent import InstallAgent

agent = InstallAgent()
agent.install_from_github(
    repo_owner="MAR9775",
    repo_name="AurIOS-Software-Repository",
    asset_pattern="Git-.*-64-bit.exe"
)
```

### Release Structure

Each release follows this naming convention:
```
Tag: v{software-name}-{version}
Example: v-git-2.43.0, v-vscode-1.85.1, v-nodejs-20.10.0
```

---

## 📥 Download Software

### For End Users (via AurIOS)
```bash
# Use AurIOS automated installation
python demo.py
# Select software from the menu
```

### For Manual Download
1. Navigate to [Releases](https://github.com/MAR9775/AurIOS-Software-Repository/releases)
2. Select the software version you need
3. Download the installer from "Assets"
4. Run the installer (requires admin privileges)

---

## 🔐 Security & Verification

All software packages in this repository:
- ✅ Are sourced from official vendor websites or repositories
- ✅ Include SHA-256 checksums for verification
- ✅ Are scanned for malware before release
- ✅ Match official release signatures

### Verify Download Integrity
```bash
# Windows PowerShell
Get-FileHash -Path "Git-2.43.0-64-bit.exe" -Algorithm SHA256

# Compare with checksum in release notes
```

---

## 📖 Software Details

### Git for Windows
- **Official Source:** [git-for-windows/git](https://github.com/git-for-windows/git)
- **Installation Type:** Silent (`/VERYSILENT /NORESTART`)
- **Install Location:** `C:\Program Files\Git`
- **Validation:** `git --version`

### Visual Studio Code
- **Official Source:** [microsoft/vscode](https://github.com/microsoft/vscode)
- **Installation Type:** User Installer (silent)
- **Install Location:** `%LOCALAPPDATA%\Programs\Microsoft VS Code`
- **Validation:** `code --version`

### Node.js
- **Official Source:** [nodejs/node](https://github.com/nodejs/node)
- **Installation Type:** MSI Silent (`/quiet /norestart`)
- **Install Location:** `C:\Program Files\nodejs`
- **Validation:** `node --version`, `npm --version`

---

## 🛠️ For Contributors

### Adding New Software

1. **Obtain Official Installer**
   - Download from vendor's official site
   - Verify digital signature
   - Test installation manually

2. **Create Release**
   ```bash
   # Tag format: v-{software}-{version}
   git tag -a v-git-2.43.0 -m "Git for Windows 2.43.0"
   git push origin v-git-2.43.0
   ```

3. **Upload to GitHub Release**
   - Go to Releases → Draft a new release
   - Select the tag you created
   - Upload installer file
   - Add SHA-256 checksum
   - Publish release

4. **Update Documentation**
   - Add entry to `docs/SOFTWARE_LIST.md`
   - Update this README's software table
   - Document installation flags and paths

---

## 🔗 Related Repositories

- **[FYP-AurIOS](https://github.com/MAR9775/FYP-AurIOS)** - Main automation system
- **[AurIOS-Docs](https://github.com/MAR9775/AurIOS-Docs)** - Documentation (planned)
- **[AurIOS-UI](https://github.com/MAR9775/AurIOS-UI)** - Electron desktop app (planned)

---

## 📊 Statistics

- **Total Software Packages:** 3+ (actively growing)
- **Target Coverage:** 20+ essential developer tools
- **Average Download Size:** 50-100 MB per package
- **Supported Platforms:** Windows 10/11 (64-bit)

---

## 📜 License

This repository follows **MIT License** for distribution infrastructure.

**Note:** Individual software packages retain their original licenses:
- Git for Windows: GPL v2
- Visual Studio Code: MIT License
- Node.js: MIT License

See individual software documentation for licensing details.

---

## 🤝 Contributing

We welcome contributions! To suggest new software packages:

1. Open an issue with the software name and justification
2. Provide official download links
3. Document installation requirements
4. Submit via Pull Request (for documentation updates)

---

## 📞 Support

- **Issues:** [Report a problem](https://github.com/MAR9775/AurIOS-Software-Repository/issues)
- **Main Project:** [FYP-AurIOS](https://github.com/MAR9775/FYP-AurIOS)
- **Contact:** MAR9775@github

---

## 🗓️ Roadmap

### Phase 1: Core Developer Tools ✅ (Current)
- [x] Git for Windows
- [x] Visual Studio Code
- [x] Node.js

### Phase 2: Extended Toolkit (Q1 2024)
- [ ] GitHub Desktop
- [ ] Postman API Client
- [ ] Google Chrome

### Phase 3: Backend Infrastructure (Q2 2024)
- [ ] Docker Desktop
- [ ] MySQL Server
- [ ] MySQL Workbench
- [ ] .NET SDK

### Phase 4: Data Science Stack (Q2 2024)
- [ ] Python 3.11+
- [ ] JupyterLab
- [ ] R-Studio Desktop

### Phase 5: General Purpose (Q3 2024)
- [ ] VLC Media Player
- [ ] Notepad++
- [ ] 7-Zip

---

## ⚠️ Disclaimer

This repository **redistributes software packages** from their original vendors for convenience and automation purposes. All software:
- Remains property of original authors/vendors
- Is distributed under original licenses
- Should be used in compliance with vendor terms
- Is provided "as-is" without warranty

**Always verify downloads against official vendor checksums.**

---

## 🌟 Acknowledgments

Special thanks to all open-source software vendors who make their tools freely available:
- Git for Windows Team
- Microsoft (VS Code)
- Node.js Foundation
- And many more...

---

<div align="center">

**Built with ❤️ for the developer community**

⭐ Star this repo if you find it useful!

</div>
