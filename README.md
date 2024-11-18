Prerequisites

Before you begin, ensure the following:

You are using a Linux-based OS (Ubuntu/Debian recommended).
The script is written in Bash, so Bash should be installed (this is the default shell for most Linux distributions).
Git is installed on your system (to clone the repository).

Step 1: Create a bin Directory in Your Home Folder

To ensure you can run the App-Manager script from anywhere on your system, create a bin directory in your home folder.

Open a terminal and run the following commands:

    mkdir ~/bin
    cd ~/bin

This will create a bin folder in your home directory and navigate into it.
Step 2: Clone the Repository

Next, you need to clone the App-Manager repository into the bin folder. Run the following command:

    git clone https://github.com/Dillrex/APP-Manager.git

This will clone the repository into the ~/bin/APP-Manager directory.
Step 3: Make the Script Executable

After cloning the repository, navigate to the APP-Manager folder and make the script executable. Run the following commands:

    cd APP-Manager
    chmod +x app-manager

This gives execution permissions to the app-manager script, allowing you to run it from the terminal.
Step 4: Edit .bashrc to Run the Script from Anywhere

To be able to run the App-Manager script from anywhere, you need to add its location to your system's PATH. This is done by editing the .bashrc file.

Open the .bashrc file in a text editor:

    nano ~/.bashrc

Add the following line at the end of the .bashrc file:

    export PATH="$HOME/bin/APP-Manager:$PATH"

This adds the APP-Manager folder to your system's PATH, enabling you to run the app-manager script from anywhere.

Save the file and exit the text editor:
Press Ctrl + X to exit.
Press Y to confirm changes.
Press Enter to save the file.

Step 5: Apply the Changes

To apply the changes made to .bashrc, run the following command:

    source ~/.bashrc

This will reload the .bashrc file and apply the changes.
Step 6: Run the Script

Now, you can run the App-Manager script from anywhere by simply typing:

    app-manager <command> [arguments]

For example, to list installed apps:

    app-manager listapps

Optional: Verify the Installation

To ensure everything is working correctly, you can run:

    which app-manager

This should return the path to the app-manager script, indicating it's correctly set up and available globally.
Troubleshooting

If you encounter any issues:

Permission Denied: Ensure that the script has the correct executable permissions by running:

    chmod +x ~/bin/APP-Manager/app-manager

Command Not Found: If the app-manager command is not found, make sure the line added to .bashrc is correct, and run:

    source ~/.bashrc
