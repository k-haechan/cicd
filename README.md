# cicd

## 1. dev branch 생성

## 2. Settings > General > Pull Request 수정
- Allow squash merging : Pull request title

## 3. Branch Protection Rules 설정
- Ruleset Name : main branch ruleset
- Bypass list : Repository admin
- Branch name pattern : main
- Branch protection rules
  - Restrict updates (관리자만 업데이트 가능)
  - Restrict deletions (관리자만 삭제 가능)
  - Require linear history (병합 시 rebase 방식으로 병합)
  - Require pull request before merging
    - Require approvals : 0 (개인 개발 환경에서는 0으로 설정)
    - Dismiss stale pull request approvals when new commits are pushed(추가 커밋 시 기존 승인 무효화)
    - Require review from Code Owners (코드 소유자 리뷰 필요)
    - Require status checks to pass before merging (병합 전 상태 검사 통과 필요)
    - Allowed merge methods
      - Allow rebase merging (리베이스 병합 허용)

[//]: # (  - Require status to pass)

[//]: # (    - Require branches to be up to date before merging &#40;병합 전 브랜치 최신 상태 필요&#41;)

[//]: # (    - Do not require status checks on creation &#40;생성 시 상태 검사 필요 없음&#41;)
