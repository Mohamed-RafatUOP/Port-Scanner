Python Port Scanner

A simple multi-threaded port scanner written in Python. This tool scans a target IP address over a specified range of ports and reports which ports are open. Results are printed to the console and saved into a timestamped log file.

---

Features

* Multi-threaded scanning for faster results
* Custom port range input
* Automatic logging of results
* Thread-safe operations using locks
* Organized log files with timestamps

---

## 📁 Project Structure

```
.
├── port_scanner.py
└── logs/
    └── scan_YYYY-MM-DD_HH-MM-SS.txt
```

---

Requirements

* Python 3.x

No external libraries are required — everything uses built-in Python modules.

---

Usage

1. Clone the repository:

```
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. Run the script:

```
python port_scanner.py
```

3. Enter the required inputs:

```
Enter IP: 192.168.1.1
Start port: 1
End port: 1000
```

---

How It Works

* The script creates a socket connection to each port in the given range.
* It uses a `ThreadPoolExecutor` to scan multiple ports simultaneously.
* If a connection is successful, the port is marked as open.
* All results are:

  * Printed to the console
  * Saved in a log file under the `logs/` directory

---

Logging

* Logs are stored automatically in the `logs/` folder.
* Each scan generates a new file with a timestamped name:

```
logs/scan_2026-04-19_12-30-45.txt
```
