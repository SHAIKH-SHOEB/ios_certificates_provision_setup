# iOS Certificates Provision Setup
#### To set up an Apple Developer Certificate and Provisioning Profile, you need to go through a few steps using Apple Developer Account and Xcode (or manually via developer portal). Here's a clear breakdown:
---

## ✅Prerequisites
##### 1) Apple Developer Account
- Must be enrolled in the Apple Developer Program ($99/year).
- Organization accounts require D-U-N-S Number and legal authority.
##### 2) Xcode installed on a Mac (latest version recommended).

## 📜 Certificates & Provisioning Profiles Overview
| Component | Purpose |
| ------ | ------ |
| Certificates | Identify you (or your team) as the developer. Used to sign the app. |
| Provisioning Profiles | Connect your app, device, and certificate together to run or distribute the app. |
---
## 🛠️ How to Set Up
#### 🔐 1. Create a Certificate (Distribution)
You can do this using Xcode (automatic) or manually via Apple Developer Portal.

###### 🔸 Using Xcode (Recommended for simplicity)
1) Open Xcode → Settings → Accounts.
2) Add your Apple ID.
3) Xcode will auto-manage certificates and provisioning profiles.
4) When archiving, it will create and use the right certificate/profile.
###### 🔸 Manual (Using Developer Portal)
1) Go to: https://developer.apple.com/account
2) Under Certificates, Identifiers & Profiles → Certificates.
3) Click ➕ (plus) to create a new certificate.
4) Choose:
    - iOS Distribution (App Store and Ad Hoc) → for App Store
    - iOS Development → for dev/testing

5) Follow the steps:
    - Generate a Certificate Signing Request (CSR) using Keychain Access on your Mac.
    - Upload the .certSigningRequest file.
    - Download the certificate (.cer) and double-click to install it in Keychain.

#### 🆔 2. Create an App ID
1) Go to Developer Portal → Identifiers → Click ➕.
2) Register a new App ID (Bundle ID, like com.companyname.appname).
3) Select necessary capabilities (e.g., Push Notifications, iCloud).

#### 📄 3. Create a Provisioning Profile
1) Go to Profiles → Click ➕.
2) Choose App Store (for distribution) or Development (for dev/test).
3) Select the App ID you created earlier.
4) Choose the certificate(s) you want to include.
5) Name the profile and download it.
6) Double-click the .mobileprovision file to install it.

#### 🔄 Summary Flow (Manual)
1) ✅ Enroll in Apple Developer Program
2) 🔐 Generate CSR → Create Certificate
3) 🆔 Create App ID (Bundle Identifier)
4) 📄 Create Provisioning Profile (Select App ID & Certificate)
5) 💻 Install Certificate and Profile in Keychain/Xcode
