# 🖥️ PVE 自動アイドルシャットダウン設定

Proxmox VE (PVE) のサーバーを**アイドル時に自動でシャットダウン**させる設定手順です。  

---

## 🚀 スクリプトのダウンロードと設置

以下のコマンドをターミナルで実行してください。

```bash
sudo curl https://raw.githubusercontent.com/kyusumya/pve-login-idle-shutdown/refs/heads/main/pve-login-idle-shutdown.sh%20 | sudo tee /usr/local/bin/pve-login-idle-shutdown.sh
sudo chmod +x /usr/local/bin/pve-login-idle-shutdown.sh

## ⏰ cron で定期実行

ターミナルで以下を実行して、cron に登録しましょう。

```bash
sudo crontab -e
