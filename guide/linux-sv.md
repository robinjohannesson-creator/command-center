# Command Center på Bazzite (och Docker)

Samma Command Center som på Windows, men för Linux. På Bazzite får du ett eget fönster i appmenyn, och appen körs i bakgrunden även när du inte är inloggad.

## Bazzite: installera

1. Öppna **Konsole** (appmenyn → System → Konsole).
2. Klistra in kommandot från nedladdningssidan (det börjar med `curl -fsSL`) och tryck Enter. Inget lösenord behövs: allt hamnar i din egen hemmapp.
3. Efter någon minut står det **Klart!** och Command Center öppnas i ett eget fönster.
4. Följ samma tio korta steg som i [Windows-guiden](sv.md#2-ställ-in-tio-korta-steg). Anteckningarna hamnar i **Dokument/Command Center**.

## Bra att veta

- **Nya versioner:** en rad överst i appen säger till. Klicka på den och sedan **UPPDATERA NU**. Datorn hämtar den nya versionen, fönstret visar "svarar inte än" en kort stund och kommer sedan tillbaka.
- **Mobilen:** som på Windows, skanna koden under **Inställningar → Mobilen**. Bazzite släpper igenom mobiler på hemnätet utan att du behöver göra något.
- **Säkerhetskopior till USB-minne:** sätt i minnet, öppna det en gång i filhanteraren, och välj det under **Inställningar → Säkerhetskopior**.
- **Tailscale** (borta hemifrån) finns redan i Bazzite. För att Command Center själv ska få slå på HTTPS-adressen: kör en gång i Konsole `sudo tailscale set --operator=$USER`.
- **Installera igen** (eller laga en trasig installation): kör samma kommando igen. Dina inställningar och anteckningar finns kvar.

## Ta bort

Appmenyn → **Avinstallera Command Center**. Den frågar samma sak som på Windows: behåll dina inställningar eller ta bort allt. Dina anteckningar och säkerhetskopior tas **aldrig** bort.

## Docker (server eller NAS)

1. Ladda ner `compose.yaml` från nedladdningssidan till en tom mapp.
2. Kör `docker compose up -d` i den mappen och öppna `http://<serverns adress>:3100/`.
3. **Gör inställningarna direkt:** tills lösenordet är satt kan vem som helst på nätet öppna sidan.
4. Uppdatera: `docker compose pull && docker compose up -d` (appen säger till när en ny version finns).

Data, anteckningar och säkerhetskopior hamnar i mapparna `data`, `notes` och `backups` bredvid `compose.yaml`.
