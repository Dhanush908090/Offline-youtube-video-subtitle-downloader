# Offline-youtube-video-subtitle-downloader
this is a repo of a python file which automatically fetches all videos in all formats and get their name and search for that name in youtube and get the url of the first video and give that yt-dlp and download its subtitles and its all automated you can select your language and then boom all video in your location have subtitles ready as srt format


# 🎥 Subtitle Downloader Utility (`subdown.py`)

This Python script automates the process of finding the YouTube match for your local video files and downloading the corresponding subtitles in a selected language. It utilizes **Selenium** for browser automation and **yt-dlp** for reliable subtitle extraction and conversion.

## 🚀 Key Features

* **Batch Processing:** Scans a folder for video files and processes them all automatically.

* **YouTube URL Finder:** Uses a headless Chrome browser (via Selenium) to search YouTube using your video's filename and finds the corresponding watch URL.

* **Language Selection:** Prompts the user to select one subtitle language (English, Hindi, or Tamil) to apply to all downloads.

* **SRT Output:** Downloads and converts subtitles directly into the standard `.srt` format, compatible with most media players.

## ⚙️ Setup and Installation Guide

Follow these steps precisely to get the script running on your local machine.

### Step 1: Prerequisites

You must have the following tools installed and configured before starting:

1.  **Python 3.x:** Installed and configured with its path added to your system's environment variables. (`python.org` this is that website download python )

    **NOTE:** DONT FORGET TO TICK “ADD TO PATH “ WHILE INSTALLING PYTHON

2.  **Google Chrome:** The browser must be installed for Selenium to work.

3.  **FFmpeg:** **This is CRITICAL.** `yt-dlp` needs FFmpeg to process and convert the raw subtitle data into the required `.srt` file format. (`winget install ffmpeg` run this in cmd that’s all simple )

4.  download `subdown.py` from this repo

### Step 2: Install Python Dependencies

Open your terminal or command prompt, and run the following command to install the required Python libraries:

    
        pip install selenium yt-dlp
    

### Step 3: Configure ChromeDriver (Web Browser Automation)

The script uses a specific executable to control your Chrome browser for the YouTube search.

1.  **Download ChromeDriver:**

    * Download the correct `chromedriver.exe` file that matches your **installed Google Chrome browser version**.

    * **Direct Link Reference (64-bit Windows):** Use this link to download the zip file and extract the executable:
        `https://storage.googleapis.com/chrome-for-testing-public/142.0.7444.59/win64/chromedriver-win64.zip`
        *(Note: If you need a 32-bit version, you must search for the correct 32-bit build for your Chrome version.)*

2.  **Placement:** Extract the **`chromedriver.zip`** file and it has a file named “chromedriver.exe” place it **directly in the same folder** as `subdown.py`.

### Step 4: Prepare Videos and Run

1.  **Video Preparation:** Place all your local video files (e.g., `.mp4`, `.mkv`, etc.) for which you need subtitles into the same project folder.

2.  **Run:** Execute the script from your terminal:

    ```
    python subdown.py
    
    
    ```

3.  **Language Prompt:** The script will first ask you to select a target subtitle language.

4.  **Completion:** The script will automatically process your video files. New **`.srt`** subtitle files will be saved next to the corresponding video files in the same directory upon successful download.
