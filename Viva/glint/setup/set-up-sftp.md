---
title: Set up Secure File Transfer Protocol (SFTP) in Viva Glint
description: Use Microsoft Viva Glint Secure File Transfer Protocol (SFTP) to establish regular, automated imports of employee data.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: sftp, public ip address, pgp encryption, data transfer, ssh key, data transfer
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/22/2025
---

# Set up Secure File Transfer Protocol (SFTP) in Viva Glint

Use Microsoft Viva Glint [Secure File Transfer Protocol (SFTP)](sftp-data-automation.md) to establish regular, automated imports of employee data. In Viva Glint General settings: 

- Import SSH Public Keys
- Specify public IP addresses to connect (optional)
- Select users that receive data upload notification emails
- Set up PGP encryption (optional)
- View credentials and select a port number to access your SFTP account

> [!NOTE]
> - Your IT team may need to [add an IP exception or add hosts and ports to an allowlist](allowed-list.md) to connect to SFTP.
> - There are no size limits for files uploaded to Viva Glint SFTP.

Learn more about how to set up SFTP with this video and the guidance in this article:
> [!VIDEO 641b5e1a-e628-4c7d-a0e4-62828c91b123]

## Manage SFTP in General Settings

Manage SFTP settings to connect to your Viva Glint SFTP account:

1. From the admin dashboard, select the **Configuration** symbol, then in **Service configuration**, choose **General settings**.
1. In the **Technical configuration** section, go to **SFTP setup** and select **Manage**.
1. In the SFTP pane that appears, review each field and enter information as needed:

   |Setup item   |Required or optional   |More information   |
   |:----------|:-----------|:-----------|
   |**SSH Public Key***     |Required       |<ul><li>Enter the full text of your public SSH key: `ssh-rsa ...` .</li><li>**DO NOT** share your private key with Viva Glint.</li><li>To generate a key pair, see:  [Generate an SSH key pair](sftp-ssh-key-gen.md).</li><li>To convert a key to the required format, see: [Convert a key to OpenSSH format](convert-ssh-key.md).</li><li>Add up to three public SSH keys.</li></ul>|
   |**SFTP IP Addresses****     |Optional       |<ul><li>**Leave this field blank to allow any account to connect.**</li><li>Specify public IP addresses to limit accounts that can connect.</li><li>Contact your IT team, HR information system (HRIS) vendor, or use [online tools](https://ifconfig.io/) to determine your public IP addresses.</li><li>This field supports subnets, or ranges of IP addresses. Enter ranges (for example: 1.1.1.0/24) rather than individual IP addresses in each field, if needed.</li></ul>     |
   |**Notify People**     |Required       |<ul><li>Search for and add users that should receive file upload notification emails.</li><li>Users must be active and exist in Viva Glint.</li></ul>       |
   |**PGP Encryption**     |Optional       |<ul><li>Switch toggle to **On** to enable file encryption and reveal Viva Glint's public PGP key to encrypt employee data files.</li><li>When this setting is enabled, SFTP accepts files with and without encryption.</li><li>This key expires every 12 months. Viva Glint sends a [notification 30 days before expiration](#pgp-key-expiration).</li></ul>      |
   |**SFTP Credentials**     |Required       |Select a port number (22 or 1122) and copy credentials shown in the platform to connect to SFTP. Your host name changes based on your region (US or EU) and selected port. Allow at least one hour after entering public SSH keys and optional IP addresses before testing your connection.<br><br><ul><li>**File Protocol**: _SFTP_</li><li>**Port**: Select 22 or 1122</li> <li>**Host Name**: _Varies based on region (US or EU) and selected port. Copy from the platform for the correct host name._</li> <li>**Username:** _Company ID_</li> <li>**Password:** _Not applicable, use your private SSH key file_</li></ul>        |

   \* When a tenant is deprovisioned or considered in a "LockedOut" state, public SSH keys are deleted and SFTP no longer works.<br><br>
   
   \** Private IP ranges aren't internet routable and don't allow SFTP connection. Don't include private IP addresses, which fall in these ranges:
   - **10.0.0.0/8 IP addresses:** 10.0.0.0 – 10.255.255.255
   - **172.16.0.0/12 IP addresses:** 172.16.0.0 – 172.31.255.255
   - **192.168.0.0/16 IP addresses:** 192.168.0.0 – 192.168.255.255 <br><br>

   > [!NOTE]
   > For more information about deprovisioning, read about [Deleting a Microsoft Entra tenant](/entra/identity/users/directory-delete-howto) and [Data deletion in Microsoft 365](/compliance/assurance/assurance-data-retention-deletion-and-destruction-overview).

## PGP key expiration

The public PGP key provided by Viva Glint that your organization can optionally use to encrypt data files expires every 12 months. Users selected in the **Notify People** field in SFTP setup receive a notification email 30 days before the key's expiration date letting them know that they need to generate a new key. 

:::image type="content" source="../../media/glint/setup/pgp-expire-email.png" alt-text="Screenshot of the PGP key expiration email which Viva Glint sends 30 days before the expiration date.":::

To create a new public PGP key:

1. Go to **Configuration** and select **General settings** in the **Service configuration** section.
2. Select **Technical configuration** in the menu and then in **SFTP setup** choose **Manage**.
3. To generate a new key, go to **PGP Encryption** and switch the toggle from **On** to **Off**, and then back to **On**.
4. Select the copy icon next to the **Public Key** field or select the **Download .asc file** option to get the newly generated key.
