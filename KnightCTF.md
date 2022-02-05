### This is a CTF that I participated myself, the main purpose is to gain more experience and skills on different kinds of CTF competition.
# Programming
## Keep Calculating
![image](https://user-images.githubusercontent.com/83162708/152657529-95e54b42-d2c4-4ef5-8fe9-fdd58642ce56.png)
</br> 
<b>Codes:</b>
</br>
![image](https://user-images.githubusercontent.com/83162708/152657552-8a020af4-ea79-4938-963f-8b752a55a560.png)
</br>
Flag: KCTF{2666664}

## Reverse The Answer
![image](https://user-images.githubusercontent.com/83162708/152658004-c19baa91-4866-4f69-9294-56fcf4ce45d0.png)
</br> My code: </br>
![image](https://user-images.githubusercontent.com/83162708/152658021-9c1cb03f-b368-4643-bda2-4215259cba53.png)
</br>
Flag: KCTF{12252696}

## Something In Common
![image](https://user-images.githubusercontent.com/83162708/152658034-d6dd228b-7dc6-41f6-ba94-c1aeec3763e7.png)
</br>
We will use online tool for this to find the GCD </br>
http://www.alcula.com/calculators/math/gcd/#gsc.tab=0 </br>
![image](https://user-images.githubusercontent.com/83162708/152658041-8db185f0-b12c-4b53-a392-f72c59fb0b3c.png)
</br>
`Calculation:
4+3+0+5+1+2+5 = 20` </br>
`Flag = 20 * 1234 = 24680`
Flag: KCTF{24680}


## Find the Number
![image](https://user-images.githubusercontent.com/83162708/152658132-9e881d63-e805-4b7b-9c2b-06e630cbe77c.png)
![image](https://user-images.githubusercontent.com/83162708/152658148-3267195a-91c8-4990-843c-3c63e91ae196.png)
</br>
Basically for this challenge we just have to write down the codes in the picture and calls it we will get the answer.

My code:

![image](https://user-images.githubusercontent.com/83162708/152658177-813ed7fc-f020-4634-bbb7-061299c5a8ce.png)

Flag: KCTF{1.9999999701976776}

# Networking
## Robots.txt
![image](https://user-images.githubusercontent.com/83162708/152658293-9747b414-6f09-4cf9-b3ec-6bc390fa8c0a.png) </br>
From the HTTP files we downloaded from compromised CTF Platform challenge, we are able to see this robots.txt:</br>
![image](https://user-images.githubusercontent.com/83162708/152658299-03014b84-92ae-4fda-a626-72ffad9f1c8b.png)
![image](https://user-images.githubusercontent.com/83162708/152658301-9dc0c80e-b771-4c16-81a7-375ed7aadf39.png)

Flag: KCTF{/includes/user.php}

## FTP Flag
![image](https://user-images.githubusercontent.com/83162708/152658409-2024cb08-7afe-4bed-be80-35d3eb45482f.png)</br>
From the wireshark from compromised CTF Platform challenge, we are able to follow follow the ftp-data and we got this:</br>
![image](https://user-images.githubusercontent.com/83162708/152658462-0844e4e1-294d-4229-b2d1-d72f5a58dc0f.png)

Suspected it was base64 encoded and we will use a decoder

![image](https://user-images.githubusercontent.com/83162708/152658523-10308281-554c-49ab-9641-82ecdd17ba32.png)

Flag: KCTF{P4SsW0rD_SH0ulD_B3_Str0nG_En0uGh_T0_gu3sS}


## How's the Shark?
![image](https://user-images.githubusercontent.com/83162708/152657949-bdcdc46d-3fc5-42c3-834e-c488b7d90416.png)
</br>
By opening up the Wireshark packet and View HTTP Object we are able to get this:
</br>
![image](https://user-images.githubusercontent.com/83162708/152657968-c0832cad-6fce-445f-8d42-a13d31eed9d2.png)
</br>
This caught my attention: “something%20something.png” </br>
After downloading it, I am able to get this:</br>
![image](https://user-images.githubusercontent.com/83162708/152657998-ad53275d-afcc-48f6-a920-96b3f42f8ec4.png)
</br>
Flag: KCTF{A_ShARk_iN_tHe_WirE}

## Compromised CTF Platform
![image](https://user-images.githubusercontent.com/83162708/152658211-65eb79bf-0a57-4f57-89ee-e06135de6129.png)
![image](https://user-images.githubusercontent.com/83162708/152658217-2fc49933-a745-41ef-8d79-bd31de49bee3.png)


Export all the HTTP objects and the last login caught my attention

![image](https://user-images.githubusercontent.com/83162708/152658242-95956ccb-eeed-492a-8b6c-a4ca25e94990.png)
![image](https://user-images.githubusercontent.com/83162708/152658250-de44ee0e-0ead-4078-9c17-f88d596c5b72.png)

We are able to get the username and password

Flag: KCTF{demo_demo}

# Steganography
## QR Code From the Future
![image](https://user-images.githubusercontent.com/83162708/152658541-13fc72f2-cc21-4616-94d0-ac2a449a77c8.png)
![Picture1](https://user-images.githubusercontent.com/83162708/152658787-3fbca828-ccd7-4e27-800e-8cce36a010e4.gif)

</br>
This is a very interesting challenges where the QR code keep on changing and I use this 2 tools to help me:

https://demo.dynamsoft.com/barcode-reader/ - for scanning multiple QR code

https://ezgif.com/split - split the gif into frames

We will able to get this from each QR code:

![image](https://user-images.githubusercontent.com/83162708/152658585-dd010943-26e5-4a45-a2d5-1307878e1b12.png)


Doesnt seen KCTF keyword, It seems encoded, I tried using ROT13

![image](https://user-images.githubusercontent.com/83162708/152658615-957cee9a-9d6a-4fb3-a6c7-58f380df606d.png)

We are able to get the KCTF keyword

After remixing we are able to get the flag.

Flag: KCTF{QR_code_got_evolved_from_static_to_dynamic}

# Cryptography
## Passwd
![image](https://user-images.githubusercontent.com/83162708/152657795-eadf4d84-a09e-4cf1-882d-46dbd3b692fd.png)
![image](https://user-images.githubusercontent.com/83162708/152657801-db682084-69d7-476c-988c-d552aada556b.png)
</br>
Password Hash: 708697c63f7eb369319c6523380bdf7a
</br>
By using Hash Analyzer we are akle to know that it is MD5:</br>
![image](https://user-images.githubusercontent.com/83162708/152657840-1ffe4f21-b9bb-4262-affc-8b98dcb36736.png)
</br>
The we will use MD5 Decrypter:
</br>
![image](https://user-images.githubusercontent.com/83162708/152657867-04a549f0-4b89-4034-ba5c-e1bccba5e262.png)
</br>
Flag: KCTF{exploit}

# OSINT
## Canada Server
![image](https://user-images.githubusercontent.com/83162708/152657896-1bc3b6d3-cbf3-40e0-b67b-62fdd895d575.png)
</br>
Using Google Search:
</br>
![image](https://user-images.githubusercontent.com/83162708/152657913-ab4b1f26-8226-4e11-9f0d-d0af56ca1fe9.png)
</br>
https://clients.nstechvalley.com
</br>
We are able to get this IP address: </br>
![image](https://user-images.githubusercontent.com/83162708/152657918-e576bd21-24c5-496e-842d-8f0d819de86f.png)
</br>
Flag: KCTF{192.99.167.83}

