# Installing and Configuring Git

## Step 1: Install Git 

Update your package list and install Git:

```bash sudo apt update && sudo apt install git -y```

## Step 2: Configure Git

Set your global Git configuration details:

    ```bash
    git config --global user.name "Your Name"
    git config --global user.email "you@exampleemail.com"
    git config --global init.defaultBranch main
    ```

**Note:**  
    Replace `"Your Name"`, `"you@exampleemail.com"`, and `"main"` with your preferred name, email address, and default branch name.

## Step 3: Verify the Installation

Check the installed Git version:

``` bash
git --version
``
