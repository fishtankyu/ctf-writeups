## WIDE Category:Reversing

Lets see what type it is:
![image](https://user-images.githubusercontent.com/83162708/184398850-23e9e3c8-f40d-4e80-92e0-571d8d557854.png)
Its an ELB 64-bit LSB executable.

Strings inside:
![image](https://user-images.githubusercontent.com/83162708/184398944-3e947e4b-3789-4525-a5a6-659daceab6d9.png)
sup3rs3cr3tww1d3 looks interesting

Execute it and enter the decryption key and we get the flag.
![image](https://user-images.githubusercontent.com/83162708/184399060-c7cf6b66-9104-46ce-8449-e59fce0049ca.png)


## Compressor Category:Misc

There are few option to choose from but when we tried to choose the option 5 (cd <dirname>) it seems it doesn’t work at all.
![image](https://user-images.githubusercontent.com/83162708/184399448-ffc7bf05-13e8-46b3-a0e4-502a68949c72.png)

However something is interesting, which is option 2 cat ./name
I google search and found this, which means we can cat multiple files although they are from different directory

![image](https://user-images.githubusercontent.com/83162708/184399730-bdde37fb-01ff-439e-92ae-66ce58df0a4e.png)
Execute!
  
I tried:
qwe ; cat /home/ctf/Xxp80wAmE2bfwc3LYwvPelKScG2TAczo/flag.txt
qwe ; cat /home/ctf/flags.txt
qwe ; cat /home/ctf/flag.txt (This work!)

![image](https://user-images.githubusercontent.com/83162708/184399872-7e05f484-4f5c-497e-99e0-4c67234565f7.png)



  

