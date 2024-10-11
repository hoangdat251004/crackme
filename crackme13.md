This crackme combine 3 types of previous is packed, anti-debugger and cracking serial key

![image](https://github.com/user-attachments/assets/543f9cd6-ee68-40d6-a9be-daf7d04cf2ca)

Here we can see Debugger status is `Debugger Is Not Detected` because the ScyllaHide plugin in the previous crackme is still open and hide the debugger from anti-debugger.

So first thign we do is unpack this file by doing this.

Click `F8` to run one line, we can see the address is loaded to the `EBP`, this is the address will lead to the real entrypoint of program because it is packed.

![image](https://github.com/user-attachments/assets/ec87560c-a989-40c3-90c9-3a880d7083b8)

In the right-lower section, right-click in the address like in `EBP` and choose `Follow in DUMP`

![image](https://github.com/user-attachments/assets/b4207d05-196c-45a8-9302-f1eb80fadcd6)

Now we can see it in the memory

![image](https://github.com/user-attachments/assets/d38f2639-120d-451f-b993-aa8e46162c70)

What we need to do next is put a hardware breakpoint in this address.

So choose the address and right click and choose like this.

![image](https://github.com/user-attachments/assets/b0e49c8e-7408-4c0d-ab00-d516be12b8dd)

We just put a bp now click run to get the bp.

![image](https://github.com/user-attachments/assets/15a0a2c8-07e9-4d2d-a392-2fa9cc097ab2)

We now at the bp, to bypass the loop here we do like this. Click out of the loop and choose Debug and Run util selection.

![image](https://github.com/user-attachments/assets/7630f30c-fdd7-44bb-b45f-ccd3063b3434)

Just press `F8` to run and we can get to the real entrypoint.

![image](https://github.com/user-attachments/assets/a27849a3-30e1-4829-a935-c91af0516431)

Now to upack the file we do like this.

Click to the Scylla icon at the rigth-top then click `file` and `dump memory` and look for this line and click `Dump PE`

![image](https://github.com/user-attachments/assets/1ed66b35-1484-4499-9efc-00cef2486a6f)

And save it

![image](https://github.com/user-attachments/assets/560690fe-50ce-414d-b12e-fe2f422b5f01)

But the file dump is still need fixing.

In the Scylla click to IAT auto search and got the result

![image](https://github.com/user-attachments/assets/7c12c4b0-f82e-4187-961a-bc86d13ac010)

![image](https://github.com/user-attachments/assets/c8ae3f83-068b-4197-8fe5-5e5c9d401f5c)

Now click to Get Import

![Screenshot 2024-10-11 152800](https://github.com/user-attachments/assets/1c39ca2d-0903-4aca-8cdb-27a290c98281)

And Fix Dump, open the dump file before

![Screenshot 2024-10-11 152952](https://github.com/user-attachments/assets/6296a73f-079f-4421-ad05-909660b6a648)

Now we can see the dump file is fixed

![Screenshot 2024-10-11 153002](https://github.com/user-attachments/assets/390fe5d9-f54d-4b33-83b9-1184cb9c0d06)

Now the file is unpecked

![image](https://github.com/user-attachments/assets/ec6a5e84-3a7b-4075-b3c7-14bb90081bce)

And we go to the crack serial part

![image](https://github.com/user-attachments/assets/57ba43a8-2e06-4d59-9e6b-ff9243d2dbfd)

Look for the wrong message and go to it

![image](https://github.com/user-attachments/assets/31ff7d98-a8f0-4488-84c3-f99d1734e591)

We can see the serial key is being compare with the string I entered

![Screenshot 2024-10-11 153630](https://github.com/user-attachments/assets/66baac2d-1560-4f28-ad3b-9090bea01167)

Now we can easy patch the file to make and key is true by do ing this

![image](https://github.com/user-attachments/assets/f462d6ea-2cd1-4201-99ca-81aab9fbe4f5)

Patch the file

![image](https://github.com/user-attachments/assets/b1c7f232-7eb1-49d8-b050-3b7d761001b7)

And we got the final result

![image](https://github.com/user-attachments/assets/dc880ddb-3003-4e06-bce1-ffa06ce8457f)
