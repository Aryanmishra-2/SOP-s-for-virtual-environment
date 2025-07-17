## Python Virtual Environment - SOP (Ubuntu)

---
## Author Information

| Created         | Created on         | Version          | Last updated by   | pre Reviewer       | L0 Reviewer     | L1 Reviewer          |    L2 Reviewer    |
|-----------------|--------------------|------------------|-------------------|--------------------|-----------------|----------------------|-------------------|
| Aryan mishra    |                    | V.1              |                  |        Siddharth    |  Ram Ratan      |      Gaurav Singla   |   Mahesh Kumar    |
 

---

##  Table of Contents

- [Introduction](#-Introduction)
- [Prerequisites](#-prerequisites)
- [Creating a Virtual Environment](#-creating-a-virtual-environment)
- [Activating the Virtual Environment](#-activating-the-virtual-environment)
- [Installing Packages](#-installing-packages)
- [Freezing Requirements](#-freezing-requirements)
- [Deactivating the Environment](#-deactivating-the-environment)
- [Deleting a Virtual Environment](#-deleting-a-virtual-environment)
- [Troubleshooting](#-troubleshooting)
- [Best Practices](#-best-practices)
- [Conclusion](#-Conclusion)
- [References](#References)

---
 ## Introduction
Python virtual environments allow developers to create isolated environments for their projects. Each virtual environment has its own Python binaries and can have its own independent set of installed packages, avoiding conflicts between different projects.

step-by-step guide to **create, activate, use, freeze, deactivate, delete**, and **troubleshoot** Python virtual environments on Ubuntu.

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
## Activating the Virtual Environment
| Shell Type          |	Command      |
|---------------------| -------------|
| Bash/Zsh	           | source venv/bin/activate |
| Fish Shell	         | source venv/bin/activate.fish |
| C Shell	            | source venv/bin/activate.csh |

---
## Installing Packages

- Install required packages using pip

```bash
pip install <package_name>
```
###  Example
```bash
pip install requests flask
```
---
## Freezing Requirements

- To generate a list of installed packages

```bash
pip freeze > requirements.txt  
```
### Example
```bash
pip install -r requirements.txt
```
---
## Deactivating the Environment

- Exit the virtual environment
```bash
deactivate
```
## Deleting a Virtual Environment
-  delete the directory
```bash
rm -rf venv
```
- Ensure you're not inside the virtual environment before deleting.

## Troubleshooting
|  Problem	          |   Cause / Solution         |
|--------------------|----------------------------|
| command not found: | python3	Python not installed: sudo apt install python3
| No module named venv	Install venv: |  sudo apt install python3-venv
| Permission denied	 | Check file permissions / avoid using sudo unnecessarily
| Activation not working	Use correct command: |  source venv/bin/activate
| pip not found in venv	Recreate venv or run: | python3 -m ensurepip
| Can't install packages	Install build tools: | sudo apt install build-essential python3-dev

---
## Best Practices

| no  | Practice                                                                |
|-----|-------------------------------------------------------------------------|
| 1.  | Use `.venv` or `venv` as a convention for naming environments.          |
| 2.  | Add the environment directory to `.gitignore`.                          |
| 3.  | Always track dependencies using `requirements.txt`.                     |
| 4.  | Use per-project virtual environments.                                   |
| 5.  | Automate setup via `Makefile` or `setup.sh`.                            |

---
## Conclusion

Python virtual environments are essential for any modern Python development workflow. By isolating dependencies and tools per project, they prevent version conflicts, streamline collaboration, and improve portability. Following this SOP ensures your environment is reproducible, clean, and aligned with Python best practices.

---

## References

| Name                              | Practice                                                                |
|-----------------------------------|-------------------------------------------------------------------------|
|  Python venv documentation:      |    [Link](https://docs.python.org/3/library/venv.html)                  |
|  pip official documentation:     |    [Link](https://pip.pypa.io/en/stable/)                               |
|  virtualenv documentation:       |    [Link](https://virtualenv.pypa.io/en/latest/)                        |
|  Real Python Tutorial:           |    [Link](https://realpython.com/python-virtual-environments-a-primer/) |
|  GeeksForGeeks Article:          |    [Link](https://www.geeksforgeeks.org/python-virtual-environment/)    |

