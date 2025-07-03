# Json Server API for Hotel Web App

---

## English Version

This repository contains the JSON file used by `json-server` to simulate the API for the Hotel Web App project.

### Background and Reason for Separate Repo

Previously, the JSON Server ran locally alongside the frontend project `Hotel-Web-App` with the API base URL:
http://localhost:8000


Since the project needed to run online (outside local), the JSON files were separated and deployed on Render.com at:

[https://json-server-repo-for-hotel-app.onrender.com](https://json-server-repo-for-hotel-app.onrender.com)

### Important Changes

In `package.json`, the start script was updated to work with Render's environment:

```json
"scripts": {
  "start": "json-server --watch server/db.json --port $PORT --host 0.0.0.0"
}
```
previous script was ("server": "json-server --watch server/db.json --port 8000",)

Uses the environment variable $PORT provided by Render

Binds the server to 0.0.0.0 to accept external requests


Usage in Frontend Project
In the Hotel-Web-App frontend, replace the local JSON Server API URL (http://localhost:8000) with the new online URL:

https://json-server-repo-for-hotel-app.onrender.com

This ensures API requests go to the online server correctly.

Running Locally
You can still run the JSON Server locally with:

npm install
npm start
and use the default port 8000 or an environment variable for the port.

***
### Persian (فارسی)

این مخزن شامل فایل JSON مورد استفاده توسط json-server برای شبیه‌سازی API پروژه Hotel Web App است.

توضیح و دلیل جدا کردن مخزن
قبلاً JSON Server به صورت محلی در کنار پروژه فرانت‌اند Hotel-Web-App اجرا می‌شد و آدرس API به شکل زیر بود:

http://localhost:8000

با توجه به نیاز اجرای پروژه به صورت آنلاین، فایل‌ها جدا شده و روی Render.com آپلود شدند:

https://json-server-repo-for-hotel-app.onrender.com
تغییرات مهم
در package.json اسکریپت start به شکل زیر تغییر کرد تا با محیط Render سازگار باشد:
"scripts": {
  "start": "json-server --watch server/db.json --port $PORT --host 0.0.0.0"
}

دستور قبلی ("server": "json-server --watch server/db.json --port 8000",)
استفاده از متغیر محیطی $PORT

تنظیم host به 0.0.0.0 برای پذیرش درخواست‌های بیرونی

استفاده در پروژه فرانت‌اند
در پروژه Hotel-Web-App به جای آدرس لوکال هاست باید آدرس زیر برای API استفاده شود:

https://json-server-repo-for-hotel-app.onrender.com

اجرای محلی
برای اجرای محلی می‌توانید با دستورات زیر سرور را اجرا کنید:
npm install
npm start


***
Frontend Project Repository
https://github.com/Alireza-Ghazanfari-0/Hotel-Web-App


