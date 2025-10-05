              TryHackMe — Neighbour (Walkthrough)
1) find open ports using nmap
Run: nmap 10.201.56.156
Screenshot:<img width="1719" height="991" alt="Screenshot 2025-10-04 at 6 08 40 PM" src="https://github.com/user-attachments/assets/be10ae7e-6d6d-47df-96e3-7640238a23f2" />
 Nmap shows 22/tcp (ssh) and 80/tcp (http) open.



2) Visit the web app
Open http://10.201.56.156 in the AttackBox browser.
Screenshot:<img width="1721" height="987" alt="Screenshot 2025-10-04 at 6 11 15 PM" src="https://github.com/user-attachments/assets/d6bbdf89-1b71-4baf-93ff-f06dbde3e249" />
 Login page — note the hint: "Use the guest account (Ctrl+U)".



3) Check the page source for hints
Press Ctrl+U (View Page Source) and look for comments or hard-coded credentials.
Screenshot:<img width="890" height="947" alt="Screenshot 2025-10-04 at 6 15 02 PM" src="https://github.com/user-attachments/assets/306a1ba7-8093-4b6a-b201-21d4477feffd" />
<img width="880" height="739" alt="Screenshot 2025-10-04 at 6 16 25 PM" src="https://github.com/user-attachments/assets/3c46246c-2e0e-48dc-a5c1-a6def566e747" />
Page source reveals a comment with credentials: guest:guest — immediate info disclosure.



4) Log in with the guest account
Use the discovered credentials guest:guest on the login form.
Screenshot:<img width="1715" height="930" alt="Screenshot 2025-10-04 at 6 17 31 PM" src="https://github.com/user-attachments/assets/bea4cc61-cfe3-4b10-8dfa-d042865ab47b" />
<img width="1714" height="959" alt="Screenshot 2025-10-04 at 6 18 10 PM" src="https://github.com/user-attachments/assets/6663f774-82dc-4a4e-9e60-e6315235ebe5" />
login using the guest account.




5)While logged in as guest, open:
http://10.201.56.156/profile.php?user=guest
Edit the URL to replace guest with admin:
http://10.201.56.156/profile.php?user=admin
