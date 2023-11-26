# Installing Apache Superset on Windows 10
⚠️ WARN: This doc might be outdated. Use with caution. Only tested with Python v3.11.6

# Pre-Requisites

1.Install Microsoft Visual C++ 14.x standalone: Build Tools for Visual Studio 2019 (x86, x64, ARM, ARM64)

1. Select latest version of MSVCv142 - VS 2019 C++ x64/x86 build tools
2. Select Windows 10 SDK

2.Install Python [3.11.6](https://www.python.org/downloads/release/python-3116/)

1. Install PIP within the installer
2. Add Python 3.11.6 to PATH

3.Use CMD to execute below commands (Recommended)

# Installation
```
:: Create directory to host the files
mkdir D:\superset
cd /d D:\superset

:: Check Versions
python --version
pip --version
systeminfo | findstr /C:"OS"

:: Upgrade Setuptools & PIP
pip install --upgrade setuptools pip

```
### 1.Install Virtual Environment
    pip install virtualenv

### 2.Create Virtual Environment named venv
    python -m venv venv

### 3.Activate Virtual Environment
    venv\Scripts\activate

### 4.Workaround - Install PIP within Virtual Environment
    curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py --ssl-no-revoke

### 5.Workaround - Run get-pip.py
    python get-pip.py

### 6. Upgrade Setuptools & PIP
    pip install --upgrade setuptools pip

## 7.Locate the geohash file in Path
python geohash file and geohash.py file into superset/venv/lib/Scripts/site_packages

### 8.Install apache superset
    pip install apache-superset

### 9.Upgrade Superset db
    superset db upgrade
