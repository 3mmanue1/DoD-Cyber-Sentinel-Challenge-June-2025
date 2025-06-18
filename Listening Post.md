📡 CTF Challenge: Listening Post
Challenge Prompt:

We've intercepted a radio broadcast being bounced off a satellite likely intended for the North Torbian cells located around the world. Do you think you can unravel what they are transmitting?

🧩 Challenge Overview
We were provided with two audio files — both containing the same content in different formats. The audio featured a sequence of DTMF tones, which are the dual-tone signals used by telephones (the familiar "beeps" you hear when pressing buttons).

🔍 Step 1: Decoding the DTMF Tones
Recognizing the audio pattern as DTMF, I uploaded one of the files to an online DTMF decoder:

👉 https://dtmf.netlify.app/

This tool decodes DTMF tones in real-time. As the audio played, the tool displayed a stream of digits. In this case, the output was primarily composed of 1s and 0s — indicating that the message was encoded in binary.
![image](https://github.com/user-attachments/assets/6729979d-36bd-446c-9b91-5d760e70f0d1)

🧮 Step 2: Translating Binary to ASCII
After copying the full binary sequence, I used a binary-to-ASCII converter to interpret the message:

👉 https://www.rapidtables.com/convert/number/binary-to-ascii.html

Pasting the binary into the converter revealed the final message — the flag.
![image](https://github.com/user-attachments/assets/2bd96b35-edbd-4419-97b2-bfb38eab91b2)

🏁 Final Flag
C1{r4d1o_k1ll3d_th3_t0rb1a_st4r}
🛠️ Tools Used
🔊 DTMF Decoder — https://dtmf.netlify.app/

💻 Binary to ASCII Converter — https://www.rapidtables.com/convert/number/binary-to-ascii.html

🧠 Takeaways
This challenge was a clever use of audio steganography, leveraging a DTMF signal to transmit binary data. By breaking the problem into layers — signal recognition, binary decoding, and ASCII conversion — we were able to successfully extract the hidden flag.

