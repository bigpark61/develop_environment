# AIO_E1-1 | 내 컴퓨터에 개발자용 작업실 꾸미기

> **제출 안내:** 이 문서는 실습 결과를 기록하는 README 템플릿입니다. `[직접 입력]`, `[실행 결과 붙여넣기]` 및 체크박스를 실제 수행 내용으로 수정한 뒤 제출합니다. 아래 명령은 주로 **Linux/macOS Bash 또는 WSL Bash** 기준입니다.

## 1. 프로젝트 개요

Linux CLI, 파일 권한, Docker, Dockerfile, 포트 매핑, Bind Mount, Docker Volume, Git/GitHub를 실습하여 재현 가능한 개발 환경을 구축합니다. 실행 명령과 **실제 출력**, 웹 접속 화면, 데이터 영속성 검증 및 문제 해결 과정을 기록합니다.

- 수행자: [박경부]
- 수행일: [2026.11월]
- GitHub 저장소: [(https://github.com/bigpark61/develop_environment)]
- 실행 환경: [Ubuntu Linux / Windows WSL2 ]

## 2. 실행 환경

| 항목               | 실제 환경/버전                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| HOST OS          | 에디션	Windows 11 Home<br>버전	25H2<br>설치 날짜	‎2025-‎10-‎15<br>OS 빌드	26200.9711<br>기능 팩	Windows 기능 경험 팩 1000.26100.372.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Shell / Terminal | Linux DESKTOP-VKSPJC7 6.18.58.1-microsoft-standard-WSL2 #1 SMP PREEMPT_DYNAMIC Tue Oct 27 00:24:11 UTC 2026 x86_64 GNU/Linux<br><br>Linux OS : Ubuntu 26.04.1 LTS <br>- Ubuntu Release :26.04 <br>- Ubuntu Codename : resolute <br>-Linux 실행 환경 :WSL (버전 확인 필요) \|<br>-Shell : Bash                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| VS Code          | Version: 1.139.1 (system setup)<br>Commit: 04c0d99f4fb0d8afe6ce4f0c58e31e183ac3e4b1<br>Date: 2026-09-25T03:40:57Z<br>Electron: 43.6.0<br>ElectronBuildId: 15274685<br>Chromium: 150.0.7871.250<br>Node.js: 24.20.0<br>V8: 15.0.245.31-electron.0<br>@github/copilot: 1.0.85.r35379093703.g3514c9a<br>@github/copilot-sdk: 1.0.15.35393089353.gfc44743<br>OS: Windows_NT x64 10.0.26200                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Docker           | Docker version 29.9.2, build a82e528<br><br>bigpark61@DESKTOP-VKSPJC7:~$ docker info<br>Client:<br> Version:    29.9.2<br> Context:    default<br> Debug Mode: false<br> Plugins:<br>  agent: Docker AI Agent Runner (Docker Inc.)<br>    Version:  v1.152.0<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-agent<br>  ai: Docker AI Agent - Ask Gordon (Docker Inc.)<br>    Version:  v1.33.0<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-ai<br>  buildx: Docker Buildx (Docker Inc.)<br>    Version:  v0.38.1<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-buildx<br>  compose: Docker Compose (Docker Inc.)<br>    Version:  v5.6.1<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-compose<br>  debug: Get a shell into any image or container (Docker Inc.)<br>    Version:  0.49.0<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-debug<br>  desktop: Docker Desktop commands (Docker Inc.)<br>    Version:  4.98.0<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-desktop<br>  dhi: CLI for managing Docker Hardened Images (Docker Inc.)<br>    Version:  v0.0.9<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-dhi<br>  extension: Manages Docker extensions (Docker Inc.)<br>    Version:  v0.2.32<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-extension<br>  init: Creates Docker-related starter files for your project (Docker Inc.)<br>    Version:  v1.4.1<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-init<br>  mcp: Docker MCP Plugin (Docker Inc.)<br>    Version:  v0.44.2<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-mcp<br>  model: Docker Model Runner (Docker Inc.)<br>    Version:  v1.2.9<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-model<br>  offload: Docker Offload (Docker Inc.)<br>    Version:  v0.7.35<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-offload<br>  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)<br>    Version:  v0.3.2<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-pass<br>  sandbox: "docker sandbox" is deprecated, use Docker Sandboxes instead (Docker Inc.)<br>    Version:  v0.13.0<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-sandbox<br>  scout: Docker Scout (Docker Inc.)<br>    Version:  v1.27.0<br>    Path:     /usr/local/lib/docker/cli-plugins/docker-scout<br><br>Server:<br> Containers: 10<br>  Running: 1<br>  Paused: 0<br>  Stopped: 9<br> Images: 3<br> Server Version: 29.9.2<br> Storage Driver: overlayfs<br>  driver-type: io.containerd.snapshotter.v1<br> Logging Driver: local<br> Cgroup Driver: cgroupfs<br> Cgroup Version: 2<br> Plugins:<br>  Volume: local<br>  Network: bridge host ipvlan macvlan null overlay<br>  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog<br> CDI spec directories:<br>  /etc/cdi<br>  /var/run/cdi<br> Discovered Devices:<br>  cdi: docker.com/gpu=webgpu<br> Swarm: inactive<br> Runtimes: io.containerd.runc.v2 nvidia runc<br> Default Runtime: runc<br> Init Binary: docker-init<br> containerd version: b7a25261e029d68978bbf290df0a62fc819b3c51<br> runc version: v1.5.2-0-g29dd3dc2<br> init version: de40ad0<br> Security Options:<br>  seccomp<br>   Profile: builtin<br>  cgroupns<br> Kernel Version: 6.18.58.1-microsoft-standard-WSL2<br> Operating System: Docker Desktop<br> OSType: linux<br> Architecture: x86_64<br> CPUs: 8<br> Total Memory: 3.685GiB<br> Name: docker-desktop<br> ID: 1f990b51-ee06-4d81-9f6c-26b4d40195d2<br> Docker Root Dir: /var/lib/docker<br> Debug Mode: false<br> HTTP Proxy: http.docker.internal:3128<br> HTTPS Proxy: http.docker.internal:3128<br> No Proxy: hubproxy.docker.internal<br> Labels:<br>  com.docker.desktop.address=unix:///var/run/docker-cli.sock<br> Experimental: false<br> Insecure Registries:<br>  hubproxy.docker.internal:5555<br>  127.0.0.0/8<br>  ::1/128<br> Live Restore Enabled: false<br> Firewall Backend: iptables |
| Git              | git version 2.53.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Docker 엔진        | Docker Desktop                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
[확인 명령어]
```bash
uname -a
docker --version
docker info
git --version
code --version
```

## 3. 수행 항목 체크리스트

> 완료한 항목만 `[x]`로 변경합니다.

- [ ] 터미널에서 파일 및 디렉터리 생성·이동·복사·삭제
- [ ] 파일과 디렉터리 권한 변경 전후 비교
- [ ] Docker 설치 및 엔진 동작 확인
- [ ] Docker 이미지·컨테이너·로그·자원 사용량 확인
- [ ] `hello-world`와 `ubuntu` 실행
- [ ] Dockerfile을 활용한 커스텀 웹 서버 이미지 빌드
- [ ] 포트 매핑 및 브라우저 접속 확인
- [ ] Bind Mount의 실시간 파일 변경 반영 확인
- [ ] Docker Volume의 데이터 영속성 확인
- [ ] Git 설정·GitHub Push·VS Code 연동 확인
- [ ] 트러블슈팅 2건 이상 기록

## 4. Linux CLI 실습

### 4.1 파일 및 디렉터리 조작

```bash
pwd
mkdir -p ~/codyssey/practice
cd ~/codyssey/practice
touch test.txt
echo "Hello Codyssey" > test.txt
cat test.txt
ls -la
cp test.txt copy.txt
mv copy.txt renamed.txt
mkdir sample_dir
mv renamed.txt sample_dir/
ls -la sample_dir
rm sample_dir/renamed.txt
```

**실제 출력 및 관찰 결과:**

```text
[현재 위치, ls -la, cat 출력 및 파일 이동·삭제 확인 결과 붙여넣기]
```

### 4.2 파일·디렉터리 권한 변경

```bash
ls -l test.txt
ls -ld sample_dir
chmod 600 test.txt
chmod 700 sample_dir
ls -l test.txt
ls -ld sample_dir
```

| 대상 | 변경 전 | 변경 후 | 의미 |
|---|---|---|---|
| `test.txt` | [실제 값] | [실제 값] | 소유자 읽기·쓰기만 허용 (`600`) |
| `sample_dir` | [실제 값] | [실제 값] | 소유자만 접근 가능 (`700`) |

**실제 출력:**

```text
[ls -l / ls -ld 변경 전후 출력 붙여넣기]
```

## 5. Docker 기본 점검 및 운영

### 5.1 이미지·컨테이너 실행

```bash
docker run --name hello-test hello-world
docker run -it --name ubuntu-test ubuntu bash
# Ubuntu 컨테이너 내부에서:
pwd
ls
echo "Hello from Ubuntu"
exit
```

**실제 출력:**

```text
[hello-world 성공 메시지와 Ubuntu 내부 명령 출력 붙여넣기]
```

### 5.2 운영 명령

```bash
docker images
docker ps
docker ps -a
docker logs hello-test
docker stats --no-stream
docker start ubuntu-test
docker stop ubuntu-test
```

**실제 출력:**

```text
[이미지 목록, 컨테이너 상태, 로그, 자원 사용량 출력 붙여넣기]
```

**관찰:** `docker run -it`은 새 컨테이너를 만들고 터미널을 연결합니다. `docker exec -it <실행중인_컨테이너> bash`는 실행 중인 기존 컨테이너 안에 추가 셸을 엽니다. `exit` 시 메인 프로세스가 끝나면 컨테이너가 종료될 수 있습니다.

## 6. Dockerfile로 커스텀 웹 서버 제작

### 6.1 프로젝트 구조

```text
.
├── Dockerfile
├── README.md
├── site/
│   └── index.html
└── evidence/
    ├── docker-build.txt
    ├── docker-operations.txt
    ├── web-8080.png
    ├── bind-mount.png
    └── volume-check.txt
```

### 6.2 사용한 베이스 이미지 및 커스텀 내용

- **베이스 이미지:** `nginx:alpine` — 경량 NGINX 웹 서버
- **커스텀 포인트:** 기본 정적 페이지 대신 `site/index.html` 복사
- **목적:** 동일한 웹 콘텐츠를 이미지로 빌드하고 독립적으로 실행

**Dockerfile**

```dockerfile
FROM nginx:alpine
COPY site/ /usr/share/nginx/html/
EXPOSE 80
```

**site/index.html**

```html
<!DOCTYPE html>
<html lang="ko">
<head><meta charset="UTF-8"><title>Codyssey Web</title></head>
<body><h1>Hello Codyssey!</h1><p>Docker custom image test</p></body>
</html>
```

### 6.3 빌드·실행·포트 매핑

```bash
docker build -t codyssey-web:1.0 .
docker run -d --name codyssey-web -p 8080:80 codyssey-web:1.0
docker ps
docker logs codyssey-web
curl http://localhost:8080
```

- 브라우저 접속: `http://localhost:8080`
- 포트 매핑 의미: **호스트 8080 → 컨테이너 80**
- 접속 결과: [성공/실패 및 확인 내용 직접 입력]
- 실행 증빙: [웹 접속 화면](evidence/web-8080.png) (스크린샷 첨부 후 확인)
- 빌드 로그: [docker-build.txt](evidence/docker-build.txt) (실제 로그 첨부 후 확인)

**실제 핵심 출력:**

```text
[빌드 완료 메시지, docker ps의 PORTS 열, curl 응답 붙여넣기]
```

## 7. Bind Mount 검증

호스트의 `site/index.html`을 컨테이너의 NGINX 웹 루트에 연결합니다.

```bash
docker run -d --name bind-web -p 8082:80 \
  -v "$(pwd)/site:/usr/share/nginx/html:ro" nginx:alpine
curl http://localhost:8082
# 호스트에서 site/index.html 문구를 수정한 뒤 다시 확인
curl http://localhost:8082
```

- 검증 주소: `http://localhost:8082`
- 변경 전 문구: [직접 입력]
- 변경 후 문구: [직접 입력]
- 관찰 결과: [호스트 파일 수정이 새 이미지 빌드 없이 반영되었는지 입력]
- 증빙: [bind-mount.png](evidence/bind-mount.png)

**실제 출력:**

```text
[수정 전후 curl 응답 붙여넣기]
```

## 8. Docker Volume 영속성 검증

```bash
docker volume create codyssey-data
docker run --name volume-write -v codyssey-data:/data ubuntu \
  sh -c 'echo persistent-data > /data/test.txt && cat /data/test.txt'
docker rm volume-write
docker run --rm -v codyssey-data:/data ubuntu cat /data/test.txt
docker volume inspect codyssey-data
```

- 예상 검증 기준: 새 컨테이너에서도 `persistent-data`가 출력되어야 함
- 실제 결과: [직접 입력]
- 증빙: [volume-check.txt](evidence/volume-check.txt)

**실제 출력:**

```text
[첫 컨테이너와 재생성 컨테이너의 출력, volume inspect 결과 붙여넣기]
```

**정리:** Bind Mount는 호스트 파일과 직접 연결하여 수정 사항을 반영하고, Docker Volume은 컨테이너를 삭제해도 데이터를 별도로 유지합니다.

## 9. Git / GitHub / VS Code 연동

```bash
git config --global user.name "[GitHub 표시 이름]"
git config --global user.email "[GitHub 이메일]"
git init
git branch -M main
git add .
git commit -m "docs: add AIO E1-1 workstation assignment"
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
git status
```

> `USERNAME/REPOSITORY`를 실제 저장소로 바꾸고, 비밀번호·토큰·`.env` 파일은 커밋하지 않습니다. 이미 Git 저장소가 있다면 `git init`이나 `git remote add origin`을 중복 실행하지 않습니다.

- GitHub URL: [직접 입력]
- VS Code에서 저장소 열기 및 Source Control 확인: [확인 결과 입력]
- 마지막 `git status` 결과: [직접 입력]

```text
[git status / git remote -v / git log -1 출력 붙여넣기]
```

## 10. 트러블슈팅 (최소 2건)

> 아래는 **기록 양식**입니다. 실제 발생한 문제만 작성하고, 예시를 본인 경험으로 표시하지 마세요.

### 사례 1 — [실제 오류 제목]

- **문제:** [오류 메시지 및 발생 상황]
- **원인 가설:** [추정 원인]
- **확인 방법:** `[실제로 실행한 진단 명령]`
- **확인 결과:** [명령 출력 및 원인 판단]
- **해결/대안:** [실제로 수행한 조치]
- **재검증:** [해결 확인 명령 및 결과]

### 사례 2 — [실제 오류 제목]

- **문제:** [오류 메시지 및 발생 상황]
- **원인 가설:** [추정 원인]
- **확인 방법:** `[실제로 실행한 진단 명령]`
- **확인 결과:** [명령 출력 및 원인 판단]
- **해결/대안:** [실제로 수행한 조치]
- **재검증:** [해결 확인 명령 및 결과]

## 11. 검증 결과 및 증빙 목록

| 검증 항목 | 확인 명령/방법 | 결과 | 증빙 |
|---|---|---|---|
| 터미널 조작 | `pwd`, `ls -la`, `cat` | [입력] | README 4절 |
| 권한 변경 | `ls -l`, `ls -ld` | [입력] | README 4절 |
| Docker 엔진 | `docker info` | [입력] | README 2절 |
| 컨테이너 운영 | `docker ps -a`, `docker logs`, `docker stats` | [입력] | [운영 로그](evidence/docker-operations.txt) |
| 커스텀 이미지 | `docker build`, `docker images` | [입력] | [빌드 로그](evidence/docker-build.txt) |
| 웹 접속 | 브라우저 `localhost:8080` | [입력] | [화면](evidence/web-8080.png) |
| Bind Mount | 파일 수정 전후 `curl` | [입력] | [화면](evidence/bind-mount.png) |
| Volume | 컨테이너 삭제 후 데이터 재조회 | [입력] | [검증 로그](evidence/volume-check.txt) |
| GitHub | `git status`, 원격 저장소 확인 | [입력] | [저장소 URL 입력] |

## 12. 학습 결과 및 회고

- **Linux CLI:** [학습한 내용]
- **Docker 이미지와 컨테이너:** [차이를 설명]
- **포트 매핑:** [호스트와 컨테이너 포트 관계]
- **Bind Mount와 Volume:** [실험으로 확인한 차이]
- **Git/GitHub:** [버전 관리와 원격 저장소 연동 경험]
- **추가 개선점:** [향후 보완할 내용]

---

**제출 전 확인:** 실제 명령 출력과 스크린샷을 추가하고, 깨진 증빙 링크가 없는지 확인한 다음, 완료 항목만 체크하여 GitHub에 Push합니다.
