# Markdown to Outlook

## Deployment

- **URL**: `https://jorgemarti.com/markdown/`
- **Server**: `access826803726.webspace-data.io`
- **Credentials**: stored in `~/projects/jorgemarti.com/.env` (variables `USER`, `PASS`, `HOST`)
- **Protocol**: SFTP via `lftp`
- **Remote path**: `jorgemarti.com/markdown/`

### Upload command

```bash
source ~/projects/jorgemarti.com/.env
lftp -e "set sftp:auto-confirm yes; open -u $USER,$PASS sftp://$HOST; put -O jorgemarti.com/markdown/ /home/cockemc/projects/markdown-to-outlook/web/index.html; quit"
```
