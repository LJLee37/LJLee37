# LJLee37

> **Back-end & infrastructure developer in Korea.**
> I run three personal Linux servers and manage them as code with Ansible — VPN,
> firewall, and SSH access backed by hardware security keys. When one of them was
> compromised, I took it from evidence collection through offline analysis to a
> hardened rebuild. I'm also interested in back-end development with
> Node.js/Express and Docker.
> B.S. in Computer Engineering, Gachon University. Open to back-end and
> infrastructure roles, and considering graduate school.

## 소개

가천대학교 컴퓨터공학과를 졸업했습니다(학사). 백엔드 개발과 서버 인프라에 관심을
두고 있으며, 이 분야의 취업과 대학원 진학을 함께 고려하고 있습니다.

## 서버 인프라 자동화와 보안

개인 리눅스 서버 세 대를 운영하며 설정을 Ansible 코드로 관리합니다. 구성 정보가
담겨 있어 저장소는 비공개로 두고, 무엇을 판단하고 무엇을 배웠는지는
[worklog](https://github.com/LJLee37/worklog)에 날짜별로 공개합니다. 작업에는
Claude Code를 적극적으로 활용합니다.

- **구성 관리** — VPN(strongSwan/IKEv2), 방화벽(nftables), 서비스와
  타이머(systemd)를 Ansible 역할로 작성하고, 비밀값은 ansible-vault로 분리합니다.
- **침해 사고 대응** — 운영하던 라즈베리파이 서버가 침해된 것을 발견해 진단,
  증거 보전, 차단, 오프라인 분석까지 진행했습니다. 디스크 이미지에서 삭제된 악성
  스크립트를 복구해 SSH 무차별 대입 봇이라는 것을 확인했고, 로그 전 구간을 다시
  살펴 최초 침입이 처음 추정보다 11일 앞섰다는 것을 밝혔습니다.
- **재구축과 하드닝** — 침입 경로였던 "첫 부팅 후 기본 계정이 열려 있는 구간"을
  없애기 위해, 기본 계정 삭제·키 전용 SSH·방화벽 설정을 첫 부팅 전에 오프라인
  chroot에서 끝내는 방식으로 다시 설치했습니다.
- **접근 통제** — FIDO2 하드웨어 보안 키를 SSH 로그인과 커밋 서명에 쓰고, 이 키를
  인증기관으로 삼는 단기 SSH 인증서와 호스트 키 인증서를 도입했습니다.

## 백엔드

- Node.js/Express와 Docker를 중심으로 백엔드 개발에 관심을 두고 있습니다.

## 참여했던 프로젝트

- [Lantern](https://github.com/orgs/Team-Lantern) — 초기 개발에 참여했습니다. 앱은
  앱스토어에 출시되었습니다. (저장소 비공개)

## 기술

- **인프라**: Linux(Arch Linux), Ansible, systemd, nftables, OpenSSH, strongSwan
- **백엔드**: Node.js, Express, Docker
- **언어**: Python, Shell, JavaScript

## 연락처

- Email: ljlee3759@gmail.com
