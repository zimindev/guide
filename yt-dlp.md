
# Mini Guide: Download Video without Audio using `yt-dlp`

This guide explains how to download videos using `yt-dlp` with the audio removed, making it ideal for use cases like video wallpapers.

## Prerequisites
1. Install `yt-dlp`. You can do this:
   
   ```bash
   sudo pacman yt-dlp
   ```
   ```bash
   sudo apt-get install yt-dlp
   ```
2. Install `ffmpeg`, as `yt-dlp` uses it for processing video files. On Linux, you can install it with:
   
   ```bash
   sudo pacman ffmpeg
   ```
      ```bash
   sudo apt-get install ffmpeg
   ```

## Commands

### Download Video and Remove Audio

For example download video command:
```bash
yt-dlp <URL>
```

### Download Video and Remove Audio
To download a video and strip the audio track, use the following command:
```bash
yt-dlp -f bestvideo[ext=mp4]+bestaudio --merge-output-format mp4 --remux-video mp4 --postprocessor-args "-an" <URL>
```

#### Explanation:
- **`-f bestvideo[ext=mp4]+bestaudio`**: Selects the best video quality with the specified extension (`mp4`) and adds audio (if needed for merging).
- **`--merge-output-format mp4`**: Ensures the final output is in `mp4` format.
- **`--remux-video mp4`**: Remuxes the video into `mp4` format without re-encoding.
- **`--postprocessor-args "-an"`**: Instructs `ffmpeg` to remove the audio track (`-an` flag).
- **`<URL>`**: Replace `<URL>` with the video link you want to download.

### Alternative: Download Video Without Audio Stream
If you only want to download the video stream directly without audio, use:
```bash
yt-dlp -f bestvideo[ext=mp4] <URL>
```

This command downloads only the best available video stream.

## Examples

### Example 1: Download a YouTube video without audio
```bash
yt-dlp -f bestvideo[ext=mp4] https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

### Example 2: Download and remove audio after merging
```bash
yt-dlp -f bestvideo[ext=mp4]+bestaudio --merge-output-format mp4 --remux-video mp4 --postprocessor-args "-an" https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

## Notes
- Ensure `ffmpeg` is properly installed, as it is required for post-processing operations.
- Use `--help` with `yt-dlp` to explore additional options and customizations.

## Resources
- [yt-dlp GitHub Repository](https://github.com/yt-dlp/yt-dlp)
- [ffmpeg Documentation](https://ffmpeg.org/documentation.html)
