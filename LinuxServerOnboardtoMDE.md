# Onboarding a Linux Device into Microsoft Defender for Endpoint (MDE)

## Prerequisites
- Ensure the Linux device is running a supported distribution and version.
- Verify that the device has internet access to communicate with the MDE service.
- Obtain the onboarding package from the Microsoft 365 Defender portal.

## Steps to Onboard

### 1. Download the Onboarding Package
1. Log in to the [Microsoft 365 Defender portal](https://security.microsoft.com).
2. Navigate to **Settings** > **Endpoints** > **Onboarding**.
3. Select **Linux** as the operating system.
4. Download the onboarding package and save it to your Linux device.

### 2. Extract the Onboarding Package
```bash
tar -xzvf <onboarding_package>.tar.gz
cd <onboarding_package>
```

### 3. Run the Onboarding Script
```bash
sudo bash ./onboard_linux.sh
```

### 4. Verify the Onboarding
- Check the status of the MDE service:
    ```bash
    sudo mdatp health
    ```
- Ensure that the device appears in the Microsoft 365 Defender portal under **Devices**.

## Post-Onboarding
- Configure any additional settings or policies as required.
- Monitor the device status and alerts from the Microsoft 365 Defender portal.

## Troubleshooting
- If the onboarding script fails, review the logs located in `/var/log/microsoft/mdatp/`.
- Ensure that the device meets all prerequisites and has proper network connectivity.

For more detailed information, refer to the official [Microsoft Defender for Endpoint documentation](https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/linux-install-manual).