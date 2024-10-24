This crackme require to remove nag screen and crack the regcode to make the register successfull.

![image](https://github.com/user-attachments/assets/8ca96119-0ebf-4005-a2b5-3871ad8903b5)

![image](https://github.com/user-attachments/assets/af723600-f453-4447-a839-2dc79992ad65)

Check the code I found the code to pop up the nag screen.

There is a instruction is `call MsgBox`, it make the screeen pop up to windows.

![image](https://github.com/user-attachments/assets/2c6e132b-76b2-440e-800f-5757054f7615)

Try to remove that line with `nop` to make the nag not pop up and I found another things.

![image](https://github.com/user-attachments/assets/469915b3-703a-46e3-928c-a73e4adeda99)

When run over the `jne` instruction the program will be terminated.

![image](https://github.com/user-attachments/assets/294ddfa8-feb7-4218-a229-9f61fddd1ae0)

I found a instruction after the `jne` command is `vbaEnd`. 

After sometime to explore the [`End`](https://learn.microsoft.com/en-us/office/vba/language/reference/user-interface-help/end-statement) This command make the program terminate immediately.

![image](https://github.com/user-attachments/assets/f21bf2c9-38b0-4bee-9657-07dee4cc6702)

To make program not being terminate while running I change the `jne` to `jmp` to make it jump over that terminate command.

![image](https://github.com/user-attachments/assets/1e4953b0-042a-46a5-95ae-304ccf00dfa7)

And patch it.

Now the Nag screen is no more show up when run program and run right into the RegCode.

![image](https://github.com/user-attachments/assets/5af88b66-dd38-4a33-96ca-698acd63c210)

After check the code I found a string comapre command and a string, so I put a bp there to see which string is being comared with this string.

![image](https://github.com/user-attachments/assets/cb3a8f84-cc27-420b-b2f5-52b9d3e7dd79)

The program compare the string I entered with this one `APRIL-2020`, so I can tell that this one is the RegCode.

![image](https://github.com/user-attachments/assets/0476548b-6287-4e96-b250-3a002f2b99ad)

![image](https://github.com/user-attachments/assets/4f939f73-68f6-42c2-abd1-600ea3720c60)


