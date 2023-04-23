---
title: "verified.hsim.dev"
---
# Verified Identities List

## Nostr [(nip05)](https://metadata.nostr.com/)

Contents of `.well-known/nostr.json`:

{% assign names = site.data.nostr.names %}

{% for name_key, name_value in names %}
1. **{{ name_key }}**: `{{ name_value }}`
{% endfor %}


