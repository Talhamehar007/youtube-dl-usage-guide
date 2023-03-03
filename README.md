# youtube-dl-usage-guide
A comprehensive guide to using youtube-dl and yt-dlp for downloading videos and audio from YouTube and other video-sharing sites, including installation instructions and detailed usage examples.


# How to Download youtube Videos using youtube-dl

## Table of contents

- [What us youtube-dl](#what-is-youtube-dl)
- [Installing youtube-dl](#installing-youtube-dl)
  - [Windows](#windows)
  - [MacOS](#macos)
  - [Linux](#linux)
- [Installing yt-dlp](#installing-yt-dlp)
  - [Windows](#on-windows)
  - [MacOS/Linux](#on-macoslinux)
- [Usage](#usage)
  - [Basic Usage](#basic-usage)
  - [Downloading Audio Files](#downloading-audio-only-mp3)
  - [Downloading Specific Formats](#downloading-specific-formats)
  - [Downloading a Playlist](#downloading-a-playlist)
  - [Downloading with Custom Filename](#downloading-with-custom-filename)
  - [Other Options](#other-options)
- [Conclusion](#conclusion)

---

YouTube is a popular video-sharing platform that millions of people use every day. Sometimes, you may want to download a video from YouTube for offline viewing, to save for later or share with someone who doesn't have an internet connection. YouTube itself doesn't provide an easy way to download videos, but there are several third-party tools that you can use to do so. Two of the most popular tools for downloading YouTube videos are youtube-dl and yt-dlp.

## What is youtube-dl?

youtube-dl is a command-line program for downloading videos from YouTube and other video-sharing websites. It's a free and open-source tool that runs on Windows, macOS, and Linux. It's very powerful and can download videos in various formats and resolutions, including 4K and 8K.

## Installing youtube-dl

### Dependencies

youtube-dl requires `ffmpeg` or `avconv to be installed on your system to download and process videos. These are multimedia frameworks that allow youtube-dl to convert videos to different formats and resolutions. If you don't have ffmpeg or avconv installed, you'll see an error message when you try to download a video.

Jump to [Installing Dependencies](#installing-dependencies-for-youtube-dl-and-yt-dlp) for detailed guide.

### Windows

1. Download the youtube-dl executable from the [official website](https://ytdl-org.github.io/youtube-dl/download.html).
2. Save the executable file in a directory on your computer, such as `C:\Program Files\youtube-dl`.
3. Open a command prompt in the directory where you saved the executable file.
4. Type the following command to verify that youtube-dl is working: `youtube-dl --version`.

### macOS

1. Install Homebrew if you don't already have it. Open a Terminal window and type the following command:

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. Once Homebrew is installed, run the following command to install youtube-dl:

   ```bash
   brew install youtube-dl
   ```

3. Type the following command to verify that youtube-dl is working: `youtube-dl --version`.

### Linux

#### Debian/Ubuntu-based distributions

1. Open a Terminal window.
2. Run the following command to update your system's package index:

   ```bash
   sudo apt update
   ```

3. Run the following command to install youtube-dl:

   ```bash
   sudo apt install youtube-dl
   ```

4. Type the following command to verify that youtube-dl is working: `youtube-dl --version`.

#### Fedora/RHEL-based distributions

1. Open a Terminal window.
2. Run the following command to install youtube-dl:

   ```bash
   sudo dnf install youtube-dl
   ```

3. Type the following command to verify that youtube-dl is working: `youtube-dl --version`.

#### Arch-based distributions

1. Open a Terminal window.
2. Run the following command to install youtube-dl:

   ```bash
   sudo pacman -S youtube-dl
   ```

3. Type the following command to verify that youtube-dl is working: `youtube-dl --version`.

#### Other distributions (Universal Method)

If none of the above methods work, you can use python to install youtube-dl on any of the operaing systems (either Linux or Windows, or macOS). On both Linux and MacOS, python is already installed. You can use pip to install youtube-dl.

1. Open a Terminal window.
2. Run the following command to install youtube-dl using the Python package manager, pip:

   On Windows:

   ```bash
   pip install youtube-dl
   ```

   On Linux/MacOS:

   ```bash
   pip3 install youtube-dl
   ```

3. Type the following command to verify that youtube-dl is working: `youtube-dl --version`.

### If you encounter any errors [Vist the youtube-dl Website](https://github.com/ytdl-org/youtube-dl#installation)

## Installing yt-dlp

### On Windows

1. Download the yt-dlp executable from the [official website](https://github.com/yt-dlp/yt-dlp/releases/latest).
2. Save the executable file in a directory on your computer, such as `C:\Program Files\yt-dlp`.
3. Open a command prompt in the directory where you saved the executable file.
4. Type the following command to verify that yt-dlp is working: `yt-dlp --version`.

Or using `winget`:

```powershell
winget install yt-dlp
```

### On macOS/Linux

The installation method of `yt-dlp` is similar to `youtube-dl`. Just replace `youtube-dl` with `yt-dlp`:

```bash
pip3 install yt-dlp
```

1. Debian/Ubuntu

   ```bash
   sudo apt install yt-dlp
   ```

2. MacOS

   ```bash
   brew install yt-dlp
   ```

3. Arch/Manjaro

   ```bash
   sudo pacman -S yt-dlp
   ```

4. Fedora/RHEL

   ```bash
   sudo dnf install yt-dl
   ```

For more detailed instructions visit the [yt-dlp installation guide](https://github.com/yt-dlp/yt-dlp#installation).

## Installing dependencies for youtube-dl and yt-dlp

As mentioned earlier, youtube-dl and yt-dlp both require ffmpeg or avconv to be installed on your system to download and process videos. These are multimedia frameworks that allow the tools to convert videos to different formats and resolutions.

To install ffmpeg, follow the instructions for your operating system:

- macOS: You can install ffmpeg using Homebrew. Run the following command in the Terminal:

  ```bash
  brew install ffmpeg
  ```

- Windows: Download the latest version of ffmpeg from the official website and install it.

- Linux: You can install ffmpeg using your distribution's package manager. For example, on Ubuntu or Debian, run the following command in the terminal:

  ```bash
  sudo apt install ffmpeg
  ```

## USAGE

### Basic Usage

To download a video from YouTube using youtube-dl or yt-dlp, follow these steps:

1. Copy the URL of the YouTube video you want to download.
2. Open a command prompt or terminal window.
3. Type the following command and replace `<URL>` with the URL of the video you want to download:

   ```bash
   youtube-dl <URL>
   ```

   or

   ```bash
   yt-dlp <URL>
   ```

4. Press Enter. The video will begin downloading to your current directory.

### Downloading Audio Only (MP3)

To download only the audio of a YouTube video as an MP3 file using youtube-dl or yt-dlp, follow these steps:

1. Copy the URL of the YouTube video you want to download.
2. Open a command prompt or terminal window.
3. Type the following command and replace `<URL>` with the URL of the video you want to download:

   ```bash
   youtube-dl -x --audio-format mp3 <URL>
   ```

   or

   ```bash
   yt-dlp -x --audio-format mp3 <URL>
   ```

   > `-x` is the shorthand for `--extract-audio`

4. Press Enter. The audiimage.pngo will begin downloading to your current directory as an MP3 file.

### Downloading Specific Formats

To download a video in a specific format using youtube-dl or yt-dlp, follow these steps:

1. Copy the URL of the YouTube video you want to download.
2. Open a command prompt or terminal window.
3. Type the following command and replace `<URL>` with the URL of the video you want to download:

   ```bash
   youtube-dl -f <format code> <URL>
   ```

   or

   ```bash
   yt-dlp -f <format code> <URL>
   ```

4. Press Enter. The video will begin downloading to your current directory in the specified format.

To view a list of available formats for a video, use the following command:

```bash
youtube-dl -F <URL>
```

or

```bash
yt-dlp -F <URL>
```

> `-F` is the shorthand for `--list-formats`

This will display a list of all available formats for the video, along with their format codes. To download a specific format, simply use its format code in the command above.

### Downloading a Playlist

To download an entire YouTube playlist using youtube-dl or yt-dlp, follow these steps:

1. Copy the URL of the YouTube playlist you want to download.
2. Open a command prompt or terminal window.
3. Type the following command and replace `<URL>` with the URL of the playlist you want to download:

   ```bash
   youtube-dl -f <format code> -o '%(playlist_index)s - %(title)s.%(ext)s' <URL>
   ```

   or

   ```bash
   yt-dlp -f <format code> -o '%(playlist_index)s - %(title)s.%(ext)s' <URL>
   ```

4. Press Enter. The playlist will begin downloading to your current directory.

### Downloading with Custom Filename

By default, youtube-dl and yt-dlp will save downloaded videos with a generic filename. To specify a custom filename, use the -o flag followed by the desired filename template. The template can include various placeholders such as video title, video ID, etc. For example, to save a video with the title "My Video" as "my_video.mp4", use the following command:

```bash
youtube-dl -o 'my_video.%(ext)s' <URL>
```

or

```bash
yt-dlp -o 'my_video.%(ext)s' <URL>
```

This will save the video with the filename "my_video.mp4". You can use various placeholders to customize the filename as desired.

### Other Options

Both youtube-dl and yt-dlp offer a wide range of additional options and features. To view the full list of options, use the following commands:

```bash
youtube-dl --help
```

or

```bash
yt-dlp --help
```

This will display a list of all available options and their descriptions. You can use these options to customize your downloads further or to enable additional features.

One most common option that I often use is to embed thumnails when downloading audio files from youtube.com. You can use the following commands:

```bash
yt-dlp --extract-audio --audio-format mp3 --embed-thumbnail <URL>
```

`--embed-thumbnail` flag will automatically download and embed the thumbnail of the video to the download audio file.

Note: You need `ffmpeg` for most of the operations like, converting videos to audio, format convertion(mkv to mp4), or embeding thumbnails, etc. So make sure you have installed ffmpeg.

## Conclusion

youtube-dl and yt-dlp are powerful tools for downloading videos and audio from YouTube and many other video-sharing sites. With their simple command-line interfaces and extensive feature sets, they offer a flexible and efficient way to download media for offline viewing. By following the instructions and examples above, you should be able to get started with using these tools to download videos and audio in a variety of formats.

## My Blog

Read more on my [Linux Blog](https://talhamehar.hashnode.dev/how-to-download-youtube-videos-using-youtube-dl)
