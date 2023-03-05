Temporary infrastructure to manually test the `/setup` page.

Add something like this to `/etc/hosts`:

```
127.0.0.1       snipeit.local
```

Start the application behind a reverse proxy (Caddy), with:
```
docker-compose -f docker-compose_test.yml up
```

Then visit `https://snipeit.local` in the browser and ignore the SSL warning
(or trust the CA created by Caddy by installing the
`caddy/data/caddy/pki/authorities/local/root.crt` certificate file).
