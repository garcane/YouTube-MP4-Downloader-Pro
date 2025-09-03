# YouTube Video & Audio Downloader

This Python script allows you to download YouTube videos in different resolutions or as audio-only files.
If adaptive video and audio streams are downloaded separately, the script automatically merges them into a single MP4 file using **MoviePy**.

---

## Features

* ✅ Validate YouTube URLs before downloading
* ✅ Choose from available resolutions (e.g. 360p, 720p, 1080p)
* ✅ Download audio-only files in `.m4a` format
* ✅ Merge separate video and audio streams into a single `.mp4` file
* ✅ Automatically cleans up temporary files after merging
* ✅ Simple interactive CLI interface

---

## Requirements

Make sure you have the following installed:

* Python **3.8+**
* [pytubefix](https://pypi.org/project/pytubefix/) (YouTube video downloader library)
* [moviepy](https://pypi.org/project/moviepy/) (for merging video & audio)
* [requests](https://pypi.org/project/requests/)

You can install all dependencies with:

```bash
pip install pytubefix moviepy requests
```

---

## Usage

1. Clone or download this repository.
2. Run the script:

```bash
python app.py
```

3. When prompted:

   * Paste a valid YouTube URL (`https://www.youtube.com/...` or `https://youtu.be/...`)
   * Select your desired download quality from the list (e.g. `360p`, `720p`, `1080p`, or `audio`)
   * The script will download and save the file in the current working directory.

4. After completion, you’ll be asked if you want to download another video.

---

## Example

```
Paste YouTube URL: https://www.youtube.com/watch?v=dQw4w9WgXcQ
URL check... PASS
Title: Rick-Astley-Never-Gonna-Give-You-Up
Gathering available streams...
Available streams are: ['360p', '480p', '720p', '1080p', 'audio']
Enter download quality: 720p
Downloading progressive video stream at 720p...
Your video is ready!
Do you want to download another video? (1 for yes, 2 for no):
```

---

## Output

* **Video files**: Saved as `title.mp4` (or `title_merged.mp4` if merging was required).
* **Audio files**: Saved as `title.m4a`.
* **Temporary files**: Cleaned up automatically after merging.

---

## Notes & Limitations

* ⚠️ Only works with **publicly available** YouTube videos.
* ⚠️ Some videos may not offer all resolutions or audio streams.
* ⚠️ Download speed and availability depend on YouTube’s servers.
* ⚠️ Merging can be slow for long/high-resolution videos.
* ⚠️ For best performance, install **FFmpeg** (MoviePy will use it if available).

---

## Legal Disclaimer

This script is for **personal use only**.
Downloading copyrighted videos without permission may violate **YouTube’s Terms of Service** and applicable copyright laws.
The authors assume no liability for misuse.

---

Would you like me to also add a **Dockerfile + instructions** so you can run this script in a containerized environment (avoiding local Python setup issues)?
