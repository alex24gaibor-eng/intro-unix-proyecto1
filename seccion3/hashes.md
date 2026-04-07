#Comparative Table of Hashes and Hashcat Results

+--------------------------------------+----------------------------------------------+--------------------------------------------------------------+
| Activity                             | Details / Commands                           | Results and Observations                                     |
+--------------------------------------+----------------------------------------------+--------------------------------------------------------------+
| Integrity Verification               | sha256sum [file] vs. Official Hash           | Success: Hashes match exactly. File integrity confirmed.     |
+--------------------------------------+----------------------------------------------+--------------------------------------------------------------+
| Avalanche Effect                     | Modify 1 byte using xxd                      | Total Change: A minimal modification produced a completely   |
|                                      |                                              | different hash.                                              |
+--------------------------------------+----------------------------------------------+--------------------------------------------------------------+
| Dictionary Attack (Low Entropy)      | hashcat -m 0 -a 0 hash_low.txt rockyou.txt   | Cracked in 12 seconds. Password: 12345678.                   |
|                                      |                                              | Speed: 1226 H/s.                                             |
+--------------------------------------+----------------------------------------------+--------------------------------------------------------------+
| Brute Force Attack (Medium Entropy)  | hashcat -m 0 -a 3 hash_medium.txt ?a?        | Not cracked. Estimated time: 12 years and 246 days.          |
|                                      |                                              | Process stopped after 30 minutes.                            |
+--------------------------------------+----------------------------------------------+--------------------------------------------------------------+
