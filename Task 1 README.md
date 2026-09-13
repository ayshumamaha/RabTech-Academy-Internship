# RabTech-Academy-Internship
Python Software Engineering Internship
TASK 1
# Packaged CLI Diagnostics Tool

## Overview

The Packaged CLI Diagnostics Tool is a Python-based command-line utility designed to perform basic system and development-environment diagnostics.

The tool checks important system information such as the installed Python version, available disk space, environment variables, and commonly used developer tools. It provides the results in a human-readable format and can also save the diagnostic information as a JSON file.

The project demonstrates Python command-line development, system inspection, JSON data handling, modular programming, and basic software diagnostics.

## Features

* Checks the installed Python version.
* Checks available disk space.
* Checks important environment variables.
* Detects installed developer tools such as Python and Git.
* Displays diagnostic results in a human-readable format.
* Generates a JSON diagnostic report.
* Provides a command-line interface using `argparse`.
* Uses meaningful diagnostic status values such as `OK`, `WARNING`, and `MISSING`.

## Technologies Used

* Python
* Python Standard Library
* `argparse`
* `json`
* `os`
* `shutil`
* `sys`

## How It Works

The application performs a series of diagnostic checks:

1. Python version is identified.
2. Available disk space is calculated.
3. The `PATH` environment variable is checked.
4. Python and Git availability are verified.
5. Results are displayed on the command line.
6. Results can optionally be saved to a JSON file.

## Running the Project

Run the diagnostics normally:

```bash
python cli.py
```

Generate a JSON report:

```bash
python cli.py --json
```

## Output

The application displays information similar to:

```text
==================================================
SYSTEM DIAGNOSTICS REPORT
==================================================

Check: Python Version
version: 3.x.x
status: OK

Check: Disk Space
free_gb: xx.xx
status: OK

Check: Environment Variable: PATH
status: OK

Check: Developer Tool: python
status: OK

Check: Developer Tool: git
status: OK

==================================================
```

When the `--json` option is used, a file named:

```text
diagnostics_report.json
```

is generated.

## Project Objectives

* Develop a reusable Python command-line utility.
* Practice modular Python programming.
* Understand system-level information gathering.
* Work with JSON output.
* Implement command-line arguments.
* Provide useful diagnostic information in a simple format.

## Applications

The tool can be used as a basic environment-checking utility before running Python-based software projects or development workflows.

## Author
M. Ayshwarya
