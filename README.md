# Autonomous Photo Camera 📸

This project implements an **embedded smart photo camera system** based on **Raspberry Pi**, combining computer vision, real-time face detection, accessory overlays, and a dedicated web interface for image management and editing.

## Features
- **Real-time photo and video capture** using Raspberry Pi camera module  
- **Face detection** with Haar Cascade and automatic overlay of virtual accessories (hat, mustache, glasses)  
- **Interactive control** via physical buttons (capture, gallery, filters)  
- **Media gallery** with swipe navigation for photos and videos  
- **Dedicated web application** built with Flask for:
  - Viewing and managing images and videos  
  - Applying filters (sepia, grayscale, blur, contrast, invert, brightness, etc.)  
  - Automatic face grouping and naming using `face_recognition`  
  - Secure file transfer with Paramiko (SFTP/SSH)  

## Technologies & Libraries
- **Hardware:** Raspberry Pi 4, Camera Module, GPIO buttons  
- **Computer Vision:** OpenCV, Haar Cascade Classifier, face_recognition  
- **Web Framework:** Flask  
- **Image Processing:** Pillow (PIL), NumPy  
- **System Tools:** Paramiko (SFTP/SSH), ffmpeg for video conversion  

## Project Structure
- `camera.py` – main application running on Raspberry Pi (capture, overlay, gallery)  
- `app_web.py` – Flask web interface for image management, editing, and classification  
- `templates/` – HTML templates for gallery, editing, and grouped faces  
- `imagini_capturate/` – local storage for captured images and videos  
- `nume_persoane.json`, `face_data.json` – metadata for grouped and recognized faces  

## How It Works
1. **On Raspberry Pi:**  
   - Short press on capture button → save photo  
   - Long press → start/stop video recording  
   - Filter button → cycle through accessories (hat, mustache, glasses)  
   - Gallery button → switch to media viewing mode  

2. **On Web Interface:**  
   - Access the gallery at `/galerie`  
   - Edit images with filters  
   - Group faces and assign names at `/persoane`  

## Future Improvements
- Add support for deep learning–based face detection (e.g., MTCNN or YOLO)  
- Implement cloud sync for gallery backup  
- Extend editing features with advanced filters and AR effects  

---

🚀 *Developed as an academic project (2025) at the Faculty of Automatic Control and Computers, Bucharest.*  
