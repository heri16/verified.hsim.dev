---
title: "verified.hsim.dev"
---
# A free and anonymous NIP-05 ID registration service

### How to add / register:
1. Click [this link]({{ site.github.repository_url }}/new/main/_nip05) to create a new file in the [_nip05]({{ site.github.repository_url }}/tree/main/_nip05) folder
1. Input the file-name in this format: `<your nostr username>.md`
1. Copy and Edit the template below into the file content
1. Make a new Github Pull Request (PR) - commit the new file into your own fork
1. Share the Github Pull Request link via nostr DM to [npub1hry9h6yld9lte58ldhmv0s5thdrpawet9v0suz365se6t7zgf78sq0t00c](https://dsh.re/a9ff9)

### File Template:
```md
---
pubkey: "<your nostr hex-encoded pubkey>"
---
```


## Nostr Identities ([NIP-05](https://nostr.how/en/guides/get-verified#self-hosted))

Verified IDs in [.well-known/nostr.json]({{ site.github.url }}/.well-known/nostr.json):

{%- assign site_url_host = site.github.url | split: "://" | last | split: "/" | first -%}
{%- assign nip05 = site.nip05 | where_exp: "doc", "doc.pubkey != nil" -%}

{% for doc in nip05 %}
  * [{{ doc.url | split: "/" | last | strip_html }}@{{ site_url_host }}](https://snort.social/p/{{ doc.pubkey | strip_html | url_encode }})
{% endfor %}


## Built with
- **.DEV TLD** - [Preloaded HTTPS Strict Transport Security](https://hstspreload.org/?domain={{ site_url_host }})
- **Low-latency Anycast DNS** - [DNSSEC is enabled](https://dnsviz.net/d/{{ site_url_host }}/dnssec/)
- **Github Pages** - [Enforce HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)
