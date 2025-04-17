## 🌐 IP Address Types: IPv4 and IPv6

### 📌 IPv4 and IPv6

- 📦 IPv6 are like **6-digit** (128-bit) addresses  
  📍 Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
- 🧮 IPv4 are **4-digit** (32-bit) addresses  
  📍 Example: `192.168.1.1`
- 🌍 IPv4 Range: `0.0.0.0` to `255.255.255.255`
- 🔍 Use `ping url` to find the website IP (e.g., Google often uses IPv6)
- 💬 Reddit uses IPv4

---

### 🔤 IP Address Classes (A to E)

- 🅰️ **Class A**: `1.0.0.0` to `126.255.255.255`
- 🅱️ **Class B**: `128.0.0.0` to `191.255.255.255`
- 🌐 **Class C**: `192.0.0.0` to `223.255.255.255`
- 📡 **Class D**: Used for **Multicasting**
- 🧪 **Class E**: Reserved for **Experimental** purposes

> 🚫 No `127.x.x.x` range used in classes because it is reserved for **Loopback**
> 🧪 Example:  
> `ping localhost` in CMD → will return `127.0.0.1`

---

### 🛡️ RFC-defined Private IP Ranges

| 🔢 IP Range                        | 🧾 CIDR Notation | 💡 Example        |
|-----------------------------------|------------------|------------------|
| `10.0.0.0 – 10.255.255.255`       | `10.0.0.0/8`     | `10.0.0.5`       |
| `172.16.0.0 – 172.31.255.255`     | `172.16.0.0/12`  | `172.16.1.100`   |
| `192.168.0.0 – 192.168.255.255`   | `192.168.0.0/16` | `192.168.1.1`    |

---

### 🏠 Why Private IPs Matter

- 🏡 Used for **communication inside** your home/office
- 🚫 They are **not routable** on the public internet
- 🔁 **Routers use NAT** (Network Address Translation)  
  🔄 This maps private IPs to a public IP so devices can access the internet

---
