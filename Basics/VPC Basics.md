
# ☁️ VPC Theory Concepts

---

## 📌 CIDR (Classless Inter-Domain Routing)

CIDR notation defines the IP address range and how many IPs are included:

| CIDR         | Range                     | Total IPs |
|--------------|---------------------------|-----------|
| 10.0.0.0/32  | 10.0.0.0                  | 1         |
| 10.0.0.0/31  | 10.0.0.0 - 10.0.0.1       | 2         |
| 10.0.0.0/30  | 10.0.0.0 - 10.0.0.3       | 4         |
| 10.0.0.0/29  | 10.0.0.0 - 10.0.0.7       | 8         |
| 10.0.0.0/28  | 10.0.0.0 - 10.0.0.15      | 16        |
| 10.0.0.0/27  | 10.0.0.0 - 10.0.0.31      | 32        |
| 10.0.0.0/26  | 10.0.0.0 - 10.0.0.63      | 64        |
| 10.0.0.0/25  | 10.0.0.0 - 10.0.0.127     | 128       |
| 10.0.0.0/24  | 10.0.0.0 - 10.0.0.255     | 256       |
| 10.0.0.0/22  | 10.0.0.0 - 10.0.3.255     | 1024      |

🧠 **Formula**:  
`Total IPs = 2 ^ (32 - subnet mask)`

Example:  
`190.20.5.0/27 → 2^(32-27) = 2^5 = 32 IPs`

---

## 🔓 Public vs 🔒 Private

- **Public Subnet** 🌍: Can be accessed from anywhere via the internet.
- **Private Subnet** 🏢: Can only be accessed internally within the VPC.

🎯 To isolate **public** and **private** resources in cloud architecture, **VPC** is used.

Example:
- 🖥️ Public IP → accessible globally.
- 🔒 Private IP → only accessible inside VPC.

---

## 🧱 Architecture

### 🧩 2-Tier Architecture

```text
🧑‍💻 Browser
   │
   ▼
🌐 DNS (Route 53)
   │
   ▼
🧰 Load Balancer (ELB)
   │
   ▼
🖥️ Web Server (EC2 - Apache)
   │
   ▼
🗄️ Database (EC2/RDS/DynamoDB)
```

- Static files can be served from: 🗂️ **S3 Bucket**

---

### 🧩 3-Tier Architecture

```text
🧑‍💻 Client (Browser)
   │
   ▼
🌐 DNS (Route 53)
   │
   ▼
🧰 Load Balancer (ELB)
   │
   ▼
⚙️ Application Tier (EC2 - Node.js, Spring Boot, etc.)
   │
   ▼
🖥️ Web Server Tier (EC2 - Apache/Nginx for static + dynamic content)
   │
   ▼
🗄️ Database Tier (RDS / DynamoDB / EC2-DB Server)
```

🎯 S3 can be connected at the **Web Server Tier** to store and serve static content efficiently.

---

✅ Use **VPC** to structure networking securely and scalably in AWS.
