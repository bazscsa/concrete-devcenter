---
title: Provisioning Profile and Build Certificate Export
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

To export the Provisioning Profile simply follow these steps:

* Visit the [Apple Member Center](https://developer.apple.com/membercenter/). You can use your AppleID to login.
* Choose "Certificates, Identifiers & Profiles"
* Choose Certificates

![Member Center](images/provprofile-cert-export/MemberCenter.png "Member Center")

* Select the Certificate and click download (the file extension is .cer)

![Build Certificate](images/provprofile-cert-export/BuildCert.png "Build Certificate")

* When you downloaded the file open it
* It is added to the your Keychain, you can find it in the Certificates category

![Keychain](images/provprofile-cert-export/Keychain.png "Keychain")

* It should be an expandable field
* Simply right click and select Export and it will export it with the .p12 file extension
* Visit the Application Settings page on Bitrise and upload the exported (.p12) file with the Provisioning Profile and let the building begin!
