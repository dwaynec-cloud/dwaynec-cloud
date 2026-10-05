# Hi, I'm Dwayne C 👋

Network security engineer moving into cloud infrastructure engineering. My background is enterprise networking and security (Palo Alto, Fortinet, Cisco Meraki, Microsoft Sentinel), and I'm building hands-on Azure experience while preparing for the **AZ-104 (Microsoft Azure Administrator)** exam.

**Certifications:** CCNA · CompTIA Security+ · Microsoft SC-900

**Education:** M.S. in Information Technology, Cybersecurity concentration

<!-- Optional: add your LinkedIn URL here -->
<!-- [LinkedIn](https://www.linkedin.com/in/your-profile) -->

---

## Azure lab series

Six connected projects built in one Azure environment, each extending the one before. Every repo documents the architecture, the decisions behind it, what went wrong and how I fixed it, and how each control was verified.

| # | Project | What it demonstrates |
|---|---|---|
| 1 | [VM-RBAC-Config](https://github.com/dwaynec-cloud/VM-RBAC-Config) | Linux VM, custom least-privilege RBAC role, Azure Policy tag enforcement, Encryption at Host, cost budget, Bicep |
| 2 | [VNet-Storage-Config](https://github.com/dwaynec-cloud/VNet-Storage-Config) | Subnet design, NSG isolation, storage with public access disabled, private endpoint with private DNS, Bicep |
| 3 | [Monitoring-Backup-Config](https://github.com/dwaynec-cloud/Monitoring-Backup-Config) | Azure Monitor Agent and Data Collection Rules, Log Analytics, KQL, metric alerts, Recovery Services vault backup |
| 4 | [Entra-Identity-Config](https://github.com/dwaynec-cloud/Entra-Identity-Config) | Conditional Access MFA, Privileged Identity Management with approval, Access Reviews, sign-in log analysis |
| 5 | [AppService-Config](https://github.com/dwaynec-cloud/AppService-Config) | App Service plan, GitHub Actions deployment with OIDC, deployment slots and zero-downtime swap, CPU autoscale, backup and restore |
| 6 | [Storage-Recovery-Config](https://github.com/dwaynec-cloud/Storage-Recovery-Config) | VM disk restore from backup, blob versioning and soft delete, lifecycle management, storage firewall, SAS tokens, redundancy options |

### Highlights

- **A security control breaking a platform dependency.** An outbound-deny NSG rule from Project 2 silently stopped the Azure Monitor Agent in Project 3. I traced it to three required service tags. ([Project 3](https://github.com/dwaynec-cloud/Monitoring-Backup-Config))
- **Portal vs. CLI differences.** The same private endpoint was blocked by Azure Policy in the Portal but succeeded in the CLI, and the CLI needed private DNS built by hand. ([Project 2](https://github.com/dwaynec-cloud/VNet-Storage-Config))
- **Zero downtime, measured.** A request loop during a slot swap returned HTTP 200 on every request, and showed both versions serving traffic for about 20 seconds. ([Project 5](https://github.com/dwaynec-cloud/AppService-Config))
- **Honest verification.** Each README separates what was tested from what was only configured, and documents unresolved issues instead of hiding them.

**Tools:** Azure Portal · Azure CLI · Bicep · KQL · GitHub Actions · Python (Flask)
