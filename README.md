# LAN File Sharing Web Server

A simple FastAPI-based file sharing tool for local network use. Allows uploading, downloading, and deleting files from any device connected to the same Wi-Fi network.

---

## Features

- Upload files with progress indication
- Image and PDF preview before upload
- Download saved files
- Delete unwanted files
- Auto-refresh file list
- Works on mobile and desktop browsers
- Shows local IP address for sharing
- No database required, lightweight and fast

---

## Project Structure

```
project/
│── app.py
│── templates/
│     └── index.html
│── uploads/        (created automatically)
│── README.md
│── requirements.txt
```

---

## Requirements

```
fastapi
uvicorn
jinja2
python-multipart
```

Install all requirements:

```
pip install -r requirements.txt
```

Or install manually:

```
pip install fastapi uvicorn jinja2 python-multipart
```

---

## Running the Server

Start the server:

```
python app.py
```

You will see output similar to:

```
Server running on http://192.168.x.x:8000
```

Open the link on any device connected to the same Wi-Fi network.

---

## How to Use

### Uploading Files
- Choose a file or drag and drop
- Preview shows if it's an image or PDF
- Upload progress is displayed
- File appears in the list after upload

### Downloading Files
Click the **Download** link next to the file name.

### Deleting Files
Click the **Delete** button to remove the file.

Uploaded files are stored inside:

```
uploads/
```

---

## Building Windows EXE

Install PyInstaller:

```
pip install pyinstaller
```

Build the executable:

```
pyinstaller --onefile --add-data "templates;templates" --add-data "uploads;uploads" app.py
```

Output EXE will be available inside:

```
dist/app.exe
```

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Main webpage |
| POST | `/uploadfile/` | Upload file |
| GET | `/downloadfile/{filename}` | Download file |
| POST | `/deletefile/{filename}` | Delete file |

---

## Security Notice

This tool is designed for local Wi-Fi sharing only.  
Do not expose it to the internet without proper security (authentication, HTTPS, etc.).

