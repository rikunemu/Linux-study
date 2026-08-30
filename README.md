# Linux-study

LinuC Level 1の学習内容を、解説・コマンド実行・復習の流れで整理するリポジトリです。

## 学習の進め方

1. [学習マップ](docs/README.md)から分野を選ぶ
2. 各章の「覚えるポイント」と例を読む
3. [labs](labs/)の手順をdevcontainerで実行する
4. [progress.md](progress.md)を更新する
5. 間違えた内容を[review/mistakes.md](review/mistakes.md)へ残す

> コマンドは検証用devcontainer内で実行してください。削除、権限変更、ユーザー管理などの操作を普段使いの環境で安易に試さないでください。

## 環境の始め方

VS Codeでリポジトリを開き、`Dev Containers: Reopen in Container` を実行します。
Ubuntu環境のターミナルが開いたら、次のコマンドで確認できます。

```bash
cat /etc/os-release
uname -a
whoami
pwd
```

## 教材

| 分野 | 内容 |
| --- | --- |
| [システムアーキテクチャ](docs/01-system-architecture/README.md) | 起動、ランレベル、プロセスの基礎 |
| [Linuxのインストール](docs/02-linux-installation/README.md) | パーティション、ブートローダー、共有ライブラリ |
| [GNU/Unixコマンド](docs/03-gnu-unix-commands/README.md) | ファイル操作、検索、テキスト処理 |
| [デバイスとファイルシステム](docs/04-devices-filesystem/README.md) | マウント、権限、リンク |
| [シェルとスクリプト](docs/05-shell-script/README.md) | シェル、変数、パイプ、スクリプト |
| [ユーザー管理](docs/06-user-management/README.md) | ユーザー、グループ、所有権 |
| [ネットワーク](docs/07-network/README.md) | IP、名前解決、疎通確認 |
| [セキュリティ](docs/08-security/README.md) | 権限、sudo、基本的な防御 |

## 実習と復習

- [ファイル操作](labs/file-operations/README.md)
- [パーミッション](labs/permissions/README.md)
- [プロセス管理](labs/process/README.md)
- [ネットワーク](labs/network/README.md)
- [重要コマンド一覧](review/commands.md)
- [重要ポイント](review/important-points.md)
- [間違いノート](review/mistakes.md)

## 方針

- 実行例には、結果と確認方法も書く
- 危険なコマンドには注意書きを付ける
- 試験範囲や仕様はLPI-Japanの最新情報を別途確認する
