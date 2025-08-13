# 🖥️ PVE 自動アイドルシャットダウン設定

Proxmox VE (PVE) のサーバーを**アイドル時に自動でシャットダウン**させる設定手順です。  

---

## 🚀 スクリプトのダウンロードと設置

以下のコマンドをターミナルで実行してください。

```bash
sudo curl https://raw.githubusercontent.com/kyusumya/pve-login-idle-shutdown/refs/heads/main/pve-login-idle-shutdown.sh%20 | sudo tee /usr/local/bin/pve-login-idle-shutdown.sh
sudo chmod +x /usr/local/bin/pve-login-idle-shutdown.sh
```

## ⏰ cron で定期実行

次に、スクリプトを2時間ごとに自動で実行するように **cron** を設定します。

1. crontabを編集

```bash
sudo crontab -e
```

2. ファイルの最後に以下の行を追加

```bash
0 2 * * * /usr/local/bin/pve-login-idle-shutdown.sh
```
