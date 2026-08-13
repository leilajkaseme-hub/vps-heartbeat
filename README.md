# vps-heartbeat

External uptime check for the self-hosted analytics box. A scheduled GitHub Action
pings the health endpoint every ~10 minutes from GitHub's servers (outside the VPS,
so it catches a full-box outage) and sends a phone alert if it is not healthy.

Config lives in repository secrets: `HEARTBEAT_URL`, `NTFY_URL`. Nothing sensitive
is committed here.
