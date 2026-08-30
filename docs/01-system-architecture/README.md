# システムアーキテクチャ

## 覚えるポイント

- BIOS/UEFIからブートローダー、カーネル、initシステムへ進む起動の流れ
- `systemd`ではPID 1の`systemd`がサービスを管理する
- プロセスにはPID、親プロセス、状態、優先度がある

## コマンド例

```bash
ps aux
ps -ef
systemctl list-units --type=service
journalctl -b
uname -r
```

devcontainerではsystemdがPID 1でない場合があり、`systemctl`の一部操作は失敗します。その場合はコマンドの意味と出力形式を確認してください。

## 確認問題

1. Linuxの起動処理を大まかな順番で説明できるか
2. PID 1が担う役割は何か
3. `ps aux`と`ps -ef`は何を表示するか
