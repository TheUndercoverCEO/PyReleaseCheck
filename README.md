# Update-Checker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Description

This module allows you to check if the most recent release from a github repo is newer than the version localy on the users PC.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Changelog](#changelog)

## Installation
Currently this module is not available through pypi so you must clone the repo and drag the Pycheck.py file into your project directory. You will also require the beautifulsoup4, win10toast and platform modules.

## Usage
To use this module we first need to import the module into our python project.

```py
import pyceck
```

<br/>

Once we have the module imported we can use the isCurrent function to check if there is a new version of the program available based on the name of the most recent github release. In this example the rep (Example/ExampleRepo) has a new version available.

```py
version = "0.1.0" # Current Version of program
repo = "Example/ExampleRepo" # The owner of the repo/the name of the repo

print(pycheck.isCurrent(version, repo))
# Will return False as a bool
```

<br/>
If the user is on windows we can also send a notification.

```py
notify = True # Show notification, default is False
notifyDuration = 5 # The amount of seconds the notification will show for. default is 3

print(pycheck.isCurrent(version, repo, notify, notifyDuration))
# Will return False as a bool and show a desktop notification.
```

## Changelog
### V0.1.0
- Can now check local version against github release name
- Added ability to notify
