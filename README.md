# Goscan

A fast, simple script to perform quick network port scans using **nmap** or **rustscan**.  
Automatically organizes results into folders for each target.

---

## 📦 Features

- Full TCP port scan (`-p-`) with **nmap** or **rustscan**
    
- Auto-extract open ports and run a detailed **nmap** service scan (`-sC -sV`)
    
- Saves all results neatly inside `nmap/<target_ip>/`
    
- Works globally from anywhere after installation
    
- Colorful and clean terminal output ✨
    

---

## 🚀 Usage

bash

CopyEdit

`Goscan <IP_ADDRESS> [scanner]`

- `<IP_ADDRESS>` → Target IP to scan (Required)
    
- `[scanner]` → Choose `nmap` (default) or `rustscan` (Optional)
    

---

### 📚 Examples

Full nmap scan:

bash

CopyEdit

`Goscan 192.168.242.189`

Using rustscan:

bash

CopyEdit

`Goscan 192.168.242.189 rustscan`

---

## ⚙️ Installation

Make `Goscan` available globally:

bash

CopyEdit

`chmod +x Goscan sudo mv Goscan /usr/local/bin/Goscan`

Now you can run `Goscan` from anywhere!

---

## 🗂️ Output Structure

Results are saved under:

markdown

CopyEdit

`nmap/  └── 192_168_242_189/       ├── ports_only.txt       └── nmap_result.txt`

---

