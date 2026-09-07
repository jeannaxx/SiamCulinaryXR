# SiamCulinaryXR — Daily Development Log

ไฟล์นี้ใช้บันทึกว่างานในแต่ละวันทำอะไรไปแล้ว กำลังทดสอบอะไร และควรทำอะไรต่อ

## 7 September 2026

### Direction and project setup

- ปรับแผนตามคำแนะนำของอาจารย์ให้เริ่มจาก Unity VR/XR Project ตั้งแต่ต้น
- สร้างโปรเจกต์ใหม่จาก Unity VR Template
- สำรองโปรเจกต์เดิมไว้ใน Git branch `legacy`
- ย้ายไฟล์จากโปรเจกต์ VR ใหม่มาเป็นโปรเจกต์หลักบน branch `main`
- ล้าง Unity cache เก่าที่ไม่ควรเก็บใน Git ได้แก่ `Library`, `Logs` และ `UserSettings`
- Commit การเปลี่ยนโปรเจกต์หลักเป็น VR Template
  - Commit: `8be8a7e`
  - Message: `Replace main project with VR template`

### Scene setup

- สร้าง Scene ใหม่ชื่อ `MainVR`
- นำ `XR Origin Hands (XR Rig)` จาก Sample Scene มาใช้ใน `MainVR`
- ลบ Main Camera เดิมเพื่อไม่ให้ซ้ำกับกล้องภายใน XR Origin
- ตั้งตำแหน่งและมุมหมุนของ XR Origin กลับเป็นศูนย์
- สร้างพื้นทดสอบชื่อ `TestFloor` ขนาดประมาณ 5 × 5 เมตร

## 8 September 2026

### XR Foundation prototype

- เพิ่ม `Teleportation Area` ให้ `TestFloor`
- สร้าง Cube สำหรับทดสอบ Interaction
- เพิ่ม `Rigidbody` และ `XR Grab Interactable` ให้ Cube
- Import `XR Interaction Simulator` จาก XR Interaction Toolkit
- เปิด `Use XR Interaction Simulator in scenes`
- ตั้ง `Camera Y Offset` เป็น 1.6 เมตร สำหรับจำลองระดับสายตาผู้ใหญ่

### Tests completed

- XR Interaction Simulator เปิดและทำงานใน Play Mode
- ควบคุมมุมมองและการเคลื่อนที่ด้วยเมาส์และคีย์บอร์ดได้
- Cube ตกและชนพื้นตาม Physics ได้
- หยิบ ปล่อย โยน และหยิบ Cube ซ้ำได้
- Teleport บนพื้นทดสอบได้

### Current milestone

Phase 1 — XR Foundation prototype ผ่านการทดสอบพื้นฐานแล้ว:

```text
XR Origin
→ Keyboard/Mouse Simulation
→ Movement and Turning
→ Teleport
→ Grab, Drop, and Throw
```

### Next work

- บันทึกและ Commit ผลการทดสอบ XR Foundation
- เริ่ม Phase 2 — Environment Blockout
- สร้างบ้านเรือนไทยขนาดเล็กแบบ Blockout
- แบ่งพื้นที่เป็นจุดเริ่มต้น/รับภารกิจ สวน และครัวไทย
- ทดสอบขนาดพื้นที่และตำแหน่งวัตถุด้วย XR Simulation

---

## Daily entry template

### Date

#### Completed

- 

#### Tested

- 

#### Problems / decisions

- 

#### Next work

- 
