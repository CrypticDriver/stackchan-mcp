# Security Policy

## Supported Branch

Security fixes are handled on the default branch. This project does not publish
long-term support branches.

## Reporting A Vulnerability

Do not open a public issue for a vulnerability that exposes credentials, private
network details, live-device access, or remote execution paths.

Report privately through GitHub Security Advisories when available, or contact
the repository owner directly. Include:

- Affected commit or release.
- Reproduction steps.
- Impact and whether a live Stack-chan device or public tunnel is involved.
- Any logs with tokens, local IPs, voice transcripts, and tunnel hostnames
  redacted.

## Public Exposure

The firmware HTTP API is intended for a trusted LAN. Do not expose the CoreS3
device directly to the internet.

The MCP HTTP helper starts only the local MCP server by default. Public
cloudflared tunnel startup requires `STACKCHAN_ENABLE_PUBLIC_MCP_TUNNEL=1`.
Treat any public MCP URL as sensitive operational infrastructure.

Voice upload endpoints should use `STACKCHAN_VOICE_UPLOAD_TOKEN` whenever they
are reachable from another device or through a tunnel.

## Dependency Updates

Dependency updates follow the repository cooldown and pinning policy in
`CONTRIBUTING.md`. Security updates may bypass cooldown when the advisory and
verification are documented in the PR or commit.
