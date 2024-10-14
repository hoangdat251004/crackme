In first run it automatically show this screen. There is one file is create let use xAnalyzer plugin to see how the program run.

![image](https://github.com/user-attachments/assets/115cabc6-27d1-48c7-baa0-7e72e43f4f30)

Select the code and right-click, choose xAnalyzer -> analyse selected.

![image](https://github.com/user-attachments/assets/0a7708b9-e6ee-4b4a-bf2d-be5e6363b4a3)

Now we can have a better look at the program.
 
After run 1-by-1 instructions I realize that prog will try to find a file name `Keyfile.dat` to read.

In this case there is no file, so the jump is not taken the ZF is 1, and show this message.

![image](https://github.com/user-attachments/assets/70f8ad26-7bf5-4fc9-ab27-8ed84dd33141)

![image](https://github.com/user-attachments/assets/bb01c8c4-93a9-4add-94a5-8a28696d9df4)

Now create a blank file like this

![image](https://github.com/user-attachments/assets/6b962afe-f490-4a85-acd9-7f8bbc581603)

Run again, because there is nothing in this file so program cant read to compare the key and this screen show up.

![image](https://github.com/user-attachments/assets/2723e1d4-a456-456c-8d2f-5e93a0858707)

Here is a function to check the content of file, cause file is blank so the jump is taken and shows up the screen like above.

![image](https://github.com/user-attachments/assets/37e78bb3-7533-4176-8403-19f3155346a7)

Let’s look at this function

![image](https://github.com/user-attachments/assets/41397394-bb80-469b-8cfb-cfe197630aae)

We can see it is a function to read each character in this file, the important is the length of the content in the file must be 16 characters 10 in hexa if not it will break out the funtion, and there is a counter `esi` that take 8 first characters compared to character `G` is 47 in hexa. If the esi counter is less than 8 it also jump to the bad message, that mean the file has to have at least 8 character `G` to jump to the good message.

![image](https://github.com/user-attachments/assets/046c4464-ea27-427e-82de-81fed03ff65a)

To do this let’s change the content of file to this and see what happens.

![image](https://github.com/user-attachments/assets/25e12957-cf64-41ed-98d6-52c7b42f2b83)

As we can see here it will take each one character to compare until the end of content.

![image](https://github.com/user-attachments/assets/28b114e7-ca34-4cb0-877b-7160146e6576)

After 8 loops compare 8 first characters to `G` the `esi` increase to 8 and stop increasing from here.

The function keeps compare each character to the `null terminator :0` this will show up if there no more characters to be read.

![image](https://github.com/user-attachments/assets/874d6305-93cb-4575-8987-5ea6af1d10b8)

![image](https://github.com/user-attachments/assets/b4c15d0b-5780-485c-82d6-a65191892334)

When break out the loop program will compare the esi counter to 8 to confirm that is the file has 8 characters G then take a jmp to the following message.

![image](https://github.com/user-attachments/assets/35c24f1f-1450-4909-a010-afb824283a5a)
