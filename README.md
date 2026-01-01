## 💾 Windows Server Backup & Restore Configuration Guide

This guide explains how to **install, configure, perform backup, and restore data** using **Windows Server Backup**.  
It is useful for **IT Support, System Administrator, and Windows Server lab practice**.

---

## 🧰 1️⃣ Fix Windows Server Backup Error (Feature Not Installed)

If you see an error like **Windows Server Backup failure / not detected**, it means the feature is not installed.

## ✅ Solution: Install Windows Server Backup Feature

- Open **Server Manager**
- Click **Add Roles and Features**
- Click **Next** until **Features**
- Select:


 ☑ Windows Server Backup
   - Click Install
   - After installation, click Close

---
##⚙️ 2️⃣ Configure Backup (Backup Once)
🔹 Open Windows Server Backup
 - Open Server Manager
- Go to Tools → Windows Server Backup
- Right-click Local Backup
- Click Backup Once…
- Click Next

🔹 Choose Backup Configuration

 You can choose:

- Full Server Backup
- Custom Backup

👉 Selected: Custom Backup
- Select Custom Backup
- Click Next
- Click Add Items
- Select the files/folders you want to back up
- Click Next

🔹 Select Backup Destination

- Choose Local drive
- Click Next
- Select the backup destination drive
(Example: Local Drive C / D / E)
- Click Backup
- Click Close

✅ Backup completed successfully

---

##🗑️ 3️⃣ Delete File (For Restore Testing)

- Go to the original file location
- Delete the file/folder manually
(This step is done to test restore functionality)
---
##♻️ 4️⃣ Restore Deleted File (Recovery Process)
🔹 Start Recovery Wizard

- Open Server Manager
- Go to Tools → Windows Server Backup
- Right-click Local Backup
- Click Recover

🔹 Recovery Configuration

- Choose Backup location
- Select: This server
- Click Next
- Select Backup date and time
- Click Next
- Choose Files and folders
- Click Next

🔹 Select File to Restore

- Browse and select the deleted file/folder
- Click Next

✅ Choose Restore location:
- Original location 
- Another location

👉 Selected: Original location

- Click Recover
- Click Close

✅ Final Result

🎉 Deleted file restored successfully!

✔ Backup feature installed
✔ Custom backup configured
✔ Data backed up safely
✔ Deleted file recovered successfully

---
## 👨‍💻 Author

**Kumlesh Kurre**  
Bachelor of Computer Applications (BCA) – Pursuing  
IT Support & Networking Enthusiast  

---

⭐ If you find this project helpful, please give it a star on GitHub.
