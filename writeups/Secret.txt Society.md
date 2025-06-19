🗂️ Secret.txt Society
🔍 Challenge: Juche Jaguar – Disallowed Discovery
Prompt:
Our team suspects that a Juche Jaguar developer accidentally left something interesting behind on a public site. You’ve been tasked with examining its structure. Can you uncover what the bots were told to ignore? Start with the usual entry points a crawler might explore. One disallowed path leads to a page where someone left behind more than just code.

Target URL: https://juche.msoidentity.com/

🧭 Objective
Investigate the website’s structure
Identify disallowed directories and hidden content
Find a page where someone left behind more than code (e.g., a flag or hidden file)

🛠 Tools Used
curl (to manually inspect robots.txt)
Browser/DevTools (to explore discovered paths)

🔬 Step-by-Step Walkthrough
✅ Step 1: Check robots.txt
Before brute-forcing directories, I checked robots.txt for hints about what the site is hiding:

curl https://juche.msoidentity.com/robots.txt

💡 The disallowed paths are often where devs hide incomplete or sensitive pages from search engines.

✅ Step 2: Launch DirBuster
If that didn't work (which it did), we would launch Kali Linux’s pre-installed DirBuster:

Applications → Web Application Analysis → DirBuster
Target URL:
https://juche.msoidentity.com/

Wordlist:
/usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

File extensions to search:
html,php,txt,js

![image](https://github.com/user-attachments/assets/0b13371c-9b91-4690-9908-cd72f578f4e5)

🏁 Flag
Flag: C1{r0b0ts_arent_4lways_p0lit3}

📚 Lessons Learned
Always inspect robots.txt early — it's a treasure map in CTFs.
Tools like DirBuster and Gobuster are perfect for uncovering hidden files and folders.
Sensitive content should never be protected by obscurity alone.
