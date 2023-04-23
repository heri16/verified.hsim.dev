---
title: "verified.hsim.dev"
---
# Verified Identities List

## Nostr [(nip05)](https://metadata.nostr.com/)

Contents of `.well-known/nostr.json`:

{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}]({{ repository.html_url }})
{% endfor %}

<ol>
{% for name in site.data.nostr.names %}
  <li><strong>{{ name[0] }}</strong>: <code>{{ name[1] }}</code></li>
{% endfor %}
</ol>
