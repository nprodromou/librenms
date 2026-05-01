# LibreNMS — IFT 166 Lab 32 alternative

A minimal Docker stack for completing IFT 166 Lab 32 (Network Management) on
macOS or Linux. The original lab calls for ipMonitor or PRTG, both of which are
Windows-only.

The full lab walkthrough is in [`IFT166_Lab32.docx`](IFT166_Lab32.docx) in this
repo (your instructor may also distribute it directly). The other files in the
repo are:

- `compose.yml` — the five-container LibreNMS stack (db, redis, librenms,
  dispatcher, snmpsim)
- `.env.example` — copy to `.env` before first run
- `tools/build_lab32_docx.py` — the script that generates the lab `.docx` (for
  maintainers; students don't need this)

## Quick start

If you have git, clone:

```bash
git clone https://github.com/nprodromou/librenms.git
cd librenms
cp .env.example .env
# Edit compose.yml — replace "student" with your name in the YAML anchor at the top
docker compose up -d
```

If you don't, download
<https://github.com/nprodromou/librenms/archive/refs/heads/main.zip>,
double-click to extract, then `cd librenms-main` and run the same `cp` and
`docker compose up -d` steps.

Then open <http://localhost:8000> and follow the instructions in the lab `.docx`.
