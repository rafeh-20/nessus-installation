### Configure Nessus to Scan the Whole Network When Triggered Manually

To configure Nessus to scan the entire network on demand, follow these steps:

#### 1. Create a New Scan
- Log into the **Nessus Web Interface**.
- Navigate to the **"Scans"** tab from the top menu.
- Click on **"New Scan"**.
- Select the scan type you want to use, such as **"Basic Network Scan"** or another appropriate scan template.

#### 2. **Configure the Target IP Address for the Entire Network**
   - Under the **Targets** section, enter the IP range of your network. For example, if your network is in the `139.179.150.27/24` subnet, you would enter `139.179.150.27/24`. This will scan all devices within the specified IP range.
   - Alternatively, you can enter multiple subnets or a list of IPs, separated by commas, if you wish to scan multiple networks.

#### 3. **Set Scan to Trigger Manually**
   - Ensure that no schedule is set for the scan by leaving the **Schedule** section empty or choosing **None** under frequency options.
   - This will configure the scan to be run manually only, rather than automatically on a recurring basis.

#### 4. **Save and Launch the Scan**
   - After configuring the scan settings, click **Save** to save the scan.
   - To run the scan immediately, click the **Launch** button next to the scan in your scan list.

#### 5. **Monitor the Scan**
   - You can monitor the progress of the scan from the **Scan History** tab.
   - After the scan completes, you can review the results from the **Scan Results** section.

