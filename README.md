# Default backend

All cloud solutions need in the end a "default backend", where all web traffic
that doesn't have a known destination ends up.

This happens for example when someone tries to open the direct IP instead of a
hostname of the Load Balancer.

In this case the "default backend" is called, and they are served a pretty 404
page.

Worth mentioning that this will also always result in an invalid certificate
error, as we only create certificates for the domains we serve.
