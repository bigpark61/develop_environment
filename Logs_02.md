
<mark style="background: #FFF3A3A6;">bigpark61@DESKTOP-VKSPJC7:~$ pwd</mark>
/home/bigpark61
<mark style="background: #FFF3A3A6;">bigpark61@DESKTOP-VKSPJC7:~$ dir</mark>
codyssey  projects
bigpark61@DESKTOP-VKSPJC7:~$ cd projects/
bigpark61@DESKTOP-VKSPJC7:~/projects$ dir
myapp
bigpark61@DESKTOP-VKSPJC7:~/projects$ cd myapp
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ pwd
/home/bigpark61/projects/myapp
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ python3 -m venv .venv
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ dir
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ ls -l
total 0
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ source .venv/bin/activate
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ pip install --upgrade pip
Requirement already satisfied: pip in ./.venv/lib/python3.14/site-packages (25.1.1)
Collecting pip
  Downloading pip-26.3-py3-none-any.whl.metadata (4.6 kB)
Downloading pip-26.3-py3-none-any.whl (2.0 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.0/2.0 MB 9.6 MB/s eta 0:00:00
Installing collected packages: pip
  Attempting uninstall: pip
    Found existing installation: pip 25.1.1
    Uninstalling pip-25.1.1:
      Successfully uninstalled pip-25.1.1
Successfully installed pip-26.3
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ pip install ruff
Collecting ruff
  Downloading ruff-0.17.4-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (20 kB)
Downloading ruff-0.17.4-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (10.6 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 10.6/10.6 MB 3.7 MB/s  0:00:02
Installing collected packages: ruff
Successfully installed ruff-0.17.4
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ ruff check .
warning: No Python files found under the given path(s)
All checks passed!
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ ruff format .
warning: No Python files found under the given path(s)
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ sudo apt install -y direnv
[sudo: authenticate] Password:
Installing:
  direnv

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 77
  Download size: 2901 kB
  Space needed: 8294 kB / 1024 GB available

Get:1 http://archive.ubuntu.com/ubuntu resolute/universe amd64 direnv amd64 2.37.1-1 [2901 kB]
Fetched 2901 kB in 3s (866 kB/s)
Selecting previously unselected package direnv.
(Reading database ... 43256 files and directories currently installed.)
Preparing to unpack .../direnv_2.37.1-1_amd64.deb ...
Unpacking direnv (2.37.1-1) ...
Setting up direnv (2.37.1-1) ...
Processing triggers for man-db (2.13.1-1build1) ...
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ cho 'eval "$(direnv hook zsh)"' >> ~/.zshrc && source ~/.zshrc
Command 'cho' not found, did you mean:
  command 'chr' from snap chr (0.80.4)
  command 'who' from deb coreutils-from-gnu (0.0.0~ubuntu25)
  command 'who' from deb coreutils-from-uutils (0.0.0~ubuntu25)
  command 'who' from deb coreutils-from-busybox (0.0.0~ubuntu25)
  command 'who' from deb coreutils-from-toybox (0.0.0~ubuntu25)
  command 'cdo' from deb cdo (2.5.4-1)
  command 'chg' from deb mercurial (7.2-3build1)
  command 'co' from deb rcs (5.10.1-3)
  command 'echo' from deb coreutils-from-gnu (0.0.0~ubuntu25)
  command 'echo' from deb coreutils-from-uutils (0.0.0~ubuntu25)
  command 'echo' from deb coreutils-from-busybox (0.0.0~ubuntu25)
  command 'echo' from deb coreutils-from-toybox (0.0.0~ubuntu25)
  command 'cht' from deb chemtool (1.6.14-6build3)
  command 'chr' from deb chr (0.1.80-1)
  command 'chr' from deb chr-tiny (0.1.80-1)
See 'snap info <snapname>' for additional versions.
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ cd ~/projects/myapp
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ echo 'source .venv/bin/activate' > .envrc
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ dir
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ direnv allow
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ ls -a
.  ..  .envrc  .venv
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ ls -la
total 16
drwxr-xr-x 3 bigpark61 bigpark61 4096 Nov 12 15:02 .
drwxr-xr-x 3 bigpark61 bigpark61 4096 Nov 12 10:52 ..
-rw-r--r-- 1 bigpark61 bigpark61   26 Nov 12 15:02 .envrc
drwxr-xr-x 5 bigpark61 bigpark61 4096 Nov 12 14:56 .venv
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ docker --version
Docker version 29.9.2, build a82e528
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ docker run -d -p 8080:80 nginx
Unable to find image 'nginx:latest' locally
latest: Pulling from library/nginx
37fb86c2a767: Pull complete
512ac5e7ce8e: Pull complete
bbb080c71d50: Pull complete
1724c05f72c6: Pull complete
1962e1ff75b4: Pull complete
6d2e43921e9e: Pull complete
7cb4701ce7cd: Pull complete
4582dace95e2: Download complete
d2c7e31f04a3: Download complete
Digest: sha256:165ddde8751e75a1c907d24ef10d9f6deb08b57e0fe56caf67512486aff76d82
Status: Downloaded newer image for nginx:latest
795dfdc55026c854a6619f5709d7103a24e0e96c073da5cc1a89cce65154388e
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ code .
Installing VS Code Server for Linux x64 (04c0d99f4fb0d8afe6ce4f0c58e31e183ac3e4b1)
Downloading: 100%
Unpacking: 100%
Unpacked 4237 files and folders to /home/bigpark61/.vscode-server/bin/04c0d99f4fb0d8afe6ce4f0c58e31e183ac3e4b1.
Looking for compatibility check script at /home/bigpark61/.vscode-server/bin/04c0d99f4fb0d8afe6ce4f0c58e31e183ac3e4b1/bin/helpers/check-requirements.sh
Running compatibility check script
Compatibility check successful (0)
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ code --install-extension eamodio.gitlens
Installing extensions...
(node:5010) [DEP0169] DeprecationWarning: `url.parse()` behavior is not standardized and prone to errors that have security implications. Use the WHATWG URL API instead. CVEs are not issued for `url.parse()` vulnerabilities.
(Use `node --trace-deprecation ...` to show where the warning was created)
Installing extension 'eamodio.gitlens'...
Extension 'eamodio.gitlens' v19.6.0 was successfully installed.
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ code --install-extension github.vscode-pull-request-github
Installing extensions...
(node:5166) [DEP0169] DeprecationWarning: `url.parse()` behavior is not standardized and prone to errors that have security implications. Use the WHATWG URL API instead. CVEs are not issued for `url.parse()` vulnerabilities.
(Use `node --trace-deprecation ...` to show where the warning was created)
Installing extension 'github.vscode-pull-request-github'...
Extension 'github.vscode-pull-request-github' v0.166.1 was successfully installed.
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ code --install-extension ms-python.python
Installing extensions...
(node:5371) [DEP0169] DeprecationWarning: `url.parse()` behavior is not standardized and prone to errors that have security implications. Use the WHATWG URL API instead. CVEs are not issued for `url.parse()` vulnerabilities.
(Use `node --trace-deprecation ...` to show where the warning was created)
Installing extension 'ms-python.python'...
Extension 'ms-python.vscode-python-envs' v1.42.0 was successfully installed.
Extension 'ms-python.python' v2026.10.0 was successfully installed.
Extension 'ms-python.debugpy' v2026.6.0 was successfully installed.
Extension 'ms-python.vscode-pylance' v2026.4.1 was successfully installed.
(.venv) bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$