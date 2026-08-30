# GNU/Unixコマンド

## ls

ディレクトリの内容を一覧表示します。

| オプション | 意味 |
| --- | --- |
| `-a` | 隠しファイルを含める |
| `-d` | ディレクトリの中身ではなく、ディレクトリ自身を表示する |
| `-F` | 種類を示す記号を付ける |
| `-l` | 権限、所有者、サイズなどを長い形式で表示する |
| `-r` | 並び順を逆にする |
| `-t` | 更新時刻順に並べる |

```bash
ls -la /etc
ls -ld /tmp
ls -ltr
```

## ファイル操作

```bash
pwd
touch sample.txt
cp sample.txt copy.txt
mv copy.txt renamed.txt
mkdir -p work/subdir
rm renamed.txt
```

`rm`は基本的に元に戻せません。パスを確認してから実行します。

## 検索とテキスト処理

```bash
find /etc -maxdepth 1 -type f 2>/dev/null
grep -n "root" /etc/passwd
cut -d: -f1 /etc/passwd
sort names.txt | uniq
head -n 5 /etc/passwd
tail -n 5 /etc/passwd
```

## リダイレクトとパイプ

- `>`: 上書き
- `>>`: 追記
- `2>`: 標準エラー出力
- `|`: 左の標準出力を右の標準入力へ渡す

```bash
printf '%s\n' beta alpha alpha | sort | uniq
find /not-found 2>errors.log
```

## 確認問題

1. `ls -d /etc`と`ls /etc`の違いは何か
2. 標準出力と標準エラー出力を別々のファイルへ保存できるか
3. `find`と`grep`の用途を区別できるか
