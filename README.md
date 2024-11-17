# TakeoverOneLiner
Subdomain takeover one liner
# One-liner
`cat takeover.txt | xargs -n 1 -I {} sh -c 'cname=$(dig +short CNAME {}); if [ -n "$cname" ]; then echo -e "\033[34m{}:\033[0m \033[32m$cname\033[0m"; fi'`


replace `takeover.txt` with the discoverd subdomains you found
## Alternatively:
`assetfinder target.com | xargs -n 1 -I {} sh -c 'cname=$(dig +short CNAME {}); if [ -n "$cname" ]; then echo -e "\033[34m{}:\033[0m \033[32m$cname\033[0m"; fi'`
