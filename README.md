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
python3 -m pip install --index-url https://test.pypi.org/simple/ --extra-index-url  https://pypi.org/simple/ gocli==0.1.8.3
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

# `gocli`

**Usage**:

```console
$ gocli [OPTIONS] COMMAND [ARGS]...
```

**Options**:

* `--install-completion`: Install completion for the current shell.
* `--show-completion`: Show completion for the current shell, to copy it or customize the installation.
* `--help`: Show this message and exit.

 

**Commands**:

* `brp`: Generates the Bug report.
* `bug`: Generates the Bug Description from the connected device.
* `cmt`: Generates the Comment Description from the connected device.
* `sr`: Captures the Screen Record.
* `ss`: Captures the screenshot.
* `ti`: Enters the user given text input.
* `vm`: Fetches the packages from the device.

---

## `gocli brp`

Generates the Bug report from the Connected Android device 📲.

**Examples**:

    $ gocli brp

**Usage**:

```console
$ gocli brp [OPTIONS]
```

**Options**:

* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

## `gocli bug`

Generates Bug description from the Connected Android device 📲.

**Options**:

    --with-bugreport, -w: Include a bug report in the output.
    --upload, -u: Uploads the Bug Description to buganizer.

**Examples**:

    $ gocli bug --with-bugreport
    $ gocli bug -w
    $ gocli bug --upload
    $ gocli bug -u
    $ gocli bug -wu  [Recommended]  # Generates bugreport, also Uploads
                                      bug description to buganizer.

**Usage**:

```console
$ gocli bug [OPTIONS]
```

**Options**:

* `-w, --with-bugreport`: Captures the Bug Report.
* `-u, --upload`: Exports the Bug Description to Buganizer.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

## `gocli cmt`

Generates Comment description from the Connected Android device 📲.

**Options**:

    --with-bugreport, -w: Include a bug report in the output.
    --upload, -u: Uploads the Comment Description to buganizer bug ID.

**Examples**:

    $ gocli cmt --with-bugreport
    $ gocli cmt -w
    $ gocli cmt --upload
    $ gocli cmt -u
    $ gocli cmt -wu  [Recommended]  # Generates bugreport, also exports Comment description
                                      to buganizer bug ID.

**Usage**:

```console
$ gocli cmt [OPTIONS]
```

**Options**:

* `-w, --with-bugreport`: Exports the Comment Description to Buganizer.
* `-u, --upload`: Captures the Bug Report.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

## `gocli sr`

Captures the Screen Recording from the Connected Android device 📲.

**Options**:

    --file-name, -f: Name of the screen recording.
    --duration, -d: Duration of the screen recording (default: 180 seconds).

**Examples**:

    $ gocli sr -f "Name of the recording"      # Captures the Screen recording from the device.
    $ gocli sr -d 10  [Recommended]            # Captures the Screen recording with
                                                 10 sec duration.

**Usage**:

```console
$ gocli sr [OPTIONS]
```

**Options**:

* `-f, --file-name TEXT`: Name of the Screen Recording.
* `-d, --duration INTEGER`: Duration of the Screen Recording.  [default: 180]
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

## `gocli ss`

Captures the screenshot from the Connected Android device 📲.

**Options**:

    --upload, -u: Uploads the screenshot to the http://screen/


**Examples**:

    $ gocli ss                      # Takes the screenshot and copies to the clipboard.
    $ gocli ss --upload             # uploads to the screenshot/
    $ gocli ss -u  [Recommended]    # Captures and uploads the screenshot.

**Usage**:

```console
$ gocli ss [OPTIONS]
```

**Options**:

* `-u, --upload`: Uploads the screenshot to http://screen/
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

## `gocli ti`

Enters the User given text input in the text fields.

**Examples**:

    $ gocli ti test@gmail.com
    $ gocli ti This is a test text input

**Usage**:

```console
$ gocli ti [OPTIONS] TEXT_IP...
```

**Arguments**:

* `TEXT_IP...`: Enters the user given text input.
  [required]

**Options**:

* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

## `gocli vm`

Fetches all the packages (user & system) from the connected device 📲.

**Options**:

    --type, -t:        all - default, 3 for user installed, s for system packages
    --display, -d:     Displays the fetched packages in the terminal.

**Examples**:

    $ gocli vm          # Fetches all the packages.
    $ gocli vm -d       # Displays the packages in tabular format
    

**Usage**:

```console
$ gocli vm [OPTIONS]
```

**Options**:

* `-t, --type TEXT`: Fetches based on type. s = system packages, u = user installed, else all packages.  [default: all]
* `-s, --simple`: Gives the simplified output [Package, Version, Version code ].
* `-d, --display`: Prints the packages in the terminal.
* `-v, --version`: Prints the CLI Version and Changelog.
* `--help`: Show this message and exit.

---

Developed by Govardhan 👨‍💻 v0.1.8.2
