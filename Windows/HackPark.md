![image](https://github.com/user-attachments/assets/33bf058d-e71e-4d89-a643-5808ca794e63)
![image](https://github.com/user-attachments/assets/b155098d-429c-4a97-9d99-eab1e6cefb3c)
![image](https://github.com/user-attachments/assets/a9c7bc7d-d001-4775-b60e-b1335646cad6)
![image](https://github.com/user-attachments/assets/d037ae14-46fd-488a-aa05-8270eb14e745)
![image](https://github.com/user-attachments/assets/20700291-696e-498a-b935-9e5cb176dd6c)
![image](https://github.com/user-attachments/assets/747cf21c-89b1-4485-be39-00c5be5a4c60)
![image](https://github.com/user-attachments/assets/f79f2273-c289-49e3-bcb3-d5c6359f8453)
![image](https://github.com/user-attachments/assets/fc04a2ea-727f-446b-b1e4-c47c98914d8a)
![image](https://github.com/user-attachments/assets/49c8fb75-c210-4c64-bd3d-dcb52237c9f8)
![image](https://github.com/user-attachments/assets/42b4cf46-de6a-4a1b-b071-57e2a006cdd7)
![image](https://github.com/user-attachments/assets/feeeccd1-49fb-4c98-93c9-24c46efe2e57)
![image](https://github.com/user-attachments/assets/22297af7-dcbc-4b9c-99c8-bcc3ebc7de80)
![image](https://github.com/user-attachments/assets/0baae781-53bb-4f4e-83d2-465cc5d9e0c1)
![image](https://github.com/user-attachments/assets/a87bd0ef-748c-4709-ba0d-1a69f90eb485)
![image](https://github.com/user-attachments/assets/bd748140-4778-45a4-ade8-1c9f141ab62f)
![image](https://github.com/user-attachments/assets/42e3ad02-2948-447e-848d-6fcf7aee800f)
![image](https://github.com/user-attachments/assets/0b70bea8-c14e-4730-b8dd-361d39363b31)
![image](https://github.com/user-attachments/assets/eb85bbe6-9714-4707-914b-c598732752d5)
![image](https://github.com/user-attachments/assets/db83806c-e71e-4c72-ac18-776d40817913)
![image](https://github.com/user-attachments/assets/9c3bf6e4-ccd7-4998-83ba-ba4bcc36270e)
![image](https://github.com/user-attachments/assets/eb2c1f41-2cde-476c-a495-3f8b8d2e4bdc)
![image](https://github.com/user-attachments/assets/dd008c37-001f-4e0d-a2bc-7e69a0779516)
![image](https://github.com/user-attachments/assets/b30ab679-f1a3-4945-a3b5-4ee5f254b69f)
![image](https://github.com/user-attachments/assets/8cf22fb6-4377-48e1-96fa-ee1a05bd2613)
![image](https://github.com/user-attachments/assets/c4937ba1-9e9f-4cfc-8cb9-eb997ee91e34)
![image](https://github.com/user-attachments/assets/b0ee5aaf-05fa-4162-9cb3-04c6e69bb80f)

1. hydra brute force password

2. upload file to post as per 46353.cs (rename to PostView.ascx)

3. visit URL (http://IP/?theme=../../App_Data/files) to trigger payload, get reverse shell, user iis apppool

4. upload winPEAS and another shell.exe to global writable directory C:\Windows\Temp

5. revese shell, run winPEAS, see:
   
   WindowsScheduler(Splinterware Software Solutions - System Scheduler Service)
   [C:\PROGRA~2\SYSTEM~1\WService.exe] - Auto - Running
   File Permissions: Everyone [WriteData/CreateFiles]
   Possible DLL Hijacking in binary folder: C:\Program Files (x86)\SystemScheduler (Everyone [WriteData/CreateFiles])

7. Exploit-DB 45072 --> C:\Program Files (x86)\SystemScheduler --> tasklist a couple times until Message.exe appears --> rename original & replace with shell --> open listener and wait --> PE to Admin
