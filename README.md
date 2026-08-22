# natural-korean

번역어투와 격언조를 걷어내고 쉬운 말로 쓰는 한국어 문체 규칙을 담은 Claude Code 플러그인.

출력 스타일 하나가 들어 있다. 켜두면 모든 답변에 규칙이 붙는다.
`keep-coding-instructions: true` 라서 코딩 지침은 그대로 두고 문체만 얹는다.

## 설치

세 단계다. 앞의 둘은 파일만 가져다 놓고, 실제로 답변이 바뀌는 건 셋째다.

### 1. 마켓플레이스 등록

```
/plugin marketplace add predictorsSH/natural-korean
```

### 2. 플러그인 설치

```
/plugin install natural-korean@natural-korean
```

앞은 플러그인 이름, 뒤는 마켓플레이스 이름이다. 우연히 같다.

### 3. 스타일 켜기

```
/config
```

Output style 항목에서 `자연스러운 한국어` 를 고른다.
예전 `/output-style` 은 `/config` 로 합쳐졌다.

고른 뒤 Claude Code를 새로 띄운다. 설정은 시작할 때 읽는다.

## 모든 프로젝트에 적용하려면

`/config` 로 고른 값은 그 프로젝트의 `.claude/settings.local.json` 에 저장된다.
프로젝트마다 켜기 싫으면 `~/.claude/settings.json` 에 직접 넣는다.

```json
{
  "outputStyle": "자연스러운 한국어"
}
```

프로젝트 설정이 전역보다 우선한다. 특정 프로젝트에서만 끄려면 거기서 `/config` 로 다른 걸 고르면 된다.

## 터미널에서 하려면

`/` 로 시작하는 건 Claude Code 안에서만 먹는다. 쉘에서는 `claude` 를 앞에 붙이고 슬래시를 뺀다.

```
claude plugin marketplace add predictorsSH/natural-korean
claude plugin install natural-korean@natural-korean
```

`/config` 는 화면을 띄우는 거라 Claude Code 안에서만 된다.

## 끄기

`/config` 에서 default 를 고르거나, `outputStyle` 줄을 지운다.

## 규칙 고치기

[output-styles/natural-korean.md](output-styles/natural-korean.md)를 고치고 푸시한다.
쓰는 쪽에서는 이렇게 받는다.

```
/plugin marketplace update natural-korean
/plugin install natural-korean@natural-korean
```
