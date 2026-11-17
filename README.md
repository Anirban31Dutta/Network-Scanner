# Network Scanner

A Python-based network scanning tool developed using **Scapy**. This project helps identify active hosts, scan TCP ports, and discover devices on a local network using ICMP, TCP SYN, and ARP scanning techniques.

## Features

- **ICMP Scanning:** Checks whether a target IP address is reachable.
- **TCP SYN Scanning:** Identifies open, closed, and filtered TCP ports.
- **ARP Scanning:** Discovers active devices on a local network and retrieves their IP and MAC addresses.
- **IP Validation:** Validates IP address formats.
- **Network Validation:** Validates network addresses and CIDR notation.
- **Multiple Scan Modes:** Supports ICMP, TCP, ARP, and combined scanning.

## Technologies Used

- Python
- Scapy
- Socket
- IP Addressing (`ipaddress`)

## Project Structure

```text
Network-Scanner/
│
├── src/
│   ├── main.py
│   └── scanner.py
│
├── venv/
├── README.md
└── requirements.txt
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Anirban31Dutta/Network-Scanner.git
```

### 2. Navigate to the Project Directory

```bash
cd Network-Scanner
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Virtual Environment

For Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### 5. Install Dependencies

```bash
pip install scapy
```

Alternatively, install dependencies from the requirements file:

```bash
pip install -r requirements.txt
```

### 6. Windows Configuration

For Windows users, install [Npcap](https://npcap.com/#download) to enable Layer 2 packet operations.

During installation, enable **Install Npcap in WinPcap API-compatible Mode** if available.

Run the terminal with administrator privileges when required.

## How to Run

Run the following commands from the project root directory.

### ICMP Scan

```bash
python src/main.py 192.168.29.214 -t icmp
```

### TCP Scan

Use the supported port argument format to scan selected TCP ports.

### ARP Scan

Use the network address in CIDR notation to discover devices on your local network.

### Available Scan Types

| Scan Type | Description |
|---|---|
| `icmp` | Checks host availability |
| `tcp` | Checks TCP port status |
| `arp` | Discovers devices on a local network |
| `all` | Performs all supported scan types |

To view available command-line arguments:

```bash
python src/main.py --help
```

## Sample Scan Results

The scanner can display information such as:

- Host status: UP or DOWN
- TCP port status: OPEN, CLOSED, or FILTERED
- Discovered device IP addresses
- Discovered device MAC addresses

## Learning Outcomes

Through this project, I explored:

- Computer networking fundamentals
- IP addressing and subnetting
- ICMP, TCP, and ARP protocols
- Network discovery techniques
- TCP port scanning
- Python packet manipulation using Scapy

## Future Improvements

- Implement multithreaded port scanning.
- Add CSV and JSON report generation.
- Develop a graphical user interface.
- Improve network interface selection.
- Add service detection and operating system identification.

## Disclaimer

This project is intended for educational purposes and authorized network testing only.

**Only scan networks and devices that you own or have explicit permission to test.**

## Author

**Anirban Dutta**

- GitHub: [Anirban31Dutta](https://github.com/Anirban31Dutta)
- Repository: [Network-Scanner](https://github.com/Anirban31Dutta/Network-Scanner)