# Cutter - Setup help

Everything you need to get **Cutter** running, step by step. If something goes wrong, check *Troubleshooting* at the end.

## What you need

- Windows 10 or Windows 11 (64-bit)
- ffmpeg and ffprobe on your PATH - `winget install Gyan.FFmpeg` (Windows) or download from ffmpeg.org

## Install and start

1. Download **`Cutter.exe`** from the [Releases page](../../releases) - or directly from the file list of this repository.
2. Put it anywhere you like, for example in its own folder. There is **no installer**.
3. Double-click it.
4. Windows may show a blue **SmartScreen** window ("Windows protected your PC"), because the file is not code-signed. Click **More info**, then **Run anyway**. Your antivirus may also scan the file for a few seconds on the first start.

## First start

1. Start `Cutter.exe` and click **Open file ▸** to pick a video.
2. Drag the timeline handles (or use the ±second buttons) to select the part you want.
3. Pick **WhatsApp** or **Discord** at the top for an automatic size-targeted export, or set a quality/resolution in *Settings* and press **EXPORT** for a plain trim.
4. Choose where to save - the export runs in the background, the sidebar tells you when it's done.

## Troubleshooting

**It says ffmpeg/ffprobe was not found**

Install it with `winget install Gyan.FFmpeg` and restart Cutter so it picks up the updated PATH.

**NVENC options do nothing / fail**

NVENC needs a supported NVIDIA GPU and driver. Switch the Codec dropdown to a CPU option (libx264/libx265) if you don't have one.

**The exported file is a bit over the limit**

The size math is an estimate; very short or already highly compressed clips can overshoot slightly. Nudge the target size a little lower and retry.

**Nothing happens when I double-click it**

Wait 10-20 seconds on the very first start (antivirus scan / first-time unpacking). If it still does not appear, right-click the file -> *Properties* -> tick *Unblock* -> *OK*, then start it again.

**SmartScreen or my antivirus complains**

The file is unsigned, which triggers warnings for every small tool. Use *More info* -> *Run anyway*. If your antivirus quarantines it, add the folder to its exclusions or re-download.

## Uninstall

Delete the `.exe`. If the program stored settings (see above), delete that folder too.

## Still stuck?

Open an **Issue** on this repository and tell me your Windows / Minecraft version and what you see (a screenshot helps).

---

Made by **dev:#2444** - [github.com/hash2444](https://github.com/hash2444)
