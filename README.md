# Obsidian Vault Template

These are my current Obsidian vault settings, templates and directory structure. The base template
was taken from [kepano](https://github.com/kepano/kepano-obsidian) with additional templates and
changes in settings built on top by myself.

The main idea behind this template is to create symlinks for all of the settings files, templates
etc. in a new directory dedicated to the new vault using an install script. Any changes to those
files inside Obsidian can then easily be versioned using git, without having to manually copy the
changed files into this repository each time settings have been changed.

The install script will also function as a vault initializer by additionally creating all other
directories necessary for the first install (e.g. a "Daily" or "Attachments" directory).

## Usage

To use this template for a completely new vault follow these steps:

```sh
# Change to the directory you want to create your vault at
cd your/desired/location


```

## Limitations

The install script will only work for a new vault, or if all of the settings on an existing vault
will be deleted before running the script. This is because the scripts assumes there to not be
existing files of the same name in order to create the symlinks (like an existing `.obsidian/app.json` file).

Support when it comes to the install script will also be limited to Unix operating systems
(Linux/macOS/WSL).
