<p align="center">
  <img src="https://github.com/osu/cybersci-2024/blob/main/img/cybersci.png" alt="Cybersci-2024" width="80%">
</p>


<p align="center">
  <b>Fall 2024 Challenges and Writeups</b>
</p>


Crypto 🔐

Leaked and Loaded (100 Points) - SOLVED

💡 Prompt:
One of the opposition’s candidate’s campaign managers considers themselves to know a lot about security! So before they sent an email to their colleague with their account password, they decided to “protect” it first. Can we retrieve the passcode?

📜 Flag Format: cybersci{[A-Za-z0-9_-]+}

Parts (930 Points)

💡 Prompt:
We’ve intercepted this high-profile message. Can you find anything of value?

📜 Flag Format: cybersci{[A-Za-z0-9_-]+}

Cloud ☁️

Voter Emailer 1 (100 Points) - SOLVED (too late)

💡 Prompt:
We’ve been trying to leverage AI to help automate emailing voters to ensure they know all the important campaign dates and details.
	•	A developer has set up a FastAPI endpoint at http://10.0.2.21:8000. The VM should have restricted access to https://rgnl2025voteremailer.blob.core.windows.net/voters/voters.txt, but we suspect they misconfigured it.

🧐 Question: What is the request URL for the tool calling?

📜 Answer Format: http://10.0.2.21:8000/<PathValueHereWithoutParameters>

Web 🌐

Ballot Scanner 1 (100 Points) - SOLVED

💡 Prompt:
This ballot scanner is top-notch. Nothing has come up in TESTING that would alarm anyone.

🔗 URL: https://10.0.2.41

Ballot Scanner 2 (100 Points) - PARTIALLY SOLVED

💡 Prompt:
We need to validate the BALLOT COUNT for auditing purposes.

🔗 URL: https://10.0.2.41

Ballot Scanner 3 (1000 Points) - PARTIALLY SOLVED

💡 Prompt:
What else can you find?

📜 Flag: Serial number of the ballot scanner machine.

🔗 URL: https://10.0.2.41

Forensics 🔍

Data is the New Currency 1 (100 Points) - SOLVED

💡 Prompt:
Corrupt government officials are offering the voter information as a service for a profit. You have been tasked with uncovering this hidden service.

💡 Hint: The two types of crypto used are AES CBC and RSA.

🧐 Question: What file is sent to the customer, who just purchased access to the voter information service?

📜 Answer Format: Full path

Data is the New Currency 2 (1000 Points) - PARTIALLY SOLVED

💡 Prompt:
Corrupt government officials are offering the voter information as a service for a profit. You have been tasked with uncovering this hidden service.

💡 Hint: The two types of crypto used are AES CBC and RSA.

🧐 Question: What is the occupation of Tatiana Castro?

Spyware 1 (826 Points) - PARTIALLY SOLVED

💡 Prompt:
We have received intelligence that someone has planted a malicious application on the Electoral Commission’s server (10.0.2.52). Please help us identify it and figure out what it does.

🧐 Question: Analyze the machine, find this malicious application, and report its full path.

💻 Command: ssh -i defence_ed25519 vpcadmin@10.0.2.52

Defence 🛡️

Voter Registry 2 (793 Points) - SOLVED (too late)

💡 Prompt:
The Central Electoral Commission hosts a Voter Registry website that they asked us to test. The attacks that we tried have yielded a number of vulnerabilities that you need to help us fix.

🔗 Attack Portal: http://10.0.2.50
🔗 Voter Registry Website: https://10.0.2.52

💻 Command: ssh -i defence_ed25519 vpcadmin@10.0.2.52


