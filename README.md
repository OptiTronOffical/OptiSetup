[![IMG-20261031-052052.jpg](https://i.postimg.cc/prmDV6mn/IMG-20261031-052052.jpg)](https://postimg.cc/BPG8MNcq)
[![Screenshot-2026-10-31-05-26-39.png](https://i.postimg.cc/pT2CvCQw/Screenshot-2026-10-31-05-26-39.png)](https://postimg.cc/jWFPQzFc)

# ps4 torrent client — Easy Setup README

NOTE: the full torrents library causes crashes, put the torrents folder in the supplied zip somewhere safe and only put on the torrents you want at the time

**Credits**
- **Original ps4torrent project:** **sergiopoverony**
  - https://github.com/sergiopoverony/ps4torrent
  - https://github.com/sergiopoverony/ps4torrent_client
- **2,600-game library:** supplied by **optitronoffical**

> **Testing note:** This has been tested only as far as **running and downloading on a PS4 Pro on firmware 13.52**. No further testing has been done. Use at your own risk.

---

## What the supplied `data.zip` contains

The `data.zip` I supply already contains everything in the **correct folder structure**:

- the **payload**
- the **PKG app**
- the **2,600-game library** supplied by **optitronoffical**

You do **not** need to rearrange or rename anything. Just extract it and copy the `data` folder to the HDD root.

---

## 1. Install the library / files

1. Download the supplied **`data.zip`**.
2. Extract it.
3. Copy the extracted **`data`** folder to the **root of the PS4 HDD**.
   - The HDD root should contain a folder named `data`.
   - Do not put it inside another subfolder.
4. This adds the **2,600-game library supplied by optitronoffical**, plus the payload and PKG app in the correct structure.

---

## 2. Load the payload

You can load the payload either manually or by using GoldHEN's built-in tools. The methods below assume you are using a recent version of GoldHEN (v2.4b18.10 or later), which includes the **Payload LaunchPad** and **AutoRun** features.

### Option A: Use GoldHEN Payload LaunchPad (Recommended)

GoldHEN's **Payload LaunchPad** lets you load ELF and BIN payloads directly from an on-screen menu, with no external tools needed.

1.  **Prepare the payload folder:** On your USB drive (or the PS4's internal HDD), create a folder named **`payloads`**.
2.  **Add the payload:** Place the `ps4torrentd.elf` payload file (from the `data` folder you extracted) into this **`payloads`** folder.
    - *Optional:* To give the payload a custom icon in the menu, place a PNG image in the same folder with the exact same name as the payload, plus `.png` (e.g., `ps4torrentd.elf.png`).
3.  **Launch the payload:**
    - Open the GoldHEN menu on your PS4.
    - Go to the **Utilities** menu and select **Payload LaunchPad**.
    - Select the `ps4torrentd.elf` file from the list to load it.

### Option B: Set the payload to Autoload

GoldHEN's **AutoRun** feature can automatically load the payload every time GoldHEN is activated.

1.  **Place the payload:** Ensure the `ps4torrentd.elf` payload is in the **`payloads`** folder on your USB drive or the PS4's internal HDD, as described in Option A.
2.  **Enable AutoRun:** In the GoldHEN menu, go to the **Utilities** section and find the **AutoLoader** option. From there, you can select the payload you want to run automatically at startup.
    - Once set, the payload will load each time GoldHEN starts.

### Option C: Manual load via BinLoader (Alternative)

If you prefer to send the payload from a computer or phone:

1.  Ensure GoldHEN's **BinLoader** server is running on your PS4 (it listens on **port 9090** by default).
2.  Use a BinLoader-compatible payload sender on a device connected to the same network to send the `ps4torrentd.elf` file to your PS4's IP address on port **9090**.

---

## 3. Open the PKG app

Once the payload is loaded (or running via AutoRun), open the **ps4torrent PKG app**.

From the app you can:
- browse/use the supplied library
- start downloads
- pause/resume torrents
- check progress
- manage torrents with the controller

Controller basics:
- **D-Pad** — select
- **Cross** — pause/resume
- **Triangle** — delete
- **Options** — shut down the payload

---

## 4. Optional: use the Web UI

Once the payload is running, open this in a browser on the same network:

```text
http://<YOUR_PS4_IP>:8787/
```

From the Web UI you can add torrents, pause/resume, check progress, and adjust upload/seeding settings.

---

## Final credits

- **Original ps4torrent project:** **sergiopoverony**
- **2,600-game library:** **optitronoffical**
- **Testing:** only running/downloading on **PS4 Pro 13.52**; no further testing has been done.
