# 📋 Complete Software List

## Overview
This document tracks all software planned for AurIOS automation, their current implementation status, and technical details.

---

## 🛠️ Developer Toolkit (6 packages)

### 1. Git for Windows ✅ IMPLEMENTED
- **Official Source:** https://github.com/git-for-windows/git
- **Download Size:** ~50 MB
- **Installer Type:** `.exe` (Inno Setup)
- **Silent Install Flags:** `/VERYSILENT /NORESTART /NOCANCEL /SP- /CLOSEAPPLICATIONS /RESTARTAPPLICATIONS /COMPONENTS="icons,ext\reg\shellhere,assoc,assoc_sh"`
- **Install Path:** `C:\Program Files\Git`
- **Validation Commands:**
  - `git --version`
  - `git config --list`
- **Release Tag Format:** `v-git-{version}`
- **Current Version:** 2.43.0+

### 2. Visual Studio Code ✅ IMPLEMENTED
- **Official Source:** https://github.com/microsoft/vscode
- **Download Size:** ~90 MB
- **Installer Type:** `.exe` (User Installer)
- **Silent Install Flags:** `/VERYSILENT /NORESTART /MERGETASKS=!runcode`
- **Install Path:** `%LOCALAPPDATA%\Programs\Microsoft VS Code`
- **Validation Commands:**
  - `code --version`
  - `code --list-extensions`
- **Release Tag Format:** `v-vscode-{version}`
- **Current Version:** 1.85.0+

### 3. Node.js (includes npm) ✅ IMPLEMENTED
- **Official Source:** https://github.com/nodejs/node
- **Download Size:** ~30 MB
- **Installer Type:** `.msi`
- **Silent Install Flags:** `/quiet /norestart`
- **Install Path:** `C:\Program Files\nodejs`
- **Validation Commands:**
  - `node --version`
  - `npm --version`
  - `npm config list`
- **Release Tag Format:** `v-nodejs-{version}`
- **Current Version:** 20.x LTS

### 4. GitHub Desktop 🔄 IN PROGRESS
- **Official Source:** https://github.com/desktop/desktop
- **Download Size:** ~120 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `--silent`
- **Install Path:** `%LOCALAPPDATA%\GitHubDesktop`
- **Validation Commands:**
  - Check if process exists
  - Desktop shortcut created
- **Release Tag Format:** `v-githubdesktop-{version}`
- **Target Version:** Latest stable

### 5. Postman 📋 PLANNED
- **Official Source:** https://www.postman.com/downloads/
- **Download Size:** ~150 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/S`
- **Install Path:** `%LOCALAPPDATA%\Postman`
- **Validation Commands:**
  - Desktop shortcut exists
  - Application launches
- **Release Tag Format:** `v-postman-{version}`
- **Note:** Not on GitHub, requires direct download automation

### 6. Google Chrome 📋 PLANNED
- **Official Source:** https://www.google.com/chrome/
- **Download Size:** ~80 MB
- **Installer Type:** `.exe` (standalone)
- **Silent Install Flags:** `/silent /install`
- **Install Path:** `C:\Program Files\Google\Chrome\Application`
- **Validation Commands:**
  - `chrome --version`
  - Registry key check
- **Release Tag Format:** `v-chrome-{version}`
- **Note:** Requires Google's enterprise installer

---

## 🐳 Web Development (Backend) (3 packages)

### 7. Docker Desktop 📋 PLANNED
- **Official Source:** https://www.docker.com/products/docker-desktop
- **Download Size:** ~500 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `install --quiet --accept-license`
- **Install Path:** `C:\Program Files\Docker\Docker`
- **Post-Install:** Requires system restart
- **Validation Commands:**
  - `docker --version`
  - `docker-compose --version`
  - Docker service running
- **Release Tag Format:** `v-docker-{version}`
- **Special Notes:**
  - Requires Hyper-V or WSL2
  - Admin privileges mandatory
  - System restart required

### 8. .NET SDK 📋 PLANNED
- **Official Source:** https://dotnet.microsoft.com/download
- **Download Size:** ~200 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/quiet /norestart`
- **Install Path:** `C:\Program Files\dotnet`
- **Validation Commands:**
  - `dotnet --version`
  - `dotnet --list-sdks`
  - `dotnet --list-runtimes`
- **Release Tag Format:** `v-dotnet-{version}`
- **Target Version:** .NET 8.0+

---

## 🗄️ Database Management (3 packages)

### 9. MySQL Server 📋 PLANNED
- **Official Source:** https://dev.mysql.com/downloads/mysql/
- **Download Size:** ~300 MB
- **Installer Type:** `.msi`
- **Silent Install Flags:** `/quiet /norestart ADDLOCAL=ALL`
- **Install Path:** `C:\Program Files\MySQL\MySQL Server 8.0`
- **Post-Install:** Service configuration required
- **Validation Commands:**
  - Service status: `mysql80` running
  - `mysql --version`
  - Port 3306 listening
- **Release Tag Format:** `v-mysql-{version}`
- **Special Notes:**
  - Requires root password setup
  - Service configuration needed

### 10. MySQL Workbench 📋 PLANNED
- **Official Source:** https://dev.mysql.com/downloads/workbench/
- **Download Size:** ~40 MB
- **Installer Type:** `.msi`
- **Silent Install Flags:** `/quiet /norestart`
- **Install Path:** `C:\Program Files\MySQL\MySQL Workbench 8.0`
- **Validation Commands:**
  - Application launches
  - Desktop shortcut exists
- **Release Tag Format:** `v-mysqlworkbench-{version}`
- **Dependency:** Requires Visual C++ Redistributable

### 11. DBeaver 📋 PLANNED
- **Official Source:** https://dbeaver.io/download/
- **Download Size:** ~120 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/S`
- **Install Path:** `C:\Program Files\DBeaver`
- **Validation Commands:**
  - Application launches
  - JDBC drivers present
- **Release Tag Format:** `v-dbeaver-{version}`
- **Dependency:** Requires Java Runtime (JRE 11+)

---

## 📊 Data Science and AI (3 packages)

### 12. Python 3.x 📋 PLANNED
- **Official Source:** https://www.python.org/downloads/
- **Download Size:** ~25 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/quiet InstallAllUsers=1 PrependPath=1 Include_test=0`
- **Install Path:** `C:\Program Files\Python311`
- **Validation Commands:**
  - `python --version`
  - `pip --version`
  - `pip list`
- **Release Tag Format:** `v-python-{version}`
- **Target Version:** 3.11+

### 13. JupyterLab 📋 PLANNED
- **Official Source:** https://jupyter.org/install
- **Installation Method:** `pip install jupyterlab`
- **Installer Type:** Python package (`.whl`)
- **Dependency:** Requires Python 3.7+
- **Validation Commands:**
  - `jupyter lab --version`
  - `jupyter --paths`
- **Release Tag Format:** `v-jupyterlab-{version}`
- **Note:** Installed via pip after Python

### 14. R-Studio Desktop 📋 PLANNED
- **Official Source:** https://posit.co/download/rstudio-desktop/
- **Download Size:** ~200 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/S`
- **Install Path:** `C:\Program Files\RStudio`
- **Dependency:** Requires R (base) pre-installed
- **Validation Commands:**
  - Application launches
  - R version detected
- **Release Tag Format:** `v-rstudio-{version}`

---

## 🎵 General Software (3 packages)

### 15. VLC Media Player 📋 PLANNED
- **Official Source:** https://www.videolan.org/vlc/
- **Download Size:** ~40 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/L=1033 /S`
- **Install Path:** `C:\Program Files\VideoLAN\VLC`
- **Validation Commands:**
  - `vlc --version`
  - Desktop shortcut exists
- **Release Tag Format:** `v-vlc-{version}`
- **Note:** Hosted on VideoLAN, not GitHub

### 16. Notepad++ 📋 PLANNED
- **Official Source:** https://notepad-plus-plus.org/downloads/
- **Download Size:** ~4 MB
- **Installer Type:** `.exe`
- **Silent Install Flags:** `/S`
- **Install Path:** `C:\Program Files\Notepad++`
- **Validation Commands:**
  - Application launches
  - Start menu entry exists
- **Release Tag Format:** `v-notepadpp-{version}`
- **Note:** GitHub mirror available at notepad-plus-plus/notepad-plus-plus

---

## 📈 Implementation Priority

### Phase 1: Presentation Demo ✅
- [x] Git for Windows
- [x] Visual Studio Code
- [x] Node.js

### Phase 2: Developer Essentials (Target: Week 2)
- [ ] GitHub Desktop
- [ ] Postman
- [ ] Google Chrome

### Phase 3: Backend Stack (Target: Week 3-4)
- [ ] Docker Desktop
- [ ] MySQL Server
- [ ] MySQL Workbench
- [ ] .NET SDK

### Phase 4: Data Science (Target: Week 5)
- [ ] Python 3.11+
- [ ] JupyterLab
- [ ] R-Studio Desktop
- [ ] DBeaver

### Phase 5: General Tools (Target: Week 6)
- [ ] VLC Media Player
- [ ] Notepad++

---

## 🔧 Technical Implementation Notes

### Silent Installation Flags Reference

| Installer Type | Common Flags | Example |
|----------------|--------------|---------|
| Inno Setup | `/VERYSILENT /NORESTART /SP-` | Git for Windows |
| NSIS | `/S` | Notepad++, VLC |
| MSI | `/quiet /norestart` | Node.js, MySQL |
| Microsoft Store | N/A (uses winget) | Future consideration |

### Validation Strategy

Each software requires 3-5 validation checks:
1. **File Existence:** Primary executable exists
2. **Command Availability:** Runs successfully from PATH
3. **Version Verification:** Matches expected version
4. **Path Configuration:** Added to system/user PATH
5. **Service Status:** (For databases/daemons only)

---

## 📊 Statistics

- **Total Planned Software:** 16 packages
- **Implemented:** 3 (18.75%)
- **In Progress:** 1 (6.25%)
- **Planned:** 12 (75%)
- **Average Download Size:** ~120 MB
- **Total Repository Size (projected):** ~2 GB

---

## 🔐 Security Checklist

For each software added to repository:
- [ ] Downloaded from official source
- [ ] SHA-256 checksum verified
- [ ] Digital signature validated
- [ ] Scanned with Windows Defender
- [ ] Tested in isolated environment
- [ ] Documentation updated
- [ ] Release notes created

---

**Last Updated:** November 2024  
**Maintained by:** MAR9775  
**Project:** AurIOS (FYP)
