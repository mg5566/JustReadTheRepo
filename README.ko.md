# JustReadTheRepo

프로젝트의 메인 저장소입니다. 클라이언트와 서버가 서브모듈로 구성되어 있습니다.

## 프로젝트 구조

- `client/`: 클라이언트 측 애플리케이션 (서브모듈)
- `server/`: 서버 측 애플리케이션 (서브모듈)

## 시작하기

1. 서브모듈을 포함하여 저장소 클론하기:

   ```bash
   git clone --recurse-submodules <저장소-주소>
   ```

2. 이미 저장소를 클론한 경우, 서브모듈 초기화 및 업데이트:
   ```bash
   git submodule init
   git submodule update
   ```

## 서브모듈 업데이트

모든 서브모듈을 최신 master 브랜치로 업데이트:

```bash
git submodule update --remote --merge
```

이 명령어는 각 서브모듈의 원격 저장소에서 최신 변경사항을 가져와 병합합니다.

특정 버전(브랜치/커밋/태그)으로 업데이트하려면:

```bash
# 서브모듈 디렉토리로 이동
cd client  # 또는 server

# 원하는 브랜치/커밋/태그로 체크아웃
git checkout <브랜치명>  # 또는 <커밋해시> 또는 <태그명>

# 상위 디렉토리로 이동
cd ..

# 서브모듈 업데이트 사항 커밋
git add client  # 또는 server
git commit -m "서브모듈 버전 업데이트"
```

## 서브모듈 작업 가이드

- 모든 서브모듈의 상태 확인:

  ```bash
  git submodule status
  ```

- 모든 서브모듈 초기화 및 업데이트 (중첩된 서브모듈 포함):

  ```bash
  git submodule update --init --recursive
  ```

- 저장소와 서브모듈의 변경사항 한 번에 가져오기 (느릴 수 있음):
  ```bash
  git pull --recurse-submodules
  ```
- 특정 서브모듈만 업데이트하기 (더 빠름):

  ```bash
  # client 서브모듈만 업데이트
  git submodule update --remote client

  # server 서브모듈만 업데이트
  git submodule update --remote server
  ```
