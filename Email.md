# Configure Nessus to E-mail the Results to Specific People

## Step 1: Configure SMTP Server Settings
1. Log in to the Nessus web interface.
2. Navigate to **Settings > SMTP Server**.
3. Fill in the following details:
   - **Host**: `asmtp.bilkent.edu.tr`
   - **Port**: `587`
   - **From (Sender Email)**: `rafeh.hussain@ug.bilkent.edu.tr`
   - **Encryption**: Select `Force TLS`.
   - **Hostname (for email links)**: Leave it blank
   - **Auth Method**: Select `Login`.
4. Enter your email credentials:
   - **Username**: `rafeh.hussain@ug.bilkent.edu.tr`
   - **Password**: Your Bilkent email password.
5. Save the settings.

## Step 2: Configure Scan Notification
1. Open the **Scan** settings for the scan you want to configure.
2. Go to the **Notifications** section.
3. Enter the recipient email address (e.g., your other email) in the **Recipients** field.

## Step 3: Test the SMTP Configuration
1. Navigate to **Settings > SMTP Server**.
2. Click **Send Test Email** to verify that the SMTP configuration is working.
3. Check the recipient email for a test message. If it fails, review the SMTP settings.

## Step 4: Run the Scan
1. Run the configured scan.
2. After the scan completes, Nessus should automatically email the results to the specified address.
