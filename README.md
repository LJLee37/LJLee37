# LJLee37

> Backend and infrastructure developer in Korea. B.Eng. in Computer Engineering,
> Gachon University. As an early member of a project team, I spent a year and seven
> months on the backend of a personal-safety app (Node.js, Express, MariaDB), where I
> added the team's first logging and integration tests. Now I run three servers as
> code with Ansible, with SSH access built on FIDO2 hardware keys, working together
> with Claude Code. Open to backend and infrastructure roles.

## 소개

가천대학교 컴퓨터공학과를 졸업했습니다(공학사). 백엔드와 서버 인프라, 두 갈래에
관심을 두고 있으며 이 분야의 직무를 찾고 있습니다.

만든 것을 반드시 검증하고 넘어가려고 합니다. 서비스가 제대로 돌고 있다는 것,
문제가 생겨도 빨리 알아채고 고칠 수 있다는 것을 저도 믿고 팀원도 믿을 수 있게
하고 싶어서, 팀에 없던 로깅과 테스트를 처음 만들었습니다.

## 프로젝트

### Lantern, 여성 안심귀가 서비스 백엔드 (2023.01 ~ 2024.08)

8인 프로젝트팀의 초기 멤버로 Node.js, Express, MariaDB 백엔드를 개발했습니다.

- winston 기반 로깅을 처음 구축했습니다. 제가 팀을 떠나고 2년이 지난 지금도
  서비스에서 쓰이고 있습니다.
- 운영 API에 대한 통합 테스트를 mocha로 작성했습니다(팀 최초).
- 1:1 통화 기능을 10개월간 맡아 대화 주제 추천 API를 만들고, 매칭 대기열에 Redis를
  도입했습니다. 기획이 폐기되면서 Redis도 직접 걷어냈습니다.
- PR 32건을 올려 모두 병합되었고, 동료의 PR 51건을 리뷰했습니다.
- 사회복무 소집으로 개발에서 빠진 뒤에도 5개월간 코드 리뷰로 인수인계를
  마쳤습니다. 서비스는 팀이 이어받아 2025년 9월 App Store에 출시했습니다.

### 개인 서버 인프라 (2022 ~, 복무 기간 중단)

대학 시절부터 집에서 Arch Linux 서버를 운영해 왔고, 2026년 8월부터 설정을
Ansible 저장소로 옮겨 관리합니다. 지금은 x86_64 Arch Linux 서버, Raspberry Pi
(aarch64 Arch Linux ARM), 클라우드 VM(Debian) 세 대를 한 플레이북으로 운영합니다.

- VPN(strongSwan IKEv2), 방화벽(nftables), 인증서 자동 갱신, systemd 타이머를
  role로 관리합니다.
- 비밀값은 ansible-vault로 분리하고, pre-commit 훅으로 평문 커밋을 막습니다.
- SSH 접속은 FIDO2 보안 키로 서명한 단기 SSH 인증서로 합니다. 서버끼리 자동으로
  접속할 수 있도록 각 서버의 호스트 키도 같은 보안 키로 서명해 인증서로 확인합니다.
- 커밋 서명도 FIDO2 보안 키로 합니다.

이 작업은 Claude Code와 함께 합니다. 방향과 설계는 제가 정하고, 구현과 진단은
AI에 맡깁니다. sudo나 보안 키 터치가 필요한 단계는 제가 직접 실행하고, VPN 같은
변경은 실제 기기로 접속해 확인합니다. 무엇을 판단했고 무엇이 틀렸는지는
[worklog](https://github.com/LJLee37/worklog)에 날짜별로 남깁니다.

### 그 밖에

- **daily-briefing** (비공개): 할 일, 날씨, 뉴스 브리핑을 매일 아침 Discord와
  메일로 보냅니다. 두 호스트가 중복 발송하지 않도록 별도 조정 서버 없이 git
  저장소를 조정 지점으로 썼습니다.
- **[settingfiles](https://github.com/LJLee37/settingfiles)**: 2020년부터 쓰는
  닷파일 저장소입니다. OS별 브랜치로 나눠 관리하고, 새 기기 설정과 Arch Linux 설치
  과정을 단계별 셸 스크립트로 만들어 썼습니다.
- **[Baekjoon](https://github.com/LJLee37/Baekjoon)**: 알고리즘 문제 풀이(Python, C++)

## 기술

- **백엔드**: Node.js, Express, MariaDB, knex, Redis, mocha
- **인프라**: Linux(Arch Linux), Ansible, systemd, nftables, strongSwan(IKEv2),
  OpenSSH(인증서, FIDO2)
- **언어**: JavaScript, Python, Shell, C++
- **협업**: Git, GitHub, 코드 리뷰

## 약력

- 2020.03 ~ 2024.02: 가천대학교 컴퓨터공학과 (공학사)
- 2023.01 ~ 2024.08: Lantern 백엔드 (프로젝트팀)
- 2024.11 ~ 2026.08: 사회복무요원 (소집해제)

## 연락처

- Email: ljlee3759@gmail.com
