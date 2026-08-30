# ユーザーとグループ管理

## 覚えるポイント

- ユーザー情報は`/etc/passwd`、パスワード関連情報は`/etc/shadow`
- グループ情報は`/etc/group`
- UID、GID、プライマリグループ、補助グループを区別する
- 所有者は`chown`、グループは`chgrp`で変更する

## コマンド例

```bash
id
whoami
getent passwd "$(whoami)"
getent group
ls -l /etc/passwd /etc/shadow
```

`useradd`、`usermod`、`passwd`などは管理者権限と環境変更を伴います。まずはオプションを`man`で確認してください。

## 確認問題

1. `/etc/passwd`の各フィールドを説明できるか
2. プライマリグループと補助グループの違いは何か
