iMAS - iOS Mobile Application Security
======================================

iOS secure application framework research to reduce iOS application vulnerabilities and information loss

![screenshot](https://github.com/project-imas/about/raw/master/imas_logo.png)

Researchers: [Gregg Ganley](https://github.com/gandg) and [Shawn Valle](https://github.com/SecurityShawn) 


In Short
========
- iOS security controls that go beyond Apple's model
- iMAS wrapped applications will reduce the iOS app attack surface and increase your apps security
- Security control research across static and dynamic vulnerabilities
- iOS vulnerability vector focus
  - Lost / stolen device, physical access attacks
  - Mitigate(1) threat of attacker  that has device, bruteforces the system passcode, and then steals private application information
  - Mitigate(2) malware using system passcode to gain access to private application data
- Industry security standards applied to each control, via Common Weakness Enumeration (CWE) software weaknesses.
- Controls open sourced for community use, feedback, and improvement
- Browse our project, download and give it a try, tell us what you think, or better yet, get involved and participate!


About
=====

iMAS is a collaborative research project from the MITRE corporation. In summary: iMAS is an iOS secure application framework research project focused on reducing iOS application vulnerabilities and information loss.
- The research is investigating how to protect iOS applications and data beyond the Apple provided security model.
- iOS meets enterprise security needs of customers, however many security experts cite critical vulnerabilities and have demonstrated exploits, which pushes enterprises to augment iOS deployments with commercial solutions.
- iMAS will research areas concentrated on reducing an adversary’s ability and efficiency to perform recon, exploitation, control and execution on iOS mobile applications.
- iMAS will transform and increase the effectiveness of the existing iOS security model across major vulnerability areas including the System Passcode, jailbreak, debugger / run-time, flash storage, and keychain. Further, research into a secure application container, including application framework, developer and validation tools/techniques will be done.
- iMAS will apply several software security standards, applicable to many diciplines.
  - Common Weakness Enumerations (CWE), better known as software errors, are applied to each vulnerability addressed. This will better help security engineers identify the value of each implementation. More CWE details can be found at http://cwe.mitre.org.
  - Defense Information Security Agency (DISA) has published a Mobile Application Security Reference Guide (SRG) for U.S. Department of Defense (DoD) mobile app developers.  iMAS addresses DISA's Mobile App SRG where applicable. More SRG details can be found at http://iase.disa.mil/stigs/net_perimeter/wireless/smartphone.html.
- The primary use case is Healthcare PHI information on a mobile device; research will support other use cases.
- Throughout the project, we plan to open source security controls, encourage community developers to get involved, and continue research to maintain relevance and currency. 

![screenshot](https://github.com/project-imas/about/raw/master/iMAS_framework.png)
 

iMAS Custom Security Controls
=============================

iMAS is researching both static and dynamic security defense in the form of custom iOS security controls. Currently four components are available to the open source community:
     
1. [*Secure Foundation Control*](https://github.com/project-imas/securefoundation)
   - Cipherlib, crypto manager, keychain crypto
2. [*AppPassword Control*](https://github.com/project-imas/app-password)
   - Custom iOS user authentication mechanism (password with security questions for self reset)
3. [*PasscodeCheck Control*](https://github.com/project-imas/passcode-check)
   - Allows an application to verify if an iOS passcode has been set and what complexity.  Based on this, an application can programtically decide to execute fully or in a degraded state given this system evidence
4. [*Encrypted Core Data*](https://github.com/project-imas/encrypted-core-data)
   - Provides a Core Data encrypted SQLite store using [SQLCipher](http://sqlcipher.net). 
 
All components are available in an iMAS github repo.

*In the works*

- Jailbreak detection library
  - Developer can programatically decide how its application operates in a jailbroken or standard environment
- Application self-signing integrity check at run-time
  - Developer can programatically determine if the application image has been tampered with
- Run-time memory encryption and post use scrub
  - Elliminate clear-text sensitive data from memory after app use
- Independant security audit conducted on all security controls; updates to follow therafter

How To Use
==========

Browse the README files of each security control, clone, try out the sample app, incorporate into your iOS application, email us with feedback, contribute and participate !!

Why iMAS?
=========

A large percentage of iOS user have a weak system passcode (e.g. simple 4 digit passcode or no passcode at all).  The passcode is integral to the underlying security that supports iOS applications.  With a weak passcode, an attacker within a short of amount of time could connect a laptop to an iPhone/iPad, bruteforce guess the passcode, and steal enterprise information from iOS applications that are protected with standard iOS security.  With iMAS a developer can add security controls that prevent this easy attack.  Enterprises can augment their custom built iOS solutions with iMAS to ensure application security is bolstered and a deeper trust is established. As more and more important information, like a families personal health records, is pushed to mobile devices, measurable increases in security is critical.  With iMAS, we believe the application layer is a key area as part of a balanced, defense in depth security approach.

hReader
=======
iMAS has partnered with hReader to bolster the Apple provided security model. The developers added iMAS security controls to the application resulting in an experience that proved to be a great test-bed and partnership. hReader is a patient-centric mobile health data manager that securely provides patients and their families with their complete health information. To learn more about the application, go to [hReader.org](http://hReader.org) or check out their [source code](https://github.com/projecthreader/hReader).   

*In the works*

iMAS plans to publish a technical report describing the hReader security audit and its resulting, measured security increase along with the labor costs.  Based on this, the iMAS community can add measured security to their applications in a cost effective manner.

Use, Feedback, and Improvement
==============================

We strongly encourage developers to clone and use iMAS. Once you’ve had a chance to use iMAS, tell us what you think by providing us with feedback on your intended use. This information will enable us to address relevancy and need - which will help to keep our research funded in the long run. Lastly, feel free to enhance and improve the actual controls by submitting pull requests early and often!

License
-------

Copyright 2012 The MITRE Corporation, All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
