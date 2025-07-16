## Python Virtual Environment - SOP (Ubuntu)

## Author Information

| Created | Reviewer |
|---------|----------|

---
 Aryan mishra | Siddharth
## Objective
This SOP provides a step-by-step guide to **create, activate, use, freeze, deactivate, delete**, and **troubleshoot** Python virtual environments on Ubuntu. It ensures your projects run in isolated environments, avoiding conflicts and improving reproducibility.

---

##  Table of Contents
- [Prerequisites](#-prerequisites)
- [Creating a Virtual Environment](#-creating-a-virtual-environment)
- [Activating the Virtual Environment](#-activating-the-virtual-environment)
- [Installing Packages](#-installing-packages)
- [Freezing Requirements](#-freezing-requirements)
- [Deactivating the Environment](#-deactivating-the-environment)
- [Deleting a Virtual Environment](#-deleting-a-virtual-environment)
- [Troubleshooting](#-troubleshooting)
- [Best Practices](#-best-practices)
- [Example Folder Structure](#-example-folder-structure)

---

##  Prerequisites

| Requirement        | Command / Description                              |
|--------------------|-----------------------------------------------------|
| Python Installed   | `python3 --version` or install via:<br>`sudo apt install python3` |
| `venv` Module      | Install using:<br>`sudo apt install python3-venv`   |

---

## Creating a Virtual Environment

```bash
python3 -m venv <env_name>
```
---
## Example
```bash
python3 -m venv venv
```
- This creates a directory venv/ containing an isolated environment.
---
