<h1>Download Youtube from url</h1>
<p>url : https://www.youtube.com/watch?v=TI0CVCUYTG0&t=253s</p>
<h2>Step 01 : Install module </h2>
<code>pip install yt_dlp</code>
<h2>Step 02 : Run</h2>
<code>python dlyoutube.py</code>

โปรแกรมนี้เขียนด้วย Python ใช้ไลบรารี yt_dlp สำหรับดาวน์โหลดวิดีโอจาก YouTube ผู้ใช้ใส่ URL แล้วระบบจะดาวน์โหลดไฟล์วิดีโอคุณภาพดีที่สุดมาเก็บไว้ในเครื่อง
pip install yt_dlp เป็นการติดตั้งเครื่องมือที่ใช้ดาวน์โหลดวิดีโอจาก YouTube เข้ามาในเครื่อง
import yt_dlp นำไลบรารี yt_dlp มาใช้งาน
def download_youtube_video(url, save_path="."): สร้างฟังก์ชันสำหรับดาวน์โหลดวิดีโอ
ydl_opts = {
    'outtmpl': f'{save_path}/%(title)s.%(ext)s',
    'format': 'best'
} กำหนดรูปแบบไฟล์ที่ดาวน์โหลด

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download([url])สั่งให้ yt_dlp ดาวน์โหลดวิดีโอจาก URL ที่ใส่เข้าไป
video_url = input("Enter the YouTube video URL: ")ให้ผู้ใช้กรอกลิงก์ YouTube

download_youtube_video(video_url, save_path=".")เรียกฟังก์ชันเพื่อดาวน์โหลดวิดีโอ





