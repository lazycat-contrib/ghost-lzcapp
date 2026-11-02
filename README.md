# Ghost (LazyCat LPK)

Professional publishing platform for blogs and newsletters.

- Upstream: https://github.com/TryGhost/Ghost
- Image: `library/ghost:6.73.0` (official Docker Hub image, mirror mode, digest-matched)
- License: MIT (full text in `content/licenses/LICENSE`)
- Containers: Ghost + MySQL 8.0

## Notes

- Version checked via the Docker Hub API (`ordering=last_updated`), not registry tags/list —
  the latter caps at 1000 entries and would have shown an older release.
- First visit redirects to `/ghost` setup wizard: site title, name, email, password.
  The admin is created there — no seeded credential.
- DB connection via Ghost's `database__*` env convention; password from a platform stable secret.
- `url` is set to the app domain so canonical links and the admin redirect work behind the proxy.
- Content on `/lzcapp/var/content`, database on `/lzcapp/var/mysql`.
- No mail service configured (subscription confirmations / password reset unavailable).
- Not yet verified on a real device.
