# 🛡️ Microsoft Entra
## 🎯 Scenario: Block all countries except UK

**Background:**  

An accountancy firm identified multiple unauthorized sign-in attempts originating from foreign IP addresses. To reduce the risk of account compromise, a geolocation-based access control policy was required.

---

## ✅ Lab Objective  
By branding your organization’s Microsoft 365 sign-in experience, users can visually confirm they are on the real company login portal:

- Add countries locations to include UK as trusted site
- Setup conditional access policy to block all countries except UK
- Use a VPN connection to simulate a sign-in from a non-UK location.
- Create a security group in Entra ID for approved exception users.
- Test exception, reattempt the sign-in from a non-UK VPN location and confirm the user is allowed access as expected.

---

## 🧩 Step-by-Step Instructions

### Step 1: Add countries locations

Go to the Entra portal and select **Entra ID > Conditional Access > Named Locations > Countries Location**. Enter name of location. Select **Include unknown countries/regions** and all countries. Search for Unitied Kingdom and de-select country. **Create** location. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag.png" />

---

### Step 2: Setup conditional access policy 

Select **Entra ID > Conditional Access > Policies > New Policy**. Name the policy and select **All users**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag1.png" />

---

### Step 3: Add resources to policy

Select policy to include **All resources**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag2.png" />

---

### Step 4: Add network location to policy

Configure policy to include **Select networks and locations** and select **All countries except UK**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag3.png" />

---

### Step 5: Add acceess controls

Select **Grant** control access and set to **Block access**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag4.png" />

---

### Step 6: Enable policy 

Turn on policy and **Create**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag5.png" />

---

### Step 7: Enable VPN

Enable a VPN from non UK country to test policy is working 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag6.png" />

---

### Step 8: Test sign-in is blocked

Login as user to confirm that changes have now been implemented.

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag7.png" />

---

### Step 9: Create exception group 

Select **Entra ID > Groups > New group**. Enter **Group name** and **Group desciption**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag8.png" />

---

### Step 10: Add member

Select user to add to group in order to test execption works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag9.png" />

---

### Step 11: Add group to policy

Select **Entra ID > Conditional Access > Policies > Block all countries except UK**. Select **Users > Exclude > Users and groups** and select group **International Access Exceptions**

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag10.png" />

---

### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag11.png" />

---

### Step 13: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag12.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag13.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag14.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag15.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag16.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag17.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag18.png" />

---
### Step 12: Test exception group 

Login again to VPN enabled browswer to confirm exception group works. 

<img width="1767" alt="Screen Shot 2025-05-07 at 11 26 51 PM" src="https://github.com/russellcayless/Qualys/blob/d6018a2d08c2df10750c5847d7095d208de2f35f/qu_ag19.png" />

---

