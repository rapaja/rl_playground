# Reinforcement Learning Playground

## Set-Up the Environment

1. **Make sure you have `Python` 3 installed.**

    Depending on the particular setup of your system, it it typically available as `python` or `python3`, although there are numerous other possibilities.

    In the sequel we assume that it is installed and available through the `python` command.

    For more information on `Python`, please visit <https://www.python.org/>.

1. **Clone this repository into desired location on your machine.**

    The following step is to clone (or copy) the files from the repository to a
    folder in your local machine. Go to the directly in which you would like to
    store the files, open your favorite shell, and type

    ```bash
    git clone https://github.com/rapaja/rl_playground.git
    cd rl_playground
    ```

    The above will work only if you have `git` installed. If not, you may simply
    navigate to <https://github.com/rapaja/rl_playground> and download all files
    from `GitHub`. Extract the archive into the desired folder, open shell there,
    and `cd` into the extracted directory.

    Upon completion of this step, you should see all the files from the `GitHub`
    repository copied to your local workspace.

1. **Create virtual environment.**

    Virtual environments enable multiple `Python` projects to coexist on a single machine, while each of them is maintaining its own independent set of dependencies.

    There are multiple ways in which one can create and manage virtual environments in `Python`. We use arguably the simplest one, based on the `venv` standard package.

    In your favorite shell, execute the following command

    ```bash
    python -m venv env
    ```

    This will create a sub-directory within your current directory named `env`.
    This directory will contain the python interpreter, all the associated scripts (including `pip` which is used for managing dependencies, as you will see shortly) and what is more important **it contains an insulated environment for your project
    with all packages installed locally**, so that any modification affects only the
    virtual environment and not the global `Python` installation.

    More information about virtual environments in `Python` can be found in

    * <https://realpython.com/python-virtual-environments-a-primer/>
    * <https://docs.python.org/3/library/venv.html>

1. **Activate virtual environment.**

    In order to use this new environment you need to activate it. This is done
    slightly differently depending on your shell of choice

    If you are using `bash` (or some of its "derivatives"), enter

    ```bash
    source ./env/bin/activate
    ```

    If you are using `PowerShell`, enter

    ```posh
    & .\env\Scripts\activate.ps1
    ```

    If you are using just plain `Windows` `Command Prompt`, enter

    ```posh
    .\env\Scripts\activate.bat
    ```

    Once the environment is activated each call to `python` command (or `pip`)
    refers to the local interpreter and not to the global one.

    To test this, in `bash` enter

    ```bash
    which python
    ```

    and in `PowerShell`

    ```posh
    get-command python
    ```

    In either case, you will get the full path to the active `python` interpreter,
    which should point to the executable within your virtual environment (within
    the `env` folder) and **not** to the globally installed `python` executable.

    I am not aware of the way this can be done in `Windows` `Command Prompt`.

1. **Install `Jupyter`**

    `Jupyter` is an interactive environment that enables seamlessly mixing text, code and visualizations. It may be used as your only IDE, but it is also possible to
    work from any other IDE of your choice.

    ```bash
    pip install jupyter
    ```

    You may test if the jupyter was installed properly by running

    ```bash
    jupyter lab
    ```

    Here, I am using `Jupyter Lab` interface. Optionally, you could also use `Jupyter Notebook` interface (by executing `jupyter notebook`), it does not really matter.

    For more information on `Jupyter` please visit <https://jupyter.org/>.

1. **Install dependencies: PyTorch**

    The most significant dependency that we need to install is `PyTorch`.

    <https://pytorch.org/>

    Depending on your machine configuration, your operative system, the available hardware accelerators (GPUs and like), and even depending on your `Python` distribution (vanilla `python` or `conda`), there are different ways to install it. The easiest way to do this (which will most likely **not** be able to use any
    hardware acceleration devices you may have access to) is

    ```bash
    pip install torch torchvision
    ```

    For more information, please see the installation instructions on the `PyTorch` website. They are very succinct and easy to follow.

    In order to check if the `torch` has been installed correctly, enter command `python` in yur favorite shell in order to activate `python` REPL. Execute

    ```python
    import torch
    ```

    If the command is executed and no error is reported, the installation was successful.

1. **Install requirements: All the rest.**

    For convenience it is best to keep all other requirements listed within a file
    named `requirements.txt` (the name is not required, but the convention is a strong
    standard). We invoke the `pip install` command again, but add the `-r` switch just before naming the requirements file. It will tell the `pip` to simply install all requirements listed there.

    ```bash
    pip install -r requirements.txt
    ```
