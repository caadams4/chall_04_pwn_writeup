# chall_04_pwn_writeup
ret to register to win

Ok, ret to register to win. So, checksec -> no canary, no PIE. 

We open the binary with radare2 and see a 'gets' that writes to var_60 and a var_8 which is moved to rax, then rax is called.

We can smash through var_60 into var_8 ( rax ) which is then called. We want to make var_8 == the win function address. 

Ref screenshot for pwnage. 


![image](https://user-images.githubusercontent.com/79220528/159329022-39de6b3d-ac5e-4ee4-8708-d96836b6c91f.png)
