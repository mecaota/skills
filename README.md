# skills
いい感じになったスキルをここに置いておく

## 収録スキル

| スキル | 概要 |
|---|---|
| retrospective | 作業後に、モデル・effort とサブエージェントの使い方が適切だったかを振り返り、教訓をログに記録する |

## インストール

Claude Code で次を実行します。

```
/plugin marketplace add mecaota/skills
/plugin install retrospective@mecaota-skills
```

## retrospective の使い方

次のように話しかけると起動します。

- 「振り返って」
- 「過去30日を振り返って」
- 「アーカイブ済セッションだけ振り返って」

オプションは次の2つです。

| オプション | 既定 | 内容 |
|---|---|---|
| days | 0 | 0 は現在のセッションのみ。N(1以上)は直近 N 日間に活動があった全セッション |
| archived_only | オフ | オンにするとアーカイブ済セッションだけが対象 |

`days` を 1 以上にする場合と `archived_only` を使う場合は、Claude デスクトップアプリなどが提供するセッション管理ツール(`mcp__ccd_session_mgmt__*`)が必要です。使えない環境では、現在の会話だけを振り返ります。

## 学習ログについて

- 振り返りで得た教訓は、あなたのマシン上の `~/.claude/retrospective/log.md` にだけ書き込みます。外部へは送信しません。
- `~/.claude/CLAUDE.md` やエージェント定義の編集は、変更内容を示したうえで、あなたが承認した場合にだけ行います。

## ライセンス

MIT
