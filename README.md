# md_to_conf for Confluence protected by Cloudflare Access

## Usage

```
export CONFLUENCE_ORGNAME='YOUR_CF_ACCESS_PROTECTED_DOMAIN'

cloudflared access login https://$CONFLUENCE_ORGNAME > /dev/null         

export CONFLUENCE_PERSONAL_ACCESS_TOKEN=$(cloudflared access token -app=https://${CONFLUENCE_ORGNAME})

python3 ~/md_to_conf/md2conf.py YOUR_MARKDOWN_FILE_FULLPATH.md '~USERNAME' -l DEBUG
```

