Crackme-9 is a prog check the serial key.

![image](https://github.com/user-attachments/assets/84be949b-22c3-4077-a57a-fce120032224)

To find the code analysis the serial key, I search for the error message to find it.

![image](https://github.com/user-attachments/assets/a575d58b-1e8a-4d34-82e2-64f69403f35a)

Above the error message I found a string that may helpful. So I put a bp above to see what happened with this string.

![image](https://github.com/user-attachments/assets/1089a1b9-c24a-4251-8f52-183b87d4181a)

After several run through 1-by-1 instructions I found that the program compares the string that I entered before with that string I found above. It compared “DAT” with “ABC-123456”.

![image](https://github.com/user-attachments/assets/b1642271-8807-4ad7-bd22-d5d1ff7b8341)

![image](https://github.com/user-attachments/assets/52d4947c-7026-4782-ab37-e67dbafd61b7)

Here the zero flag is set to 0 so the `je` command will not jump to the good message and go to the error message.

![image](https://github.com/user-attachments/assets/351c4ac7-930e-48a1-9135-e02f47940c7d)

So the correct serial key is “ABC-123456”, to change it I click to the instruction I found it in the first time and right-click follow in dump to access the memory address.

![image](https://github.com/user-attachments/assets/eafeebb6-64ef-4885-830d-ce0c05b32d3e)

Then I get there, now I just need to change that value to another one like show as following:

![image](https://github.com/user-attachments/assets/3ca332cb-20f8-4a85-8b5f-8fe4d515bd0f)

![image](https://github.com/user-attachments/assets/bc896e4a-ba83-4e07-b224-f31974f94c67)

Then patched it and open the patched file, run enter the key I changed and here is what I got.

![image](https://github.com/user-attachments/assets/2e5f8df4-df4b-4d56-8cc0-079c107cd1cc)
