
NIST SP 800-53 Security Assessment Lab

A self-directed home lab built to practice and demonstrate security assessment methodology against the NIST SP 800-53 Rev. 5 (Moderate baseline) control set. This lab was built and documented independently as part of my GRC/compliance skill development — it does not contain, reference, or reproduce any government, military, or employer data or systems.

Overview

The lab consists of a single Windows Server Active Directory domain controller (Lab-DC01), built locally in VirtualBox. Five common security weaknesses were intentionally introduced, documented, and then remediated (four fully closed, one tracked as an open POA&M item) to mirror a real-world assessment and reporting cycle.

Environment
Component	Detail
Hypervisor	Oracle VirtualBox (local)
OS	Windows Server 2022, Evaluation build
Role	Active Directory Domain Services (Domain Controller)
Domain	lab.local
Network	Isolated host-only virtual network — no internet-facing or production exposure
Scan tool	Nessus Essentials (free tier)
Methodology
Stood up a single-domain Active Directory environment from scratch.
Selected a relevant subset of NIST SP 800-53 Rev. 5 Moderate baseline controls.
Intentionally configured five common misconfigurations tied to specific controls.
Documented each as a finding with a risk rating.
Remediated four findings; tracked the fifth as an open POA&M item with a milestone and target date.
Ran a Nessus Essentials vulnerability scan against the host for independent validation.
Findings Summary
ID	Control(s)	Weakness	Risk	Status
F-01	AC-2, AC-6	Domain Admin rights on a standard account, no justification	Moderate	Remediated
F-02	AU-2, AU-6	Logon/logoff events not captured in audit policy	Moderate	Remediated
F-03	IA-5	Password policy did not enforce length/complexity	High	Remediated
F-04	CM-6, CM-7	Legacy SMBv1 protocol enabled	Moderate	Remediated
F-05	SC-7	RDP not restricted to an approved management subnet	High	Open — POA&M

Full detail, methodology, and the Plan of Action & Milestones (POA&M) table are in the Security Assessment Report.

Repo Structure
/nist-800-53-lab
  README.md
  Sample_Security_Assessment_Report_Gantt.docx
  /screenshots
    F01-before.png
    F01-after.png
    F02-before.png
    F02-after.png
    F03-before.png
    F03-after.png
    F04-before.png
    F04-after.png
    F05-before.png
    F05-scope-update.png
    Nessus-scan-summary.png
Tools Used
Oracle VirtualBox
Windows Server 2022 (Evaluation license)
Active Directory Domain Services / Group Policy Management
Windows Event Viewer
Nessus Essentials
Author

Alexander Juan Gantt — linkedin.com/in/juan-gantt-pro
