# Bot_check_RPCLAVA_v2.1
แก้ไขการเชื่อมระหว่าง endpoint กับ RPC

1. connect_to_rpc_endpoint(file_path):อ่าน URL จากไฟล์ที่ระบุและคืนค่า URL นั้น
2. read_private_key_from_file(file_path):อ่าน private key จากไฟล์ที่ระบุและคืนค่า private key นั้น
3. toggle_wallet_connection(private_key, rpc_endpoint):เชื่อมต่อหรือตัดการเชื่อมต่อกับ Wallet โดยใช้ private key และ RPC endpoint ที่ระบุ
4. check_rpc_status(web3):ตรวจสอบสถานะการซิงค์ของ Ethereum node RPC ที่เชื่อมต่อ โดยใช้ตัวแปร web3 เพื่อเรียกใช้ Web3 API
5. check_wallet_balance(web3):ตรวจสอบยอดคงเหลือใน Wallet ที่เชื่อมต่อ โดยใช้ตัวแปร web3 เพื่อเรียกใช้ Web3 API
6. Main loop:ทำซ้ำโดยตรวจสอบ RPC endpoint และ private key จากไฟล์ที่ระบุ เชื่อมต่อหรือตัดการเชื่อมต่อกับ Wallet ตรวจสอบสถานะ RPC node และยอดคงเหลือใน Wallet และพักเฉยๆ 10 วินาที
----------------------------------------------
เตรียมความพร้อม

ติดตั้ง Python version 3 ขึ้นไป
1. sudo apt update
2. sudo apt install python3 -y
   
ติดตั้ง Module Web3
1. sudo apt update
2. sudo apt install python3 -y
3. sudo apt install python3-pip -y
4. pip3 install numpy
5. pip3 install web3

ขั้นตอนการใช้งาน
1. ทำการเพิ่ม RPC LAVA ของตัวเองในไฟล์ rpc_endpoint.txt
2. ทำการเพิ่ม Private kry wallet (EVM Chain) ไปที่ไฟล์ private_key.txt
3. หลักจากติดตั้งเรียบร้อยให้ทำการรัน command >>python3 Bot_LAVA_PKWv2.py
*** ไฟล์ Bot_LAVA_PKWv2.py , private_key.txt & rpc_endpoint.txt จะต้องอยู่ใน folder เดียวกัน ***

⚠️⚠️⚠️ Code นี้มีการใช้งาน Private key wallet โปรดใช้ด้วยความระมันระวัง ⚠️⚠️⚠️
