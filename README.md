# Cybersecurity and Networks Exercises

This repository contains a set of exercises focused on cybersecurity topics, particularly related to networks and vulnerability assesment.

### Prerequisites
Before running the scripts, make sure you have the following installed:
- Python 3.x
- Necessary Python libraries (`socket`, `argparse`, etc.)
- A Bash-compatible terminal for running the `.sh` script (i.e. GitBash for Windows)

# Repository Structure
## Network Scanning Exercise
This exercise demonstrates the basics of network communication, including how sockets and addressing work within a network.
The program scans a target IP address to identify which ports are open on devices in the network. It uses Python's socket module to attempt connections to common ports and reports their status (open or closed).
- `execute_network_scanner.sh`: A Bash script to execute the network_scanner.py Python script with predefined or user-specified parameters.
- `network_scanner.py`: A Python script for scanning a network to discover devices by their IP addresses and to identify open ports on a given target device.
## Chat Simulation Exercise
This exercise demonstrates how communication between a server and multiple clients works.
- `chat_server.py`: A Python script implementing the logic of a server that receives messages from clients and broadcasts those messages to all other connected clients.
- `chat_client.py`: A Python script implementing the logic of a client that can send messages to, and receive messages from, the server.
## File Transfer (FTP) Exercise
This exercise demonstrates how a server can receive and save files sent from a client over a network connection.
- `ftp_server.py`: A Python script implementing the logic of a server that listens for incoming file transfers from clients, receives the file, and saves it with a timestamped name.
- `ftp_client.py`: A Python script implementing the logic of a client that sends a file to the server for storage.
## Web Scraper Exercise
This exercise demonstrates how to gather and parse data from a website using HTTP requests and HTML parsing. It introduces the use of two essential libraries: `requests` for making HTTP requests and `BeautifulSoup` for parsing and extracting content from HTML.
-`simple_web_scraper.py`: A Python script that fetches the content of a specified web page, extracts the page title, paragraphs, and image links, and displays the results in the terminal.
## Password Cracking Simulation Exercise
This exercise demonstrates how hashed passwords can be brute-forced or cracked using a dictionary of common passwords.
- `hashed_password_cracking.py`: A Python script implementing the logic to brute-force or dictionary-attack a hashed password. It showcases the use of hashing algorithms and iterative attempts to match a target hash.
- `password_dictionary.txt`: A text file containing a list of commonly used passwords, which the script can use to attempt to crack the hash.

# Notes and Details

## Network Scanning Exercise

### How to Use

#### 1. Clone the Repository
To clone this repository to your local machine, run the following command:
```bash
git clone https://github.com/annalisa-zanin/cybersecurity.git
```

#### 2. Make the Bash Script Executable
To run the execute_network_scanner.sh script, you'll need to grant execution permissions to the file. You can do this by running the following command:
```bash
chmod +x execute_network_scanner.sh
```

#### 3. Run the Network Scanner
Once the Bash script is executable, you can run it with the following command:
```bash
./execute_network_scanner.sh
```
Alternatively, you can run the Python script directly using Python:
```bash
python3 network_scanner.py
```
#### 4. Security Considerations
Be cautious when using network scanning tools, as they can trigger alarms in intrusion detection systems (IDS) or be considered malicious activity on networks that you do not own or have permission to scan. Always ensure you have authorization before performing any network scans.

## Chat Simulation Exercise
### How to Use

#### 1. Clone the Repository
To clone this repository to your local machine, run the following command:
```bash
git clone https://github.com/annalisa-zanin/cybersecurity.git
```

#### 2. Run the Chat Server
First, start the chat server by running the following command in your terminal:
```bash
python3 chat_server.py
```
The server will listen for incoming connections from clients on all network interfaces (`0.0.0.0`) and port `12345` by default. You can modify the script to change the port if needed.

#### 3. Run the Chat Client
Next, open a new terminal window and start a chat client with the following command:
```bash
python3 chat_client.py
```
The client will connect to the server at `127.0.0.1` (localhost) and port `12345` by default. Ensure the server is running before starting the client. You can start multiple clients to simulate a group chat.

#### 4. Security Considerations
When running this exercise:
- Ensure the server is running in a secure environment, as it accepts connections from any client on the specified port.
- Avoid exposing the server to untrusted networks unless additional security measures, such as authentication or encryption, are implemented.
- Be mindful of network activity; excessive testing may generate unwanted traffic.

## File Transfer (FTP) Exercise
### How to Use

#### 1. Clone the Repository
To clone this repository to your local machine, run the following command:
```bash
git clone https://github.com/annalisa-zanin/cybersecurity.git
```

#### 2. Run the FTP Server
First, start the FTP server by running the following command in your terminal:
```bash
python3 ftp_server.py
```
The server will listen for incoming connections from clients on all network interfaces (`0.0.0.0`) and port `12345` by default. You can modify the script to change the port if needed.

#### 3. Run the FTP Client
Next, open a new terminal window and start an FTP client with the following command:
```bash
python3 ftp_client.py
```
The client will connect to the server at `127.0.0.1` (localhost) and port `12345` by default. Ensure the server is running before starting the client. The client can send a file to the server for storage.

#### 4. Security Considerations
When running this exercise:
- Ensure the server is running in a secure environment, as it accepts connections from any client on the specified port.
- Avoid exposing the server to untrusted networks unless additional security measures, such as authentication or encryption, are implemented.
- Be mindful of network activity; excessive testing may generate unwanted traffic.

## Web Scraper Exercise

#### 1. Clone the Repository
To clone this repository to your local machine, run the following command:
```bash
git clone https://github.com/annalisa-zanin/cybersecurity.git
```

#### 2. Install Required Libraries
Before running the web scraper, ensure you have the required Python libraries installed. You can install them using pip:
```bash
pip install requests beautifulsoup4
```

#### 3. Run the Web Scraper
To run the scraper, use the following command in your terminal:
```bash
python3 simple_web_scraper.py
```
The script will scrape a predefined website for specific information, such as titles, links, or other structured data. By default, it uses `requests` to fetch the webpage and `BeautifulSoup` to parse and extract the desired content.

#### 4. Modify the Scraper
4. Modify the Scraper
You can customize the scraper to target different websites or extract other types of information. To do this:
- Open the `simple_web_scraper.py` file in a text editor.
- Update the URL variable with the new website.
- Modify the `BeautifulSoup` selectors to match the HTML structure of the target page.

#### 5. Security Considerations
When running this exercise:
- Be respectful of the target website's Terms of Service and ensure scraping is permitted.
- Avoid sending too many requests in a short period, as this may overload the server or result in your IP being blocked.
- Do not scrape sensitive or private data without explicit permission.

## Password Cracking Simulation Exercise

#### 1. Clone the Repository
To clone this repository to your local machine, run the following command:
```bash
git clone https://github.com/annalisa-zanin/cybersecurity.git
```

#### 2. Prepare the Environment
Be sure you have Python installed on your machine. You may also need the `password_dictionary.txt` file, which contains a list of passwords for the dictionary attack. If you don’t have it, create a text file with sample passwords, one per line.

#### 3. Run the Password Cracking Script
Execute the password cracking script by running the following command:
```bash
python3 hashed_password_cracking.py 
```

#### 4. Adjust Script Parameters
The script uses default values for the target hashed password and maximum password length for brute force. You can modify these directly in the `hashed_password_cracking.py` file:
- Target Password: Replace `target_password` in the script with the desired password to test.
- Maximum Length: Adjust `max_length` to specify the maximum length of passwords to attempt during brute force.

#### 5. Security Considerations
When running this exercise:
- Be cautious about using the script on real systems or accounts without explicit permission.
- Ensure that any dictionary file used does not contain sensitive information.
- Understand the ethical (an legal!) implications of password cracking and use this exercise solely for educational purposes.