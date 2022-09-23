# Experience with applying the STIG on a Red Hat Enterprise Linux 8 machine

Computers typically ship with a considerable amount of security vulnerabilities that leave the system open for attackers, causing immense concern for national security. To counter this, the Defense Information Systems Agency (DISA) currently develops the Security Techincal Implementation Guides which consist of standards and requirements for securing computer systems for use on Department of Defense networks. The STIG provides cybersecurity guidance on a wide range of products, services, and systems. I have outlined my experience with securing a Red Hat Enterprise Linux 8 machine according to the STIG available.

## Configuration and setup

I installed Red Hat Enterprise Linux on a virtual machine utilizing the KVM hypervisor. The virtual machine has 1536 MB of RAM allocated and 2 cores allotted.

Red Hat Enterprise Linux was configured with a GUI, a root password, and an administrator account that was set up during installation.

## Thoughts and lessons learned

Doing this exercise was valuable in showing me how the STIG enforces confidentiality, integrity, and availability in computer systems. Ensuring that users are continuously authenticated, imposing strict password policies regarding the length, complexity, and expiration, as well as verifying that users, folders, and files have the correct permissions were crucial in securing a computer and maintaining least privilege. Another important focus of the STIG was logging and auditing which is incredibly useful for accountability and examining activity in the case of an investigation.

In retrospect, there were a few steps I should have taken in preparation for implementing the STIG

- Use LUKS encrypted file systems
- Separate file systems for /var, /var/log, /var/log/audit, /home, and /tmp
- Install Red Hat Enterprise Linux with FIPS enabled in the kernel parameters

## Sources

https://public.cyber.mil/stigs

https://www.titania.com/resources/guides/disa-stig-compliance-explained/