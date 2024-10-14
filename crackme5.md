First, load crackme and try to run

![image](https://github.com/user-attachments/assets/59728511-5b79-46d3-b69f-45940cb48bc7)

This program generates a serial key by the firstname, then I will find the code that lead to the wrong message

![image](https://github.com/user-attachments/assets/f3523254-3967-4c21-b068-23c5b6baae3b)

Above it I find the call to get some text maybe the input then I put a breakpoint there

![image](https://github.com/user-attachments/assets/e3b31fd7-7850-488f-b172-ed2b3e9e8c98)

Restart and run again still enter a random key and hit check, the program will pause because it hit the breakpoint.

![image](https://github.com/user-attachments/assets/6d9c0dbd-d2de-4dc4-8843-c73ac0cf575a)

Now click run and press f8 to move each line of code, then we can find a string is automatically generated.

![image](https://github.com/user-attachments/assets/c90c46f9-3a12-4216-a924-a0bf2d8374ed)

Keep press f8 I found that key string I entered is being compared with this string

![image](https://github.com/user-attachments/assets/2e599c6a-084a-4f59-a577-37059097eced)
 
![image](https://github.com/user-attachments/assets/b149a97d-911a-49a0-bf60-442cfac88377)

But jump command is not meet the conditions so it go to the bad message

![image](https://github.com/user-attachments/assets/1efde78b-986a-4608-ade4-21ebdfc22bc7)

![image](https://github.com/user-attachments/assets/64fa0544-9024-49b6-aa95-4e279cd9476f)

![image](https://github.com/user-attachments/assets/20256f04-20d3-4e67-bb69-2a71390d6ad6)

Restart and run again with old firstname and the generated strings above I can get good message.

![image](https://github.com/user-attachments/assets/cff20d75-a498-4940-bc96-4a432d7ab0ad)
