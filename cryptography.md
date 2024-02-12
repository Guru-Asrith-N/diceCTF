# cryptography

### winter

opened the challenge  
downloaded the server.py file  
went through the code  
realised that the code is based on how signatures work  
the sk is the private key and vk is public key which is used to verify signatures  
the sk is made of 32 random numbers and you get vk by hasing sk 256 times  
after going through code realised that we need to generate a message1 that after hashing 256-n times should match with message2 after hashing n times and if the values are same we get the flag   
Didn't get what to do after this   
so went through writeups  

### rpscasino 

opened the challenge   
downloaded th file  
went through the file   
realised that the most important thing about the file is LFSR  
read about LFSR   
understood that the register shifts by 1 bit and the new bit is formed by XORing 2 other bits in the register and the bit which is shifted out is discarded   
from the code the length of state is 8 bytes or 64 bits   
```
for i in range(4):
			bit = (state ^ (state >> 1) ^ (state >> 3) ^ (state >> 4)) & 1
			state = (state >> 1) | (bit << 63)
```
from the above code 'bit' is formed by multiple shift and bitwise 'or' and bitwise 'and' operators   
the new state is then formed when the 'or' function is used with 'state shifted to right by one' and 'bit shifted to left by one '    
this process is repeated 4 times since for loop is used   
