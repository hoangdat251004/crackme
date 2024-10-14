CRACKME 4:

First open x32dbg and load crackme4 into it

![image](https://github.com/user-attachments/assets/357b69a6-a6dc-47f7-b8fb-a72ee8c356d4)

Try run to see how the program work

![image](https://github.com/user-attachments/assets/e8e5550b-a26f-4fc7-bd36-4e460dd50f5c)

Close the about window and pause the program

![image](https://github.com/user-attachments/assets/3ee8a8d8-e042-41ed-b53e-11361c399bcd)

It paused

![image](https://github.com/user-attachments/assets/5191578a-9028-41a8-ae5d-88b49078ce06)

Then open Tab Call stack

![image](https://github.com/user-attachments/assets/ef22416c-dc29-461e-9a2d-287b361138df)

Find the call instructions that make program open the windows, just care the comment has the name crackme4, try that called by user.
 
This will lead to the code and somewhere above it we can found this useful code
 
![image](https://github.com/user-attachments/assets/78f94073-b195-4219-b0e0-215a4888d350)

Try to understand the code, we can see that ecx has value 1E also in hexa, eax maybe 0 then ecx – eax and we got the 16 in decimal and it’s the value shown in windown above.

![image](https://github.com/user-attachments/assets/85b70aff-1bc5-4055-9448-253bb45ca416)

To make it beyond 30 day we need to increase the value of ecx, here I change to ff and click OK
 
![image](https://github.com/user-attachments/assets/05b82eeb-0675-49af-b8f5-5338256f31b7)

And patch the file

![image](https://github.com/user-attachments/assets/0cf61334-fb74-42c3-b81c-c7f7324b9f28)

![image](https://github.com/user-attachments/assets/5378bb56-5e83-44b3-952c-765c5ae92d22)

Open the patched file and run, now it beyond 30-day
