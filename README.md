# ML-Lab

สรุปการตั้งค่าโปรเจกต์ Python สำหรับงาน Machine Learning โดยใช้ Virtual Environment (`.venv`) และพัฒนาโดยใช้ Jupyter / VS Code

---

## สรุปอย่างรวดเร็ว (Quick Start)
1. เปิด Terminal ในโฟลเดอร์โปรเจกต์
2. สร้างและ activate `.venv`
3. ติดตั้ง dependencies
4. เปิดโค้ดใน VS Code หรือรัน Jupyter

---

## ความต้องการเบื้องต้น
- Python 3.8+ ติดตั้งในระบบ
- Git (ถ้าต้อง clone)
- VS Code (แนะนำ) และส่วนขยาย Python / Jupyter

---

## การตั้งค่าสภาพแวดล้อม (.venv)

1) สร้าง virtual environment:
```bash
python -m venv .venv
```

2) เปิดใช้งาน (เลือกคำสั่งตาม shell / OS):

- PowerShell (Windows)
```powershell
.\.venv\Scripts\Activate.ps1
```
- Command Prompt (Windows)
```cmd
.\.venv\Scripts\activate
```
- macOS / Linux
```bash
source .venv/bin/activate
```

3) อัปเดต pip (ถ้ามีข้อความเตือน):
```bash
python -m pip install --upgrade pip
```

---

## ติดตั้ง Dependencies
Dependencies ถูกบันทึกไว้ใน `requirements.txt`:
```bash
pip install -r requirements.txt
```
ถ้าติดตั้งแพ็กเกจเพิ่มและต้องการบันทึก:
```bash
pip freeze > requirements.txt
```

---

## ใช้ VS Code / Jupyter
- เปิดโฟลเดอร์โปรเจกต์ใน VS Code
- เลือก Python Interpreter เป็น `.venv` (Ctrl+Shift+P → "Python: Select Interpreter")
- รัน Jupyter Notebook / Lab ขณะ `.venv` ถูก activate:
```bash
jupyter lab
# หรือ
jupyter notebook
```

---

## คำสั่งที่เป็นประโยชน์
- ตรวจสอบแพ็กเกจ: `pip list`
- ออกจาก environment: `deactivate`
- ลบ `.venv` และสร้างใหม่: ลบโฟลเดอร์ `.venv` แล้วรัน `python -m venv .venv`

---

## ปัญหาทั่วไป (Troubleshooting)
- PowerShell ไม่ยอม activate: เปิด PowerShell ด้วยสิทธิ์ผู้ใช้แล้วรัน
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```
- การติดตั้งแพ็กเกจล้มเหลว: ตรวจสอบเวอร์ชัน Python และติดตั้ง Build Tools (Windows: Visual C++ Build Tools) หากแพ็กเกจต้องคอมไพล์
- หากใช้ GPU / CUDA: ตรวจสอบความเข้ากันได้ของไดรเวอร์และเวอร์ชันไลบรารี (เช่น CUDA / cuDNN)

---

## เพิ่มเติม
- ถ้าต้องการตัวอย่างการรัน Notebook, การตั้งค่า CI, หรือการเพิ่มสคริปต์สำหรับทดลอง ให้แจ้งหัวข้อที่ต้องการมาได้
