![Screenshot 2024-10-10 234755](https://github.com/user-attachments/assets/a1a57d06-68e0-407e-afca-00abf5fd2a03)

Crackem 2 make me register the software.

Found the code that pop the message above I found a usefull command is `CreateFileA`, this is a api of windows, it has function to create a file or find a file by a name and return value that the file is exist or not, here it find the file name `keyfile.txt`.

I create a blank file with that name at the same folder like this and this happen.

![Screenshot 2024-10-10 235026](https://github.com/user-attachments/assets/0d03e1c7-c243-4e6e-9706-0566e2331b36)

![Screenshot 2024-10-10 235046](https://github.com/user-attachments/assets/7700a9ca-60d1-4255-ab74-8c347729000e)

It like the program read the content of that file.

After analysis the program by xAnalyzer I found the program read content of file and take that as the resgister name.

![Screenshot 2024-10-10 235517](https://github.com/user-attachments/assets/47d5ffd5-c103-4ee1-af4c-3bcd83692baa)

And here after I add content in the file

![Screenshot 2024-10-10 235904](https://github.com/user-attachments/assets/3ed92693-ee7f-42a9-948f-5d1e5f2b4193)

![Screenshot 2024-10-10 235911](https://github.com/user-attachments/assets/a236b496-3959-43ef-8106-2aa6f27d86fd)
