---
title: "verified.hsim.dev"
---
# Verified Identities List

## Nostr [(nip05)](https://metadata.nostr.com/)

Contents of `.well-known/nostr.json`:

{% assign names = site.data.nostr.names %}

<ol>
{% for name in names %}
  <li><strong>{{ name[0] }}</strong>: <code>{{ name[1] }}</code></li>
{% endfor %}
</ol>
