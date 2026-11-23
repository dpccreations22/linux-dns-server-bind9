# Linux DNS Server on Ubuntu (BIND9)

Commands and example config files from the video, episode 2 of the **Fix It** series.

- [`commands.txt`](commands.txt): every command, in the order of the 7 steps
- [`named.conf.options`](named.conf.options): forwarders, locked to your network
- [`named.conf.local`](named.conf.local): the `home.arpa` zone
- [`db.home.arpa`](db.home.arpa): the zone file (SOA, NS and A records)

## Before you copy

- Replace `192.168.1.0/24`, `192.168.1.10` and the device addresses with **your own**.
- Use `home.arpa` (reserved for home networks, RFC 8375). Don't use `.local`.
- Full names in the zone file end with a **dot** (`ns1.home.arpa.`).
- Serial: today's date + a 2-digit counter (`2026112301`). Raise it by 1 on every edit.
- Always run `named-checkconf` and `named-checkzone` before restarting.

Tested on Ubuntu 22.04 and 24.04 (BIND 9.18).
