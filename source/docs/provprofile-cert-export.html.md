---
title: How to export your Certificate and Provisioning Profile
---

# Provisioning Profile

To export the Provisioning Profile simply follow these steps:

* Visit the [Apple Member Center](https://developer.apple.com/membercenter/). You can use your AppleID to login.
* Choose "Certificates, Identifiers & Profiles"
* Choose Provisioning Profile

![Member Center](images/provprofile-cert-export/MemberCenter.png "Member Center")

* Find the Provisioning Profile you need, select it and click download (the file extension is .mobileprovision)

![Provisioning Profile](images/provprofile-cert-export/ProvProf.png "Provisioning Profile")

* Visit the Application Settings page on Bitrise and upload the downloaded (.mobileprovision) file  with the Build Certificate and let the building begin!


# Build Certificate

To export the Build Certificate simply follow these steps:

* The Build Certificate can be found in yout Keychain, in the Certificates category

![Keychain](images/provprofile-cert-export/Keychain.png "Keychain")

* It should be an expandable field
* Simply right click and select Export and it will export it with the .p12 file extension
* Visit the Application Settings page on Bitrise and upload the exported (.p12) file with the Provisioning Profile and let the building begin!
