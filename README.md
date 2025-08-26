# YouTube Video & Audio Downloader

This Python script allows you to download YouTube videos in different resolutions or as audio-only files. If the selected quality is only available as separate video and audio streams, the script automatically downloads both and merges them into a single file.

It provides:

* Automatic validation of YouTube links
* A choice of resolutions (excluding very low quality such as 144p)
* An audio-only option (`.m4a`)
* Automatic merging of adaptive streams using `moviepy`
* Simple command-line interaction

---

## Features

* ✅ Download progressive YouTube streams directly (video + audio)
* ✅ Download adaptive streams (video-only) and merge with audio
* ✅ Audio-only download option (`128kbps`)
* ✅ Automatic cleaning of video titles into safe file names
* ✅ Error handling for unavailable videos or invalid URLs

---

## Requirements

Install the required Python libraries before running the script:

```bash
pip install pytubefix moviepy requests
```

### Dependencies

<<<<<<< HEAD
* **pytubefix** – For accessing YouTube streams
* **moviepy** – For merging video and audio files
* **requests** – For checking video availability
=======
## Installation

1. **Clone the repository** (if applicable):
   ```bash
   git clone https://github.com/garcane/YouTube-MP4-Downloader-Pro.git
   cd YouTube-MP4-Downloader-Pro
   ```

2. **Install the required libraries**:
   ```bash
   pip install pytubefix moviepy requests
   ```

3. **Ensure FFmpeg is installed** (required by `moviepy`):
   - Download and install FFmpeg from [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html).
   - Add FFmpeg to your system's PATH.
>>>>>>> ca64dcd8c66ca01c8cca4d1ac8908e33b2849090

---

## Usage

1. Run the script:

```bash
python app.py
```

2. Paste a valid YouTube URL when prompted.
3. Choose a download quality from the list provided (e.g., `720p`, `1080p`, or `audio`).
4. The downloaded file will be saved in your current working directory.

### Example workflow

```
Paste YouTube URL: https://www.youtube.com/watch?v=example
URL check... PASS
Title: Example-Video
Available streams are: ['360p', '480p', '720p', '1080p', 'audio']
Enter download quality: 720p
Downloading progressive video stream at 720p...
Your video is ready!
Do you want to download another video? (1 for yes, 2 for no): 2
Ending the script.
```

---

## Output Files

* **Video files**: Saved as `.mp4`
* **Audio-only files**: Saved as `.m4a`
* **Merged files**: Saved as `[title]_merged.mp4`

Temporary files are removed automatically after merging.

---

## Notes

* The script trims mismatched video/audio durations to the shorter length when merging.
* Video titles are automatically cleaned (non-alphabetic characters removed and spaces replaced with hyphens).
* Only YouTube URLs are supported.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

---

## Acknowledgments

- [pytubefix](https://github.com/pytubefix/pytubefix) for YouTube video downloading.
- [moviepy](https://zulko.github.io/moviepy/) for video and audio merging.

---

Enjoy downloading YouTube videos with ease! 🎥🎶

---
