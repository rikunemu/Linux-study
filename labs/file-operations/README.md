# Lab: ファイル操作

## 目的

作成、コピー、移動、検索、削除を安全な作業用ディレクトリで練習します。

```bash
lab_dir="$(mktemp -d)"
cd "$lab_dir"
mkdir -p docs/archive
printf '%s\n' alpha beta gamma > docs/names.txt
cp docs/names.txt docs/names.bak
mv docs/names.bak docs/archive/
find . -type f -print
grep -n beta docs/names.txt
ls -laR
cd /
rm -r "$lab_dir"
```

## 確認

- `find`で2ファイルを確認できたか
- `grep`の行番号は何番だったか
- 削除前に`lab_dir`の値を確認したか
