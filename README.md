# EasyDefenderMacOS

**EasyDefenderMacOS** is a set of Intune policies that simplify onboarding macOS devices into Microsoft Defender for Business/Endpoint.

---

## 🚀 Setup Guide

1. **Verify Defender for Business/Endpoint availability**
   - Go to [security.microsoft.com](https://security.microsoft.com)  
   - Navigate to **Assets → Devices** and ensure your Defender for Business / Defender for Endpoint instance is set up in the tenant.

2. **Enable Intune connection in Defender portal**
   - Go to **System → Settings → Endpoints**  
   - Ensure that the **Microsoft Intune connection** is turned **ON**.

3. **Confirm Defender connection in Intune admin center**
   - Go to [intune.microsoft.com](https://intune.microsoft.com)  
   - Navigate to **Endpoint Security → Microsoft Defender for Endpoint**  
   - Ensure the **Connection status** is **Enabled**.

4. **Set up Apple MDM Push Certificate**
   - In the Intune admin center, go to **Devices → macOS → Enrollment**  
   - Ensure the **Apple MDM Push Certificate** is active.

5. **Device types supported**
   - Works with both **personally-owned devices (work profile)** and **corporate-owned devices**.

6. **Import policies**
   - Import all policies and MacOS app using **Micke's Intune Management Tool**. [https://github.com/Micke-K/IntuneManagement](https://github.com/Micke-K/IntuneManagement) 
     
7. - **Onboarding package**
   - Download your macOS onboarding package from the Defender portal. Follow the instructions in the policy description.
   - Replace the `.xml` file inside the policy **[macOS] - MDE Onboarding package** with the downloaded one.  
   

8. **Offboarding package**
   - Follow the instructions in the policy **[macOS] - MDE Offboarding package**.  
   - ⚠️ **Do not assign this policy** unless you actually need to offboard devices from Defender for Endpoint.

9. **Assign policies**
   - Assign every policy **except** the Offboarding package to your security groups or **All Devices**.

10. **Defender MacOS app**
    - Microsoft Defender for Endpoint (macOS app) must be assigned as **Required** to the same groups / devices.

11. **Test enrollment**
    - On a macOS device, go to [aka.ms/enrollmymac](https://aka.ms/enrollmymac)  
    - The Mac should be automatically enrolled into Defender for Endpoint after device enrollment without any manual steps.

---

## ✅ Summary
With **EasyDefenderMacOS**, onboarding and offboarding macOS devices into /from Microsoft Defender for Endpoint becomes much easier without many manual tasks!
