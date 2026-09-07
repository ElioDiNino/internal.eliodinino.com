# Homelab Landing Page ([internal.eliodinino.com](https://internal.eliodinino.com))

A simple landing page for [my internally hosted services](https://github.com/ElioDiNino/Homelab).

## Linking to a Service

Add `?next=` with a service's subdomain to land there instead of the dashboard
once the connection succeeds. The subdomain may be one or two levels deep, and
a path and query may follow it:

- <https://internal.eliodinino.com?next=service>
- <https://internal.eliodinino.com?next=service.staging>
- <https://internal.eliodinino.com?next=service/d/abc123/my-dashboard>
- <https://internal.eliodinino.com?next=service/d/abc123?from=now-6h&to=now>

Everything after `next=` belongs to the target, so it has to be the last
parameter on the link. The destination is always built from this page's own
domain, so `next` cannot point anywhere else. An unrecognised value falls back
to the dashboard.
