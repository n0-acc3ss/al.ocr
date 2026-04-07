# Autocrop

**Live app → https://download-available.github.io/autocrop**

---

Autocrop is a free, simple web tool that automatically trims the empty transparent space around images — no software to install, no sign-up required. Everything happens directly in your browser; your files never leave your device.

**Autocrop** คือเครื่องมือเว็บฟรีที่ช่วยตัดขอบโปร่งใสที่ว่างเปล่าออกจากรูปภาพโดยอัตโนมัติ ไม่ต้องติดตั้งโปรแกรม ไม่ต้องสมัครสมาชิก ทุกอย่างทำงานในเบราว์เซอร์ของคุณ — ไฟล์จะไม่ถูกส่งไปที่ใดทั้งนั้น

---

## What it does / ทำอะไรได้บ้าง

Imagine a sticker on a large transparent canvas. Autocrop finds where the sticker actually is and cuts away all the extra empty space around it, leaving only the sticker itself — at the exact same quality as the original.

ลองนึกภาพสติกเกอร์ที่วางอยู่บนผ้าใบโปร่งใสขนาดใหญ่ Autocrop จะหาตำแหน่งที่สติกเกอร์อยู่จริง ๆ แล้วตัดพื้นที่ว่างรอบ ๆ ออก เหลือแค่ตัวสติกเกอร์ — โดยที่คุณภาพรูปภาพยังคงเดิมทุกประการ

**Supported formats / รูปแบบไฟล์ที่รองรับ:** PNG, WebP

---

## How to use / วิธีใช้งาน

**English**

1. Open the app in any browser (Chrome, Safari, Firefox, Edge)
2. Drag and drop your image files onto the drop zone, or click it to browse your files
3. The cropped result appears instantly with a before/after slider — drag it left or right to compare
4. Click **Download** to save a single file, or **Download all as ZIP** to save everything at once
5. Use **Copy** to copy the cropped image directly to your clipboard for pasting into another app

**ภาษาไทย**

1. เปิดแอปในเบราว์เซอร์ใดก็ได้ (Chrome, Safari, Firefox, Edge)
2. ลากและวางไฟล์รูปภาพลงในกรอบ หรือคลิกกรอบเพื่อเลือกไฟล์จากเครื่อง
3. ผลลัพธ์จะแสดงทันที พร้อมแถบเปรียบเทียบก่อน/หลัง — ลากซ้ายขวาเพื่อดูความต่าง
4. กด **Download** เพื่อบันทึกทีละไฟล์ หรือ **Download all as ZIP** เพื่อบันทึกทั้งหมดในครั้งเดียว
5. กด **Copy** เพื่อคัดลอกรูปที่ตัดแล้วไปวางในโปรแกรมอื่นได้เลย

---

## Options / ตัวเลือก

| Option (EN) | คำอธิบาย (TH) | Default |
|---|---|---|
| **Padding** | เพิ่มขอบว่างรอบรูป (หน่วย: พิกเซล) — เหมาะถ้าต้องการให้มีพื้นที่หายใจรอบเนื้อหา | Off |
| **Strip metadata** | ลบข้อมูลที่ซ่อนอยู่ในไฟล์ เช่น วันที่ถ่าย ชื่ออุปกรณ์ ตำแหน่ง GPS | On |
| **Alpha threshold** | ความโปร่งใสขั้นต่ำที่ถือว่า "มีเนื้อหา" — เพิ่มค่านี้ถ้าขอบรูปยังมีพิกเซลจาง ๆ หลงเหลืออยู่ | 0 |
| **WebP quality** | ระดับคุณภาพของไฟล์ WebP ที่บันทึก (1–100) — ค่าสูง = คุณภาพดีกว่า ไฟล์ใหญ่กว่า | 92 |

---

## Output filename / ชื่อไฟล์ที่ได้

Files are saved with a date-based name so they stay organised automatically.

ไฟล์จะถูกบันทึกด้วยชื่อที่มีวันที่ เพื่อให้จัดระเบียบได้ง่าย

```
2026-Apr-07_01_cropped.png
│         │  │
│         │  └─ running number (01, 02, 03 …)
│         └──── date (year-month-day)
└──────────────  "cropped" suffix
```

---

## Metadata / ข้อมูลที่ซ่อนอยู่ในไฟล์

Photos often carry hidden information such as the camera model, date and time, GPS location, and editing software used. This is called **metadata**.

รูปภาพมักมีข้อมูลที่ซ่อนอยู่ เช่น รุ่นกล้อง วันเวลา พิกัด GPS และโปรแกรมที่ใช้แต่งรูป ข้อมูลนี้เรียกว่า **เมทาดาตา**

- **Strip metadata ON (default)** — all hidden data is removed from the saved file. Recommended for sharing images online.
  ลบข้อมูลที่ซ่อนทั้งหมดออกจากไฟล์ที่บันทึก แนะนำเมื่อแชร์รูปออนไลน์

- **Strip metadata OFF** — original metadata is preserved in PNG files. WebP metadata cannot be preserved (technical limitation of the format).
  เก็บข้อมูลที่ซ่อนไว้ในไฟล์ PNG ส่วน WebP ไม่สามารถเก็บเมทาดาตาไว้ได้เนื่องจากข้อจำกัดของรูปแบบไฟล์

---

## Important notes / หมายเหตุสำคัญ

- **Transparent images only / รองรับเฉพาะรูปที่มีพื้นหลังโปร่งใส**
  Autocrop works by detecting transparent pixels. If your image has a solid background (e.g. white or black), nothing will be trimmed. Use an image editor to remove the background first if needed.
  Autocrop ทำงานโดยตรวจหาพิกเซลโปร่งใส หากรูปมีพื้นหลังทึบ (เช่น สีขาวหรือดำ) จะไม่มีการตัดใด ๆ เกิดขึ้น หากต้องการ ให้ลบพื้นหลังด้วยโปรแกรมแต่งรูปก่อน

- **Your files stay private / ไฟล์ของคุณปลอดภัย**
  No files are uploaded anywhere. All processing happens inside your browser.
  ไม่มีการอัปโหลดไฟล์ไปที่ใดทั้งสิ้น การประมวลผลทั้งหมดเกิดขึ้นในเบราว์เซอร์ของคุณ

- **Works offline / ใช้งานได้แบบออฟไลน์**
  After your first visit, the app can be used without an internet connection. You can also install it to your home screen like a regular app.
  หลังจากเปิดใช้งานครั้งแรก แอปสามารถใช้งานได้โดยไม่ต้องมีอินเทอร์เน็ต และยังสามารถติดตั้งลงหน้าจอโฮมได้เหมือนแอปทั่วไป
