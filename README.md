
# Network Analysis with WireShark

## Objective
Analyzing HTTP and SMTP for malware infection of the Agent Tesla variant infection
<img width="475" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/c79cbd74-c3ba-43cc-8c9b-ecdfbadf0b9b">



### Skills Learned

- Identifying victim's MAC addresses
- Identifying victim's Host name
- identifying victim's account name
- Identifying when the  malicious traffic started
- Identifying how much RAM the victim's host has
- Identifying CPU used by the victim's host.
- Identifying the type of account login data that was  stolen by the malware

### Tools Used
- Wireshark
## Steps
- Finding the victim's IP and MAC address with the filter http.request or tls.handshake.type eq 1  this filter in Wireshark is displaying packets that are either HTTP requests or TLS handshake packets with a handshake type of 1 . This filter is useful for analyzing network traffic to identify HTTP activity or to inspect the initiation of TLS connections. Thus showcasing the IP and MAC address as shown on the screenshot 
-<img width="861" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/8aef7281-8529-4f22-98fb-4383addf259b">
- Finding victim's windows host name  using nbns(netbios name server),SMB and SMB2. Therefore  this filter in Wireshark is displaying packets that are related to either NetBIOS Name Service (NBNS), Server Message Block (SMB), or SMB2 protocol activity. This filter is useful for analyzing network traffic in Windows environments as shown
- <img width="1720" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/382aa328-f581-4cbf-937e-ef713074f41a">
- Next will Identify the date when the malicious traffic started,the victims account name, RAM,CPU used, the victim's account name login. The data  was stolen by the malware using smtp, as shown  in the diagram smtp was where Data exfiltration occured. The steps here are; select follow and then select TCP stream 
-<img width="856" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/6e1e0b73-c5be-4a39-a5d3-d982ad22ab03">
-<img width="1131" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/02ac8d10-eec3-4981-ac20-dd73a922e226">
- Further exporting   the email from wireshark , Go to file, Export objects and select IMF which gives a display of the email thus save the email first inorder to access
- <img width="765" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/e56b7f9a-b3c4-48bb-9242-b60013737455">
- Now opening up the email
- <img width="571" alt="image" src="https://github.com/chromosems/Network-analysis-with-Wireshark/assets/44053943/9a45d389-761e-42f4-b83b-1caed5ec0dbd">
*Ref : Downloaded email display*

In conclusion this project has enhanced my skills working with wireshark to perform packet analysis to identify specific details.




