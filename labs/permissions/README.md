# Lab: パーミッション

```bash
lab_dir="$(mktemp -d)"
cd "$lab_dir"
touch public.txt private.txt script.sh
chmod 644 public.txt
chmod 600 private.txt
chmod 750 script.sh
ls -l
stat -c '%A %a %n' ./*
umask
cd /
rm -r "$lab_dir"
```

## 課題

1. `640`、`755`、`700`を記号形式へ変換する
2. `chmod u+x,g-w,o-r file`が何を変えるか説明する
3. 現在の`umask`から新規ファイルの初期権限を考える
