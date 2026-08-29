# actions

The pluggable "action" modules that Bjorn's [`orchestrator`](../orchestrator.py)
schedules and runs. Each file defines one action class with a common interface,
so new capabilities are added by dropping a module here.

- `scanning.py`, `nmap_vuln_scanner.py` — network host/port discovery and Nmap
  vulnerability scanning.
- `*_connector.py` (`ssh`, `ftp`, `smb`, `rdp`, `telnet`, `sql`) — per-protocol
  connection/credential-testing modules (use the word lists in
  [`../data/input/dictionary/`](../data/)).
- `steal_files_*.py`, `steal_data_sql.py` — data-collection actions for each
  protocol.
- `IDLE.py` — the do-nothing/rest state; `log_standalone*.py` — logging helpers.

This is a security-testing tool; only run it against systems you are authorized
to test. See the [root README](../README.md) for the project overview.
