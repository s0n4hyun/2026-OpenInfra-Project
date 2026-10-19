# 02. About Git Branch

## 1. Git Branch란?

Git Branch는 기존 코드를 유지하면서 별도로 작업할 수 있도록 만드는 기능이다.

- **main** : 프로젝트의 기본 브랜치
- **작업 브랜치** : 새로운 기능 추가나 수정 작업을 진행하는 브랜치
- **Merge** : 서로 다른 브랜치의 변경 내용을 합치는 과정

브랜치를 사용하면 여러 사람이 같은 프로젝트에서 각자의 작업을 독립적으로 진행할 수 있다.

## 2. 주요 명령어

| 명령어 | 기능 |
|---|---|
| `git branch` | 브랜치 목록 확인 |
| `git branch -a` | 로컬 및 원격 브랜치 확인 |
| `git branch <name>` | 새로운 브랜치 생성 |
| `git switch <name>` | 브랜치 전환 |
| `git switch -c <name>` | 브랜치 생성 후 바로 전환 |
| `git merge <name>` | 다른 브랜치의 변경사항 병합 |
| `git branch -d <name>` | 로컬 브랜치 삭제 |

## 3. 실습 내용

1. GitHub에서 `docs-setup` 브랜치 생성
2. `git clone`으로 Fork한 저장소를 로컬에 복제
3. `git switch docs-setup`으로 작업 브랜치 전환
4. `git branch`로 현재 브랜치 확인
5. Sphinx 문서 파일 작성 후 Commit 및 Push
6. 원본 저장소에 Pull Request 생성

**실습 결과:** [Pull Request #1](https://github.com/openstack-kr/openstack-kubernetes-students/pull/1)

## 4. 새롭게 알게 된 점

Branch를 사용하면 기본 브랜치를 직접 수정하지 않고 별도로 작업할 수 있다는 것을 알게 되었다.

또한 Commit과 Push만으로 원본 저장소가 변경되는 것은 아니며, Pull Request를 통해 변경사항을 제안하고 Merge해야 반영된다는 점을 이해했다.
