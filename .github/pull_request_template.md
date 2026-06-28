## What changed

-

## Checks run

- [ ] `uv run ruff check .`
- [ ] `uv run pytest`
- [ ] `cd firmware && pio test -e native`
- [ ] `cd firmware && pio run -e m5stack-cores3`
- [ ] `cd firmware && pio check -e m5stack-cores3 --severity=high --fail-on-defect=high`

## Hardware impact

- [ ] No live-device behavior changed
- [ ] Device behavior changed and was tested on hardware
- [ ] HTTP/MCP contract changed and docs/tests were updated

## Safety notes

- [ ] No `.env`, API keys, Wi-Fi credentials, public tunnel URLs, or local device IPs were committed
- [ ] No live-device endpoint that consumes state, such as `GET /audio`, was used unintentionally
