# Gocli
🚀 Go Command Line Interface All-in-One. 🚀

### Installation guide:

- Create a virtual environment.
```commandline
python3 -m venv ~/gocli
```
- Activate the virtual environment.
```commandline
source ~/gocli/bin/activate
```
- Install gocli package from the testpypi.
```commandline
python3 -m pip install --index-url https://test.pypi.org/simple/ --extra-index-url  https://pypi.org/simple/ gocli==2.4.5.5
```

- Add this in the dotfile (for bash shell add in ~/.bashrc for zsh shell add in ~/.zshrc).
  
```
For Bash Shell
$ nano ~/.bashrc
$ source ~/gocli/bin/activate   # add this line at the bottom.

For ZSH Shell
$ nano ~/.zshrc
$ source ~/gocli/bin/activate   # add this line at the bottom.
```

---

### Usage guide:

**Usage**:

```console
$ gocli [OPTIONS] COMMAND [ARGS]...
```

**Options**:

* `-v, --version`: Prints the Version and Changelog.
* `--install-completion`: Install completion for the current shell.
* `--show-completion`: Show completion for the current shell, to copy it or customize the installation.
* `--help`: Show this message and exit.


**Commands**:

* `bug`: [Bug Descriptor]     Generates the Bug Description from the connected device.
* `cmt`: [Comment Descriptor] Generates the Comment Description from the connected device.
* `qa`: [QA Assist]          Helpful functions for QA Testers.
* `env`: [Environment Info]   Prints the Environment Info.
* `brp`: [Bug Report]         Generates the Bug report.
* `ss`: [Screenshot]         Captures the screenshot.
* `sr`: [Screen Record]      Captures the Screen Record.
* `ti`: [Text Input]         Enters the user given text in text fields.
* `vm`: [Version Manager]    Fetches the packages from the device.
* `edit`: Opens the config file in either vscode or...
* `reset`: Resets the config file.
* `update`: Updates the gocli if there is a new version.
* `feedback`: Opens the Google Form for providing the...

## `gocli bug`

Generates Bug description from the Connected Android device 📲.

Options:

    --with-bugreport, -w: Include a bug report in the output.
    --upload, -u: Uploads the Bug Description to buganizer.

Examples:

    $ gocli bug --with-bugreport
    $ gocli bug -w
    $ gocli bug --upload
    $ gocli bug -u
   

**Usage**:

```console
$ gocli bug [OPTIONS]
```

**Options**:

* `-w, --with-bugreport`: Captures the Bug Report.
* `-u, --upload`: Exports the Bug Description to Buganizer.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli cmt`

Generates Comment description from the Connected Android device 📲.

Options:

    --with-bugreport, -w: Include a bug report in the output.
    --upload, -u: Uploads the Comment Description to buganizer bug ID.

Examples:

    $ gocli cmt --with-bugreport
    $ gocli cmt -w
    $ gocli cmt --upload
    $ gocli cmt -u
   

**Usage**:

```console
$ gocli cmt [OPTIONS]
```

**Options**:

* `-w, --with-bugreport`: Exports the Comment Description to Buganizer.
* `-u, --upload`: Captures the Bug Report.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli qa`

Contains list of actions which are help for QA.

Instructions:

    c - Clears current package.
    C - Clears User selected package.
    f - Force stops current package.
    F - Force stops User selected package.
    v - Prints current package version details.
    V - Prints User selected package  details.
    i - Installs User selected package from Downloads folder.
    u - Uninstalls the User selected package.
    r - Reboots the connected Android device.
    x - Exits the Qa Assist.

**Usage**:

```console
$ gocli qa [OPTIONS]
```

**Options**:

* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli env`

Prints the Environment info in a Markdown format.

**Usage**:

```console
$ gocli env [OPTIONS]
```

**Options**:

* `-s, --select`: Allows the user to select the packages more interactively.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli brp`

Generates the Bug report from the Connected Android device 📲.

Example:

    $ gocli brp         # Explicitly generates the bugreport from the connected device.

**Usage**:

```console
$ gocli brp [OPTIONS]
```

**Options**:

* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli ss`

Captures the screenshot from the Connected Android device 📲.

Options:

    --upload, -u: Uploads the screenshot to the http://screen/


Examples:

    $ gocli ss                      # Takes the screenshot and copies to the clipboard.
    $ gocli ss --upload             # uploads to the screenshot/

**Usage**:

```console
$ gocli ss [OPTIONS]
```

**Options**:

* `-u, --upload`: Uploads the screenshot to http://screen/.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli sr`

Captures the Screen Recording from the Connected Android device 📲.

Options:

    --file-name, -f: Name of the screen recording.
    --duration, -d: Duration of the screen recording (default: 180 seconds).

Examples:

    $ gocli sr -f "Name of the recording"       # Captures the Screen recording from the device.
    
**Usage**:

```console
$ gocli sr [OPTIONS]
```

**Options**:

* `-f, --file-name TEXT`: Name of the Screen Recording.
* `-d, --duration INTEGER`: Duration of the Screen Recording.  [default: 180]
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli ti`

Enters the User given text input in the text fields.

Examples:

    $ gocli ti test@gmail.com
    $ gocli ti This is a test text input

**Usage**:

```console
$ gocli ti [OPTIONS] INPUT_TEXT...
```

**Arguments**:

* `INPUT_TEXT...`: [Text Input]         Enters the user given text in text fields.
  [required]

**Options**:

* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli vm`

Fetches all the packages (user &amp; system) from the connected device 📲.

Options:

    --type, -t:        all - default, u for user installed, s for system packages
    --Print, -p:       Prints the fetched packages in the terminal.

Examples:
    Simple Mode

        $ gocli vm               # Fetches all the packages.
        $ gocli vm -pt s         # Prints System packages.
        $ gocli vm -pt u         # Prints User installed packages,Detailed Mode
        $ gocli vm -d            # Fetches all the packages.
        $ gocli vm -d -pt s      # Prints System packages.
        $ gocli vm -d -pt u      # Prints User installed packages,


**Usage**:

```console
$ gocli vm [OPTIONS]
```

**Options**:

* `-t, --type TEXT`: Fetches based on type. s = system packages, u = user installed, else all packages.
* `-d, --detailed`: Gives the simplified output [Package, Version, Version code].
* `-p, --display`: Prints the packages in the terminal.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.


## `gocli edit`

Opens the config file in either vscode or default text editor.

**Usage**:

```console
$ gocli edit [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.


## `gocli reset`

Resets the config file.
NOTE: Use this only when you get configuration errors. This will delete previous configuration file.

**Usage**:

```console
$ gocli reset [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.


## `gocli update`

Updates the gocli if there is a new version.

**Usage**:

```console
$ gocli update [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.


## `gocli feedback`

Opens the Google Form for providing the Feedback and Suggestions.

**Usage**:

```console
$ go feedback [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.

