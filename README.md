📄 Step 2: Create a Password File
nano passwords.txt


Insert:

user1:5f4dcc3b5aa765d61d8327deb882cf99
user2:e99a18c428cb38d5f260853678922e03


Save → Ctrl + X → Y → Enter

🔓 Step 3: Crack Passwords
john --format=raw-md5 passwords.txt


Output example:

user1:password
user2:abc123

👁️ Step 4: View Cracked Results
john --show --format=raw-md5 passwords.txt

🧾 Step 5: Custom Wordlist
nano wordlist.txt


Add:

password
123456
password123
admin


Clear previous results:

rm ~/.john/john.pot


Run with wordlist:

john --wordlist=wordlist.txt --format=raw-md5 passwords.txt

💡 Reflection

This lab shows how quickly weak passwords are cracked, reinforcing the need for strong, unique, and regularly changed credentials.

🧹 Cleanup
rm passwords.txt wordlist.txt


✅ You have successfully performed password cracking with John the Ripper.


---

Would you like me to:
1. Generate this complete **GitHub repository as a ZIP** (with all folders, Markdown, and placeholders)?  
2. Or just output the `README.md` files for each lab so you can copy them into GitHub manually?
