# Intro

## Living dangerously

- 새 파일을 만들면 상태가 **untracked**로 표시됨  
- `git add` 로 스테이징, `git commit` 으로 저장  

```bash
git add .
git commit -m "첫 번째 커밋"
```

---

## Making backups

* 작업 내용을 저장하고 커밋을 쌓아나감
* `git log` 로 커밋 히스토리 확인

```bash
git add .
git commit -m "백업 저장"
git log
```

---

## Enter the time machine

- 이전 커밋으로 되돌아가기 (타임머신 개념)

```bash
git log
git checkout <커밋ID>
```

- 최신 상태로 복귀할 때:

```bash
git checkout main
```

---

## The command line

- 직접 명령어를 타이핑하여 실습
- 자주 쓰는 기본 명령:

  ```bash
  git status
  git add .
  git commit -m "메시지"
  git log --oneline
  ```

---

## Your first commit

- 새 파일을 추가하고 커밋하는 연습

```bash
echo "Hello Git!" > hello.txt
git add hello.txt
git commit -m "Add hello.txt"
```

---

## Working together

* 브랜치 개념 및 병합 연습

```bash
git branch new-feature
git switch new-feature
# 새로운 변경 작업
git add .
git commit -m "Add new feature"
git switch main
git merge new-feature
```

- 브랜치를 합치면 그래프에 선이 병합되어 표시됨
