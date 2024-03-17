# Bot_check_RPCLAVA_v2.1
แก้ไขการเชื่อมระหว่าง endpoint กับ RPC

1. connect_to_rpc_endpoint(file_path):อ่าน URL จากไฟล์ที่ระบุและคืนค่า URL นั้น
2. read_private_key_from_file(file_path):อ่าน private key จากไฟล์ที่ระบุและคืนค่า private key นั้น
3. toggle_wallet_connection(private_key, rpc_endpoint):เชื่อมต่อหรือตัดการเชื่อมต่อกับ Wallet โดยใช้ private key และ RPC endpoint ที่ระบุ
4. check_rpc_status(web3):ตรวจสอบสถานะการซิงค์ของ Ethereum node RPC ที่เชื่อมต่อ โดยใช้ตัวแปร web3 เพื่อเรียกใช้ Web3 API
5. check_wallet_balance(web3):ตรวจสอบยอดคงเหลือใน Wallet ที่เชื่อมต่อ โดยใช้ตัวแปร web3 เพื่อเรียกใช้ Web3 API
6. Main loop:ทำซ้ำโดยตรวจสอบ RPC endpoint และ private key จากไฟล์ที่ระบุ เชื่อมต่อหรือตัดการเชื่อมต่อกับ Wallet ตรวจสอบสถานะ RPC node และยอดคงเหลือใน Wallet และพักเฉยๆ 10 วินาที
