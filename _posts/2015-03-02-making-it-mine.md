---
layout: post
title: www.YOU.com
excerpt: www.YOU.github.io works great but why not www.YOU.com?
---
{{ page.excerpt }}
Buy a domain name from a registrar.
I used [GoDaddy](https://www.godaddy.com).
On the godaddy site find Domains > Manage my domains > CName (Alias).
Configure the Host: `www` to `Points To` YOU.github.io

Here is a snapshot of mine:
![Go Daddy cname screenshot](/assets/godaddycname.png)
This can take a while so be patient.

Do not forget to commit a CNAME file to your site that has the contents `YOU.com`

See:

- [Tips for configuring a CNAME record with your DNS provider](https://help.github.com/articles/tips-for-configuring-a-cname-record-with-your-dns-provider/)
- [GitHub Pages: setting up custom domain](http://stackoverflow.com/questions/23097397/github-pages-setting-up-custom-domain)
