# Homelab Landing Page ([internal.eliodinino.com](https://internal.eliodinino.com))

A simple landing page for [my internally hosted services](https://github.com/ElioDiNino/Homelab).

## Linking to a Service

Add `?next=` with a service's subdomain to land there instead of the dashboard
once the connection succeeds. A path may follow the subdomain:

- <https://internal.eliodinino.com?next=grafana>
- <https://internal.eliodinino.com?next=grafana/d/abc123/my-dashboard>

The destination is always built from this page's own domain, so `next` cannot
point anywhere else. An unrecognised value falls back to the dashboard.
