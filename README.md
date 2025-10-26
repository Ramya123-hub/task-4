# 🔥 Task 4: Firewall Configuration (Windows)

## 🎯 Objective
Configure and test custom firewall rules in **Windows Defender Firewall** to control network traffic and understand inbound/outbound filtering.

---

## ⚙️ Steps Performed
1. **Check existing rules**  
   - Opened Firewall Manager: `wf.msc`  
   - Reviewed inbound and outbound rules.

2. **Block Telnet (Port 23)**  
   - Created **Inbound Rule** → TCP → Port `23` → **Block** → All profiles  
   - Named the rule: `Block Telnet`.

3. **Allow SSH (Port 22)**  
   - Added rule to **Allow TCP port 22**.

4. **Test the rule**  
   - Command: `telnet 127.0.0.1 23`  
   - Result: `Could not open connection…` → confirmed Port 23 blocked.

5. **Clean up**  
   - Deleted the temporary block rule.

---

## 🧰 Tools Used
- Windows Defender Firewall  
- Command Prompt / PowerShell  
- Telnet Client (`dism /online /Enable-Feature /FeatureName:TelnetClient`)

---

## 💡 Key Learnings
- Inbound and outbound rules control network access.  
- Port-based filtering secures the system.  
- Blocking/allowing ports affects app communication.  
- Real-time testing (Telnet) validates firewall rules.

---

## ✅ Outcome
- Successfully blocked unsafe connections (Telnet).  
- Allowed secure connections (SSH).  
- Controlled access across **Domain, Private, and Public** profiles.

---

## 🧭 Commands Summary
| Purpose | Command / Action |
|---------|-----------------|
| Open Firewall Manager | `wf.msc` |
| Enable Telnet Client | `dism /online /Enable-Feature /FeatureName:TelnetClient` |
| Test Port 23 | `telnet 127.0.0.1 23` |
| Verify Rules | View **Inbound Rules** tab |

---

## 🔒 Conclusion
Windows Defender Firewall filters network traffic by port, protocol, and profile. Testing with Telnet confirmed the rules work, demonstrating how firewall rules protect systems from unauthorized access.
