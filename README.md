## 🌐 Cloudflare DDNS Updater

This script automates updating your Cloudflare DNS A record when your public IP changes, keeping your domain accessible despite ISP IP changes.

### 🚀 Features

* Automatically detects your current public IP
* Compares it with your existing Cloudflare DNS record
* Updates the DNS A record if the IP has changed
* Sends notifications via Slack or Discord if configured
* Logs updates using the `logger` command for auditing

### 🛠️ Requirements

* Bash
* curl
* Cloudflare Global API Key or Scoped API Token
* Slack/Discord Webhook URLs (optional)

### 📌 Usage

1. Clone the repo:

   ```
   git clone https://github.com/mikecozier/cloudflare-ddns.git
   cd cloudflare-ddns
   ```
2. Edit the script with your Cloudflare credentials and domain info.
3. Make it executable:

   ```
   chmod +x cloudflare.sh
   ```
4. Run manually or set up a cron job for automated updates:

   ```
   */5 * * * * /path/to/cloudflare.sh >> /var/log/ddns.log 2>&1
   ```
