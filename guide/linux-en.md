# Command Center on Bazzite (and Docker)

The same Command Center as on Windows, for Linux. On Bazzite you get its own window in the app menu, and the app keeps running in the background even when you're logged out.

## Bazzite: install

1. Open **Konsole** (app menu → System → Konsole).
2. Paste the command from the download page (it starts with `curl -fsSL`) and press Enter. No password needed: everything goes into your own home folder.
3. After a minute or so it says **Done!** and Command Center opens in its own window.
4. Follow the same ten short steps as in the [Windows guide](en.md#2-set-up-ten-short-steps). Your notes go in **Documents/Command Center**.

## Good to know

- **New versions:** a bar at the top of the app tells you. Click it, then **UPDATE NOW**. The PC fetches the new version; the window shows "not answering yet" for a moment and then comes back.
- **Phone:** as on Windows, scan the code under **Settings → Phone**. Bazzite lets phones on the home network through without any extra step.
- **Backups to a USB stick:** plug it in, open it once in the file manager, and pick it under **Settings → Backups**.
- **Tailscale** (away from home) comes with Bazzite. To let Command Center turn on its HTTPS address itself, run once in Konsole: `sudo tailscale set --operator=$USER`.
- **Reinstall** (or repair an install): run the same command again. Your settings and notes stay.

## Remove

App menu → **Uninstall Command Center**. It asks the same as on Windows: keep your settings or remove everything. Your notes and backups are **never** deleted.

## Docker (a server or NAS)

1. Download `compose.yaml` from the download page into an empty folder.
2. Run `docker compose up -d` there and open `http://<the server's address>:3100/`.
3. **Do the setup right away:** until the password is set, anyone on the network can open the page.
4. Update: `docker compose pull && docker compose up -d` (the app tells you when a new version is out).

Data, notes and backups go in the `data`, `notes` and `backups` folders next to `compose.yaml`.
