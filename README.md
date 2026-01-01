# 🕵️ Live Network Security Audit: HTTP Analysis

## 📌 Project Overview
This project demonstrates the security risks associated with unencrypted web traffic on a mobile hotspot environment. I captured live traffic from my host machine to analyze how data is transmitted across the network.

## 🛠️ Technical Breakdown
- **Network Interface:** Wi-Fi (Mobile Hotspot)
- **Host IP:** 192.168.77.225
- **Target:** neverssl.com (34.223.124.45)

### 🔍 Key Findings
1. **Cleartext Exposure:** By following the TCP Stream, I reconstructed the full HTTP request. All headers, including `User-Agent` and `Host`, were visible in plain text.
2. **Compression vs Encryption:** The capture revealed `Content-Encoding: gzip`. This confirms the data was compressed for speed but lacked TLS encryption, making it vulnerable to interception.

## ✅ Visual Proof
### Packet Capture List
![Wireshark List](./image_381aca.png)

### Reconstructed TCP Stream
![TCP Stream](./image_381e0f.jpg)
