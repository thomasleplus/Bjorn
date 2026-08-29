# data

Runtime inputs and outputs for the [actions](../actions/). Most subfolders ship
empty (`.gitkeep`) and are filled while Bjorn runs.

- `input/dictionary/` — word lists (`users.txt`, `passwords.txt`) used by the
  protocol connectors.
- `output/` — results written by actions: `scan_results/`, `vulnerabilities/`,
  `crackedpwd/`, `data_stolen/`, `zombies/`.
- `logs/` — run logs.

Treat everything under `output/` as generated, sensitive artifacts.
