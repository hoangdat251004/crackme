First, when run program is show a screen with status “UN-REGISTERED”.

Then find the code that lead to screen print that status like this. 

![image](https://github.com/user-attachments/assets/93fe0222-768c-4c8f-b433-0805ed198dbd)

![image](https://github.com/user-attachments/assets/592f221d-c140-4332-a256-e9f26f50c7fb)

Above the code print the status, we can see a `jump` command that triggered by a `cmp` command the jump command will be taken if the value at address [7260D0] equal to 0.

![image](https://github.com/user-attachments/assets/cd3dd3ba-a2e2-4d99-b21a-0ccb0a7ce27f)

So I add a breakpoint to the command above to see what happens.

I run over each instruction, I see that `cmp` result to a true that why the `ZF` is set to 1. 

That will trigger the jump command and run over the good message and come to the bad message.

![image](https://github.com/user-attachments/assets/c158c607-fde5-4922-a9bd-7c7c116f2daa)

In the previous I just changed the command and patched the program to make it run correctly.

But now in this case I will do the other method to make it run correctly. It’s puts hardware breakpoints on memory addresses and then patch it to register the program.

To do it we need to find the address that make the result compare come true, here is the way we find that address in this case. We need to know what is the value in that address.

![image](https://github.com/user-attachments/assets/aecaacfb-16b4-4368-a9a1-277a031288cd)

Here we can see the memory address. And the value in the address is 0 so that why the jump is taken and program print that “UN-REGISTERED” message.

![image](https://github.com/user-attachments/assets/1db0d129-7783-4b7d-9881-b7cd37121507)

To put a hardware breakpoint we right click on the value like this. Because value in the address is 1 byte so we just need choose type is byte. Then remove the breakpoint I just added above.

![image](https://github.com/user-attachments/assets/348f18a3-532a-4342-afd0-cd8be867999f)

Then click restart and run again this way work like we put breakpoint in the instruction.

![image](https://github.com/user-attachments/assets/4f57a65c-5553-4ae0-87b5-753bcd558465)

To make the jump not work we need to change value in the address that is being compared to 0. To edit we right click to the value we want to change go to `binary` then `edit` then change value to another different to 0.

![image](https://github.com/user-attachments/assets/65975ad7-a701-4621-8444-fa6f72c56d54)

Patch the program and run it again we can gain “REGISTERED” message.

![image](https://github.com/user-attachments/assets/ee2274e0-b601-4861-8610-6a9e250240be)
