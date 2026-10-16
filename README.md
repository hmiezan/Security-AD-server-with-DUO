
<img width="355" height="109" alt="DUO" src="https://github.com/user-attachments/assets/a04fdcb7-a340-46b8-a78b-a66903e5118a" />


# Security-AD-server-with-DUO
In this lab, I will enhance the security of my Active Directory Server by integrating Multi-Factor Authentication (MFA) using Duo Security for Remote Desktop Protocol (RDP) access and local connection.

In today's world of evolving cyber threats, protecting your digital assets is essential.

This project focuses on strengthening my Active Directory Server environment by adding an extra layer of authentication, ensuring that only authorized users can gain access.

# Environments and Technologies Used
- Proxmox Virtual enviromment 9.1.4 and RDP
- Microsoft Windows Server 2022
- Cisco Duo Security RDP: https://duo.com/docs/rdp#first-steps


# Step 1: Sign in for Duo Security and Create user (exiting domain user)

Register for a free trial on Duo Security (https://signup.duo.com/) and login to admin dashboard (https://admin.duosecurity.com/login?next=%2F).

<img width="350" height="395" alt="Admin SIgn in" src="https://github.com/user-attachments/assets/ff6757a3-7c6b-482f-85c5-a709e83e984d" />



Create a user already existed in Active Directory with domain admin Role

<img width="1000" height="481" alt="Duo User" src="https://github.com/user-attachments/assets/0f6109a9-4fec-44fe-9a18-62485311ea01" />



Complete the necessary fields, and an email confirmation will be sent for login access.

<img width="1509" height="833" alt="Enrollment" src="https://github.com/user-attachments/assets/858df1ca-4811-488f-a55c-14967f7a81e8" />


Launch the mobile application on your smartphone and scan the QR code.

The application will guide you through the steps.

<img width="284" height="430" alt="QR" src="https://github.com/user-attachments/assets/9b158e40-9a0e-4045-bec8-d551c7a15270" />

# Step 2: Install the RDP application

Navigate to the left side and select "Applications", then choose "+Add Application".

<img width="1872" height="483" alt="Application" src="https://github.com/user-attachments/assets/12a57d67-cf94-4f10-9060-b1b7d93a69df" />

Search for RDP and click on "+ Add" to proceed.
<img width="814" height="519" alt="SearchRDP" src="https://github.com/user-attachments/assets/80c97125-c01f-494a-adf8-9a0d54be98ef" />

Download the DUO Authentication for windows in the documentation > First steps

<img width="1415" height="418" alt="Document" src="https://github.com/user-attachments/assets/88aea1c5-76ab-4748-a3d3-7729f92b5bb7" />

Copy and paste the API Hostname, Integration Key, and Secret Key into the Installer.
<img width="741" height="321" alt="Api" src="https://github.com/user-attachments/assets/b41f68e6-419d-4600-a434-6a011e4d14ef" />

<img width="693" height="270" alt="Secret" src="https://github.com/user-attachments/assets/ebd46803-f990-494a-9606-1718e0cbfd83" />

# Step 3: Connnect on local server access
After the installer completes, log in to the Server 2022 through Promox

<img width="1678" height="678" alt="proxmox connection" src="https://github.com/user-attachments/assets/2fafc4fc-b4a2-44e2-a1b7-64ed5ce4798f" />
<img width="4032" height="3024" alt="IMG_0893" src="https://github.com/user-attachments/assets/9fde514d-3b88-46e3-ab47-e5b119f11ee9" />
<img width="4032" height="3024" alt="IMG_0894" src="https://github.com/user-attachments/assets/53ed964c-ae13-48b1-893c-38eaabaa8ae2" />

Verification in the authentication log

<img width="1874" height="437" alt="image" src="https://github.com/user-attachments/assets/57d0778e-9d53-4c7f-aca9-16b98e4f9548" />

The Server  will now require Multi-Factor Authentication (MFA) each time a user logs and try to RDP.

# Conclusion

The Duo Security-powered Multi-Factor Authentication (MFA) elevates On premise Security by seamlessly introducing an Additional Layer of Authentication.

Featuring easy configuration, real-time monitoring, and customizable policies, it offers strong protection for your digital assets.

Adopt this enhanced security to navigate the ever-changing landscape of cybersecurity with confidence.

# Next 
I will integrate DUO to external Directories to sync in real time with domain accounts



