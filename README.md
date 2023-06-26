# Bash scripts to create nginx sites proxied by Cloudflare

## Prerequisite:

- `sudo apt-get install jq` to install `jq` - a tool to parse json

## Instructions:

1. `git clone https://github.com/KhoiUna/cloudflare-nginx-dns-sh-scripts dns-scripts` at your `/home/<user>` directory
2. `sudo cp sample.config.json config.json` then `sudo nano config.json`. Configure `config.json` with your info
3. `sudo sh dns-scripts/create-site <your full site's domain name>`.
   - **Eg:** `sudo sh dns-scripts/create-site test.example.com`. This will run all the scripts to create your own site folder in `/var/www/test.example.com` and create `/etc/nginx/sites-available/test.example.com` symlink in `/etc/nginx/sites-enabled`
