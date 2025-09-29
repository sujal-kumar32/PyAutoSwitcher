# PyAutoSwitcher
PyAutoSwitcher

PyAutoSwitcher is a smart Python project launcher that automatically chooses the best Python interpreter for your project based on its dependencies and Python version requirements. It ensures that your scripts run smoothly without manual version juggling or environment conflicts.

Key Features

Automatic Python version selection: Detects the optimal Python interpreter installed on your system according to project requirements (pyproject.toml, setup.cfg, requirements.txt, or PyPI metadata).

Environment management: Creates and uses isolated virtual environments automatically.

Dependency handling: Installs missing packages in the selected environment to make sure your script runs without errors.

Import probing: Checks that required modules are available before executing the script.

Caching for speed: Remembers previously selected interpreters and environments for faster execution on repeated runs.

Flexible strategy: Choose the highest, lowest, or current preferred Python version for maximum compatibility or latest features.

How It Works

Discover interpreters: Scans your system for installed Python versions.

Parse project constraints: Reads pyproject.toml, setup.cfg, inline # requires-python, and package-level Python constraints from PyPI.

Filter interpreters: Selects interpreters compatible with all requirements.

Probe modules: Checks if required packages are installed in the chosen interpreter.

Create venv & install packages: Sets up a virtual environment and installs any missing dependencies.

Run script: Launches the target script in the isolated environment.

Use Cases

Multi-version Python environments where different projects require different versions.

Avoiding manual venv management for dependency-heavy projects.

Testing scripts across multiple Python versions seamlessly.

Getting Started

Clone the repo:

git clone https://github.com/<yourusername>/PyAutoSwitcher.git
cd PyAutoSwitcher


Install required packages:

pip install -r requirements.txt


Run your script using PyAutoSwitcher:

python pyauto.py --script path/to/your_script.py --requirements path/to/requirements.txt