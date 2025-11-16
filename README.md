```markdown
# LAN File Sharing Web Server

This is simple FastAPI based file sharing website for local network. Using this you can upload, download, delete files from any device in same Wi-Fi. Very fast and easy to use.

---

## Features

### ✔ Easy File Upload
- Drag and drop file
- Progress bar coming
- Image and PDF preview also working
- Simple alerts showing

### ✔ File Management
- Download any file
- Delete file fast
- Auto refresh file list

### ✔ LAN Support
- Show your local IP address
- Works on mobile, laptop, PC everything in same Wi-Fi
- Mobile friendly webpage

### ✔ Lightweight
- No database
- Pure FastAPI backend
- Very fast working

---

## Project Structure

```
project/
│── app.py
│── templates/
│     └── index.html
│── uploads/         ← created automatically
│── README.md
│── requirements.txt
```

---

## Installation

### 1) Install required packages

requirements.txt:

```
fastapi
uvicorn
jinja2
python-multipart
```

Install:

```
pip install -r requirements.txt
```

Or manually:

```
pip install fastapi uvicorn jinja2 python-multipart
```

---

## Run the Server

Run:

```
python app.py
```

Then you will see something like:

```
Server running on http://192.168.X.X:8000
```

Open this link in phone or laptop inside same Wi-Fi.

---

## How to Use

### Upload Files
- Drag file or select file  
- Upload progress showing  
- Preview image or pdf  

### Download Files
Just click **Download** button.

### Delete Files
Press **Delete** button.

Files saved inside:

```
uploads/
```

---

## Build EXE (Windows)

Install pyinstaller:

```
pip install pyinstaller
```

Build exe:

```
pyinstaller --onefile --add-data "templates;templates" --add-data "uploads;uploads" app.py
```

Your exe will come here:

```
dist/app.exe
```

---

## API Endpoints

| Method | Endpoint | Work |
|--------|----------|------|
| GET | `/` | Show webpage |
| POST | `/uploadfile/` | Upload file |
| GET | `/downloadfile/{filename}` | Download file |
| POST | `/deletefile/{filename}` | Delete file |

---

## Security Note
This is only for local Wi-Fi use.  
Don’t use on public internet without password, HTTPS, etc.
```
