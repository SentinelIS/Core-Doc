---
layout: single
title: Installation
permalink: /installation/

toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---

## Downloading

Download the entire project folder from the GitHub repository and open it in your code editor if you want to use it as-is. If you’d like to customize the software to suit your needs, feel free to fork the repository. For general improvements, you can clone the repo and submit a pull request.

#### Github
[SentinelIS Information Security Management System](https://github.com/SentinelIS/SentinelIS-Core)

#### Clone
``` bash
git clone https://github.com/SentinelIS/SentinelIS-Core.git
```

## Setup Guide

### Step 1: Ports
Before starting the setup, please make sure that all required ports are free and not being used by any other software. You can change the ports for your local installation if needed. However, if you plan to contribute to this project, changing the ports is not allowed.

### Step 2: Create .env files
For all the different databases and services, you will need to set up a ```.env``` file containing all your keys and credentials. Please make sure to follow **exactly** this format:

```yaml
MYSQL_HOST=localhost
MYSQL_PORT=3307
MYSQL_ROOT_PASSWORD= ..
MYSQL_DATABASE= ..
MYSQL_USER= ..
MYSQL_PASSWORD= ..

MONGO_INITDB_ROOT_USERNAME= ..
MONGO_INITDB_ROOT_PASSWORD= ..
MONGO_INITDB_DATABASE= ..
MONGO_CONNECTION_STRING= ..

SQLITE_DB_PATH=/sqlite/data/mydb.sqlite
SQLITE_GUI_PORT=8081
```

For all database connections, Python test scripts are available. You can use these scripts to avoid testing the connections manually. If you choose not to use the Python scripts, you can safely delete the testing/ directory in the backend folder.