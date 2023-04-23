---
title: "verified.hsim.dev"
---
# Verified Identities List

## Nostr [(nip05)](https://metadata.nostr.com/)

Contents of `.well-known/nostr.json`:

{% assign names = site.data.nostr.names %}

{% for name in names %}
1. **{{ name[0] }}**: `{{ name[1] }}`
{% endfor %}



