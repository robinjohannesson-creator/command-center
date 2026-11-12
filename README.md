# Command Center

*English below.*

Din egen lilla startsida på datorn: väder, att göra, inköpslista, påminnelser till mobilen och dina anteckningar. Allt stannar på din dator.

## Ladda ner

**[Senaste versionen → CommandCenter-Setup-….exe](../../releases/latest)** (Windows 10/11, 64-bit)

Så installerar och ställer du in den: **[guiden](guide/sv.md)** (ungefär tio minuter).

Windows varnar "Windows skyddade datorn" eftersom programmet inte är signerat med ett köpt certifikat. Klicka **Mer information → Kör ändå**.

## Bazzite (Linux)

Öppna **Konsole** och klistra in:

```
curl -fsSL https://github.com/robinjohannesson-creator/command-center/releases/latest/download/install.sh | sh
```

Command Center hamnar i appmenyn med ett eget fönster. Mer i **[Linux-guiden](guide/linux-sv.md)** (även Docker för en server eller NAS).

## Nya versioner

Command Center kollar själv en gång om dagen och säger till i appen när en ny version finns. Klicka **UPPDATERA NU**, så tar datorn en säkerhetskopia och installerar den.

Du kan också ladda ner den nya installationsfilen härifrån och köra den. Den installerar över den gamla och behåller allt.

Bredvid varje installationsfil finns en `.sha256`-fil med dess kontrollsumma.

---

# Command Center (English)

Your own small start page on your PC: weather, to-do, shopping list, reminders to your phone and your notes. Everything stays on your PC.

**[Latest version → CommandCenter-Setup-….exe](../../releases/latest)** (Windows 10/11, 64-bit) · **[Guide](guide/en.md)**

Windows says "Windows protected your PC" because the program isn't signed with a bought certificate: click **More info → Run anyway**.

**New versions:** Command Center checks once a day and tells you in the app; **UPDATE NOW** takes a backup and installs it. Running a newer installer by hand also works and keeps everything.

**Bazzite (Linux):** open Konsole and run `curl -fsSL https://github.com/robinjohannesson-creator/command-center/releases/latest/download/install.sh | sh` · **[Linux guide](guide/linux-en.md)** (Docker too).

This repo holds the installers only.
