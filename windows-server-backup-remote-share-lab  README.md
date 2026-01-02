## 💾 windows-server-backup-remote-share-lab

Windows Server lab demonstrating static IP configuration,client network setup, shared folder access, and backup and restore using Windows Server Backup with a remote
shared folder.


## 🌐 Windows Server IP Address Configuration

---

### Steps Performed
1. Open **Server Manager**
2. Click on **Local Server**
3. Click on **IPv4** (Network settings)
4. Right-click on the active **Network Adapter**
5. Select **Properties**
6. Choose **Internet Protocol Version 4 (TCP/IPv4)**
7. Click **Properties**
8. Assign a static IP address:
9. Click **OK** and **Close**

---

## 🌐 Client machine  Configure Network (IP Address)

## 🧩 Step 1: Configure Network (IP Address)

### 🔧 open Network Settings 

* **Run Window:** `Windows + R`
* Type : `ncpa.cpl`
* **Enter** press karein

### 🌐  Configure Active Adapter

* Right-click on the active network adapter → Properties
* Select: **Internet Protocol Version 4 (TCP/IPv4)**
* Click: **Properties**

### 🧾 IP Configuration

```text
IP Address        : 10.0.0.2
Subnet Mask       : 255.0.0.0
Preferred DNS     : 10.0.0.1
```

* **Apply → OK**

---

## 📡 Step 2: Check Network Connectivity

### 💻 Open Command Prompt 

```cmd
ping 10.0.0.1
```

✅ **The ping Reply should be successfully **

## 1️⃣  Share Folder on 
- Open **File Explorer** on the  client machine
- Go to the required drive (e.g. `D:`)
- Right-click → **Properties**
- Go to **Sharing → Advanced Sharing**
- Enable **Share this folder**
- Click **Permissions**
- Allow **Full Control**
- Click **Apply → OK**

## Copy network sharing path  
win-62QTLAIRTKE\d (It is local d drive path)


##⚙️ 2️⃣ Windows server Configure Backup (Backup Once)
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

- Choose Remote shared folder
- Click Next
- Select the backup destination location
(Location: \\10.0.0.2\d) (ip address\foldername)
- insert Client machine username and password
- Click backup and Close

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
- Select: A backup stored on other location and Remote share folder
- give(Location: \\10.0.0.2\d) (ip address\foldername)
- Click Next
- insert Client machine username and password
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

👉 Selected: Anotherl location

- select location
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


