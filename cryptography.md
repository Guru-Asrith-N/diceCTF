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
