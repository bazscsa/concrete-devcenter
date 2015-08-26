---
title: How to export your Certificate and Provisioning Profile
---

# How to export your Certificate and Provisioning Profile

The Provisioning Profile and Build Certificate are crucial part of the development process. The Provisioning Profile contains application related data, the list of devices that can run the given application, the connected Certificates and many more. The type can be development and distribution. The Build Certificate contains information about the developer and makes it possible to sign the application. Both of these files are needed to build your application, test them on devices or upload them to the AppStore. Bitrise also uses the Build Certificate and Provisioning Profile you upload so you can install the application on your devices.

## Provisioning Profile

To export the Provisioning Profile simply follow these steps:

1. Visit the [Apple Member Center](https://developer.apple.com/membercenter/). You can use your AppleID to login and while you're there you should look around a bit. You can download new beta software, find forums and so much more
2. When you no longer hunger for further explorations on the site choose the "Certificates, Identifiers & Profiles"
3. Here we need the Provisioning Profile link

   ![Member Center](images/provprofile-cert-export/MemberCenter.png "Member Center")

4. Find the Provisioning Profile you need, select it and click download (the file extension is .mobileprovision)

   ![Provisioning Profile](images/provprofile-cert-export/ProvProf.png "Provisioning Profile")

5. Visit the Application Settings page on Bitrise and upload the downloaded (.mobileprovision) file  with the Build Certificate and let the building begin!


## Build Certificate

To export the Build Certificate simply follow these steps:

1. ***If you already requested your Build Certificate and downloaded it continue from step 8***
2. Request a Certificate from your Xcode's Accounts section in the Settings
3. When approved visit the [Apple Member Center](https://developer.apple.com/membercenter/). You can use your AppleID to login
4. Choose "Certificates, Identifiers & Profiles"
5. Choose Certificates

   ![Member Center](images/provprofile-cert-export/MemberCenter.png "Member Center")

6. Select the Certificate and click download (the file extension is .cer)

   ![Build Certificate](images/provprofile-cert-export/BuildCert.png "Build Certificate")

7. When you downloaded the file open it
8. The Build Certificate can be found in your Keychain along with other safety-critical information. It is in the Certificates category

   ![Keychain](images/provprofile-cert-export/Keychain.png "Keychain")

9. It should be an expandable field
10. Simply right click and select Export and it will export it with the .p12 file extension
11. Visit the Application Settings page on Bitrise and upload the exported (.p12) file with the Provisioning Profile and let the building begin!
