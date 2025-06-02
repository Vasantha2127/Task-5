# Task-5
Wireshark is a widely used network protocol analyzer that allows users to capture and inspect packets in real time. It is commonly utilized for troubleshooting network issues, performing security analysis, and learning protocol behavior by providing detailed visibility into network traffic.

To begin the network analysis process, Wireshark was installed on the system.

After connecting to a Wi-Fi network, I initiated packet capture in Wireshark without accessing any websites beforehand. Despite this, several packets were captured, indicating background network activity or system-level communications.

Subsequently, I accessed the website http://testphp.vulnweb.com/userinfo.php to analyze HTTP packet transmission. Since the website does not use HTTPS encryption, I was able to capture and inspect the transmitted username and password in plaintext using Wireshark. This demonstrates how unsecured websites can expose sensitive user credentials to potential attackers monitoring network traffic.

Following the initial capture, I applied protocol-specific filters in Wireshark to isolate DNS, TCP, and UDP traffic. This allowed for focused analysis of each protocol's packet behavior. The filtered results showed that:

DNS packets were used for domain name resolution, typically sent over UDP port 53.

TCP packets established reliable connections, such as those used in HTTP communication and web-based logins.

UDP packets were observed in connectionless services, including DNS queries and other lightweight communications.

This filtering approach enabled a better understanding of the different types of packets transmitted over the network and their respective purposes.

The captured network traffic was then saved to a file named capture.pcap for further analysis and documentation. Storing the capture in .pcap format allows for easy review and sharing using tools like Wireshark or tcpdump.

Conclusion 

The network traffic analysis revealed multiple background activities occurring even before website access. Upon visiting the unsecured website http://testphp.vulnweb.com/userinfo.php, sensitive information such as usernames and passwords were transmitted in plaintext, exposing significant security risks. Filtering the captured data by DNS, TCP, and UDP protocols provided insight into domain resolution, connection-oriented communication, and lightweight packet exchanges respectively. The capture was saved as a .pcap file for detailed examination and future reference. Overall, this exercise highlights the importance of secure communication protocols to protect user data from interception.
