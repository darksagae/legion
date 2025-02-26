# legion
**Legion** is a powerful open-source penetration testing tool included in Kali Linux. It provides a GUI for managing various penetration testing tasks, particularly focusing on network reconnaissance and vulnerability scanning.

### Installation

If Legion is not already installed on your Kali Linux system, you can install it using:

```bash
sudo apt-get install legion
```

### Basic Usage

Legion is user-friendly and operates through a graphical interface. To start Legion, simply run:

```bash
legion
```

### Features

1. **Target Management**: You can add targets manually or import them from files.
2. **Service Enumeration**: Legion can perform service enumeration on identified hosts.
3. **Vulnerability Scanning**: It integrates with various scanners to identify vulnerabilities.
4. **Exploit Frameworks**: It can utilize frameworks like Metasploit for exploitation.

### Common Tasks and Examples

1. **Adding Targets**:
   - You can add a target by entering an IP address or a range in the "Targets" tab.

2. **Service Enumeration**:
   - After adding a target, navigate to the "Service" tab and select the enumeration methods (e.g. Nmap, Netcat).
   - **Expected Output**:
     - You will see a list of open ports and services running on the target.

3. **Vulnerability Scanning**:
   - Select the target and go to the "Vuln" tab to choose a vulnerability scanner.
   - **Expected Output**:
     - A report detailing any vulnerabilities found, including severity levels.

4. **Exploitation**:
   - After identifying vulnerabilities, you can use the "Exploit" tab to launch attacks using integrated tools.
   - **Expected Output**:
     - Results from the exploitation attempts, such as successful access or further enumeration.

### Conclusion

Legion is a versatile tool for penetration testing, offering an intuitive interface for managing tasks from reconnaissance to exploitation. Its integration with various scanning and exploitation tools makes it an essential asset for security professionals.

For detailed guidance, refer to the [Legion GitHub Repository](https://github.com/GoVanguard/legion) for documentation and updates.






                                                     ALTERNATIVE
Legion is a Kali Linux tool that provides a graphical user interface (GUI) for various security testing and penetration testing tools. It aims to simplify the process of launching and managing these tools, making it more accessible for both beginner and experienced security professionals.

Here's how to use Legion and some examples with expected output:

**Installation**
Legion is usually pre-installed on Kali Linux. If not, you can install it using the following command:

```
sudo apt-get install legion
```

**Launching Legion**
To launch Legion, you can run the following command in the terminal:

```
legion
```

This will open the Legion GUI, which consists of several tabs and modules for different security tools and tasks.

**Using Legion**
1. **Information Gathering**
   - In the Legion GUI, click on the "Information Gathering" tab.
   - Here, you'll find various tools like Nmap, DNSRecon, and Whatweb.
   - For example, to run Nmap on a target, select the "Nmap" module, enter the target IP or domain, and click "Run".
   - **Expected Output:**
     ```
     Starting Nmap scan on 192.168.1.100
     Nmap scan report for 192.168.1.100
     Port     State Service
     22/tcp   open  ssh
     80/tcp   open  http
     443/tcp  open  https
     ```

2. **Vulnerability Analysis**
   - In the "Vulnerability Analysis" tab, you'll find tools like Nikto, Searchsploit, and Sqlmap.
   - For example, to run Nikto on a target, select the "Nikto" module, enter the target URL, and click "Run".
   - **Expected Output:**
     ```
     Starting Nikto scan on http://example.com
     + Target IP:          192.168.1.100
     + Target Hostname:    example.com
     + Target Port:        80
     + Start Time:         2023-02-26 12:34:56
     + Scan Completed Time:2023-02-26 12:35:12
     + Bugs in 0 URLs
     ```

3. **Exploitation**
   - The "Exploitation" tab contains tools like Metasploit, Sqlmap, and MSFvenom.
   - For example, to use Metasploit, select the "Metasploit" module, choose an exploit and a payload, configure the options, and click "Launch".
   - **Expected Output:**
     ```
     Starting Metasploit module: exploit/windows/smb/ms17_010_eternalblue
     [*] Started reverse TCP handler on 192.168.1.101:4444
     [*] 192.168.1.100:445 - Connecting to target for exploitation...
     [*] 192.168.1.100:445 - Exploiting target...
     [+] Exploit completed, a shell is now open!
     Microsoft Windows [Version 10.0.17763.737]
     (c) 2018 Microsoft Corporation. All rights reserved.

     C:\Windows\system32>
     ```

Legion provides a user-friendly interface to access and manage a wide range of security tools. By organizing these tools into different tabs and modules, Legion simplifies the process of performing various security tasks, making it easier for both beginners and experienced users to leverage the power of Kali Linux tools.





                                            ALTERNATIVE
Legion is a Kali Linux tool used for network reconnaissance and discovery. It's a wrapper around several other tools, including masscan, nmap, and dnsrecon, to provide a comprehensive view of a target network.

**Basic Usage:**
The basic syntax for using Legion is:
```
legion <target>
```
Here, `<target>` can be an IP address, a hostname, or a network range.

**Examples:**

1. **Basic Scan:**
To perform a basic scan on a single IP address:
```
legion 192.168.1.1
```
This will run a series of scans using masscan, nmap, and dnsrecon to gather information about the target host.

2. **Scanning a Range of IP Addresses:**
To scan a range of IP addresses, for example, 192.168.1.1 to 192.168.1.254:
```
legion 192.168.1.1-254
```
This will scan all IP addresses in the specified range and provide a comprehensive report.

**Output:**
The output of Legion will vary depending on the target system's configuration and the options used. However, it typically includes information such as:

* Open ports and services
* Operating system and version
* Device type and vendor
* DNS records and domain information
* Network topology and mapping

Here's an example output:
```
Legion Scan Report:

Target: 192.168.1.1

**Masscan Output:**
PORT      STATE SERVICE
22/tcp    open  ssh
80/tcp    open  http
111/tcp   open  rpcbind
139/tcp   open  netbios-ssn
445/tcp   open  microsoft-ds

**Nmap Output:**
OS: Linux 3.10 - 3.14
Device type: general purpose
Running: Linux 3.X|4.X

**Dnsrecon Output:**
DNS Records:
  A Record: 192.168.1.1 -> example.com
  NS Record: example.com -> ns1.example.com
  MX Record: example.com -> mail.example.com
```
This output provides a comprehensive view of the target host, including open ports, operating system, device type, and DNS records.

Remember to use Legion responsibly and ethically, as it can be used to gather sensitive information about target systems. Always ensure you have permission to scan a target network or IP address.


                                        ALTERNATIVE
Legion is a semi-automatic network penetration testing framework included in Kali Linux. It is designed to perform tasks such as discovery, reconnaissance, and vulnerability assessment. Legion integrates various tools and scripts to facilitate penetration testing, making it a versatile option for security professionals.

### How to Use Legion

1. **Installation**:
   Legion can be installed using Docker or through a traditional installation method. The Docker method is recommended due to its simplicity and reduced dependency issues. Here’s how to install it using Docker:

   ```bash
   sudo apt-get update
   sudo apt-get install -y docker.io python-pip
   sudo groupadd docker
   pip install --user docker-compose
   git clone https://github.com/GoVanguard/legion.git
   cd legion/docker
   chmod +x runIt.sh
   ./runIt.sh
   ```

   For traditional installation, you can use:

   ```bash
   git clone https://github.com/GoVanguard/legion.git
   cd legion
   sudo chmod +x startLegion.sh
   sudo ./startLegion.sh
   ```

2. **Launching Legion**:
   After installation, you can start Legion by running:

   ```bash
   ./startLegion.sh
   ```

   This command opens the Legion dashboard, which is divided into three main sections: input, output, and logs.

3. **Performing Scans**:
   - **Adding Hosts**: In the input section, you can add single IPs, multiple IPs, or ranges of IPs. You can choose between "easy" and "hard" modes, where "hard" mode allows for more advanced scanning options.
   - **Scan Options**: The "Scan" option performs host discovery, information gathering, and vulnerability scanning. You can specify parameters such as service/version detection and OS detection.

4. **Analyzing Results**:
   The output section displays the results of your scans. You can view details such as host status, MAC addresses, and operating system information. Additionally, you can explore vulnerabilities by clicking on the relevant tabs in the output section.

### Example Usage

1. **Adding Hosts**:
   Suppose you want to scan a range of local network IPs. You would add the range in the input section and select "hard" mode with custom port scanning options.

2. **Initiating a Scan**:
   After configuring your scan options, you would initiate the scan. As the scan progresses, live hosts will populate in the left section of the interface, while the right section displays detailed scan results.

3. **Viewing Vulnerabilities**:
   By clicking on the "Nikto" module tab, you can view any vulnerabilities detected during the scan, which may include potential attack vectors against the target systems.

### Conclusion

Legion is a powerful tool for network penetration testing, offering a user-friendly graphical interface and a modular approach to security assessments. Its ability to integrate various tools and automate scanning processes makes it a valuable asset for cybersecurity professionals.

---
Learn more:
1. [Legion Tool in Kali Linux - GeeksforGeeks](https://www.geeksforgeeks.org/legion-tool-in-kali-linux/)
2. [Network Penetration Testing with Legion Framework](https://www.hackingloops.com/legion-framework/)
3. [Exploring Kali Linux: NMAP, Wireshark, Legion, Nikto, and - Course Sidekick](https://www.coursesidekick.com/information-systems/1069451)
