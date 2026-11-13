
Microsoft Windows [Version 10.0.26200.9711]
(c) Microsoft Corporation. All rights reserved.

C:\Users\PC>git --version
git version 2.52.0.windows.1

C:\Users\PC>docker --version
Docker version 29.9.2, build a82e528

C:\Users\PC>docker info
Client:
 Version:    29.9.2
 Context:    desktop-linux
 Debug Mode: false
 Plugins:
  agent: Docker AI Agent Runner (Docker Inc.)
    Version:  v1.152.0
    Path:     C:\Users\PC\.docker\cli-plugins\docker-agent.exe
  ai: Docker AI Agent - Ask Gordon (Docker Inc.)
    Version:  v1.33.0
    Path:     C:\Users\PC\.docker\cli-plugins\docker-ai.exe
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.38.1
    Path:     C:\Users\PC\.docker\cli-plugins\docker-buildx.exe
  compose: Docker Compose (Docker Inc.)
    Version:  v5.6.1
    Path:     C:\Users\PC\.docker\cli-plugins\docker-compose.exe
  debug: Get a shell into any image or container (Docker Inc.)
    Version:  0.49.0
    Path:     C:\Users\PC\.docker\cli-plugins\docker-debug.exe
  desktop: Docker Desktop commands (Docker Inc.)
    Version:  4.98.0
    Path:     C:\Users\PC\.docker\cli-plugins\docker-desktop.exe
  dhi: CLI for managing Docker Hardened Images (Docker Inc.)
    Version:  v0.0.9
    Path:     C:\Users\PC\.docker\cli-plugins\docker-dhi.exe
  extension: Manages Docker extensions (Docker Inc.)
    Version:  v0.2.32
    Path:     C:\Users\PC\.docker\cli-plugins\docker-extension.exe
  init: Creates Docker-related starter files for your project (Docker Inc.)
    Version:  v1.4.1
    Path:     C:\Users\PC\.docker\cli-plugins\docker-init.exe
  mcp: Docker MCP Plugin (Docker Inc.)
    Version:  v0.44.2
    Path:     C:\Users\PC\.docker\cli-plugins\docker-mcp.exe
  model: Docker Model Runner (Docker Inc.)
    Version:  v1.2.9
    Path:     C:\Users\PC\.docker\cli-plugins\docker-model.exe
  offload: Docker Offload (Docker Inc.)
    Version:  v0.7.35
    Path:     C:\Users\PC\.docker\cli-plugins\docker-offload.exe
  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)
    Version:  v0.3.2
    Path:     C:\Users\PC\.docker\cli-plugins\docker-pass.exe
  sandbox: "docker sandbox" is deprecated, use Docker Sandboxes instead (Docker Inc.)
    Version:  v0.13.0
    Path:     C:\Users\PC\.docker\cli-plugins\docker-sandbox.exe
  scout: Docker Scout (Docker Inc.)
    Version:  v1.27.0
    Path:     C:\Users\PC\.docker\cli-plugins\docker-scout.exe

Server:
failed to connect to the docker API at npipe:////./pipe/dockerDesktopLinuxEngine; check if the path is correct and if the daemon is running: open //./pipe/dockerDesktopLinuxEngine: The system cannot find the file specified.

C:\Users\PC>code --version
1.139.1
04c0d99f4fb0d8afe6ce4f0c58e31e183ac3e4b1
x64

C:\Users\PC>

====================================
리눅스 명령어 실습
windows 에서 Ubuntu 실행

bigpark61@DESKTOP-VKSPJC7:~$ pwd
/home/bigpark61
bigpark61@DESKTOP-VKSPJC7:~$ mkdir -p ~/codyssey
bigpark61@DESKTOP-VKSPJC7:~$ dir
codyssey
bigpark61@DESKTOP-VKSPJC7:~$ pwd
/home/bigpark61
bigpark61@DESKTOP-VKSPJC7:~$ cd codyssey
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ mkdir practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ dir
practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ cd practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ pwd
/home/bigpark61/codyssey/practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ touch test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ ls
test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ dir
test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ ls -l
total 0
-rw-r--r-- 1 bigpark61 bigpark61 0 Nov 11 17:17 test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ dir -l
total 0
-rw-r--r-- 1 bigpark61 bigpark61 0 Nov 11 17:17 test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ cat "Hello Codyssey" > text.txt
cat: 'Hello Codyssey': No such file or directory
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ ls
test.txt  text.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ dir -l
total 0
-rw-r--r-- 1 bigpark61 bigpark61 0 Nov 11 17:17 test.txt
-rw-r--r-- 1 bigpark61 bigpark61 0 Nov 11 17:18 text.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ rm text.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ echo "Hello Codyssey" > test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ cat test.txt
Hello Codyssey
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ pwd
/home/bigpark61/codyssey/practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ ls
test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ cp test.txt copy.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ mv copy.txt result.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ dir -l
total 8
-rw-r--r-- 1 bigpark61 bigpark61 15 Nov 11 17:25 result.txt
-rw-r--r-- 1 bigpark61 bigpark61 15 Nov 11 17:23 test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ ls -la
total 16
drwxr-xr-x 2 bigpark61 bigpark61 4096 Nov 11 17:25 .
drwxr-xr-x 3 bigpark61 bigpark61 4096 Nov 11 17:16 ..
-rw-r--r-- 1 bigpark61 bigpark61   15 Nov 11 17:25 result.txt
-rw-r--r-- 1 bigpark61 bigpark61   15 Nov 11 17:23 test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ rm result.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$
-----------------------------------------------------------------
bigpark61@DESKTOP-VKSPJC7:~$ git --version
git version 2.53.0
bigpark61@DESKTOP-VKSPJC7:~$ docker --version
Docker version 29.9.2, build a82e528
bigpark61@DESKTOP-VKSPJC7:~$ docker info
Client:
 Version:    29.9.2
 Context:    default
 Debug Mode: false
 Plugins:
  agent: Docker AI Agent Runner (Docker Inc.)
    Version:  v1.152.0
    Path:     /usr/local/lib/docker/cli-plugins/docker-agent
  ai: Docker AI Agent - Ask Gordon (Docker Inc.)
    Version:  v1.33.0
    Path:     /usr/local/lib/docker/cli-plugins/docker-ai
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.38.1
    Path:     /usr/local/lib/docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v5.6.1
    Path:     /usr/local/lib/docker/cli-plugins/docker-compose
  debug: Get a shell into any image or container (Docker Inc.)
    Version:  0.49.0
    Path:     /usr/local/lib/docker/cli-plugins/docker-debug
  desktop: Docker Desktop commands (Docker Inc.)
    Version:  4.98.0
    Path:     /usr/local/lib/docker/cli-plugins/docker-desktop
  dhi: CLI for managing Docker Hardened Images (Docker Inc.)
    Version:  v0.0.9
    Path:     /usr/local/lib/docker/cli-plugins/docker-dhi
  extension: Manages Docker extensions (Docker Inc.)
    Version:  v0.2.32
    Path:     /usr/local/lib/docker/cli-plugins/docker-extension
  init: Creates Docker-related starter files for your project (Docker Inc.)
    Version:  v1.4.1
    Path:     /usr/local/lib/docker/cli-plugins/docker-init
  mcp: Docker MCP Plugin (Docker Inc.)
    Version:  v0.44.2
    Path:     /usr/local/lib/docker/cli-plugins/docker-mcp
  model: Docker Model Runner (Docker Inc.)
    Version:  v1.2.9
    Path:     /usr/local/lib/docker/cli-plugins/docker-model
  offload: Docker Offload (Docker Inc.)
    Version:  v0.7.35
    Path:     /usr/local/lib/docker/cli-plugins/docker-offload
  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)
    Version:  v0.3.2
    Path:     /usr/local/lib/docker/cli-plugins/docker-pass
  sandbox: "docker sandbox" is deprecated, use Docker Sandboxes instead (Docker Inc.)
    Version:  v0.13.0
    Path:     /usr/local/lib/docker/cli-plugins/docker-sandbox
  scout: Docker Scout (Docker Inc.)
    Version:  v1.27.0
    Path:     /usr/local/lib/docker/cli-plugins/docker-scout

Server:
 Containers: 5
  Running: 0
  Paused: 0
  Stopped: 5
 Images: 2
 Server Version: 29.9.2
 Storage Driver: overlayfs
  driver-type: io.containerd.snapshotter.v1
 Logging Driver: local
 Cgroup Driver: cgroupfs
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Discovered Devices:
  cdi: docker.com/gpu=webgpu
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 nvidia runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: b7a25261e029d68978bbf290df0a62fc819b3c51
 runc version: v1.5.2-0-g29dd3dc2
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.18.58.1-microsoft-standard-WSL2
 Operating System: Docker Desktop
 OSType: linux
 Architecture: x86_64
 CPUs: 8
 Total Memory: 3.685GiB
 Name: docker-desktop
 ID: 1f990b51-ee06-4d81-9f6c-26b4d40195d2
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 HTTP Proxy: http.docker.internal:3128
 HTTPS Proxy: http.docker.internal:3128
 No Proxy: hubproxy.docker.internal
 Labels:
  com.docker.desktop.address=unix:///var/run/docker-cli.sock
 Experimental: false
 Insecure Registries:
  hubproxy.docker.internal:5555
  127.0.0.0/8
  ::1/128
 Live Restore Enabled: false
 Firewall Backend: iptables

bigpark61@DESKTOP-VKSPJC7:~$ code --version
1.139.1
04c0d99f4fb0d8afe6ce4f0c58e31e183ac3e4b1
x64
bigpark61@DESKTOP-VKSPJC7:~$ pwd
/home/bigpark61
bigpark61@DESKTOP-VKSPJC7:~$ dir
codyssey
bigpark61@DESKTOP-VKSPJC7:~$ cd codyssey
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ dir -l
total 4
drwxr-xr-x 2 bigpark61 bigpark61 4096 Nov 11 17:26 practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ cd prcatice
-bash: cd: prcatice: No such file or directory
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ ls -l
total 4
drwxr-xr-x 2 bigpark61 bigpark61 4096 Nov 11 17:26 practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ dir
practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ cd practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ dir -l
total 4
-rwxr-xr-x 1 bigpark61 bigpark61 15 Nov 11 17:23 test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ ls -la
total 12
drwxr-xr-x 2 bigpark61 bigpark61 4096 Nov 11 17:26 .
drwxr-xr-x 3 bigpark61 bigpark61 4096 Nov 11 17:16 ..
-rwxr-xr-x 1 bigpark61 bigpark61   15 Nov 11 17:23 test.txt
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker run hello-world

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

bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED              STATUS                      PORTS     NAMES
eb51dc453964   hello-world   "/hello"   About a minute ago   Exited (0) 59 seconds ago             elated_bell
db90d2921c5e   ubuntu        "bash"     14 hours ago         Exited (129) 11 hours ago             ubuntu-test
3a35ab41fbeb   hello-world   "/hello"   14 hours ago         Exited (0) 14 hours ago               nice_mendeleev
3053026743be   hello-world   "/hello"   17 hours ago         Exited (0) 17 hours ago               blissful_sinoussi
1e22ecdd9c32   hello-world   "/hello"   17 hours ago         Exited (0) 17 hours ago               ecstatic_lamarr
4fb4e73ccaf0   hello-world   "/hello"   17 hours ago         Exited (0) 17 hours ago               sad_kare
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker images
                                                                 i Info →   U  In Use
IMAGE                ID             DISK USAGE   CONTENT SIZE   EXTRA
hello-world:latest   c567b231f656       25.9kB         9.49kB    U
ubuntu:latest        6a06111c3b0a        163MB         45.9MB    U
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker logs ubntu
Error response from daemon: No such container: ubntu
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker logs ubntu-test
Error response from daemon: No such container: ubntu-test
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker logs hello-world
Error response from daemon: No such container: hello-world
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker status --no-stream
unknown flag: --no-stream

Usage:  docker [OPTIONS] COMMAND [ARG...]

Run 'docker --help' for more information
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ docker images
                                                                 i Info →   U  In Use
IMAGE                ID             DISK USAGE   CONTENT SIZE   EXTRA
hello-world:latest   c567b231f656       25.9kB         9.49kB    U
ubuntu:latest        6a06111c3b0a        163MB         45.9MB    U
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ wls --verion
Command 'wls' not found, but there are 16 similar ones.
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ wls --version
Command 'wls' not found, but there are 16 similar ones.
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ wsl --version
Command 'wsl' not found, but can be installed with:
sudo apt install wsl
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ sudo apt update && sudo apt upgrade -y
[sudo: authenticate] Password:
Get:1 http://security.ubuntu.com/ubuntu resolute-security InRelease [137 kB]
Hit:2 http://archive.ubuntu.com/ubuntu resolute InRelease
Get:3 http://archive.ubuntu.com/ubuntu resolute-updates InRelease [137 kB]
Get:4 http://security.ubuntu.com/ubuntu resolute-security/main amd64 Packages [717 kB]
Get:5 http://archive.ubuntu.com/ubuntu resolute-backports InRelease [137 kB]
Get:6 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 Packages [868 kB]
Get:7 http://security.ubuntu.com/ubuntu resolute-security/main Translation-en [157 kB]
Get:8 http://security.ubuntu.com/ubuntu resolute-security/main amd64 Components [46.7 kB]
Get:9 http://security.ubuntu.com/ubuntu resolute-security/universe amd64 Packages [220 kB]
Get:10 http://security.ubuntu.com/ubuntu resolute-security/universe Translation-en [72.5 kB]
Get:11 http://security.ubuntu.com/ubuntu resolute-security/universe amd64 Components [62.7 kB]
Get:12 http://security.ubuntu.com/ubuntu resolute-security/restricted amd64 Packages [586 kB]
Get:13 http://security.ubuntu.com/ubuntu resolute-security/restricted Translation-en [122 kB]
Get:14 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 Components [110 kB]
Get:15 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 Components [201 kB]
Get:16 http://archive.ubuntu.com/ubuntu resolute-backports/universe amd64 Components [1056 B]
Fetched 3575 kB in 4s (814 kB/s)
77 packages can be upgraded. Run 'apt list --upgradable' to see them.
Error: dpkg was interrupted, you must manually run 'sudo dpkg --configure -a' to correct the problem.
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ sudo dpkg --configure -a
Setting up python3-pyasn1 (0.6.3-1ubuntu0.2) ...
bigpark61@DESKTOP-VKSPJC7:~/codyssey/practice$ cd ..
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ dir
practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ cd ~
bigpark61@DESKTOP-VKSPJC7:~$
bigpark61@DESKTOP-VKSPJC7:~$ cd ..
bigpark61@DESKTOP-VKSPJC7:/home$
bigpark61@DESKTOP-VKSPJC7:/home$
bigpark61@DESKTOP-VKSPJC7:/home$ cd
bigpark61@DESKTOP-VKSPJC7:~$ pwd
/home/bigpark61
bigpark61@DESKTOP-VKSPJC7:~$ dir
codyssey
bigpark61@DESKTOP-VKSPJC7:~$ cd codyssey
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ mkdir -p ~/projects
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ dir
practice
bigpark61@DESKTOP-VKSPJC7:~/codyssey$ cd ~
bigpark61@DESKTOP-VKSPJC7:~$
bigpark61@DESKTOP-VKSPJC7:~$
bigpark61@DESKTOP-VKSPJC7:~$ pwd
/home/bigpark61
bigpark61@DESKTOP-VKSPJC7:~$ dir
codyssey  projects
bigpark61@DESKTOP-VKSPJC7:~$ cd ~/projects && mkdir myapp && cd myapp
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ pwd
/home/bigpark61/projects/myapp
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ explorer.exe
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ explorer.exe .
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ git config --global user.name "Kyoungboo"
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ it config --global user.email "kyoungboo.park@gmail.com"
it: command not found
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ git config --global user.email "kyoungboo
.park@gmail.com"
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ git config --global --list
user.name=Kyoungboo
user.email=kyoungboo.park@gmail.com
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ git config --global init.defaultBranch main
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ sudo apt install -y gh
Installing:
  gh

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 77
  Download size: 8547 kB
  Space needed: 37.1 MB / 1024 GB available

Get:1 http://archive.ubuntu.com/ubuntu resolute/universe amd64 gh amd64 2.46.0-4 [8547 kB]
Fetched 8547 kB in 9s (967 kB/s)
Selecting previously unselected package gh.
(Reading database ... 35908 files and directories currently installed.)
Preparing to unpack .../archives/gh_2.46.0-4_amd64.deb ...
Unpacking gh (2.46.0-4) ...
Setting up gh (2.46.0-4) ...
Processing triggers for man-db (2.13.1-1build1) ...
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations on this host? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: 8789-CBDE
Press Enter to open github.com in your browser...
! Failed opening a web browser at https://github.com/login/device
  exec: "xdg-open,x-www-browser,www-browser,wslview": executable file not found in $PATH
  Please try entering the URL in your browser manually
✓ Authentication complete.
- gh config set -h github.com git_protocol https
✓ Configured git protocol
! Authentication credentials saved in plain text
✓ Logged in as bigpark61
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$

--------------------------------------------------------
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ sudo apt install -y python3-pip python3-venv
Installing:
  python3-pip  python3-venv

Installing dependencies:
  build-essential          gcc-x86-64-linux-gnu       libitm1
  bzip2                    libalgorithm-diff-perl     liblsan0
  cpp                      libalgorithm-diff-xs-perl  libmpc3
  cpp-15                   libalgorithm-merge-perl    libquadmath0
  cpp-15-x86-64-linux-gnu  libasan8                   libstdc++-15-dev
  cpp-x86-64-linux-gnu     libc-dev-bin               libtsan2
  dpkg-dev                 libc6-dev                  libubsan1
  fakeroot                 libcc1-0                   linux-libc-dev
  g++                      libcrypt-dev               lto-disabled-list
  g++-15                   libdpkg-perl               make
  g++-15-x86-64-linux-gnu  libfakeroot                manpages-dev
  g++-x86-64-linux-gnu     libfile-fcntllock-perl     python3-pip-whl
  gcc                      libgcc-15-dev              python3-setuptools-whl
  gcc-15                   libgomp1                   python3-wheel
  gcc-15-base              libhwasan0                 python3.14-venv
  gcc-15-x86-64-linux-gnu  libisl23                   rpcsvc-proto

Suggested packages:
  bzip2-doc                  gcc-15-doc    gcc-doc
  cpp-doc                    gcc-multilib  gcc-15-multilib
  gcc-15-locales             autoconf      gdb-x86-64-linux-gnu
  cpp-15-doc                 automake      libc-devtools
  debian-keyring             libtool       glibc-doc
  debian-tag2upload-keyring  flex          bzr
  g++-multilib               bison         libstdc++-15-doc
  g++-15-multilib            gdb           make-doc

Recommended packages:
  python3-dev

Summary:
  Upgrading: 0, Installing: 50, Removing: 0, Not Upgrading: 77
  Download size: 83.2 MB
  Space needed: 287 MB / 1024 GB available

Get:1 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 libc-dev-bin amd64 2.43-2ubuntu2.4 [23.3 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 linux-libc-dev amd64 7.0.0-43.43 [1885 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute/main amd64 rpcsvc-proto amd64 1.4.3-1build1 [68.3 kB]
Get:4 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 libc6-dev amd64 2.43-2ubuntu2.4 [2294 kB]
Get:5 http://archive.ubuntu.com/ubuntu resolute/main amd64 gcc-15-base amd64 15.2.0-16ubuntu1 [39.0 kB]
Get:6 http://archive.ubuntu.com/ubuntu resolute/main amd64 libisl23 amd64 0.27-1build1 [691 kB]
Get:7 http://archive.ubuntu.com/ubuntu resolute/main amd64 libmpc3 amd64 1.3.1-3 [54.6 kB]
Get:8 http://archive.ubuntu.com/ubuntu resolute/main amd64 cpp-15-x86-64-linux-gnu amd64 15.2.0-16ubuntu1 [12.9 MB]
Get:9 http://archive.ubuntu.com/ubuntu resolute/main amd64 cpp-15 amd64 15.2.0-16ubuntu1 [1030 B]
Get:10 http://archive.ubuntu.com/ubuntu resolute/main amd64 cpp-x86-64-linux-gnu amd64 4:15.2.0-5ubuntu1 [5840 B]
Get:11 http://archive.ubuntu.com/ubuntu resolute/main amd64 cpp amd64 4:15.2.0-5ubuntu1 [22.4 kB]
Get:12 http://archive.ubuntu.com/ubuntu resolute/main amd64 libcc1-0 amd64 16-20260322-1ubuntu1 [51.2 kB]
Get:13 http://archive.ubuntu.com/ubuntu resolute/main amd64 libgomp1 amd64 16-20260322-1ubuntu1 [162 kB]
Get:14 http://archive.ubuntu.com/ubuntu resolute/main amd64 libitm1 amd64 16-20260322-1ubuntu1 [30.0 kB]
Get:15 http://archive.ubuntu.com/ubuntu resolute/main amd64 libasan8 amd64 16-20260322-1ubuntu1 [3184 kB]
Get:16 http://archive.ubuntu.com/ubuntu resolute/main amd64 liblsan0 amd64 16-20260322-1ubuntu1 [1394 kB]
Get:17 http://archive.ubuntu.com/ubuntu resolute/main amd64 libtsan2 amd64 16-20260322-1ubuntu1 [2849 kB]
Get:18 http://archive.ubuntu.com/ubuntu resolute/main amd64 libubsan1 amd64 16-20260322-1ubuntu1 [1240 kB]
Get:19 http://archive.ubuntu.com/ubuntu resolute/main amd64 libhwasan0 amd64 16-20260322-1ubuntu1 [1731 kB]
Get:20 http://archive.ubuntu.com/ubuntu resolute/main amd64 libquadmath0 amd64 16-20260322-1ubuntu1 [155 kB]
Get:21 http://archive.ubuntu.com/ubuntu resolute/main amd64 libgcc-15-dev amd64 15.2.0-16ubuntu1 [2866 kB]
Get:22 http://archive.ubuntu.com/ubuntu resolute/main amd64 gcc-15-x86-64-linux-gnu amd64 15.2.0-16ubuntu1 [25.4 MB]
Get:23 http://archive.ubuntu.com/ubuntu resolute/main amd64 gcc-15 amd64 15.2.0-16ubuntu1 [539 kB]
Get:24 http://archive.ubuntu.com/ubuntu resolute/main amd64 gcc-x86-64-linux-gnu amd64 4:15.2.0-5ubuntu1 [1208 B]
Get:25 http://archive.ubuntu.com/ubuntu resolute/main amd64 gcc amd64 4:15.2.0-5ubuntu1 [5010 B]
Get:26 http://archive.ubuntu.com/ubuntu resolute/main amd64 libstdc++-15-dev amd64 15.2.0-16ubuntu1 [2920 kB]
Get:27 http://archive.ubuntu.com/ubuntu resolute/main amd64 g++-15-x86-64-linux-gnu amd64 15.2.0-16ubuntu1 [14.4 MB]
Get:28 http://archive.ubuntu.com/ubuntu resolute/main amd64 g++-15 amd64 15.2.0-16ubuntu1 [26.7 kB]
Get:29 http://archive.ubuntu.com/ubuntu resolute/main amd64 g++-x86-64-linux-gnu amd64 4:15.2.0-5ubuntu1 [968 B]
Get:30 http://archive.ubuntu.com/ubuntu resolute/main amd64 g++ amd64 4:15.2.0-5ubuntu1 [1100 B]
Get:31 http://archive.ubuntu.com/ubuntu resolute/main amd64 make amd64 4.4.1-3 [197 kB]
Get:32 http://archive.ubuntu.com/ubuntu resolute/main amd64 libdpkg-perl all 1.23.7ubuntu1 [289 kB]
Get:33 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 bzip2 amd64 1.0.8-6ubuntu0.1 [34.3 kB]
Get:34 http://archive.ubuntu.com/ubuntu resolute/main amd64 lto-disabled-list all 79 [14.2 kB]
Get:35 http://archive.ubuntu.com/ubuntu resolute/main amd64 dpkg-dev all 1.23.7ubuntu1 [1062 kB]
Get:36 http://archive.ubuntu.com/ubuntu resolute/main amd64 libcrypt-dev amd64 1:4.5.1-1 [122 kB]
Get:37 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 build-essential amd64 12.12ubuntu2.26.04.2 [5158 B]
Get:38 http://archive.ubuntu.com/ubuntu resolute/main amd64 libfakeroot amd64 1.37.2-1 [34.0 kB]
Get:39 http://archive.ubuntu.com/ubuntu resolute/main amd64 fakeroot amd64 1.37.2-1 [68.3 kB]
Get:40 http://archive.ubuntu.com/ubuntu resolute/main amd64 libalgorithm-diff-perl all 1.201-1 [41.8 kB]
Get:41 http://archive.ubuntu.com/ubuntu resolute/main amd64 libalgorithm-diff-xs-perl amd64 0.04-9 [11.5 kB]
Get:42 http://archive.ubuntu.com/ubuntu resolute/main amd64 libalgorithm-merge-perl all 0.08-5 [11.4 kB]
Get:43 http://archive.ubuntu.com/ubuntu resolute/main amd64 libfile-fcntllock-perl amd64 0.22-4ubuntu6 [32.8 kB]
Get:44 http://archive.ubuntu.com/ubuntu resolute/main amd64 manpages-dev all 6.17-1 [2183 kB]
Get:45 http://archive.ubuntu.com/ubuntu resolute/universe amd64 python3-wheel all 0.46.3-2 [27.9 kB]
Get:46 http://archive.ubuntu.com/ubuntu resolute/universe amd64 python3-pip all 25.1.1+dfsg-1ubuntu2 [1416 kB]
Get:47 http://archive.ubuntu.com/ubuntu resolute/universe amd64 python3-pip-whl all 25.1.1+dfsg-1ubuntu2 [1430 kB]
Get:48 http://archive.ubuntu.com/ubuntu resolute/universe amd64 python3-setuptools-whl all 78.1.1-0.1build1 [1174 kB]
Get:49 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 python3.14-venv amd64 3.14.4-1ubuntu0.2 [5356 B]
Get:50 http://archive.ubuntu.com/ubuntu resolute/universe amd64 python3-venv amd64 3.14.3-0ubuntu2 [1032 B]
Fetched 83.2 MB in 16s (5264 kB/s)
Extracting templates from packages: 100%
Selecting previously unselected package libc-dev-bin.
(Reading database ... 36100 files and directories currently installed.)
Preparing to unpack .../00-libc-dev-bin_2.43-2ubuntu2.4_amd64.deb ...
Unpacking libc-dev-bin (2.43-2ubuntu2.4) ...
Selecting previously unselected package linux-libc-dev:amd64.
Preparing to unpack .../01-linux-libc-dev_7.0.0-43.43_amd64.deb ...
Unpacking linux-libc-dev:amd64 (7.0.0-43.43) ...
Selecting previously unselected package rpcsvc-proto.
Preparing to unpack .../02-rpcsvc-proto_1.4.3-1build1_amd64.deb ...
Unpacking rpcsvc-proto (1.4.3-1build1) ...
Selecting previously unselected package libc6-dev:amd64.
Preparing to unpack .../03-libc6-dev_2.43-2ubuntu2.4_amd64.deb ...
Unpacking libc6-dev:amd64 (2.43-2ubuntu2.4) ...
Selecting previously unselected package gcc-15-base:amd64.
Preparing to unpack .../04-gcc-15-base_15.2.0-16ubuntu1_amd64.deb ...
Unpacking gcc-15-base:amd64 (15.2.0-16ubuntu1) ...
Selecting previously unselected package libisl23:amd64.
Preparing to unpack .../05-libisl23_0.27-1build1_amd64.deb ...
Unpacking libisl23:amd64 (0.27-1build1) ...
Selecting previously unselected package libmpc3:amd64.
Preparing to unpack .../06-libmpc3_1.3.1-3_amd64.deb ...
Unpacking libmpc3:amd64 (1.3.1-3) ...
Selecting previously unselected package cpp-15-x86-64-linux-gnu.
Preparing to unpack .../07-cpp-15-x86-64-linux-gnu_15.2.0-16ubuntu1_amd64.deb ...
Unpacking cpp-15-x86-64-linux-gnu (15.2.0-16ubuntu1) ...
Selecting previously unselected package cpp-15.
Preparing to unpack .../08-cpp-15_15.2.0-16ubuntu1_amd64.deb ...
Unpacking cpp-15 (15.2.0-16ubuntu1) ...
Selecting previously unselected package cpp-x86-64-linux-gnu.
Preparing to unpack .../09-cpp-x86-64-linux-gnu_4%3a15.2.0-5ubuntu1_amd64.deb ...
Unpacking cpp-x86-64-linux-gnu (4:15.2.0-5ubuntu1) ...
Selecting previously unselected package cpp.
Preparing to unpack .../10-cpp_4%3a15.2.0-5ubuntu1_amd64.deb ...
Unpacking cpp (4:15.2.0-5ubuntu1) ...
Selecting previously unselected package libcc1-0:amd64.
Preparing to unpack .../11-libcc1-0_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libcc1-0:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libgomp1:amd64.
Preparing to unpack .../12-libgomp1_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libgomp1:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libitm1:amd64.
Preparing to unpack .../13-libitm1_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libitm1:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libasan8:amd64.
Preparing to unpack .../14-libasan8_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libasan8:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package liblsan0:amd64.
Preparing to unpack .../15-liblsan0_16-20260322-1ubuntu1_amd64.deb ...
Unpacking liblsan0:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libtsan2:amd64.
Preparing to unpack .../16-libtsan2_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libtsan2:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libubsan1:amd64.
Preparing to unpack .../17-libubsan1_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libubsan1:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libhwasan0:amd64.
Preparing to unpack .../18-libhwasan0_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libhwasan0:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libquadmath0:amd64.
Preparing to unpack .../19-libquadmath0_16-20260322-1ubuntu1_amd64.deb ...
Unpacking libquadmath0:amd64 (16-20260322-1ubuntu1) ...
Selecting previously unselected package libgcc-15-dev:amd64.
Preparing to unpack .../20-libgcc-15-dev_15.2.0-16ubuntu1_amd64.deb ...
Unpacking libgcc-15-dev:amd64 (15.2.0-16ubuntu1) ...
Selecting previously unselected package gcc-15-x86-64-linux-gnu.
Preparing to unpack .../21-gcc-15-x86-64-linux-gnu_15.2.0-16ubuntu1_amd64.deb ...
Unpacking gcc-15-x86-64-linux-gnu (15.2.0-16ubuntu1) ...
Selecting previously unselected package gcc-15.
Preparing to unpack .../22-gcc-15_15.2.0-16ubuntu1_amd64.deb ...
Unpacking gcc-15 (15.2.0-16ubuntu1) ...
Selecting previously unselected package gcc-x86-64-linux-gnu.
Preparing to unpack .../23-gcc-x86-64-linux-gnu_4%3a15.2.0-5ubuntu1_amd64.deb ...
Unpacking gcc-x86-64-linux-gnu (4:15.2.0-5ubuntu1) ...
Selecting previously unselected package gcc.
Preparing to unpack .../24-gcc_4%3a15.2.0-5ubuntu1_amd64.deb ...
Unpacking gcc (4:15.2.0-5ubuntu1) ...
Selecting previously unselected package libstdc++-15-dev:amd64.
Preparing to unpack .../25-libstdc++-15-dev_15.2.0-16ubuntu1_amd64.deb ...
Unpacking libstdc++-15-dev:amd64 (15.2.0-16ubuntu1) ...
Selecting previously unselected package g++-15-x86-64-linux-gnu.
Preparing to unpack .../26-g++-15-x86-64-linux-gnu_15.2.0-16ubuntu1_amd64.deb ...
Unpacking g++-15-x86-64-linux-gnu (15.2.0-16ubuntu1) ...
Selecting previously unselected package g++-15.
Preparing to unpack .../27-g++-15_15.2.0-16ubuntu1_amd64.deb ...
Unpacking g++-15 (15.2.0-16ubuntu1) ...
Selecting previously unselected package g++-x86-64-linux-gnu.
Preparing to unpack .../28-g++-x86-64-linux-gnu_4%3a15.2.0-5ubuntu1_amd64.deb ...
Unpacking g++-x86-64-linux-gnu (4:15.2.0-5ubuntu1) ...
Selecting previously unselected package g++.
Preparing to unpack .../29-g++_4%3a15.2.0-5ubuntu1_amd64.deb ...
Unpacking g++ (4:15.2.0-5ubuntu1) ...
Selecting previously unselected package make.
Preparing to unpack .../30-make_4.4.1-3_amd64.deb ...
Unpacking make (4.4.1-3) ...
Selecting previously unselected package libdpkg-perl.
Preparing to unpack .../31-libdpkg-perl_1.23.7ubuntu1_all.deb ...
Unpacking libdpkg-perl (1.23.7ubuntu1) ...
Selecting previously unselected package bzip2.
Preparing to unpack .../32-bzip2_1.0.8-6ubuntu0.1_amd64.deb ...
Unpacking bzip2 (1.0.8-6ubuntu0.1) ...
Selecting previously unselected package lto-disabled-list.
Preparing to unpack .../33-lto-disabled-list_79_all.deb ...
Unpacking lto-disabled-list (79) ...
Selecting previously unselected package dpkg-dev.
Preparing to unpack .../34-dpkg-dev_1.23.7ubuntu1_all.deb ...
Unpacking dpkg-dev (1.23.7ubuntu1) ...
Selecting previously unselected package libcrypt-dev:amd64.
Preparing to unpack .../35-libcrypt-dev_1%3a4.5.1-1_amd64.deb ...
Unpacking libcrypt-dev:amd64 (1:4.5.1-1) ...
Selecting previously unselected package build-essential.
Preparing to unpack .../36-build-essential_12.12ubuntu2.26.04.2_amd64.deb ...
Unpacking build-essential (12.12ubuntu2.26.04.2) ...
Selecting previously unselected package libfakeroot:amd64.
Preparing to unpack .../37-libfakeroot_1.37.2-1_amd64.deb ...
Unpacking libfakeroot:amd64 (1.37.2-1) ...
Selecting previously unselected package fakeroot.
Preparing to unpack .../38-fakeroot_1.37.2-1_amd64.deb ...
Unpacking fakeroot (1.37.2-1) ...
Selecting previously unselected package libalgorithm-diff-perl.
Preparing to unpack .../39-libalgorithm-diff-perl_1.201-1_all.deb ...
Unpacking libalgorithm-diff-perl (1.201-1) ...
Selecting previously unselected package libalgorithm-diff-xs-perl.
Preparing to unpack .../40-libalgorithm-diff-xs-perl_0.04-9_amd64.deb ...
Unpacking libalgorithm-diff-xs-perl (0.04-9) ...
Selecting previously unselected package libalgorithm-merge-perl.
Preparing to unpack .../41-libalgorithm-merge-perl_0.08-5_all.deb ...
Unpacking libalgorithm-merge-perl (0.08-5) ...
Selecting previously unselected package libfile-fcntllock-perl.
Preparing to unpack .../42-libfile-fcntllock-perl_0.22-4ubuntu6_amd64.deb ...
Unpacking libfile-fcntllock-perl (0.22-4ubuntu6) ...
Selecting previously unselected package manpages-dev.
Preparing to unpack .../43-manpages-dev_6.17-1_all.deb ...
Unpacking manpages-dev (6.17-1) ...
Selecting previously unselected package python3-wheel.
Preparing to unpack .../44-python3-wheel_0.46.3-2_all.deb ...
Unpacking python3-wheel (0.46.3-2) ...
Selecting previously unselected package python3-pip.
Preparing to unpack .../45-python3-pip_25.1.1+dfsg-1ubuntu2_all.deb ...
Unpacking python3-pip (25.1.1+dfsg-1ubuntu2) ...
Selecting previously unselected package python3-pip-whl.
Preparing to unpack .../46-python3-pip-whl_25.1.1+dfsg-1ubuntu2_all.deb ...
Unpacking python3-pip-whl (25.1.1+dfsg-1ubuntu2) ...
Selecting previously unselected package python3-setuptools-whl.
Preparing to unpack .../47-python3-setuptools-whl_78.1.1-0.1build1_all.deb ...
Unpacking python3-setuptools-whl (78.1.1-0.1build1) ...
Selecting previously unselected package python3.14-venv.
Preparing to unpack .../48-python3.14-venv_3.14.4-1ubuntu0.2_amd64.deb ...
Unpacking python3.14-venv (3.14.4-1ubuntu0.2) ...
Selecting previously unselected package python3-venv.
Preparing to unpack .../49-python3-venv_3.14.3-0ubuntu2_amd64.deb ...
Unpacking python3-venv (3.14.3-0ubuntu2) ...
Setting up manpages-dev (6.17-1) ...
Setting up python3-setuptools-whl (78.1.1-0.1build1) ...
Setting up lto-disabled-list (79) ...
Setting up libfile-fcntllock-perl (0.22-4ubuntu6) ...
Setting up python3-pip-whl (25.1.1+dfsg-1ubuntu2) ...
Setting up libalgorithm-diff-perl (1.201-1) ...
Setting up linux-libc-dev:amd64 (7.0.0-43.43) ...
Setting up libgomp1:amd64 (16-20260322-1ubuntu1) ...
Setting up bzip2 (1.0.8-6ubuntu0.1) ...
Setting up python3-wheel (0.46.3-2) ...
Setting up libfakeroot:amd64 (1.37.2-1) ...
Setting up python3.14-venv (3.14.4-1ubuntu0.2) ...
Setting up fakeroot (1.37.2-1) ...
update-alternatives: using /usr/bin/fakeroot-sysv to provide /usr/bin/fakeroot (fakeroot) in auto mode
Setting up rpcsvc-proto (1.4.3-1build1) ...
Setting up python3-venv (3.14.3-0ubuntu2) ...
Setting up make (4.4.1-3) ...
Setting up libquadmath0:amd64 (16-20260322-1ubuntu1) ...
Setting up libmpc3:amd64 (1.3.1-3) ...
Setting up python3-pip (25.1.1+dfsg-1ubuntu2) ...
Setting up libdpkg-perl (1.23.7ubuntu1) ...
Setting up libubsan1:amd64 (16-20260322-1ubuntu1) ...
Setting up libhwasan0:amd64 (16-20260322-1ubuntu1) ...
Setting up libcrypt-dev:amd64 (1:4.5.1-1) ...
Setting up libasan8:amd64 (16-20260322-1ubuntu1) ...
Setting up libtsan2:amd64 (16-20260322-1ubuntu1) ...
Setting up libisl23:amd64 (0.27-1build1) ...
Setting up libc-dev-bin (2.43-2ubuntu2.4) ...
Setting up gcc-15-base:amd64 (15.2.0-16ubuntu1) ...
Setting up libalgorithm-diff-xs-perl (0.04-9) ...
Setting up libcc1-0:amd64 (16-20260322-1ubuntu1) ...
Setting up liblsan0:amd64 (16-20260322-1ubuntu1) ...
Setting up libitm1:amd64 (16-20260322-1ubuntu1) ...
Setting up libalgorithm-merge-perl (0.08-5) ...
Setting up libgcc-15-dev:amd64 (15.2.0-16ubuntu1) ...
Setting up cpp-15-x86-64-linux-gnu (15.2.0-16ubuntu1) ...
Setting up dpkg-dev (1.23.7ubuntu1) ...
Setting up gcc-15-x86-64-linux-gnu (15.2.0-16ubuntu1) ...
Setting up cpp-15 (15.2.0-16ubuntu1) ...
Setting up libc6-dev:amd64 (2.43-2ubuntu2.4) ...
Setting up cpp-x86-64-linux-gnu (4:15.2.0-5ubuntu1) ...
Setting up gcc-x86-64-linux-gnu (4:15.2.0-5ubuntu1) ...
Setting up gcc-15 (15.2.0-16ubuntu1) ...
Setting up libstdc++-15-dev:amd64 (15.2.0-16ubuntu1) ...
Setting up cpp (4:15.2.0-5ubuntu1) ...
Setting up g++-15-x86-64-linux-gnu (15.2.0-16ubuntu1) ...
Setting up gcc (4:15.2.0-5ubuntu1) ...
Setting up g++-x86-64-linux-gnu (4:15.2.0-5ubuntu1) ...
Setting up g++-15 (15.2.0-16ubuntu1) ...
Setting up g++ (4:15.2.0-5ubuntu1) ...
update-alternatives: using /usr/bin/g++ to provide /usr/bin/c++ (c++) in auto mode
Setting up build-essential (12.12ubuntu2.26.04.2) ...
Processing triggers for man-db (2.13.1-1build1) ...
Processing triggers for libc-bin (2.43-2ubuntu2.4) ...
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$ python3 --version && pip3 --version
Python 3.14.4
pip 25.1.1 from /usr/lib/python3/dist-packages/pip (python 3.14)
bigpark61@DESKTOP-VKSPJC7:~/projects/myapp$
