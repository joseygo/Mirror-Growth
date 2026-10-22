# Mirror

A database-backed dashboard for growth analysis: point Mirror at your MySQL /
PostgreSQL / StarRocks and instantly get order tracking, new-user metrics,
user profiles and segmentation — **no SQL, no dependencies**.

## Download & run (Windows 10 / 11)

1. Get the latest `mirror.exe` from the
   [Releases](../../releases) page — single file, no installer.
2. Double-click it. Your browser automatically opens the connection page at
   `http://127.0.0.1:8765`.
3. Enter your database address — that is all it takes to see the dashboards
   (connect **read-only**; Mirror never writes to your database).

## Privacy — nothing ever leaves your machine

- Mirror connects **only** to your own database, using connection strings you
  enter yourself.
- The connection is **strictly read-only** — Mirror never writes a single row
  to your business database.
- There is **no upload pipeline at all**: no telemetry, no CDN, no analytics,
  no remote server — the binary contains nothing that phones home.
- All derived metrics, session state and preferences stay in local storage on
  your own computer.

## Requirements

- Windows 10 / 11 (64-bit)
- A database: MySQL 5.7+ or PostgreSQL 12+, with a read-only account

## License

© Josey. Mirror is distributed as a free executable for personal and
internal business use; decompiling, repackaging or commercial redistribution
is not permitted.
