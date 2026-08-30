# Linuxのインストールとパッケージ

## 覚えるポイント

- `/`、`/boot`、swapなどの役割
- MBRとGPT、BIOSとUEFIの組み合わせ
- Debian系の`dpkg`/`apt`とRPM系の`rpm`/`dnf`
- 共有ライブラリの探索と`ldconfig`

## コマンド例

```bash
lsblk
df -h
du -sh .
dpkg -l | head
apt-cache policy bash
ldd /bin/ls
```

`apt install`など環境を変更する操作は、必要性を確認してから実行します。

## 確認問題

1. `df`と`du`の違いは何か
2. パッケージ管理の低水準・高水準ツールを区別できるか
