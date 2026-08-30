# ネットワーク

## 覚えるポイント

- IPアドレス、サブネット、デフォルトゲートウェイ
- ホスト名からIPアドレスを得る名前解決
- `/etc/hosts`、`/etc/resolv.conf`、`/etc/nsswitch.conf`の役割
- TCP/UDPとポート番号

## コマンド例

```bash
ip address
ip route
getent hosts localhost
cat /etc/resolv.conf
ss -tuln
ping -c 3 127.0.0.1
```

環境によって`ping`や外部通信が制限される場合があります。まずループバックで確認します。

## 切り分けの順番

1. インターフェースとIPアドレス
2. ルーティング
3. 名前解決
4. 接続先ポート
