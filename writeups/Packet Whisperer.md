🦈Packet Whisperer🦈

📁 Challenge: Leaked Login (Network Forensics)
Description:
Our Blue Team intercepted a network capture file (login.pcap) containing unencrypted HTTP traffic. Analysts believe someone exposed their login credentials in plaintext. Your mission is to review the packet capture and extract the password.

🧠 Objective
Analyze the .pcap file

Isolate HTTP traffic

Find POST request(s) that reveal login credentials

Extract the password

🛠️ Tools Used
Wireshark (GUI packet analyzer)

tshark (terminal-based packet sniffer)

🔬 Step-by-Step Walkthrough
🧪 1. Load the PCAP File
Open login.pcap in Wireshark:
wireshark login.pcap

🔍 2. Filter HTTP Traffic
Use the filter:
http.request
This reveals all HTTP GET/POST requests.

🧵 3. Identify Login Request
Scroll through or search for a POST request to a login page:

Common endpoints: /login, /auth, /signin

Right-click the POST request → Follow → HTTP Stream

🔐 4. Extract the Credentials
Within the HTTP stream, inspect the request body:

POST /login HTTP/1.1
username=?&password=?

![image](https://github.com/user-attachments/assets/2ab538de-0101-4280-985d-7f7af2bf5ab5)

🔑 Credentials Found:

Username: ironpotatoadmin

Password: C1%7Bmaybe_TLS_would_be_nice%7D

🏁 Flag / Result
Here is the filtered flag:

C1{maybe_TLS_would_be_nice}

📚 Lessons Learned
Sensitive information (e.g., credentials) should never be transmitted over HTTP.

Always use HTTPS to secure login forms.

Network packet analysis can quickly uncover misconfigurations or bad practices.

📂 Repository Notes
File: login.pcap
Category: Forensics / Traffic Analysis
