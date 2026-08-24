# Obsidian Vault Template

These are my current [Obsidian](https://obsidian.md/) vault settings, templates and directory structure. The base template
was taken from [kepano](https://github.com/kepano/kepano-obsidian) with additional templates and
changes in settings built on top by myself.

The main idea behind this template is to create symlinks for all of the settings files, templates
etc. in a new directory dedicated to the new vault using an initiation script. Any changes to those
files inside Obsidian can then easily be versioned using git, without having to manually copy the
changed files into this repository each time settings have been changed.

The initiation script will also function as a complete vault initializer by creating the vault
directory itself and additionally creating all other directories necessary for the first install
(e.g. a "Daily" or "Attachments" directory).

## Usage

To use this template for a completely new vault follow these steps:

```sh
# make init.sh executable
chmod +x init.sh

# initiate a new vault
./init.sh "~/path/to/your/desired/vault/location"

# Note: The directory provided to the script should not yet exist as it will be created during the
# initiation
```

After the vault is created you can then open Obsidian and select the option "Open folder as vault"
using your newly created vault directory.

## Limitations

The initiation script will only work for a new vault, or if all of the settings on an existing vault
will be deleted before running the script. This is because the scripts assumes there to not be
existing files of the same name in order to create the symlinks (like an existing `.obsidian/app.json` file).

Support when it comes to the initiation script will also be limited to Unix operating systems
(Linux/macOS/WSL).
