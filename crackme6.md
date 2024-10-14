This crackme also make me register and remove nag screen.

![image](https://github.com/user-attachments/assets/d4bc8498-c10d-4143-a17e-8eb625e96edd)

To go through the nag and bullshit screen, I change the jump command from `je` to `jne`at [74 1A] and [74 27]. I also do the same at [75 1A] and [75 22]

![image](https://github.com/user-attachments/assets/cf506f33-0d60-4d74-8f15-ef89354bff5d)

![image](https://github.com/user-attachments/assets/021f3a12-1c43-447c-b553-01c50caf5a4d)

Here is the result I got after patching the file after change command.

No nag screen, status change to “Clean crack”, “Thank you” windows open when click re-check.

![image](https://github.com/user-attachments/assets/93cd32f1-18e9-4dc0-82a0-4406a9b4aeda)
