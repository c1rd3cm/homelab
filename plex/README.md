# Plex

Using Ubuntu Server 

## Plex Installation
Open terminal and execute the following 2 commands
```bash
echo deb https://downloads.plex.tv/repo/deb public main | sudo tee /etc/apt/sources.list.d/plexmediaserver.list

curl https://downloads.plex.tv/plex-keys/PlexSign.key | sudo apt-key add -
```

Update the repository sources
```bash
sudo apt update
```

Install plex
```bash
sudo apt install plexmediaserver
```

Continue installation from a web browser using `http://<IP_ADDRESS>:32400/web`

### Accessing web installation from a different network or subnet
1. Open a Terminal window or your command prompt
2. Enter the following command (substituting the IP address of your Plex Media Server as appropriate):
```bash
ssh -L 8888:127.0.0.1:32400 ip.address.of.server
```
3. Open a browser window
4. Type http://127.0.0.1:8888/web into the address bar
5. The browser will connect to the server as if it were local and load Plex Web App

You can read more details from Plex support [here](https://support.plex.tv/articles/account-requires-password-reset/#toc-2).

## Hardware acceleration

Install latest kernel:
```bash
sudo apt install --install-recommends linux-generic-hwe-24.04
```
