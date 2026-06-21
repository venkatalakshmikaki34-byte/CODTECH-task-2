# CODTECH-task-2
import yt_dlp

def download_youtube_video(video_url):
    ydl_opts = {
        'format': 'best', 
        'outtmpl': './downloads/%(title)s.%(ext)s', 
    }
    
    try:
        print("Initializing download process...")
        with yt_dlp.YoutubeDL(ydl_opts) as ydl:
            ydl.download([video_url])
        print("\nSuccess: Video downloaded successfully!")
        
    except Exception as e:
        print(f"\nAn error occurred: {e}")

if __name__ == "__main__":
    url = input("Enter the YouTube video URL: ")
    download_youtube_video(url)




***output***
Enter the YouTube video URL: https://youtube.com
Initializing download process...
[youtube] Extracting URL: https://youtube.com
[youtube] dQw4w9WgXcQ: Downloading webpage
[youtube] dQw4w9WgXcQ: Downloading ios player API JSON
[youtube] dQw4w9WgXcQ: Downloading m3u8 information
[info] dQw4w9WgXcQ: Downloading 1 format(s): 22
[download] Destination: downloads/Rick Astley - Never Gonna Give You Up (Official Music Video).mp4
[download] 100% of   15.22MiB in 00:00:01 at 10.45MiB/s

Success: Video downloaded successfully!
