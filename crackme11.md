This crackme packed and we have to unpack and crackthe serial key of it.

![Screenshot 2024-10-14 132646](https://github.com/user-attachments/assets/a6fbfb11-f552-4678-aee9-36624b109c50)

Take few minute to analyse the code I got the flow and try to change the code like this to make the taken and show the good message.

![Screenshot 2024-10-14 133103](https://github.com/user-attachments/assets/899806c1-4bcd-4b8e-8c36-152b76e51ce0)

But I can patch the file because it is packed.

![Screenshot 2024-10-14 133028](https://github.com/user-attachments/assets/e2887543-e135-489c-9efb-2ca00e60f63a)

Now we need unpack it that we can patch the file

Run again we look at the stack at the `EBP` we can see the real entrypoint

![Screenshot 2024-10-14 133513](https://github.com/user-attachments/assets/766f4929-45fe-4f19-a7fe-ff0ddf4f6b8f)

Look at the right-low section right click at the address -> Follow in dump

![Screenshot 2024-10-14 133547](https://github.com/user-attachments/assets/0e206187-8783-4c4b-bd1e-cdffaaf254e3)

![Screenshot 2024-10-14 133604](https://github.com/user-attachments/assets/a485fb39-0e04-45e9-9cb8-011e080152ac)

Choose the address and put a bp like this

![Screenshot 2024-10-14 133621](https://github.com/user-attachments/assets/ff8d199b-6000-40dd-9081-fe6b53f86476)

We got to this 

![Screenshot 2024-10-14 133647](https://github.com/user-attachments/assets/81f99542-9157-4f4b-b5ec-f19c5fbf1ee8)

Break out the loop

![Screenshot 2024-10-14 133705](https://github.com/user-attachments/assets/7a68786d-a9d6-4cf5-aa67-5a4e00b6c360)

We now in the real entry point, here we need to press `F8` one times to make `EIP` run to the instruction at the head of  red arrow.

![Screenshot 2024-10-14 134108](https://github.com/user-attachments/assets/12f2d06c-b8cd-4265-b936-a2e18026407b)

To unpack we click to the Scylla icon the red `S` icon

![Screenshot 2024-10-14 134129](https://github.com/user-attachments/assets/f0ccdc52-b81a-4bed-a838-9584a447f298)

Click Dump PE

Then click Search IAT

![Screenshot 2024-10-14 134558](https://github.com/user-attachments/assets/0848ecc0-ebce-430b-a8a9-898e40959363)

Get Import

![Screenshot 2024-10-14 134621](https://github.com/user-attachments/assets/483801a3-0046-401c-b7f8-4e3b5303808c)

Fix Dump, open the file at the step Dump PE

![Screenshot 2024-10-14 134655](https://github.com/user-attachments/assets/9fbcfaa5-fc0d-4309-9ad2-84e636dee018)

Now it unpacked

Open the unpacked file

![Screenshot 2024-10-14 134712](https://github.com/user-attachments/assets/f46d77fa-f4e1-4d49-a56e-198ba9d11de2)

Change the code normaly

![Screenshot 2024-10-14 134913](https://github.com/user-attachments/assets/05da7db1-7cff-4672-a726-452ed39a48be)

We now can patch the file

![image](https://github.com/user-attachments/assets/d5fc4e0b-6a67-45a9-aa46-842aade240bc)

And here the result

![Screenshot 2024-10-14 134941](https://github.com/user-attachments/assets/bc0015ef-9787-4dff-9f1f-8de8783bd534)
