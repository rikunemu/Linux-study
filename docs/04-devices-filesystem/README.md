# デバイスとファイルシステム

## 覚えるポイント

- デバイスファイルは主に`/dev`にある
- マウントするとファイルシステムがディレクトリツリーへ接続される
- 権限は所有者・グループ・その他に対する`rwx`
- ハードリンクはinodeを共有し、シンボリックリンクはパスを参照する

## コマンド例

```bash
lsblk
findmnt
df -hT
stat /etc/passwd
ls -li /etc/passwd
umask
```

## 権限

```text
r = 4, w = 2, x = 1
755 = rwxr-xr-x
640 = rw-r-----
```

```bash
touch sample.txt
chmod 640 sample.txt
ln sample.txt hard-link.txt
ln -s sample.txt symbolic-link.txt
ls -li
```

## 確認問題

1. `chmod 754`を記号形式で表せるか
2. ハードリンクとシンボリックリンクの違いは何か
3. `df`、`findmnt`、`lsblk`の用途は何か
