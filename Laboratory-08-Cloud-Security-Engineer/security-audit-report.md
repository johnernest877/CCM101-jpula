# Security Audit Report

## The Principle of Least Privilege (PoLP)
The Principle of Least Privilege is a security concept where a user or system is only granted the minimum level of access necessary to perform their specific job functions. In cloud environments, this is crucial because if an account is compromised, the attacker's access is strictly limited to what that specific account can do, preventing them from taking over the entire system.

## Attack Surface
An attack surface refers to the sum of all the different points (or "vectors") where an unauthorized user can try to enter data into or extract data from an environment. For a virtual machine, this includes open network ports, running services, user accounts, and software vulnerabilities; the larger the attack surface, the more vulnerable the system is to cyberattacks.

## Default Deny Policy
A Default Deny policy means that a firewall or security system blocks all incoming and outgoing traffic by default, unless a rule explicitly states that specific traffic is allowed. This is much safer than a "Default Allow" policy because it ensures that any new, unknown, or malicious traffic is automatically blocked, rather than accidentally letting hackers in through unconfigured ports.