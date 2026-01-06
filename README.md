# Globus at the Smithsonian

Globus is a secure, high-performance data transfer platform that enables Smithsonian staff to move large datasets between storage systems and share data with external collaborators. Whether you're transferring terabytes of genomic data, archival video collections, high-resolution imagery, or field research files, Globus handles it reliably, even if you close your laptop or your connection drops mid-transfer.

**All Smithsonian staff can log into Globus right now at [app.globus.org](https://app.globus.org/) using their Smithsonian network credentials, no registration, VPN, or Smithsonian network connection required.**

## Which Guide Do I Need?

| I want to... | Start here |
|--------------|------------|
| **Learn the basics** — log in, navigate Globus, transfer files | [Guide 1: Globus Basics and File Transfers](guide1-basics.md) |
| **Share data with an external collaborator** — someone outside Smithsonian needs access to files | [Guide 2: Creating Guest Collections](guide2-sharing-data.md) |
| **Transfer files from my laptop or external drive** — get data from a personal device onto Smithsonian storage | [Guide 3: Globus Connect Personal](guide3-globus-connect-personal.md) |
| **Automate transfers** — set up recurring syncs, scheduled transfers, or multi-step workflows | [Guide 4: Advanced Globus Features](guide4-advanced-features.md) |

### New to Globus?

Start with **[Guide 1](guide1-basics.md)**. It covers everything you need to log in, find collections, and complete your first transfer. The other guides build on these fundamentals.

### Quick Decision Tree

```
What are you trying to do?
│
├── Transfer files between Smithsonian storage systems
│   └── Guide 1: Globus Basics
│
├── Get files FROM my laptop/external drive TO Smithsonian storage
│   └── Guide 3: Globus Connect Personal → then Guide 1 for the transfer
│
├── Share files with someone outside Smithsonian
│   │
│   ├── Is your data already on Smithsonian storage (Hydra, DAMS, STRI, etc.)?
│   │   ├── Yes → Guide 2: Creating Guest Collections
│   │   └── No → Guide 3 first (upload your data), then Guide 2
│   │
│   └── Are YOU the external collaborator receiving shared data?
│       └── Guide 2: "For Your Collaborators" section
│
└── Automate or schedule recurring transfers
    └── Guide 4: Advanced Globus Features
```
## Access & Subscription

**Smithsonian is an institutional subscriber to Globus.** All subscriber features are available to all Smithsonian staff.

| Access Level | What You Get | Requirements |
|--------------|--------------|--------------|
| **Globus Web Application** | Log in, browse collections, manage transfers, use all subscriber features | Smithsonian network credentials (same as email) |
| **Smithsonian Institutional Storage** | Access to Hydra, DAMS staging, STRI servers, network drives, etc. | Smithsonian credentials + account on specific storage system |

**In short:** Any Smithsonian staff member can log into Globus immediately using their network credentials. However, to access data on Smithsonian storage systems, you also need an account on that specific system.

### Need Access to Storage?

| Storage System | Contact |
|----------------|---------|
| Hydra (HPC cluster) | [Request an HPC account on the SI Service Portal](https://smithsonianprod.servicenowservices.com/si?id=sc_cat_item&sys_id=962e05331b96e05078932f41f54bcb3b)|
| DAMS NAS Staging | SI-Globus@si.edu |
| STRI Data Transfer Server | STRIhelp@si.edu |
| Other systems | SI-Globus@si.edu for guidance |

## Quick Links

| Resource | Link |
|----------|------|
| Globus Web App | [app.globus.org](https://app.globus.org) |
| Globus Connect Personal Download | [globus.org/globus-connect-personal](https://www.globus.org/globus-connect-personal) |
| Official Globus Documentation | [docs.globus.org](https://docs.globus.org) |

## Getting Help

| Contact | For |
|---------|-----|
| SI-Globus@si.edu | General Globus support, questions, troubleshooting |
| SI-HPC@si.edu | Hydra system support |
| STRIhelp@si.edu | STRI Data Transfer Server accounts and support |

---

*These guides are maintained by ODI's Chief Data and AI Office. Last updated: 12/19/25. For corrections or suggestions, contact SI-Globus@si.edu or submit an issue in this repository.*
