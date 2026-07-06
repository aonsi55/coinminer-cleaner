# coinminer-cleaner
Find and evict the hidden cryptominer that's cooking your laptop — and undo the Windows Defender damage it left behind.


# Cryptominer Malware Cleaner — Read Me First

A free, no-install tool that finds and removes a sneaky **cryptocurrency-mining virus** that hides inside Windows, wrecks your battery, overheats your laptop, and secretly uses your computer to make money for a stranger. It also repairs the damage this virus does to Windows Defender (your built-in antivirus).

If your laptop is **always hot, the fan is always loud, and the battery dies fast** — but nothing looks wrong — this tool is worth running.

---

## Is this me? (Signs of infection)

You might have this exact malware if you notice several of these:

- The laptop runs **hot and the fans are loud even when you're barely doing anything**.
- The **battery drains extremely fast** (sometimes only 20–40 minutes).
- The computer feels **sluggish**, and the CPU sits high for no reason.
- In Task Manager you see a process with a **random name like `u950780.exe`**.
- Windows Security says **"This setting is managed by your administrator"** — even though it's your own personal PC and there is no administrator.
- You can't open **Virus & threat protection**, or Tamper Protection is switched off and greyed out.

This kind of infection usually arrives through **cracked or "free" versions of paid software, game cheats/mods, or fake downloads**.

---

## What the tool does

1. **Scans** your PC for the specific fingerprints of this malware (hidden mining files, the "watchdog" that keeps bringing it back, and the changes it made to Windows Defender).
2. **Shows you exactly what it found** and then **stops and waits**. It changes nothing until you type `REMOVE` and press Enter.
3. **Backs everything up first**, then removes it:
   - Malware files are copied to a **quarantine** folder (not just deleted), so nothing is lost forever.
   - Any registry settings it changes are **exported to backup files first**.
4. **Repairs Windows Defender** — removes the malicious "ignore these folders" rules, deletes the fake "managed by administrator" lockdown, and turns real-time protection back on.
5. **Writes a full log** of everything it did.

All backups and the log are saved to a new folder on your **Desktop** called `MinerCleanup_` followed by the date and time.

---

## How to run it (step by step)

1. Save `MinerMalwareCleaner.cmd` somewhere easy, like your Desktop.
2. **Right-click** it and choose **"Run as administrator."**
   - If you forget, it will ask for admin permission itself — click **Yes**.
   - If Windows SmartScreen warns you, click **More info → Run anyway** (this happens with any small script; the file is plain text you can open and read in Notepad first).
3. A black window opens and lists what it found. **Read it.**
4. If threats are found, it asks you to type **`REMOVE`** to clean, or anything else to just exit without changes.
5. When it finishes, it shows a summary and a short list of final steps to do yourself.

> Tip: You can open the `.cmd` file in Notepad to read exactly what it does before running it. Nothing is hidden.

---

## Important: what it CANNOT do

- **It can't turn Tamper Protection back on for you.** Microsoft blocks scripts from doing that on purpose (it's a good thing). You must flip it on yourself: **Windows Security → Virus & threat protection → Manage settings → Tamper Protection → On.**
- **It's a targeted cleaner, not a full antivirus.** After running it, also do a **Full scan** and an **Offline scan** in Windows Security (Scan options).
- **On work/company laptops** it will *not* change Defender settings, because on those machines a real IT department may have set them on purpose.

---

## After cleaning — please do these

1. **Turn Tamper Protection ON** (see above) so nothing can disable Defender again.
2. **Run a Full scan, then an Offline scan** in Windows Security.
3. **Reboot and run the tool again** if it said any file was "locked."
4. **Change your important passwords** (email, banking, social media) — and do it from a **different, trusted device**. This malware could run attacker commands, so treat passwords you typed on the infected PC as exposed. Turn on **two-factor authentication** everywhere you can.
5. **For total peace of mind:** back up your personal files (documents, photos — not programs) and do a **clean reinstall of Windows**. After a long infection, that's the only 100% guarantee it's gone.

---

## How to stay safe going forward

- **Never install cracked / pirated / "free" versions of paid software or game cheats.** This is the #1 way this infection spreads.
- **Always download software from its official source.**
- Keep **Windows Defender's Tamper Protection ON** and check its **exclusions list** is empty.
- Occasionally open **Task Manager** and look for unknown, random-named processes using lots of CPU.
- Remember: **"managed by your administrator" on a personal PC is not normal — it's a warning sign.**

---

*This tool targets one specific miner family and repairs the Defender damage it causes. It is provided as-is to help people recover. It is not a replacement for a reputable antivirus or, in serious cases, a clean Windows reinstall.*
