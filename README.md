# takeoverOneLiner
Subdomain takeover one liner
# One-liner
`cat takeover.txt | xargs -n 1 -I {} sh -c 'echo -e "\033[34m{}:\033[0m \033[32m$(dig +short CNAME {})\033[0m"'`
replace `takeover.txt` with the discoverd subdomains you found
## Alternatively:
`assetfinder target.com | xargs -n 1 -I {} sh -c 'echo -e "\033[34m{}:\033[0m \033[32m$(dig +short CNAME {})\033[0m"'`
