# Project: Installing Windows 11 on Nina's new ASUS Vivobook

## Rules for Claude in this project
- The user is Alex. Reply in Russian, informal ("ты").
- **Every answer must be appended to `README.md`** (section "Журнал вопросов и ответов") BEFORE replying in chat. Alex's son may exhaust tokens at any moment; the file is the durable record.
- Each README entry starts with a timestamp `_YYYY-MM-DD HH:MM_` (use `date '+%Y-%m-%d %H:%M'` in Bash).
- Ask Alex questions **one at a time**.
- README.md must contain only things related to the Windows installation. Off-topic answers (chit-chat, Apple vs ASUS, AI models, etc.) go to chat only, not to the file.
- Alex calls the Claude model "Сказка" (Skazka, "Fable").

## Hardware facts
- ASUS Vivobook, exact model not yet known (sticker on the bottom not checked). Serial number: W6N0CV00X099236.
- Shipped **without OS** (MyASUS in UEFI Dashboard on boot).
- SSD 512 GB (476.9 GB shown unallocated), was completely empty.
- Fans ran at full speed in UEFI (normal without OS drivers; fixed later via MyASUS app / Fn+F).
- Unknown whether the screen is touch; check in Windows: Settings → System → About → "Pen and touch".

## Progress so far (session 1, 2026-10-25)
1. Bootable USB with Windows 11 was prepared by Alex (done before this session).
2. Booted from USB via Esc on power-on. Installer loaded fine.
3. Chose: language Russian, "I don't have a product key", edition **Windows 11 Pro** (activation key later must be a Pro key), accepted license, Custom install, selected unallocated space 476.9 GB.
4. Copying files 0→100%, first reboot (USB removed), "Installing 41%", "Не выключайте компьютер", reboot, "Подождите...", then **sound appeared = OOBE (first-time setup) started.**
5. **Current position:** at the very beginning of OOBE (country/region screen or just before it).
6. Alex was about to move the Ethernet cable from the desktop PC to the laptop, so the laptop will have wired internet for OOBE.

## Pending decision
- **Local account vs Microsoft account** — Alex will decide when the "Let's connect you to a network" screen appears. For a local account: on that screen press Shift+F10 and run `start ms-cxh:localonly`. Reference text already written in README.md.

## Next steps (OOBE)
1. Country: Россия → Да. 2. Keyboard: Russian → Да, second layout skip.
3. Network screen (wired cable connected, should pass automatically) — decision point above.
4. Updates check, possible reboot. 5. PC name (e.g. "Nina"). 6. "For personal use".
7. Sign in to Microsoft account or create local user. 8. PIN. 9. Privacy screens: turn all off → Accept. 10. Skip Office/Game Pass/OneDrive offers.

## After OOBE (README Step 4)
- Windows Update several times until "You're up to date" (fixes fan noise, brings most drivers).
- ASUS support site → enter exact model → drivers + MyASUS app. Set fan mode (Whisper) in MyASUS.
- Activate Windows 11 Pro with a key: Settings → System → Activation.
- Install browser, 7-Zip, office. Check Device Manager for missing drivers; test sound, camera, touchpad, Wi-Fi, brightness.

## Files
- `README.md` — the human-readable log for Alex (Russian). Keep appending there.
- Full unredacted backup of an earlier README version (with off-topic entries) is in the session scratchpad; not important.

## Session 1 ended 2026-10-25 ~14:00
- Repo published: https://github.com/veretennikovalexey/nina (SSH remote `git@github.com:veretennikovalexey/nina.git`, branch `main`).
- Alex is switching to a MacBook (Wi-Fi) for the next session; the Ethernet cable moves to the laptop.
- Alex likes to run shell commands himself from the Claude Code prompt via the `!` prefix (practising git). Offer that instead of running git for him unless asked.
- Laptop state when session ended: Windows 11 Pro installed, sitting at the start of OOBE (country/region screen). Next: walk through OOBE (see "Next steps" above), decide local vs Microsoft account at the network screen.
- Keep committing and pushing README.md after each entry so the Mac can pull the latest.
