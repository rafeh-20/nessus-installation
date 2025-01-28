# Nessus Vulnerability Scanner

## Installing Nessus Server

This section provides a step-by-step guide for installing the latest LTS, stable, major version of Nessus server on a vanilla installation of Ubuntu Server 24.04 LTS. 

---

## Step 1: Update the System

Before starting, update the system to ensure all packages are up to date.

`sudo apt update && sudo apt upgrade -y`

## Step 2: Install Required Tools
Install curl and wget for downloading the Nessus installer.

`sudo apt install curl wget -y`

## Step 3: Download the Nessus Installer
Use the curl command to download the Nessus .deb package from the Tenable website. Replace the URL with the latest version if needed.

`curl --request GET \`
  `--url 'https://www.tenable.com/downloads/api/v2/pages/nessus/files/Nessus-10.8.3-ubuntu1604_amd64.deb' \`
  `--output 'Nessus-10.8.3-ubuntu1604_amd64.deb'`

## Step 4: Install the Nessus Package
Use the dpkg command to install the .deb package.

`sudo dpkg -i Nessus-10.8.3-ubuntu1604_amd64.deb`

## Step 5: Enable Nessus Service to Start Automatically on Boot

`sudo systemctl enable nessusd`

## Step 6: Start the Nessus Service

`sudo systemctl start nessusd.service`

## Step 7: Verify the Nessus Service
Check the status of the Nessus service to ensure it is running:

`sudo systemctl status nessusd`

You should see Active: active (running) in the output.

## Step 8: Access the Nessus Web Interface
Nessus runs on port 8834. Access it from a web browser on your network:

`https://<server-ip>:8834`

Replace <server-ip> with the IP address of your Ubuntu Server.

## Step 9: Set Up Nessus Web Interface

After accessing the Nessus web interface, follow these steps to complete the initial setup:

### 1. **Welcome Page**
   - On the first page, titled **Welcome to Nessus**, click **Continue** to proceed.

### 2. **Choose Deployment Option**
   - On the next screen, titled **Choose how you want to deploy Nessus**, select **Register for Nessus Essentials**.

### 3. **Register for Activation Code**
   - Fill out the registration form with the following details:
     - **First Name**: Enter your first name.
     - **Last Name**: Enter your last name.
     - **Email**: Use your university email address.
   - Once registered, you will receive an **activation code**. Example:
     ```
     Activation Code: J67E-JEEU-YCRP-5MND-WEBD
     ```
   - Enter the activation code and click **Continue**.

### 4. **Create Administrator Account**
   - Set up an administrator account by entering:
     - **Username**: Choose a username for the admin account.
     - **Password**: Create a strong password.
   - Click **Submit**.

### 5. **Initialization**
   - Nessus will initialize and download plugins. The screen will display the message:
     ```
     Please wait while Nessus is initializing.
     Downloading plugins...
     ```

### 6. **Nessus Ready**
   - Once initialization completes, the Nessus home page will appear, and the system will be ready for use.

---

You can now proceed to configure Nessus for the required tasks.
