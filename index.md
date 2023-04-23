---
title: "verified.hsim.dev"
---
# Verified Identities List

How to add:
1. Click [this link]({{ site.github.repository_url }}/new/main/_nip05) to create a new file in the [./_nip05](_nip05) folder.
1. File name should be in this format: `<your chosen name>.md`.
1. The content of this file must follow the template below.
1. Commit the new file into your own fork and make a new Pull Request on Github.
1. Send the PR link via nostr DM to [free-nip05@verified.hsim.dev](https://dsh.re/a9ff9) - `npub1hry9h6yld9lte58ldhmv0s5thdrpawet9v0suz365se6t7zgf78sq0t00c`.

```md
---
pubkey: "<your hex encoded pubkey>"
---
```

## Nostr [(nip05)](https://metadata.nostr.com/)

Contents of `.well-known/nostr.json`:

{%- assign nip05 = site.nip05 | where_exp: "doc", "doc.pubkey != nil" -%}

{% for doc in nip05 %}
  * [{{ doc.url | split: "/" | last | strip_html }}@{{ site.github.url }}](https://snort.social/p/{{ doc.pubkey | strip_html | url_encode }})
{% endfor %}

### Built with
- Google Domains
- Google DNSSEC
- Github Pages
