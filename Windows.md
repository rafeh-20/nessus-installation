### Configure Nessus to Scan a Windows Server Every Day

To configure Nessus to scan a Windows server every day, follow these steps:

#### 1. Create a New Scan
- Log into the **Nessus Web Interface**.
- Navigate to the **"Scans"** tab from the top menu.
- Click on **"New Scan"**.
- Select the scan type you want to use, such as **"Basic Network Scan"** or another appropriate scan template.
  
#### 2. Configure the Scan for the Windows Server
- In the **Scan Settings**, under **"Targets"**, enter the **IP address** or **hostname** of the Windows server that you want to scan.
  - Example: `139.179.150.27` (replace this with your actual server IP).

#### 3. Set the Scan Schedule
- Click on **"Schedule"** to open the scheduling options.
- Enable the **"Recurring Scan"** option.
- Set the frequency to **"Daily"** to ensure the scan runs every day.
- Specify the time you want the scan to run daily (e.g., set the time to run during off-peak hours).

#### 4. Save and Activate the Scan
- Click **"Save"** to create the scan.
- Your scan will now be scheduled to run daily on the Windows server at the specified time.

#### 5. Monitor the Scan
- You can monitor the scan results by going to the **"Scans"** section in the Nessus interface.
- Once the scan completes, you can view the report for any vulnerabilities or issues found on the Windows server.

By following these steps, Nessus will automatically scan the Windows server every day, and you can view the results after each scan.
