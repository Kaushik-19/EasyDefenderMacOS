# EasyDefenderMacOS

**EasyDefenderMacOS** is A set of importable Intune policies that simplify onboarding/offboarding MacOS devices to/from Defender for Business/Endpoint.

**Device types supported**
   - Works with both **personally-owned devices (work profile)** and **corporate-owned devices**

## 🚀 Setup Guide

1. **Verify Defender for Business/Endpoint availability**
   - Go to [security.microsoft.com](https://security.microsoft.com)  
   - Navigate to **Assets → Devices** and ensure your Defender for Business / Defender for Endpoint instance is set up in the tenant.
  
<img width="1435" height="660" alt="image" src="https://github.com/user-attachments/assets/d4cd25aa-b369-4046-9fec-7af049784305" />


2. **Enable Intune connection in Defender portal**
   - Go to **System → Settings → Endpoints**  
   - Ensure that the **Microsoft Intune connection** is turned **ON**.
  
<img width="1846" height="996" alt="image" src="https://github.com/user-attachments/assets/020b15de-161a-4662-b787-e7a5ea2174f2" />


3. **Confirm Defender connection in Intune admin center**
   - Go to [intune.microsoft.com](https://intune.microsoft.com)  
   - Navigate to **Endpoint Security → Microsoft Defender for Endpoint**  
   - Ensure the **Connection status** is **Enabled**.
  
<img width="1030" height="353" alt="image" src="https://github.com/user-attachments/assets/4622ac18-83ec-47cf-9e15-92c883d00981" />


4. **Set up Apple MDM Push Certificate**
   - In the Intune admin center, go to **Devices → macOS → Enrollment**  
   - Ensure the **Apple MDM Push Certificate** is active.
  
<img width="1529" height="695" alt="image" src="https://github.com/user-attachments/assets/e48aa0c6-5b64-4157-a8df-a6ac80db084f" />



5. **Import policies**
   - Import all policies and MacOS app using **Micke's Intune Management Tool**. [https://github.com/Micke-K/IntuneManagement](https://github.com/Micke-K/IntuneManagement)
  
<img width="391" height="411" alt="image" src="https://github.com/user-attachments/assets/e03b2025-83fd-45c0-9122-25f29fbb3e69" />

<img width="2256" height="861" alt="image" src="https://github.com/user-attachments/assets/ec182c21-9982-4f57-ae03-07022f66fbff" />


     
6. - **Onboarding package**
   - Download your macOS onboarding package from the Defender portal. Follow the instructions in the policy description.
   - Replace the `.xml` file inside the policy **[macOS] - MDE Onboarding package** with the downloaded one.

<img width="1532" height="950" alt="image" src="https://github.com/user-attachments/assets/3826eb7f-522a-4eb3-a212-afc183060ecb" />

<img width="814" height="996" alt="image" src="https://github.com/user-attachments/assets/0b602610-87e8-4939-9ac9-f1d6775ff665" />

<img width="811" height="724" alt="image" src="https://github.com/user-attachments/assets/1365e0b0-f215-450c-a6e8-213f431a55b8" />



7. **[ONLY FOR OFFBOARDING] SKIP THIS AND GO TO STEP 8 IF YOU DON'T NEED TO OFFBOARD DEVICES** 
   - Follow the instructions in the policy **[macOS] - MDE Offboarding package**.  
   - ⚠️ **Do not assign this policy** unless you actually need to offboard devices from Defender for Endpoint.

<img width="1799" height="890" alt="image" src="https://github.com/user-attachments/assets/b36cb547-47b6-4863-b984-c26186fc0ae5" />


8. **Assign policies in Devices -> MacOS -> Configuration** 
   - Assign all policies **except** the "[MacOS]- MDE Offboarding package" to your security **Device Group** or **All Devices**.

<img width="1981" height="668" alt="image" src="https://github.com/user-attachments/assets/012f6112-a815-446e-934f-f12e8033dc59" />

<img width="772" height="854" alt="image" src="https://github.com/user-attachments/assets/d96aadf0-816b-4d65-9e80-fc1c5d3e588e" />
     

9. **Set Defender MacOS app as required in Apps-> MacOs**
    - Microsoft Defender for Endpoint (macOS app) must be assigned as **Required** to the same **Device Group** / **All Devices**.

<img width="1593" height="866" alt="image" src="https://github.com/user-attachments/assets/bd921b3a-ffa3-46d2-b164-e6732d553ac0" />
  

10. **Test enrollment**
    - On a macOS device, go to [aka.ms/enrollmymac](https://aka.ms/enrollmymac)  
    - The Mac should be automatically enrolled into Defender for Endpoint **after device enrollment** without any manual steps.

---

## ✅ Summary
With **EasyDefenderMacOS**, onboarding and offboarding macOS devices into /from Microsoft Defender for Endpoint becomes much easier without many manual tasks!
