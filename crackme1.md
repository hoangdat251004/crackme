Crackem 1 is a challenge to crack the serial key

![image](https://github.com/user-attachments/assets/52c9ae1a-c95f-446a-bf5a-45334973a548)

After few run to test the program I found the code that has function to check the serial key, and I also found the seial key right there

![Screenshot 2024-10-10 145646](https://github.com/user-attachments/assets/2699c02a-1daf-4464-ac20-c2f37fccd5be)

So the real serial key is cr4ckingL3ssons

![Screenshot 2024-10-10 145736](https://github.com/user-attachments/assets/bed152f8-2c9b-49fb-85a3-b79ab29a0f3e)

To make the program always show the congrats at any key I need to fix few thing.

First is the `jump`, I need to remove it and change the value at the `eax` register from `1` to `0` because if I just change the value in `eax` prog will corrupted the instructio will be overwrite to another instruction cause is nnot enough byte for that instruction here.

![Screenshot 2024-10-10 153129](https://github.com/user-attachments/assets/6438defd-c2c2-4436-b350-86e80e9362cb)

![Screenshot 2024-10-10 153308](https://github.com/user-attachments/assets/47c30619-8564-488d-a43b-871acf49f752)

I delete the `jump` command to get space for the `mov` command. The `jump` take 4 bytes and the `mov al, 0` take 3 bytes so that is the reason.

Then patch the file and got the result like this.

![Screenshot 2024-10-10 153444](https://github.com/user-attachments/assets/2cc1e653-45f7-4613-9821-260d7a22eb5e)

