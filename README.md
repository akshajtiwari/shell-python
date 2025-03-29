# Custom Shell

A simple custom shell implemented in Python that supports basic shell commands like `cd`, `pwd`, `echo`, `type`, and external commands found in the system `PATH`.

## About This Project
This is a personal project created while learning Python and gaining Linux experience. It serves as a foundational step in understanding shell functionality and command execution.

## Features

- **Basic Command Execution**: Runs system commands found in `PATH`.
- **Built-in Commands**:
  - `cd`: Change directory (supports `cd ~` and relative/absolute paths).
  - `pwd`: Print the current working directory.
  - `echo`: Print given arguments.
  - `type`: Identify if a command is built-in or external.
  - `exit 0`: Exit the shell.
- **Error Handling**: Provides appropriate error messages for invalid commands and missing directories.
- **Interactive Prompt**: Displays a `$ ` prompt for user input.

## Installation

To use this shell, ensure you have Python installed (preferably Python 3.x). Clone this repository and navigate to the directory:

```sh
$ git clone https://github.com/akshajtiwari/shell-python.git
$ cd shell-python
```

## Usage

Run the shell using:

```sh
$ python3 shell.py
```

### Supported Commands

#### Built-in Commands:
- **`pwd`**: Prints the current directory.
  ```sh
  $ pwd
  /home/user
  ```
- **`cd [directory]`**: Changes the directory.
  ```sh
  $ cd Documents
  $ pwd
  /home/user/Documents
  ```
- **`cd ~`**: Moves to the home directory.
  ```sh
  $ cd ~
  $ pwd
  /home/user
  ```
- **`echo [text]`**: Prints text to the screen.
  ```sh
  $ echo Hello, World!
  Hello, World!
  ```
- **`type [command]`**: Identifies if a command is built-in or external.
  ```sh
  $ type echo
  echo is a shell builtin
  ```
- **`exit 0`**: Exits the shell.
  ```sh
  $ exit 0
  ```

#### External Commands:
The shell supports running any executable available in the system `PATH`. Examples:
```sh
$ ls
$ uname -a
$ python3 --version
```

## How It Works

1. **Command Parsing**: The shell reads user input and processes it using `shlex.split()` to correctly handle quoted arguments.
2. **Execution Flow**:
   - If the command is built-in, it is executed directly.
   - Otherwise, it checks if the command exists in `PATH` and executes it using `subprocess.run()`.
3. **Error Handling**:
   - Invalid commands return a `command not found` error.
   - Directory changes (`cd`) validate paths before executing.





## Future Enhancements
- Implement support for environment variables.
- Add piping and redirection.
- Improve error handling and user experience.
- Implement a history feature.

## Contributing
Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.



Made with ❤️ by [Akshaj Tiwari](https://github.com/akshajtiwari)

