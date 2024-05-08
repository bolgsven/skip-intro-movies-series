### Steps to Edit Your GitHub File:
1. **Navigate to Your Repository**: Open the markdown file in your GitHub repository where the code is.
2. **Edit the File**: Click the pencil icon to edit the file.
3. **Format the Code Block**: Insert the code within the triple backticks as shown above.
4. **Preview Your Changes**: Before committing, use the "Preview" tab to check the formatting and ensure everything looks correct.
5. **Commit the Changes**: Provide a descriptive commit message, then commit your changes.

```python
from moviepy.editor import VideoFileClip

def skip_intro(video_path, intro_duration, output_path):
    video = VideoFileClip(video_path)
    # Skipping the intro by cutting from the end of the intro to the end of the video
    no_intro_video = video.subclip(intro_duration, video.duration)
    no_intro_video.write_videofile(output_path, codec='libx264', audio_codec='aac')

# Example usage:
skip_intro("path_to_your_movie.mp4", 90, "output_without_intro.mp4")  # Skips the first 90 seconds


