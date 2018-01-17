# Change the Git configuration.
git config

# Add options to the Git configuration.
git config --add user.name

# Local Git configuration file.
view .git/config

# Add global options to the Git configuration.
git config --global --add user.name
git config --global --add user.email

# Global git configuration file.
view ~/.gitconfig

# List Git configuration options.
git config --list

# View specific Git configuration options.
git config --get user.name

# Remove options from the Git configuration.
git config --unset <value>

# Set a default editor for Git actions.
git config --global --add core.editor <your editor vim/nano/emacs>

# Edit the Git configuration with the editor.
git config --edit


# Separate track: config aliases
# Separate track: config colors






In addition to configuring a remote repo URL, you may also need to set global Git configuration options such as username, or email. The git config command lets you configure your Git installation (or an individual repository) from the command line. This command can define everything from user info, to preferences, to the behavior of a repository. Several common configuration options are listed below.

Git stores configuration options in three separate files, which lets you scope options to individual repositories (local), user (Global), or the entire system (system):

Local: <repo>/.git/config – Repository-specific settings.
Global: /.gitconfig – User-specific settings. This is where options set with the --global flag are stored.
System: $(prefix)/etc/gitconfig – System-wide settings.



# Files
.git/config vs ~/.gitconfig

# Config levels
Define the author name to be used for all commits in the current repository.
Typically, you’ll want to use the --global flag to set configuration options for the current user.

# Writing values
--add

--get
--get-all

--unset

# Deleting values

# Global config
Define the author name to be used for all commits by the current user.
git config --global user.name <name>

# Local config
Adding the --local option or not passing a config level option at all, will set the user.name for the current local repository.
git config --local user.email <email>

# Aliases
Create a shortcut for a Git command. This is a powerful utility to create custom shortcuts for commonly used git commands. A simplistic example would be:
git config --global alias.ci commit
This creates a ci command that you can execute as a shortcut to git commit.

# Editor
git config --system core.editor <editor>
Define the text editor used by commands like git commit for all users on the current machine. The <editor> argument should be the command that launches the desired editor (e.g., vi). This example introduces the --system option. The --system option will set the configuration for the entire system, meaning all users and repos on a machine.

# Edit git config in file
git config --global --edit
Open the global configuration file in a text editor for manual editing.

# Viewing config
git config --list

# Merge tools

# Colored output

# Formatting and whitespace
fix lineendings
