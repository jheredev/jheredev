### Hi there 👋 I'm Jheremias Pulache (`jheredev`)

I build **business software and then run the infrastructure it lives on** — the
less common half. Most of my code is around Peruvian electronic invoicing:
turning SUNAT's SOAP web services into APIs a product can actually rely on, plus
the ERP, POS and printing layers around them. The rest of the time I am in the
network: hypervisors, VLANs, firewall policy and self-hosted services.

- 🔭 **Currently building:** FactuGO, a multi-tenant billing ERP — React
  frontend, Python backend and a .NET service that speaks to SUNAT.
- 🧾 **Compliance-critical code:** electronic payment documents (CPE), digital
  signatures and tax validation. Code that produces a legal document has to be
  right the first time.
- 🛡️ **Networking and security:** segmented VLANs with explicit stateful deny
  policies, a segregated network for the internet-facing mail servers, and
  self-audits of my own firewall and switch configurations.
- 🖥️ **Self-hosting in production:** Proxmox, a NAS with a **tested** restore,
  AdGuard + Pi-hole as redundant resolvers, Postal for mail, Prometheus +
  Grafana for monitoring. Twelve runbooks, each with its rollback boundary.
- ⚙️ **Engineering philosophy:** the boring parts have to be boring. Money, tax
  documents and firewall rules are not places for clever code.
- 💬 **Ask me about:** SUNAT integrations, multi-tenant SaaS, Go and .NET
  services, VLAN segmentation, self-hosting, or hardening a home network.
- 📍 **Based in:** Lima, Peru
- 📫 **Reach me:** pulachejheremias@gmail.com

### ✨ Tech stack

**Building it**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

**Running it**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![UniFi](https://img.shields.io/badge/UniFi-0559C9?style=for-the-badge&logo=ubiquiti&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

### 🚀 Featured projects

- **FactuGO — multi-tenant billing ERP** `SaaS`
  Billing platform where each subscribed company's staff runs their business end
  to end: documents, series, and the tax workflow in between.
  **Stack:** React · TypeScript · Python · .NET · PostgreSQL · Docker

- **sunat-cpe-dotnet** `SUNAT · .NET`
  Service for Peruvian electronic payment documents. Speaks to SUNAT so the
  product does not have to.
  **Stack:** C# · .NET

- **factugo-printer-agent** `POS · Go`
  Local agent that prints ERP documents to POS printers. Small, native, and
  installed where the printer actually is.
  **Stack:** Go

- **facturacion-electronica-sunat-api** `Integration`
  REST API over SUNAT's SOAP web services — the layer that turns an unfriendly
  tax protocol into something a modern application can call.
  **Stack:** C# · .NET

- **devops** `Infrastructure`
  Containerised stack behind my own services: Docker Compose, Cloudflare
  Tunnel, Postgres and scripts, driven by a Makefile.
  **Stack:** Docker · Shell · Cloudflare

### 🛡️ Infrastructure I run and audit

- **Network edge** — a UDM Pro with three WANs and a documented failover order,
  behind a MikroTik CRS310 that strips the ISP's QinQ tags at layer 2, plus
  policy-based routing for per-network egress.
- **Segmentation** — separate VLANs for IoT and for the internet-facing mail
  servers, with explicit stateful deny policies between them and the trusted
  network. Written down, including *why* each rule exists.
- **DNS** — AdGuard Home and Pi-hole as two resolvers, with local records kept
  in sync on both so no client silently loses resolution.
- **Mail** — self-hosted Postal and Postfix with SPF, DKIM and DMARC aligned,
  TLS issued over DNS-01, and the reverse-DNS request chased with the ISP.
- **Backups** — weekly hypervisor-level backups to a NAS over NFS with
  retention, and a restore that was **actually performed** rather than assumed.
- **Self-audit** — captured firewall and managed-switch configurations,
  correlated every endpoint, hashed the evidence, and wrote the findings up
  with severity and rollback.
