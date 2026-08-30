# Lab: ネットワーク確認

設定を変更せず、現在の状態を読み取ります。

```bash
ip address
ip route
getent hosts localhost
cat /etc/resolv.conf
ss -tuln
ping -c 3 127.0.0.1
```

## 記録すること

- ループバックインターフェース名とアドレス
- デフォルトルートの有無
- 名前解決に使われる設定
- 待ち受け中のTCP/UDPポート
