[source](https://youtu.be/tZop-zjYkrU)
A terminal is a text-based interface for interacting with a computer system, usually by entering commands. In the past, it referred to hardware devices (e.g. CRT monitor and keyboard)
In modern computing, it is usually a software that provides command-line interface(CLI). It doesn't process commands but relays them to a **shell** (such as Bash, PowerShell, Command Prompt), which interprets and executes them.
- Shell: program that interprets commands
Thus, Windows Terminal is the terminal emulator - it provides an interface to enter commands that are processed by a shell. PowerShell is the default shell. It is an emulator since terminals used to be physical systems, but are being emulated by software. This is just like how a Game Boy can be emulated using software as opposed to physical components.

# What is Telnet?
It is a terminal emulation program used for accessing remote servers as if you were sitting in front of it. Also used to test ports. Can be used on Windows/MacOS but usually used on Linux/Unix systems. Since there are no graphics, it is very fast. All commands are sent in clear text (no encryption), so someone could easily intercept this information, which could be usernames, passwords, etc. Thus, it is used locally or with older systems that don't support SSH

How to enable Telnet in windows:
1. Control Panel
2. Programs
3. Under Programs and Features, click Turn Windows features on or off
4. Check the box next to Telnet Client and click OK
Note: It failed the first time I did this, but succeeded the next. idk why
Then, do Windows key + X and select Terminal

# What is SSH?
Stands for Secure Shell.
Accomplishes the same purpose as Telnet but encrypts the data. Provides password and public key authentication.
Password authentication: user enters a username and password to connect to an SSH server.
Public key authentication: 
1. Server sends challenge (random data) to the client
2. Client signs challenge using a **private key** (key that is kept secret on the client machine). If the private key solves the challenge, a digital signature is sent back to the server.
3. The server checks the signature using the client's **public key** (stored on the server). If the signature matches, authentication succeeds

