🕵️ Field Reports Mayhem — CTF Writeup
Challenge Name: Field Reports Mayhem
CTF Description:

We've gained access to the Juche Jaguar’s Field Reports archive through an operative's use of weak credentials. Upon logging in, the operative sees their previous field reports and can file new ones. Somewhere in here, I am sure some 'leet' agent stashed the Supreme Leader's secret pizza discount code!

Access Portal: http://35.245.106.190/login.html
Credentials:

Username: 1234  
Password: spudpotato

🧠 Initial Approach
During the competition, I managed to log in with the provided weak credentials and gained access to the portal. The page displayed some field report entries and a form to submit new ones. I explored the interface but wasn’t able to find the flag immediately.

Unfortunately, I ran out of time during the CTF. However, after revisiting the challenge post-competition, I noticed a crucial clue in the prompt — the term "leet".

💡 Post-CTF Discovery
Anyone in the hacking community knows that "leet" is a reference to the number 1337. That number turned out to be the key.

By inspecting the page’s structure and tampering with the ID values associated with reports or users, I changed the report ID in the URL or form submission to 1337. Once I submitted that value and interacted with the selections on the page (such as toggling dropdowns or clicking report entries), the hidden flag was revealed.

![image](https://github.com/user-attachments/assets/6c0eb7d0-bd1a-4291-a3d1-331b03a080ec)

🏁 The Flag
The Supreme Leader’s secret pizza discount code — aka the flag — was embedded in the report for ID 1337.

🔍 Lessons Learned
Pay attention to subtle hints in challenge descriptions — even a single word like "leet" can unlock the entire challenge.

Don’t ignore manual ID manipulation; sometimes it’s just that simple.

Returning to a challenge after the competition can still be a great learning experience and help improve pattern recognition for future CTFs.
