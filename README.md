# Reinforcement Learning Playground

## Set-Up the Environment

1. **Make sure you have `Python` 3 installed.**

    Depending on the particular setup of your system, it it typically available as `python` or `python3`, although there are numerous other possibilities.

    In the sequel we assume that it is installed and available through the `python` command.

1. **Clone this repository into desired location on your machine.**

    ```bash
    git clone https://github.com/rapaja/rl_playground.git
    cd rl_playground
    ```

1. **Create and activate a virtual environment.**

    Virtual environments enable multiple `Python` projects to coexist on a single machine, while each of them is maintaining its own independent set of dependencies.

    There are multiple ways in which one can create and manage virtual environments in `Python`. We use arguably the simplest one, based on the `venv` standard package.

    ```bash
    python -m venv env
    ```

    This command will create a new folder named `env` in the root of your working directory. In order to use this new environment you need to activate it.

    ```bash
    source ./env/bin/activate
    ```

1. **Install `Jupyter`**

    `Jupyter` is an interactive environment that enables seamlessly mixing text, code and visualizations.

    ```bash
    pip install jupyter
    ```

1. **Install dependencies.**

    First you need to install `PyTorch`.

    ```bash
    pip install torch torchvision
    ```

    Then, install other required dependencies using

    ```bash
    pip install -r requirements.txt
    ```
