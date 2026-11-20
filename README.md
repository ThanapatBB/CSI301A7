# Assignment 7 — Bank DApp บน Ethereum Hoodi

**ผู้จัดทำ:** นาย ธนภัทร หนูบุญมี  
**รหัสนักศึกษา:** 66031036

[เปิดเว็บ Bank DApp](https://thanapatbb.github.io/CSI301A7/)

เว็บสำหรับฝาก ถอน และตรวจสอบยอดเงินฝากใน Smart Contract บน Ethereum Hoodi โดยใช้ MetaMask ยืนยันธุรกรรม และใช้ Infura อ่านยอดจากสัญญา

## วิธีทดสอบ

1. เปิดเว็บในเบราว์เซอร์ที่ติดตั้ง MetaMask แล้วเลือกเครือข่าย **Hoodi** (Chain ID `560048`)
2. ใส่ **Contract Address บน Hoodi** จาก **Remix → Deploy & Run Transactions → Deployed Contracts** และกรอก **Infura API Key** ในหน้าเว็บ
3. กด **Connect MetaMask** แล้วอนุญาตให้เว็บเชื่อมกระเป๋า
4. กรอกจำนวน ETH แล้วกด **Deposit** หรือ **Withdraw** จากนั้นยืนยันธุรกรรมใน MetaMask
5. กด **Check Balance** เพื่อดูยอดเงินฝากของบัญชีในสัญญา

ตัวอย่างการทดสอบเมื่อยอดเริ่มต้นเป็นศูนย์ ให้ฝาก `0.001 ETH` แล้วถอน `0.0005 ETH` ยอดฝากในสัญญาควรเหลือ `0.0005 ETH` เมื่อธุรกรรมยืนยันแล้ว โดยต้องมี ETH ทดสอบบน Hoodi สำหรับค่าธรรมเนียมด้วย

หน้าเว็บอยู่ในไฟล์ [`index.html`](index.html) และรองรับสัญญาที่มีฟังก์ชัน `deposit()`, `withdraw(uint256)` และ `checkBalance()` ตาม ABI ในไฟล์
