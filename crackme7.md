Crackme 7 is simpler than previous one

![image](https://github.com/user-attachments/assets/77d97ce5-c662-4132-8947-8ea7f3f98f10)

Here we need change something at `eax` register to make program run right.

![image](https://github.com/user-attachments/assets/856ab5be-9719-4d31-b068-49f8488fea26)

Let analyse the code

When the program it will give eax and ecx same value and do the subtraction between them.

Then a `test` is call it compare value of eax and ecx after subtraction.

The `test` command is like AND command, if one of them is 0 the test will result 0 and run into bad message is “Unregistered”.

What we do here is make the test result not 0 so we have to change value of eax or ecx to make the subtraction not get result is  0. Therefore two `je` command is not triggered.

Here I changed value of `ecx` to 3 so the result of subtraction now no more is 0 and will go to good message is “Registered” 

![image](https://github.com/user-attachments/assets/0734129d-dc5f-4269-b626-a6719e010fa8)

And here is the result

![image](https://github.com/user-attachments/assets/6c5b2b12-db5c-4c43-a79c-929643ce764b)
