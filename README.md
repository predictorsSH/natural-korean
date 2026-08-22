# natural-korean

번역어투와 격언조를 걷어내고 쉬운 말로 쓰는 한국어 문체 규칙을 담은 Claude Code 플러그인.

## 설치

```
/plugin marketplace add /Users/sanghyun/Projects/natural-korean
/plugin install natural-korean@natural-korean
```

깃허브에 올린 뒤에는 경로 대신 `owner/repo`를 쓴다.

## 들어 있는 것

- **스킬 `natural-korean`** — 한국어를 쓰거나 고칠 때 자동으로 불러온다.
- **명령어 `/polish-korean [파일|문장]`** — 지정한 글을 규칙대로 다듬는다. 인자가 없으면 방금 쓴 한국어 텍스트를 다듬는다.

## 항상 켜두려면

스킬은 필요할 때만 불러온다. 모든 답변에 규칙을 적용하려면 `CLAUDE.md`에 한 줄 넣는다.

```
한국어로 답할 때는 `natural-korean` 스킬을 먼저 읽고 그 규칙을 지킨다.
```

## 규칙 고치기

[skills/natural-korean/SKILL.md](skills/natural-korean/SKILL.md)를 고치면 된다.
로컬 경로로 설치했으면 `/plugin` 에서 다시 불러온다.
