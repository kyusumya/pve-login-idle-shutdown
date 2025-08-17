# 🖥️ PVE 自動アイドルシャットダウン設定

Proxmox VE (PVE) のサーバーを**アイドル時に自動でシャットダウン**させる設定手順です。  

---

## 🚀 スクリプトのダウンロードと設置

以下のコマンドをターミナルで実行してください。

```bash
sudo curl https://raw.githubusercontent.com/kyusumya/pve-login-idle-shutdown/refs/heads/main/pve-login-idle-shutdown.sh | sudo tee /usr/local/bin/pve-login-idle-shutdown.sh
sudo chmod +x /usr/local/bin/pve-login-idle-shutdown.sh
sudo curl https://raw.githubusercontent.com/kyusumya/pve-login-idle-shutdown/refs/heads/main/pve-login-idle-shutdown.service | sudo tee /etc/systemd/system/pve-login-idle-shutdown.service
sudo curl https://raw.githubusercontent.com/kyusumya/pve-login-idle-shutdown/refs/heads/main/pve-login-idle-shutdown.timer | sudo tee /etc/systemd/system/pve-login-idle-shutdown.timer
sudo systemctl enable --now pve-login-idle-shutdown.timer
```
