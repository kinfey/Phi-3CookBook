เดโมนี้แสดงให้เห็นวิธีการใช้โมเดลที่ถูกฝึกมาแล้วในการสร้างโค้ด Python โดยอ้างอิงจากภาพและข้อความคำสั่ง

[ตัวอย่างโค้ด](../../../../../../code/06.E2E/E2E_OpenVino_Phi3-vision.ipynb)

คำอธิบายแบบทีละขั้นตอน:

1. **การนำเข้าและการตั้งค่า**:
   - ไลบรารีและโมดูลที่จำเป็นจะถูกนำเข้า รวมถึง `requests`, `PIL` สำหรับการประมวลผลภาพ และ `transformers` สำหรับจัดการโมเดลและการประมวลผล

2. **การโหลดและแสดงภาพ**:
   - ไฟล์ภาพ (`demo.png`) ถูกเปิดด้วยไลบรารี `PIL` และแสดงผล

3. **การกำหนดคำสั่ง (Prompt)**:
   - ข้อความถูกสร้างขึ้นซึ่งรวมถึงภาพและคำขอให้สร้างโค้ด Python เพื่อประมวลผลภาพและบันทึกด้วย `plt` (matplotlib)

4. **การโหลดโปรเซสเซอร์**:
   - `AutoProcessor` ถูกโหลดจากโมเดลที่ถูกฝึกมาแล้วซึ่งระบุโดยไดเรกทอรี `out_dir` โดยโปรเซสเซอร์นี้จะจัดการอินพุตทั้งข้อความและภาพ

5. **การสร้างคำสั่ง (Prompt)**:
   - ใช้เมธอด `apply_chat_template` เพื่อจัดรูปแบบข้อความให้เป็นคำสั่งที่เหมาะสมสำหรับโมเดล

6. **การประมวลผลอินพุต**:
   - คำสั่งและภาพถูกประมวลผลเป็นเทนเซอร์ที่โมเดลสามารถเข้าใจได้

7. **การตั้งค่าพารามิเตอร์สำหรับการสร้าง**:
   - กำหนดพารามิเตอร์สำหรับกระบวนการสร้างของโมเดล รวมถึงจำนวนโทเค็นใหม่สูงสุดที่จะสร้าง และการสุ่มผลลัพธ์หรือไม่

8. **การสร้างโค้ด**:
   - โมเดลสร้างโค้ด Python โดยอ้างอิงจากอินพุตและพารามิเตอร์การสร้างที่กำหนดไว้ โดยใช้ `TextStreamer` เพื่อจัดการผลลัพธ์ โดยข้ามคำสั่งและโทเค็นพิเศษ

9. **ผลลัพธ์**:
   - โค้ดที่ถูกสร้างจะถูกพิมพ์ออกมา ซึ่งควรเป็นโค้ด Python สำหรับประมวลผลภาพและบันทึกตามที่ระบุในคำสั่ง

เดโมนี้แสดงให้เห็นถึงวิธีการใช้โมเดลที่ถูกฝึกมาแล้วผ่าน OpenVino เพื่อสร้างโค้ดแบบไดนามิกโดยอ้างอิงจากอินพุตของผู้ใช้และภาพ

**ข้อจำกัดความรับผิดชอบ**:  
เอกสารนี้ได้รับการแปลโดยใช้บริการแปลภาษาอัตโนมัติที่ขับเคลื่อนด้วยปัญญาประดิษฐ์ (AI) แม้ว่าเราจะพยายามอย่างเต็มที่เพื่อให้การแปลถูกต้อง แต่โปรดทราบว่าการแปลอัตโนมัติอาจมีข้อผิดพลาดหรือความไม่ถูกต้องเกิดขึ้นได้ เอกสารต้นฉบับในภาษาดั้งเดิมควรถือเป็นแหล่งข้อมูลที่ถูกต้องที่สุด สำหรับข้อมูลที่สำคัญ ขอแนะนำให้ใช้บริการแปลภาษามนุษย์ที่เป็นมืออาชีพ เราไม่รับผิดชอบต่อความเข้าใจผิดหรือการตีความที่ผิดพลาดอันเกิดจากการใช้การแปลนี้