# シェルとスクリプト

## 覚えるポイント

- シェル変数と環境変数の違い
- クォートによる展開の違い
- 終了ステータスは成功が0、失敗が0以外
- `&&`、`||`、パイプの評価

## コマンド例

```bash
name=linux
echo "$name"
export STUDY_MODE=linuc
env | grep STUDY_MODE
printf '%s\n' "$PATH" | tr ':' '\n'
true && echo success
false || echo failed
echo $?
```

## 最小スクリプト

```bash
#!/usr/bin/env bash
set -u

name="${1:-learner}"
printf 'Hello, %s\n' "$name"
```

変数は意図しない単語分割を避けるため、通常は`"$name"`のように引用します。
