# Tools Guidelines
This is a brief introduction to useful commands for the tools used in this project. For more information, please refer to the official documentation of each tool.

## pyenv
This tool allows you to manage multiple Python versions in your machine. It is highly configurable and it allows you to run different versions of Python in different projects. You can configure a global version of Python, and then override it in a project-specific (local) manner. <br>
We won't be using it, but there is a pyenv extension called `pyenv-virtualenv` that allows you to manage virtual environments with pyenv. We will be using `poetry` for that purpose, but it is good to know that this tool exists.

A few useful commands:
- `pyenv versions`: list all the Python versions installed in your machine
- `pyenv install <version>`: install a specific Python version
- `pyenv global <version>`: set a global Python version (this will be the default version)
- `pyenv local <version>`: set a local Python version (this will override the global version in the current directory. It will be the default version for this project)

Reference:
- [pyenv reference](https://github.com/pyenv/pyenv)
- [pyenv-virtualenv reference](https://github.com/pyenv/pyenv-virtualenv)

## pipx
This tool allows you to install Python packages globally, without polluting your global Python environment. It is useful for installing tools that you will use in your terminal, such as `poetry` or `jupyterlab`. <br>
The idea is that you install once, and use it in all of you python installations. You can just install packages as you would with `pip`, just run `pipx install <package>`.

- [pipx reference](https://pypa.github.io/pipx/)

## poetry
Poetry is a quite powerful tool. It is a dependency manager, a virtual environment manager, and a packaging tool. We will be using it mostly as a dependency manager, though going through the documentation is highly recommended.<br>
Useful commands:
- `poetry install`: Install dependencies. This wil come in handy when you clone a project with an existing `pyproject.toml` file
- `poetry add <package>`: Add a package to the project. This will install the package and add it to the `pyproject.toml` file
- `poetry shell`: Activate the virtual environment
- `poetry run <command>`: Run a command in the virtual environment

Reference:
- [poetry reference](https://python-poetry.org/docs/)

## Python tools
after installing these tools, you will be able to see the kernel you just installed by running `jupyter-kernelspec list`. 
### ipython
Ipython is an interactive shell for Python. It is a more powerful version of the default Python shell. It is highly configurable and it has a lot of useful features. It is the base for `jupyter`.
### ipykernel
This is the kernel for `jupyter`. It allows you to run a jupyter notebook with a specific Python environment. Along with `ipython`, it will be used to manage the Python kernels to be used within `jupyter`.
### jupyterlab
This is a web-based interactive development environment for Jupyter notebooks.
### python-dotenv
This is a tool that allows you to load environment variables from a `.env` file. The idea is to have all the environment variables in a file that is not tracked by git, in order to avoid leaking sensitive information. This is useful for API keys, database credentials, etc.

## References
There is a good series of blog posts by Claudio Jolowicz that explain how to use these tools. I highly recommend going at least through the [first one](https://cjolowicz.github.io/posts/hypermodern-python-01-setup/).

## Next Tools
Tools to consider:
- [Cookiecutter](https://www.cookiecutter.io/)
- [DVC (Data Version Control)](https://dvc.org/)
- [pre-commit](https://pre-commit.com/)
