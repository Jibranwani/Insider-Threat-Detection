## EMPLOYEE MONITORING SYSTEM🕵️‍♂️



### Features
- Pure Python.
- Persistence:
  - Adding to Windows Startup.
- Human-readable logs:
  - Logging keys as they actually are in your layout;
  - Logging window titles and current time where appropriate;
  - Backspace support (until the active window is changed);
  - Full upper-/ lowercase detection (capslock + shift keys).
- Privacy protection:
  - RSA public-key encryption of logs on the fly. using [PyCryptoDome](https://pycryptodome.readthedocs.io/en/latest/).


# Installation

##### **Quick start**
1. ``
2. `cd python-keylogger`
3. Customize parameters in Start.py: url_server_upload, hidden_service_check_connection.
###### **Run as a Python script**
3. `pip install requirements.txt` (alternatively `python -m pip ...`)
4. `python Start.py`
###### **Run as an executable**
3. `pip install pyinstaller`
4. `pyinstaller --onefile --noconsole --icon=icon.ico Start.py`
5. `dist\Start.exe`
###### **To use RSA log encryption/decryption (optional)**
1. Generate RSA key pair (optional): `python rsa_key_generator.py`.
1. Change the public key filename / paste the key in Start.py.
1. To decrypt logs type `python log_decryptor.py`, and then follow the instructions given by the script.

##### System arguments
`Start.py mode [encrypt]`
- **modes**:
  - **local:** store the logs in a local txt file. Filename is a MD5 hash of the current date (YYYY-Mon-DD).
  - **debug:** write to the console.
- **[optional]**
  - **encrypt:** enable the encryption of logs with a public key provided in Start.py.

