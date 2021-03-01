# Python Installation for Linux Mint

#### Python 2 Delete
```bash
sudo apt purge -y python2.7-minimal
sudo apt autoremove python
```
---
#### Python 2 Install
```bash
sudo apt-get update
sudo apt-get install build-essential checkinstall
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
sudo apt install python-is-python2
python --version
```
```
Python 2.7.18  # Output
```
---
#### Python 3 Install
```bash
sudo apt install python-is-python3
python --version
```
- Currently your main python version is seems python 3
```
Python 3.8.2  # Output
```
- If you want to switch python main version to python 2
```bash
sudo apt install python-is-python2
python --version
```
- Thats it
```
Python 2.7.18  # Output
```
---
#### Choosable Python Versions
```bash
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 1
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 2
```
- We create a list actually lets check it
```bash
sudo update-alternatives --list python
```
- Output like this
```
# Output
/usr/bin/python2
/usr/bin/python3
```

- We want to choose something
```bash
sudo update-alternatives --config python
```
```
There are 2 choices for the alternative python (providing /usr/bin/python).

  Selection    Path              Priority   Status
------------------------------------------------------------
* 0            /usr/bin/python3   2         auto mode
  1            /usr/bin/python2   1         manual mode
  2            /usr/bin/python3   2         manual mode
  Press <enter> to keep the current choice[*], or type selection number: 1
```
```bash
python --version
```

```
Python 2.7.18  # Output
```
---
