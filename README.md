# NEW-PROJECT-NAME

## Using this template
*Please delete this section after installing the necessary working tools*
### Environment Setup (Requirements)
*If you have ran these commands previously, you can ignore this section. If you have doubts, you can safely run them without the risk of negative side effects*

Make sure you have homebrew and xcode installed. If you don't, follow these steps:
1. Install Homebrew. You can do this by running the following command:
```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
2. Install developer tools with the following command:
```zsh
xcode-select --install
``` 

### Tools Setup
With the tools mentioned above installed, you can now install the tools needed:<br>
3. Run `make install-tools`. This will install general tools

### Project Setup (New Project)
*Use `project-setup` if you are starting a new project*<br>
4. Choose a Python version and run the following command: `make project-setup PYTHON=3.10.13`.<br>*In this example we chose Python 3.10.13*<br>
5. run `source ./zshrc` or open a new terminal for the changes to take effect

### Project Setup (Existing Project)
*Use `project-install` if you are installing an existing project*<br>
4. Run `make project-install`

### Explanation
These commands will install the following tools:
- pypenv: Python version manager
    - try running `pyenv versions` to see the Python version you just installed
- pipx: Python package manager. We will only use this to install `poetry`
    - try running `pipx list` to see the packages you just installed.
- poetry: Python dependency manager
    - try running `poetry env list` to see the Python environment you just created
    - try running `poetry shell` to activate that virtual environment
- ipython:
    - the `kernelspec` command is part of `ipython`, on which `jupyter` is based.<br> Try running `jupyter kernelspec list` to see the kernel you have installed (make sure you have activated the virtual environment with `poetry shell`)

So, now you should have a Python dependency manager (poetry) that also takes care of the virtual environment for you. You should also have a jupyter kernel based on that virtual environment. You can now start working on your project. Run `jupyter-lab` directly on your terminal to start the jupyter server<br>
For more information on how to use these tools, please refer to the `TOOLS.md` file.

---

## Description
Brief description of the project. **Must include project's objective and scope**

## Installation
Instructions on how to install the project

## Usage
Instructions on how to use the project

## Contributing
Instructions on how to contribute to the project

## References
Link to references used in the project (Books, posts, videos, courses, repos, etc.)
