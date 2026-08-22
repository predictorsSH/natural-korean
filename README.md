# natural-korean

번역어투와 격언조를 걷어내고 쉬운 말로 쓰는 한국어 문체 규칙을 담은 Claude Code 플러그인.

출력 스타일 하나가 들어 있다. 켜두면 모든 답변에 규칙이 붙는다.
`keep-coding-instructions: true` 라서 코딩 지침은 그대로 두고 문체만 얹는다.

## 설치

아래 세 줄을 Claude Code 안에서 차례로 친다.

```
/plugin marketplace add predictorsSH/natural-korean
/plugin install natural-korean@natural-korean
/config
```

`/config` 를 치면 설정 화면이 뜬다. Output style 항목에서 `자연스러운 한국어` 를 고른다.

고른 뒤 Claude Code를 껐다 켜야 적용된다.

두 번째 줄까지만 하면 답변은 그대로다. 설치는 스타일을 목록에 올려놓기만 하고, 켜는 건 `/config` 에서 고를 때다.

## 모든 프로젝트에 적용하려면

`/config` 에서 고른 값은 그 프로젝트의 `.claude/settings.local.json` 에 저장된다.
프로젝트를 옮길 때마다 다시 고르기 싫으면 `~/.claude/settings.json` 에 직접 적는다.

```json
{
  "outputStyle": "자연스러운 한국어"
}
```

이렇게 적어두고 특정 프로젝트에서만 끄고 싶으면, 그 프로젝트에서 `/config` 로 다른 걸 고른다.
프로젝트 설정이 전역 설정을 덮어쓴다.

## 터미널에서 설치하려면

`/plugin` 을 쉘에 그대로 치면 `command not found` 가 난다. Claude Code가 읽는 명령어라서 그렇다.
쉘에서는 `claude` 를 앞에 붙이고 슬래시를 뺀다.

```
claude plugin marketplace add predictorsSH/natural-korean
claude plugin install natural-korean@natural-korean
```

스타일을 고르는 건 설정 화면에서만 되니, `/config` 는 Claude Code 안에서 친다.

## 끄기

`/config` 에서 default 를 고른다. 전역 설정에 적어뒀다면 `outputStyle` 줄을 지운다.

## 규칙 고치기

[output-styles/natural-korean.md](output-styles/natural-korean.md)를 고치고 푸시한다.
설치해서 쓰던 사람은 아래 두 줄로 새 버전을 받는다.

```
/plugin marketplace update natural-korean
/plugin install natural-korean@natural-korean
```
