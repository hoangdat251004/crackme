The crackme12 using a anti-debugger technique so if we run it in debugger it will show this message and quit.

picture

To solve we got 2 method first one is find the api for the anti-debugger and patch it another one is using a plugin to bypass.

For the first method I will set a breakpoint to the api call the anti-debugger is `bp IsDebuggerPresent`.

![Screenshot 2024-10-11 132924](https://github.com/user-attachments/assets/4deeeece-4ef5-440d-b123-e5b66f8027b1)

Hit `Enter`

![Screenshot 2024-10-11 133004](https://github.com/user-attachments/assets/5023b202-348a-4846-ba9a-3dc5729850f3)

Click `run`

![Screenshot 2024-10-11 133027](https://github.com/user-attachments/assets/e5a9657c-132f-4db8-a91a-1dfc20d20321)

![Screenshot 2024-10-11 133044](https://github.com/user-attachments/assets/aa483b2d-89cc-4d1f-99b0-b3c159d74466)

I can go to the api call.

Now click to `run to user code` the symbol is the face.

![Screenshot 2024-10-11 133127](https://github.com/user-attachments/assets/56e3c0f9-3ae6-4570-95e2-6d69249faf0d)

I can run into the code that analyse the anti-debugger api.

![Screenshot 2024-10-11 133920](https://github.com/user-attachments/assets/8e0eded2-3341-46dc-a479-4385da8d3732)

![image](https://github.com/user-attachments/assets/3e20afaa-df32-4eb5-8ce4-98a44b9e7861)

As we can see here the jump will not be taken because the eax is set to `1` and the bad message will show up rigth after this.

To solve this we can just simple assemble the jump from `je` to `jmp` to make the jump taken and run to good message like this.

![image](https://github.com/user-attachments/assets/f112c344-5790-4b83-bf00-7f65b51bdc21)

Press `F8` we can see jump is taken

![image](https://github.com/user-attachments/assets/bafb21dd-7ca0-444f-bc40-22167af0ec9e)

And good message is now show up

![image](https://github.com/user-attachments/assets/bc898cda-f04a-46f2-87ae-ce45b6342127)

Patch the file and run it in debugger, the good message will show instead of bad message.

![image](https://github.com/user-attachments/assets/9e85546d-8501-4c64-b151-408ee90d034f)

Method 2 is using plugin to bypass, here I use ScyllaHide

First we open it and choose basic option, click ok and ok

![Screenshot 2024-10-11 142001](https://github.com/user-attachments/assets/959980f7-f84e-460c-a486-fec7b3ee1856)

![Screenshot 2024-10-11 142019](https://github.com/user-attachments/assets/2de4b572-b92c-4ecd-913e-19d76417bf1a)

![Screenshot 2024-10-11 142028](https://github.com/user-attachments/assets/6390011e-954d-4ceb-abea-0b1e07155b46)

Now just run as normal the plugin has bypassed the anti-debugger easily.

![Screenshot 2024-10-11 142551](https://github.com/user-attachments/assets/40e4c7dd-61c0-4fa8-94f6-0b5592dfa1b4)
