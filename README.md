# CVE-2023-2982
WordPress Social Login and Register (Discord, Google, Twitter, LinkedIn) &lt;= 7.6.4 - Authentication Bypass

Info
---
`
The WordPress Social Login and Register (Discord, Google, Twitter, LinkedIn) plugin for WordPress is vulnerable to authentication bypass in versions up to, and including, 7.6.4. This is due to insufficient encryption on the user being supplied during a login validated through the plugin. This makes it possible for unauthenticated attackers to log in as any existing user on the site, such as an administrator, if they know the email address associated with that user. This was partially patched in version 7.6.4 and fully patched in version 7.6.5.
`

`This exploit will crawl the website for any email addresses it can find and try them if an email address it not supplied.`

Requires
---
* Katana - `go install github.com/projectdiscovery/katana/cmd/katana@latest`
* Nuclei - `go install -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest`


Usage
---
```
usage: CVE-2023-2982.py [-h] -w WEBSITE_URL [-e EMAIL]

CVE-2023-2982.py

options:
  -h, --help            show this help message and exit
  -w WEBSITE_URL, --website_url WEBSITE_URL
                        Website URL
  -e EMAIL, --email EMAIL
                        Email
```
