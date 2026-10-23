# CEN437 – Network Programming: Project 1

## 1. About the Project

This project is a Python-based network diagnostic tool developed to demonstrate socket programming, network diagnostics, time synchronization, socket settings, and error management.

The application can be accessed through two main entry points:

- **GUI Mode:** Provides a graphical user interface through `menu_gui.py`.
- **Terminal Mode:** Provides a text-based menu through `menu.py`.

The application includes machine information, echo testing, SNTP time synchronization, socket settings, error management, and chat functionality.

When the Chat option is selected from the terminal menu, the graphical chat interface opens automatically. Alternatively, the chat module can be started directly from the terminal.

## 2. Requirements and Libraries

- Python 3
- `socket`
- `time`
- `psutil`
- `logging`
- `datetime`
- `os`
- `sys`
- `subprocess`
- `threading`
- `queue`
- `tkinter`

The project was developed in a Windows environment.

### Installation

Make sure Python 3 is installed on your system.

Install the external dependency with the following command:

```bash
python -m pip install psutil
```

The following modules are part of Python's standard library and do not require separate installation:

- `socket`
- `time`
- `logging`
- `datetime`
- `os`
- `sys`
- `subprocess`
- `threading`
- `queue`

`tkinter` is generally included with standard Windows Python installations.

## 3. Project Structure

| File                        | Description                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------- |
| `menu_gui.py`               | Main graphical interface for accessing the network tools.                                     |
| `menu.py`                   | Terminal-based menu for selecting and running the available modules.                          |
| `chat_gui.py`               | Provides the graphical user interface for the chat application.                               |
| `chat_module.py`            | Implements the chat functionality using socket communication.                                 |
| `echo_client.py`            | Implements the client side of the echo test.                                                  |
| `echo_server.py`            | Implements the server side of the echo test.                                                  |
| `machine_module.py`         | Retrieves local machine and network information.                                              |
| `settingAnderror_module.py` | Manages socket settings, including timeout, blocking modes, buffer sizes, and error handling. |
| `time_syn_module.py`        | Retrieves time information from an SNTP server.                                               |

## 4. How to Run

Open a terminal in the project directory before running the commands.

### 4.1. GUI Mode

To launch the main graphical interface, run:

```bash
python3 menu_gui.py
```

### 4.2. Terminal Mode

To launch the terminal-based main menu, run:

```bash
python3 menu.py
```

The terminal menu allows users to select the available network tools. When the **Chat** option is selected, the graphical chat interface opens automatically.

### 4.3. Run the Chat Module Directly

To run the chat module directly from the terminal, use:

```bash
python3 chat_module.py
```

To launch only the graphical chat interface, without opening the main menu, use:

```bash
python3 chat_gui.py
```

**Note:** Depending on the Python installation and operating system, `python` may be used instead of `python3` on Windows.

## 5. Terminal Menu

When `menu.py` is executed, the following menu is displayed:

```text
NETWORK TOOL
1  Machine Information
2  Echo Test
3  SNTP Time Check
4  Socket Settings
5  Chat
6  Error Management
0  Exit

Choice:
```

Enter the corresponding number to select a module.

- **1 — Machine Information:** Displays local machine and network information.
- **2 — Echo Test:** Tests communication between an echo client and server.
- **3 — SNTP Time Check:** Retrieves time information from an SNTP server.
- **4 — Socket Settings:** Displays and modifies socket configuration.
- **5 — Chat:** Opens the graphical chat interface.
- **6 — Error Management:** Provides access to socket settings and error management.
- **0 — Exit:** Exits the application.

## 6. Socket Settings Menu

The Socket Settings section provides the following options:

```text
SOCKET SETTINGS
1  Current settings
2  Change timeout
3  Blocking mode
4  Non-blocking mode
5  Send buffer size
6  Receive buffer size
7  Show buffer sizes
0  Back
```

These options allow users to inspect and modify socket settings, including timeout values, blocking modes, and send/receive buffer sizes.

## 7. Logging

The application uses log files to record relevant events and error information.

The following log files are generated automatically when the corresponding modules run and write log entries:

- **`eror_module.log`** — Records error management and socket-related log messages.
- **`chat_module.log`** — Records chat-related log messages.

The log files do not need to be created manually. They are created automatically by the logging configuration when a log message is written. The files are stored in the application's working directory unless another path is configured.

## 8. GUI Screenshot

The following screenshot illustrates the application's graphical interface.



Make sure that `image.png` is located in the same directory as this README file, or update the image path accordingly.

## 9. Notes

- Run commands from the project directory so that the application can locate its modules and log files.
- An active network connection is required for features that communicate with external servers, such as SNTP time synchronization.
- The echo test requires the server to be running and reachable by the client.
- The chat module uses socket communication to exchange messages.
- Selecting Chat from the terminal menu automatically opens the graphical chat interface.
- Log files are generated automatically when logging is configured and a log message is written.

