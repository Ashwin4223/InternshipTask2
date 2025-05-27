# InternshipTask2
ElevateLabs Internship Task2

# 🛡️ Phishing Email Analysis 

## 📂 Sample Used:
**Phishing Email Theme**: Microsoft Account Security Alert  
**Type**: Credential Phishing  
**Purpose**: Trick users into clicking a malicious link under the guise of a login alert

---

## 🔍 Step-by-Step Analysis Based on Email Phishing

### 1. **Obtain a Sample Phishing Email**
I have used a **spoofed Microsoft security alert** email claiming there was a suspicious login attempt from Russia. The user is prompted to click a link to verify activity.

**Sample Email:**
![Screenshot 2025-05-27 121122](https://github.com/user-attachments/assets/e67d3aeb-1e44-43b2-9fa2-af97af486478)

### 2. **Examine Sender’s Email Address For Spoofing**
**From Address:**  
`account-security@microsoft-supportcenter.com`  
🧨 **Issue:** This is a **spoofed domain**. The real Microsoft domain would be something like `@account.microsoft.com` or `@accountprotection.microsoft.com`.

### 3. **Check Email Headers for Discrepancies**
**Screenshot:**
![Screenshot 2025-05-27 121705](https://github.com/user-attachments/assets/a00ee0f3-fc4a-4561-90fd-176780e20e4e)
**Key Header Findings:**
- **Return-Path:** `account-security@microsoft-supportcenter.com`
- **Received IP:** `185.22.61.134` (not a Microsoft-owned IP)
- **Message-ID:** Not linked to a trusted domain  
🧨 **Red Flag:** The IP and path don’t match Microsoft’s infrastructure.

### 4. **Identify Suspicious Links or Attachments**
**Link Text:** “🔐 Review Recent Activity”  
**Real Link:** `http://microsoft.verify-activity-alert.com`  
🧨 **Red Flag:** Fake domain that looks like Microsoft’s but isn’t.  
**Attachments:** None (common tactic to avoid detection).

### 5. **Look for Urgent or Threatening Language**
**Examples:**
- “Your account may be **temporarily locked** if no action is taken within 24 hours.”  
- “Secure your account **immediately**.”  
🧨 **Red Flag:** Creates false urgency to trick users into quick decisions.

### 6. **Note Any Mismatched URLs**
The CTA button **looks like a safe link**, but hovering shows a **malicious or misleading URL** not associated with Microsoft.

### 7. **Verify Presence of Spelling or Grammar Errors**
- Minor grammatical clues like **“temporarily locked”** used for psychological pressure.
- Generic salutation: “Dear User” instead of using the recipient’s name.

### 8. **Summarize Phishing Traits Found**
| Trait | Status | Notes |
|-------|--------|-------|
| Spoofed sender address | ✅ | Fake Microsoft domain |
| Suspicious IP in header | ✅ | 185.22.61.134 not from Microsoft |
| Malicious link | ✅ | Redirects to phishing site |
| Urgency/threats | ✅ | Claims account will be locked |
| Generic greeting | ✅ | “Dear User” instead of real name |
| Typos/grammar errors | ✅ | Found in email body |
| Visual design | ⚠️ | Looks real but faked |
