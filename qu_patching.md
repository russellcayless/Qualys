# ⚠️ Qualys
## 🎯 Scenario: Agent Setup and Patch Remediation 

**Background:**  

Qualys cloud agent needs to be setup on Windows 11 PC and any outstanding patches required being applied. 

---

## ✅ Lab Objective  

- Download and install Qualys cloud agent on Windows 11 device
- Identify if any patches are required 
- Create Windows deployment job to install outstanding patches

---

## 🧩 Step-by-Step Instructions

### Step 1: Locate Activation Keys

Go to the Qualys portal and select **Cloud Agent > Asset Management > Activation Keys**. Locate agent for endpoints and select **Install Agents** and select **Install instructions** for Windows (exe)

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag.png" />

---

### Step 2: Download agent 

Select **Download.exe** to download the Windows agent. Copy command for installation. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag1.png" />

---

### Step 3: Copy agent to device

On Windows device copy agent in to folder ready for install.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag2.png" />

---

### Step 4: Install agent

Open command prompt with admin privleges. Copy and run command for installing the agent. Confirm successful by checking agent is running within task manager. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag3.png" />

---

### Step 5: View device in Qualys

Navigate to **Cloud Agent > Asset Management > Agents** to confirm you can see device in cloud platform. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag4.png" />

---

### Step 6: View device in Patch Management

Navigate to **Patch Management > Assets > Windows** to see if any patches are missing on device. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag5.png" />

---

### Step 7: Asset Details

Select the asset name to view asset details. Select **Patch Management** to view missing patches then **View** to see patch list for device. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag6.png" />

---

### Step 8: New Patch Job

Select the patches and then **Actions > Add to new job**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag7.png" />

---

### Step 9: Create Windows Deployment Job

Enter title of the job and **Next**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag8.png" />

---

### Step 10: Select Asset

Select the asset which is to receive patches and **Next**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag9.png" />

---

### Step 11: Pre Actions

Select **Next** for pre actions.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag10.png" />

---

### Step 12: Select Patches

Select the patches for manual installation and **Next**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag11.png" />

---

### Step 13: Post Actions 

Select **Next** for post actions. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag12.png" />

---
### Step 14: Schedule

Select **On-Demand** and **Next**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag13.png" />

---
### Step 15: Reboot Request

Enable reboot request for user and select **Next**.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag14.png" />

---
### Step 16: Reboot Countdown

Enable reboot countdown and select **Next**.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag15.png" />

---
### Step 17: Job Access 

Select **Next**.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag16.png" />

---
### Step 18: Enable Deployment

Select **Save & Enable**.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag17.png" />

---
### Step 19: Execute Deployment

Verify deployment is exectuting on device. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag18.png" />

---
### Step 20: Confirm job success 

Confirm that job successfully has completed.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag19.png" />

---

