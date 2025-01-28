### Configure Nessus to scan a second GNU/Linux server every week.

To configure Nessus to scan a second GNU/Linux server every week, follow these steps:

#### 1. Create a New Scan
- Log into the **Nessus Web Interface**.
- Navigate to the **"Scans"** tab from the top menu.
- Click on **"New Scan"**.
- Select the scan type you want to use, such as **"Basic Network Scan"** or another appropriate scan template.
  
#### 2. Configure the Scan for the Linux Server
- In the **Scan Settings**, under **"Targets"**, enter the **IP address** of the second GNU/Linux server that you want to scan.
  - Example: `139.179.150.225` (replace this with your actual server IP).

#### 3. Set the Scan Schedule
- Click on **"Schedule"** to open the scheduling options.
- Enable the **"Recurring Scan"** option.
- In the **Frequency** dropdown, select **Weekly**.
   - Choose the **Day of the Week** and **Time** for the scan to occur. Ensure it matches your desired schedule.

#### 4. Save and Activate the Scan
- Click **"Save"** to create the scan.
- Your scan will now be scheduled to run weekly on the Linux server at the specified day and time.

#### 5. Monitor the Scan
- You can monitor the scan results by going to the **"Scans"** section in the Nessus interface.
- Once the scan completes, you can view the report for any vulnerabilities or issues found on the Linux server.

By following these steps, Nessus will automatically scan the Linux server every week, and you can view the results after each scan.
