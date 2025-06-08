### Installing Python on Ubuntu

Ubuntu typically comes with **Python** pre-installed. To verify and install Python if necessary, follow these steps:

1. Open your terminal (press <kbd>Ctrl</kbd> + <kbd>`</kbd>).
2. Check if Python is installed:
    ```bash
    python3 --version
    ```
    - If a Python version is displayed, you’re all set!
    - If not, install Python and pip with:
    ```bash
    sudo apt update
    sudo apt install python3 python3-pip -y
    ```
3. Confirm the installation:
    ```bash
    python3 --version
    pip3 --version
    ```

> **Tip:** Keeping your system updated ensures you have the latest security patches and features.
