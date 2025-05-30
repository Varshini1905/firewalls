# Windows Firewall Configuration

## Open Windows Firewall Configuration Tool

1. Go to **Control Panel > System and Security > Windows Defender Firewall**.
2. Click on **"Advanced settings"** to open the **Windows Firewall with Advanced Security**.

## List Current Firewall Rules

1. In the left pane, click on **"Inbound Rules"** to see the list of current rules.

## Add a Rule to Block Inbound Traffic on Port 23 (Telnet)

1. In the right pane, click on **"New Rule..."**![Screenshot 2025-05-30 200549](https://github.com/user-attachments/assets/499c86da-3d07-451f-a701-a8221c66ff30)   
2. Select **"Port"** and click **"Next."**
3. Choose **"TCP"** and specify **"23"** in the **"Specific local ports"** field, then click **"Next."**![Screenshot 2025-05-30 200616](https://github.com/user-attachments/assets/c46e67ba-95c1-4bf0-8d92-10515e23de01) 
4. Select **"Block the connection"** and click **"Next."**![Screenshot 2025-05-30 200637](https://github.com/user-attachments/assets/d364acb3-672a-477e-a273-8ba704eeded6)

5. Choose when the rule applies (**Domain, Private, Public**) and click **"Next."**
6. Name the rule (e.g., **"Block Telnet"**) and click **"Finish."**

## Test the Rule

Open a command prompt and try to connect to the Telnet port:

```bash
telnet localhost 23
```
![Screenshot 2025-05-30 201318](https://github.com/user-attachments/assets/f04c87c1-b6fb-4e1a-9ce5-a99f9395bd19)



