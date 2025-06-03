# Multifunctional Video Splitting Tool (多機能動画分割ツール)

This is a client-side HTML/JavaScript application that allows users to split video and audio files directly in their web browser. The user interface is in Japanese.

## Features

*   **File Upload:** Load video/audio files using a file selector or by dragging and dropping onto the designated area.
*   **Multiple Splitting Modes:**
    *   **Sequential Mode (逐次分割):** Play the video and mark split points on the fly.
    *   **Free Interval Specification Mode (自由区間指定):** Manually define the exact start and end times for each segment.
    *   **Fixed Length Mode (固定長分割):** Automatically divide the video into segments of a specified, consistent length, with an optional start offset.
*   **Segment Management:**
    *   View a list of all marked segments.
    *   Preview individual segments within the player.
    *   Edit the start and end times of segments (primarily in Free Interval Mode).
    *   Generate (process and create) individual segments or all marked segments at once.
    *   Download generated segments individually or as a single ZIP archive.
    *   Track the status of segments (e.g., marked, generating, generated, failed, cancelled).
*   **Audio-Only Extraction:** Option to extract and split only the audio track from a video file.
*   **Project Persistence:**
    *   **Export Segments:** Save the current list of defined segments (start/end times) to a JSON file.
    *   **Import Segments:** Load segment definitions from a previously exported JSON file.
*   **User Settings:** Common settings like filename prefix, audio-only mode preference, current splitting mode, and fixed-length parameters are saved in the browser's `localStorage`.
*   **Keyboard Shortcuts:** Various keyboard shortcuts are available for common actions such as play/pause, marking points, adding new segments, toggling audio-only mode, exporting/importing segments, and cancelling operations.

## How to Use

1.  **Open the Tool:** Download the `video_splitter.html` file and open it in a modern web browser (e.g., Chrome, Firefox).
2.  **Load a File:** Click the designated area or drag and drop your video/audio file into the tool.
3.  **Choose Mode & Define Segments:**
    *   Select your desired splitting mode (Sequential, Free Interval, or Fixed Length).
    *   Define the segments according to the chosen mode.
4.  **Generate Segments:**
    *   Generate individual segments or all marked segments using the provided buttons.
5.  **Download:**
    *   Download the generated segments individually or as a ZIP file.

## Technical Notes

*   The application is built entirely with HTML, CSS, and JavaScript.
*   It utilizes browser APIs such as the `MediaRecorder` API for video/audio processing and `JSZip` for creating ZIP archives.
*   All processing is done client-side; no files are uploaded to a server.
