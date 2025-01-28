# Additional Tasks Based on Feedback

Syed Rafeh Hussain
22001502

# Changing Default Port

## Objective

The goal is to configure Nessus to work with just the IP address, so that users no longer need to specify a port number (such as `8834`) in the URL. This will involve changing the default Nessus port from `8834` to `443`, which is the standard HTTPS port.

## Steps

1. **Log in to Nessus:**
   - Open the Nessus web interface in your browser using the current port:
     ```bash
     https://<IP>:8834
     ```

2. **Navigate to Settings:**
   - Once logged in, click on the **Settings** option located on the top bar of the interface.
   - Select **Advanced**.

3. **Modify the Web Server Port:**
   - Under the **User Interface** section, locate the setting named **Nessus Web Server Port**.
   - The **Identifier** for this setting is `xmlrpc_listen_port`, and the **Value** is `8834` by default.
   - Change the value from `8834` to `443` to use the default port for HTTPS connections.
   - Click **Save** to apply the changes.

4. **Restart Nessus:**
   - To apply the changes, stop and start Nessus using the following commands in the terminal:
     ```bash
     sudo systemctl stop nessusd.service
     sudo systemctl start nessusd.service
     ```

5. **Verify the Changes:**
   - After restarting, open a browser and access the Nessus interface using just the IP address:
     ```bash
     https://<IP>
     ```
   - Nessus should now be accessible on port `443`, and there should be no need to specify the port number in the URL.

## Conclusion

By following these steps, you have successfully changed the Nessus port from `8834` to the default HTTPS port `443` using the Nessus web interface.

# Firewall Configuration

## Objective

This guide demonstrates how to configure the Uncomplicated Firewall (UFW) on your Ubuntu system to allow Nessus to run.

## Steps

### 1. Install UFW

To begin, install UFW (Uncomplicated Firewall) using the following command:
```bash
sudo apt install ufw
```

### 2. Allow Nessus on Port 443
Next, allow traffic on port 443 to enable access to Nessus through HTTPS:

```bash
sudo ufw allow 443/tcp
```

### 3. Enable UFW
After configuring the firewall rules, enable UFW to apply the changes:

```bash
sudo ufw enable
```

### 4. Verify UFW Status
You can verify the status of UFW and the allowed ports by running:

```bash
sudo ufw status
```
The output should show something similar to this:
```bash
Status: active

To                         Action      From
--                         ------      ----
443/tcp                    ALLOW       Anywhere
443/tcp (v6)               ALLOW       Anywhere (v6)
```

# Nessus Advanced Scan with Credentials for Windows

## Objective

This document outlines the steps to configure and run an advanced scan on Nessus using credentials for a Windows system. The goal is to authenticate using your Windows login credentials.

## Steps to Configure and Run the Scan

1. **Open Nessus Web Interface**
    - Launch the Nessus interface in your browser using the IP address:
     ```bash
     https://<IP>
     ```
    - Log in to the Nessus interface.

2. **Create a New Scan**
    - In the Nessus dashboard, click on **New Scan**.
    - Select **Advanced Scan**.

3. **Configure Scan Settings**
    - Under the **Targets** section, enter the **IP address** of your Windows machine. For example: `139.179.150.195`.

4. **Enter Windows Credentials**
    - Click on **Credentials** to enter credential settings.
    - Choose **Host** in the Categories option.
    - Select **Windows** from the list.
    - Select Authentication method as **Password**.
    - **Username**: Enter your Microsoft account email (e.g., `yourname@hotmail.com`).
    - **Password**: Enter the password you use to sign in to your Windows account.
    - **Domain**: Leave this field blank.

6. **Launch the Scan**
    - After configuring the scan, click **Save** to save the scan.
    - Click **Launch** to start the scan. Nessus will attempt to authenticate using the provided credentials and begin the scan on your Windows system.

## Conclusion

By following these steps, you can run an advanced scan on your Windows machine using Nessus with authentication credentials. This allows for deeper vulnerability scanning, ensuring that Nessus can check for issues that require authenticated access to the system.
