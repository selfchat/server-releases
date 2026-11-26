# selfchat server releases

Downloads of **selfchat-server**, the mailbox server: it holds your
messages while your devices are off, and only ever stores encrypted data.

Each `server-vX.Y.Z` release has:

- static Linux binaries for x86-64 and ARM64 (a Raspberry Pi 3 or newer,
  most NAS boxes and servers), with checksums;
- `install.sh`, the one-command installer, and the systemd service;
- `docker-compose.yml`.

The Docker image is `ghcr.io/selfchat/server`, for x86-64 and ARM64.

The easiest way to set one up is from the app: **Settings → Mailbox → Add
a mailbox server** gives you a command to paste on the server. Each
release's notes are the setup guide, for a Raspberry Pi, a NAS, a rented
server or Docker.

The app's own downloads are in
[selfchat/client-releases](https://github.com/selfchat/client-releases).

Releases are built here from the selfchat-server source by
[the release workflow](.github/workflows/release.yml).

## Community server

**selfchat-community**, the community server, is released here too, as
`community-vX.Y.Z` releases: static Linux binaries for x86-64 and ARM64
with checksums, `docker-compose.yml` and `docker-compose.postgres.yml`.
Its Docker image is `ghcr.io/selfchat/community`, for x86-64 and ARM64.

In the app, **Create a community → Your own server** shows what to paste
on the server. Community releases are built from the selfchat-community
source by [the community release workflow](.github/workflows/community-release.yml),
and are never marked as this repository's latest release, so the
mailbox installer link keeps pointing at the newest server.
