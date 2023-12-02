#Network Scanner
This Python script utilizes the Scapy library to perform a simple network scan. The scan is designed to discover devices on a given IP range. The script sends ARP (Address Resolution Protocol) requests to the specified IP or IP range and collects the responses to identify the corresponding MAC addresses.

##Prerequisites
Make sure you have Python installed on your machine.

Install the Scapy library using the following command:



pip install scapy
Usage
Open a terminal.

Navigate to the directory containing the script.

Run the script with the target IP or IP range:



python network_scanner.py -t <target>
Replace <target> with the IP address or IP range you want to scan.

##Options
-t, --target: Specify the target IP or IP range for the scan.
Example


python network_scanner.py -t 192.168.1.1/24
Script Details
get_arguments Function
Parses command-line arguments using the optparse module.
Requires the user to specify the target IP or IP range (-t).
scan Function
Crafts ARP requests for the specified IP or IP range.
Sends ARP requests using Scapy's srp function.
Collects and extracts information from the responses, including IP and MAC addresses.
print_result Function
Prints the scan results in a formatted table, displaying IP addresses and corresponding MAC addresses.
Example

$ python network_scanner.py -t 192.168.1.1/24
IP                   MAC ADDRESS
-----------------------------------------
192.168.1.1          00:11:22:33:44:55
192.168.1.2          12:34:56:78:90:ab
192.168.1.3          aa:bb:cc:dd:ee:ff
...
##Note
The script might require root privileges to execute the ARP scan.
Scanning larger IP ranges may take more time.
Disclaimer
This script is provided as-is and without any warranty. Use it responsibly and only on networks that you have permission to scan.

##Author
Ethan Robinson

##License
This project is licensed under the MIT License.





