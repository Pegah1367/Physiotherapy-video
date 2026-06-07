# Physiotherapy Video Persian Voice Replacement

This project is a small AI and media-processing experiment created in Google Colab.

The goal was to take an educational physiotherapy-related video, translate the narration into Persian, generate a Persian voice, and replace the original English audio with the new Persian narration.

The source video was from Instagram and was used as a learning example to practice AI voice generation, audio synchronization, and video editing with code.

## Project Overview

In this project, I explored how AI and Python tools can support video localization.

The workflow included:

1. Translating the original English content into Persian
2. Testing different text-to-speech methods
3. Generating Persian AI narration
4. Checking the duration of the video and audio
5. Adjusting the audio speed to match the video
6. Replacing the original English audio with Persian narration
7. Exporting the final Persian version of the video

## Tools and Technologies

* Google Colab
* Python
* Edge TTS
* FFmpeg
* IPython Display
* CapCut Web
* GitHub

## What I Tried

### 1. Subtitle Translation

First, I used CapCut Web to help with the subtitle and translation part. This was useful for preparing and reviewing the Persian version of the content.

### 2. Coqui TTS / XTTS Test

I also tested Coqui XTTS for multilingual voice cloning in Google Colab.

The model worked technically, but Persian/Farsi was not properly supported in the setup. Since I had to use Arabic as the closest available language option, the generated voice sounded closer to Arabic than natural Persian.

Because of this limitation, I decided not to use this method for the final result.

### 3. Edge TTS Persian Voice

After that, I tested `edge-tts`, which supports Persian/Iranian voices.

Available Persian voices included:

* `fa-IR-DilaraNeural`
* `fa-IR-FaridNeural`

I selected `fa-IR-DilaraNeural` and generated a Persian AI voice from the translated text.

### 4. Audio and Video Synchronization

The generated Persian audio was slightly longer than the original video.

To solve this, I measured both durations using `ffprobe` and calculated the required speed adjustment.

Then I used FFmpeg’s `atempo` filter to slightly speed up the Persian audio so it matched the video duration more closely.

### 5. Final Video Creation

Finally, I used FFmpeg to replace the original English audio with the adjusted Persian AI voice.

The final output is a Persian-narrated version of the original physiotherapy educational video.

## Files in This Repository

* `physiotherapy_video (2).ipynb`
  Main Google Colab notebook containing the full workflow.

* `english.mp4`
  Original English video.

* `persian.mp4`
  Final video with Persian AI narration.

* `recorded voice.mp4`
  Voice recording used during testing.

## Key Learning Outcomes

Through this project, I practiced:

* Working with AI text-to-speech tools
* Understanding language support limitations in TTS models
* Using Persian voices with Edge TTS
* Measuring audio and video duration with FFmpeg
* Synchronizing audio and video
* Replacing video audio using command-line tools
* Building a small real-world AI workflow in Google Colab

## Final Reflection

This project started as a simple translation task, but it became an enjoyable coding and AI experiment.

It helped me understand that no-code tools are useful, but coding gives more control when working with audio, video, and AI workflows.

Sometimes a small real-world problem is the best way to practice technical skills.
