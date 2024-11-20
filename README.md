App-Manager

A lightweight and user-friendly application manager for Linux-based systems. Manage your installed applications with ease using an interactive GUI or manual commands.
Prerequisites


**NEW**
*You can now check for updates and it will automaticly update your APP-Manager*

**You can add custom configuration or data files to the paths listed in .gitignore, and those files won't affect Git operations.**


Before you begin, ensure the following:

    Linux-based OS: The script is designed for Linux systems (Ubuntu/Debian recommended).
    Bash: The script runs in Bash (default shell for most Linux distributions).
    Git: Ensure Git is installed on your system (sudo apt-get install git).
    Zenity: The script uses Zenity for GUI dialogs. Install it with:

    sudo apt-get install zenity

Installation Steps
Step 1: Create a bin Directory in Your Home Folder

To run the App-Manager script globally, create a bin directory in your home folder:

    mkdir ~/bin
    cd ~/bin

Step 2: Clone the Repository

Clone the App-Manager repository into the bin directory:

    git clone https://github.com/Dillrex/APP-Manager.git

This will create the ~/bin/APP-Manager folder containing the script.
Step 3: Make the Script Executable

Navigate into the APP-Manager folder and give the script execution permissions:

    cd APP-Manager
    chmod +x app-manager

Step 4: Edit .bashrc to Add the Script to PATH

To run the script from anywhere, add its location to your system's PATH by editing the .bashrc file:

    Open .bashrc in a text editor:

nano ~/.bashrc

Add the following line at the end of the file:

    export PATH="$HOME/bin/APP-Manager:$PATH"

    Save and exit:
        Press Ctrl + X to exit.
        Press Y to confirm changes.
        Press Enter to save the file.

Step 5: Apply the Changes

Reload .bashrc to apply the changes:

    source ~/.bashrc

Step 6: Run the Script

You can now run the App-Manager script from anywhere:

    app-manager <command> [arguments]

For help and available commands:

    app-manager help

For example, to list installed apps:

    app-manager i

Optional: Verify the Installation

To verify the script is installed correctly, run:

which app-manager

This should return the path to the script, e.g., ~/bin/APP-Manager/app-manager.
Troubleshooting
1. Permission Denied

Ensure the script has the correct executable permissions:

    chmod +x ~/bin/APP-Manager/app-manager

2. Command Not Found

If the app-manager command is not found, verify the PATH setup:

confirm the line in .bashrc:

export PATH="$HOME/bin/APP-Manager:$PATH"

Reload .bashrc:

    source ~/.bashrc


## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) License. 

For details, see the [LICENSE](./LICENSE) file or visit [Creative Commons](https://creativecommons.org/licenses/by-nc/4.0/).

