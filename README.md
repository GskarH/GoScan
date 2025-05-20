# Goscan 🔎

**Goscan** is a quick and flexible port scanning script written in Bash. It supports scanning single IPs, IP ranges, CIDR blocks, and multiple targets using `nmap` or `rustscan`. Output is neatly organized in folders per IP address.

---

## 🚀 Features

- Scan single IPs, ranges, CIDRs, or lists from a file
- Automatically detects open ports and performs service/version enumeration
- Supports `nmap` (default) and `rustscan`
- Saves results in per-IP folders (e.g., `192_168_1_10/`)

---

## 🛠 Requirements

- `nmap` (required)
- `rustscan` (optional) (Download https://github.com/bee-san/RustScan)

---

## 📦 Installation

Make it executable and move it to your `$PATH`:

```bash
git clone https://github.com/GskarH/GoScan.git
cd GoScan
chmod +x ./Goscan
sudo mv ./Goscan /usr/local/bin/goscan
```

Then you can run it anywhere using:

```
goscan <args>
```

## 📚 Usage

### ➤ Single IP scan


```
goscan 192.168.1.10
goscan 192.168.1.10 rustscan
```

### ➤ Multiple IPs

```
goscan -i 192.168.1.10,192.168.1.20
goscan -i "192.168.1.10-13, 192.168.1.0/30"
```

### ➤ IP list from file

```
goscan -f targets.txt
```

### ➤ Output

Each scan creates a folder named after the IP (e.g., `192_168_1_10/`) with:

- `ports_only.txt`: List of open ports
- `nmap_result.txt`: Full detailed scan
