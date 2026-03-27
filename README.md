# Awesome Claw Opus 🦞🔒

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of OpenClaw security, self-hosting, and enterprise resources — covering CVEs, hardening guides, deployment patterns, and ecosystem forks.

## Contents

- [Security](#security)
  - [Known Vulnerabilities & CVEs](#known-vulnerabilities--cves)
  - [Vulnerability Reports](#vulnerability-reports)
  - [Security Audit Tools](#security-audit-tools)
  - [Security Best Practices](#security-best-practices)
  - [Security-Enhanced Variants](#security-enhanced-variants)
  - [Supply Chain Attacks (ClawHavoc)](#supply-chain-attacks-clawhavoc)
  - [Security Research](#security-research)
- [Self-Hosting](#self-hosting)
  - [Docker & Kubernetes](#docker--kubernetes)
  - [Cloud Platforms](#cloud-platforms)
  - [Reverse Proxy & Networking](#reverse-proxy--networking)
  - [Performance Optimization](#performance-optimization)
  - [Backup & Recovery](#backup--recovery)
- [Enterprise](#enterprise)
  - [Architecture & Case Studies](#architecture--case-studies)
  - [Multi-Tenant Solutions](#multi-tenant-solutions)
  - [Monitoring & Observability](#monitoring--observability)
  - [Compliance & Audit](#compliance--audit)
  - [Enterprise Tool Integrations](#enterprise-tool-integrations)
- [Ecosystem](#ecosystem)
- [Contributing](#contributing)
- [License](#license)

---

## Security

### Known Vulnerabilities & CVEs

- [CVE-2026-25253 (CVSS 8.8) — RCE One-Click Exploit](https://www.proarch.com/blog/threats-vulnerabilities/openclaw-rce-vulnerability-cve-2026-25253) — Remote code execution vulnerability, patched in v2026.1.29.
- [CVE-2026-32064](https://www.redpacketsecurity.com/cve-alert-cve-2026-32064-openclaw-openclaw/) — Recently disclosed CVE affecting OpenClaw core.
- [OpenClawCVEs Tracker](https://github.com/jgamblin/OpenClawCVEs/) — Community-maintained CVE tracking repository.
- [OpenClaw GitHub Security](https://github.com/openclaw/openclaw/security) — Official security advisories and disclosure page.
- [Adversa AI: CVE Details + Moltbook Leak + Hardening](https://adversa.ai/blog/openclaw-security-101-vulnerabilities-hardening-2026/) — In-depth CVE analysis, Moltbook credential leak, and hardening recommendations.

### Vulnerability Reports

- [The Hacker News: Prompt Injection & Data Exfiltration](https://thehackernews.com/2026/03/openclaw-ai-agent-flaws-could-enable.html) — Coverage of prompt injection flaws enabling data exfiltration.
- [Dark Reading: Critical Vulnerability](https://www.darkreading.com/application-security/critical-openclaw-vulnerability-ai-agent-risks) — Analysis of critical vulnerabilities introducing AI agent risks.
- [Kaspersky: Unsafe for Use](https://www.kaspersky.com/blog/openclaw-vulnerabilities-exposed/55263/) — Kaspersky's assessment of OpenClaw vulnerability exposure.
- [Cisco Blog: Security Nightmare](https://blogs.cisco.com/ai/personal-ai-agents-like-openclaw-are-a-security-nightmare) — Cisco's perspective on personal AI agent security risks.
- [VentureBeat: Bypassing EDR/DLP/IAM](https://venturebeat.com/security/openclaw-can-bypass-your-edr-dlp-and-iam-without-triggering-a-single-alert) — Research showing OpenClaw can silently bypass enterprise security controls.
- [Infosecurity: 42,665 Exposed Instances](https://www.infosecurity-magazine.com/news/researchers-40000-exposed-openclaw/) — Researchers discover over 42,000 publicly exposed OpenClaw instances.
- [Conscia: Security Crisis](https://conscia.com/blog/the-openclaw-security-crisis/) — Overview of the broader OpenClaw security crisis.
- [Giskard: Data Leakage & Prompt Injection](https://www.giskard.ai/knowledge/openclaw-security-vulnerabilities-include-data-leakage-and-prompt-injection-risks) — Technical breakdown of data leakage and prompt injection attack surfaces.

### Security Audit Tools

- [ClawGuard](https://www.clawguard.net/) — Open-source skill scanner that intercepts high-risk skills before execution.
- [ClawSecure](https://github.com/ClawSecure/clawsecure-openclaw-security) — OWASP ASI Top 10 coverage with 55+ threat patterns; has audited 2,890+ agents.
- [Bitdefender AI Skills Checker](https://www.bitdefender.com/en-us/consumer/ai-skills-checker) — Free skill security detection service from Bitdefender.
- [openclaw-security-monitor](https://github.com/adibirzu/openclaw-security-monitor) — Active security monitoring for running OpenClaw instances.
- [ClawDefend](https://www.clawdefend.com/) — Developer-focused security scanning for OpenClaw skills.
- [VirusTotal Official Integration](https://thehackernews.com/2026/02/openclaw-integrates-virustotal-scanning.html) — Native VirusTotal scanning for ClawHub skills.
- [claude-skill-security-auditor](https://github.com/wrsmith108/claude-skill-security-auditor) — Security auditor specifically targeting Claude Code skills.

### Security Best Practices

- [OpenClaw Security Best Practices (2026)](https://openclawroadmap.com/security-best-practices.php) — Comprehensive hardening guide covering the full OpenClaw stack.
- [Nebius: Architecture Hardening Guide](https://nebius.com/blog/posts/openclaw-security) — Architecture-level hardening recommendations for production deployments.
- [OpenClaw Expert: Hardening Guide 2026](https://www.openclaw.expert/blog/openclaw-security-hardening-2026) — Firewall, VPN, and credential rotation best practices.
- [7 Security Best Practices](https://xcloud.host/openclaw-security-best-practices/) — CVE defense and data protection checklist.
- [Official Gateway Security](https://docs.openclaw.ai/gateway/security) — Official documentation for OpenClaw gateway security configuration.
- [ClawHub Malware Crisis](https://blink.new/blog/is-openclaw-safe-clawhub-malware-guide-2026) — Guide to navigating the ClawHub malware crisis safely.

### Security-Enhanced Variants

- [IronClaw](https://github.com/nearai/ironclaw) — Rust-based fork with WebAssembly isolation, capability-based permissions, and credential injection/leak detection.
- [IronClaw Review](https://awesomeagents.ai/reviews/review-ironclaw/) — In-depth review of IronClaw's security architecture and trade-offs.
- [Cisco DefenseClaw](https://www.how2shout.com/news/cisco-defenseclaw-openclaw-security-clawhavoc-supply-chain-attack.html) — Cisco's hardened fork designed specifically to counter supply chain attacks.
- [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) — Rust-based fork with filesystem sandboxing, distributed as a 3 MB single binary.

### Supply Chain Attacks (ClawHavoc)

- [Repello AI: Inside ClawHavoc](https://repello.ai/blog/clawhavoc-supply-chain-attack) — Detailed post-mortem of the ClawHavoc attack affecting 300,000 users.
- [CyberPress: 1,184 Malicious Skills](https://cyberpress.org/clawhavoc-poisons-openclaws-clawhub-with-1184-malicious-skills/) — Report on 1,184 malicious skills distributed via ClawHub.
- [Particula: 20% Skills Malicious](https://particula.tech/blog/openclaw-security-crisis-malicious-ai-agents) — Research finding 20% of sampled ClawHub skills contain malicious behavior.
- [Security Boulevard: Securing Against ClawHavoc](https://securityboulevard.com/2026/02/securing-openclaw-againstclawhavoc/) — Defensive measures against ClawHavoc-style supply chain attacks.
- [Oathe: Audited 1,620 Skills, Scanner Missed 91%](https://oathe.ai/engineering/we-audited-1620-ai-agent-skills/) — Independent audit revealing existing scanners miss 91% of malicious skills.

### Security Research

- [The New Stack: 22,511 Skills Audit (140,963 Vulnerabilities)](https://thenewstack.io/ai-agent-skills-security/) — Large-scale audit of AI agent skills uncovering nearly 141K vulnerabilities.
- [Medium: Supply Chain Attack Analysis](https://medium.com/@shriganeshad/the-ai-agent-supply-chain-attack-you-need-to-know-about-openclaw-clawhavoc-and-corporate-e85b647649e9) — Analysis of the corporate implications of OpenClaw supply chain attacks.
- [Composed Security: OpenClaw vs IronClaw](https://composedsecurity.medium.com/openclaw-is-viral-ironclaw-is-what-comes-after-you-read-the-security-reports-7c43bbf07b86) — Comparative security analysis between OpenClaw and IronClaw.
- [Repello AI: Skill Security Audit Guide](https://repello.ai/blog/claude-code-skill-security) — Practical guide for auditing Claude Code skills.
- [OX Security: Crypto-Wallet Phishing Attack](https://www.ox.security/blog/openclaw-github-phishing-crypto-wallet-attack/) — Disclosure of a GitHub-hosted phishing campaign targeting crypto wallets via OpenClaw.

---

## Self-Hosting

### Docker & Kubernetes

- [Official Docker Guide](https://docs.openclaw.ai/install/docker) — Official documentation for running OpenClaw in Docker.
- [K8s Operator](https://github.com/openclaw-rocks/k8s-operator) — Official Kubernetes Operator for deploying OpenClaw on K8s.
- [LumaDock: Docker & K8s Tutorial](https://lumadock.com/tutorials/openclaw-docker-kubernetes) — Step-by-step tutorial covering both Docker and Kubernetes deployments.
- [LumaDock: High Availability Clustering](https://lumadock.com/tutorials/openclaw-high-availability-clustering) — Guide for setting up high-availability OpenClaw clusters.
- [Yotta Labs: Production Docker/K8s/GPU](https://www.yottalabs.ai/post/how-to-deploy-openclaw-in-production-docker-kubernetes-and-gpu-infrastructure) — Production deployment guide covering Docker, Kubernetes, and GPU infrastructure.
- [Cloud Native Deep Dive: K8s](https://www.cloudnativedeepdive.com/running-openclaw-on-kubernetes/) — Deep dive into running OpenClaw on Kubernetes in a cloud-native setup.
- [Simon Willison: Docker](https://til.simonwillison.net/llms/openclaw-docker) — Concise TIL-style guide for running OpenClaw via Docker.

### Cloud Platforms

- [Official GCP Guide](https://docs.openclaw.ai/install/gcp) — Official documentation for deploying OpenClaw on Google Cloud Platform.
- [Railway One-Click Deploy](https://railway.com/deploy/openclaw-ai-assistant-with-easy-install-) — One-click Railway deployment template.
- [DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-run-openclaw) — Community tutorial for running OpenClaw on DigitalOcean.
- [DigitalOcean App Platform](https://www.digitalocean.com/blog/openclaw-digitalocean-app-platform) — Guide for deploying on DigitalOcean's managed App Platform.
- [Hostinger VPS](https://www.hostinger.com/vps/docker/openclaw) — Hostinger VPS deployment guide using Docker.
- [Alibaba Cloud](https://www.alibabacloud.com/en/campaign/ai-openclaw) — Alibaba Cloud deployment campaign and documentation.
- [Tencent Cloud](https://www.tencentcloud.com/techpedia/139184) — Tencent Cloud deployment guide.
- [AWS](https://dev.to/brayanarrieta/how-to-set-up-openclaw-ai-on-aws-3a0j) — Community guide for setting up OpenClaw on AWS.
- [Cloudflare/Vercel Comparison](https://apidog.com/blog/how-to-deploy-openclaw-on-cloudflare-vercel-or-simpleclaw/) — Comparison of Cloudflare, Vercel, and SimpleClaw deployment options.
- [Cloud vs Local Comparison](https://help.apiyi.com/en/openclaw-cloud-vs-local-deployment-guide-en.html) — Decision guide comparing cloud hosting vs local self-hosting.

### Reverse Proxy & Networking

- [Official Trusted Proxy Auth](https://docs.openclaw.ai/gateway/trusted-proxy-auth) — Official documentation for trusted proxy authentication configuration.
- [ClawTank: Caddy/Nginx/Trusted Proxies](https://clawtank.dev/blog/openclaw-reverse-proxy-trusted-proxies) — Guide covering Caddy, Nginx, and trusted proxy configuration.
- [Nginx/Apache Reverse Proxy Tutorial](https://openclawn.com/openclaw-reverse-proxy-nginx-apache/) — Step-by-step reverse proxy setup for Nginx and Apache.
- [Multi-App Nginx Setup](https://dev.to/agent_paaru/openclaw-behind-nginx-on-a-shared-server-multi-app-reverse-proxy-setup-535) — Running OpenClaw behind Nginx alongside other applications on a shared server.
- [Cloudflare Tunnel / Tailscale](https://blog.canadianwebhosting.com/openclaw-cloudflare-tunnel-tailscale-no-public-ports/) — Exposing OpenClaw without opening public ports using Cloudflare Tunnel or Tailscale.
- [Secure Remote Access](https://open-claw.me/blog/openclaw-remote-access-safely) — Best practices for accessing a self-hosted OpenClaw instance remotely.

### Performance Optimization

- [Multi-Instance & Load Balancing](https://oepnclaw.com/en/tutorials/openclaw-multi-instance.html) — Tutorial on running multiple OpenClaw instances with load balancing.
- [Performance Tuning Docs](https://www.openclawcenter.com/docs/performance-tuning) — Official performance tuning documentation.
- [80% Cost Reduction](https://eastondev.com/blog/en/posts/ai/20260205-openclaw-performance/) — Case study achieving 80% infrastructure cost reduction through tuning.
- [Memory Architecture Guide](https://ubos.tech/configuring-tuning-and-scaling-openclaw-memory-architecture-a-developer-guide/) — Developer guide for configuring and scaling OpenClaw's memory architecture.
- [Memory, Concurrency & Context](https://medium.com/@creativeaininja/how-to-optimize-openclaw-memory-concurrency-and-context-that-actually-works-84690c2de3d7) — Practical guide to optimizing memory, concurrency, and context handling.
- [Multi-Agent Coordination](https://stormap.ai/post/multi-agent-workflows-coordinating-multiple-openclaw-instances) — Patterns for coordinating multiple OpenClaw instances in multi-agent workflows.
- [4 Weeks in Production](https://www.sitepoint.com/openclaw-production-lessons-4-weeks-self-hosted-ai/) — Real-world lessons from running OpenClaw in production for four weeks.

### Backup & Recovery

- [Official CLI Backup](https://docs.openclaw.ai/cli/backup) — Official CLI documentation for backup and restore operations.
- [Complete Backup Guide](https://www.openclawexperts.io/guides/setup/how-to-backup-and-restore-openclaw) — Comprehensive guide covering full backup and restore procedures.
- [Data Protection Guide](https://openclawblog.space/articles/openclaw-backup-and-restore-complete-data-protection-guide) — End-to-end data protection guide for OpenClaw deployments.
- [Settings & Memory Export](https://lumadock.com/tutorials/openclaw-backup-export-settings-memory) — Tutorial for exporting OpenClaw settings and memory.
- [Disaster Recovery on Hetzner](https://dev.to/clawsetup/openclaw-backup-disaster-recovery-on-hetzner-rporto-restore-drills-and-practical-failover-for-1c4e) — Disaster recovery setup with restore drills and practical failover on Hetzner.
- [openclaw-backup Tool](https://github.com/LeoYeAI/openclaw-backup) — Open-source CLI tool for automated OpenClaw backups.
- [Keep My Claw](https://keepmyclaw.com/) — Managed zero-knowledge encrypted backup service for OpenClaw.

---

## Enterprise

### Architecture & Case Studies

- [Enterprise Multi-User & Hardening](https://eastondev.com/blog/en/posts/ai/20260205-openclaw-enterprise-deploy/) — Guide for multi-user enterprise deployments with hardening applied.
- [Enterprise Security Setup](https://voxturrlabs.com/blog/openclaw-enterprise-setup-guide/) — Security-focused enterprise setup walkthrough.
- [Enterprise Automation Use Cases](https://www.digitalapplied.com/blog/openclaw-enterprise-automation-business-use-cases-guide) — Survey of enterprise automation use cases and implementation patterns.
- [Customer Service to Sales](https://openclaws.io/blog/openclaw-enterprise-use-cases/) — Case studies ranging from customer service automation to sales workflows.
- [Business Workflows & Guardrails](https://www.codebridge.tech/articles/openclaw-case-studies-for-business-workflows-that-show-where-autonomous-ai-creates-value-and-where-enterprises-need-guardrails) — Case studies examining where autonomous AI creates value and where guardrails are needed.
- [One Month Review](https://mysummit.school/blog/en/openclaw-month-later/) — Honest one-month post-deployment review of enterprise OpenClaw usage.
- [Presidio: NVIDIA Ecosystem](https://www.presidio.com/blogs/openclaw-enterprise-deployment-the-html-of-the-agentic-era-and-nvidia-just-built-the-browser/) — Enterprise deployment in the NVIDIA ecosystem with Presidio's perspective.
- [Implementation Guide](https://insights.theinteractive.studio/openclaw-for-business-what-it-is-real-use-cases-and-how-to-implement-it) — Practical implementation guide for business teams adopting OpenClaw.

### Multi-Tenant Solutions

- [RBAC Feature Request #8081](https://github.com/openclaw/openclaw/issues/8081) — Upstream issue tracking role-based access control support.
- [Agents Plane #17299](https://github.com/openclaw/openclaw/issues/17299) — Upstream issue tracking multi-tenant agent plane support.
- [openclaw-multitenant](https://github.com/jomafilms/openclaw-multitenant) — Container isolation with encrypted vault and team sharing support.
- [lobu](https://github.com/lobu-ai/lobu) — Multi-tenant OpenClaw solution designed for team deployments.
- [Session Isolation Vulnerability](https://www.penligent.ai/hackinglabs/openclaw-multi-user-session-isolation-failure-authorization-bypass-and-privilege-escalation/) — Research exposing session isolation failures, authorization bypass, and privilege escalation in multi-user setups.

### Monitoring & Observability

- [VPS Monitoring](https://lumadock.com/tutorials/openclaw-monitoring-vps-uptime-logs-metrics-alerts) — Tutorial for uptime, log, metrics, and alert monitoring on VPS deployments.
- [SigNoz: OpenTelemetry Integration](https://signoz.io/docs/openclaw-monitoring/) — Official SigNoz documentation for OpenClaw OpenTelemetry integration.
- [SigNoz: Dashboard Guide](https://signoz.io/blog/monitoring-openclaw-with-opentelemetry/) — Guide for building OpenClaw monitoring dashboards with OpenTelemetry.
- [Comet/Opik: Native Observability](https://www.comet.com/site/blog/openclaw-observability/) — Native observability integration using Comet and Opik.
- [openclaw-observability-plugin](https://github.com/henrikrexed/openclaw-observability-plugin) — Open-source observability plugin for OpenClaw.
- [ClawMetry](https://www.producthunt.com/products/clawmetry) — Real-time metrics dashboard for OpenClaw instances.
- [BytePlus: Trace Monitoring](https://docs.byteplus.com/en/docs/Observability_Platform/OpenClaw_trace_monitoring) — Distributed trace monitoring for OpenClaw via BytePlus Observability Platform.

### Compliance & Audit

- [SOC 2 / HIPAA / GDPR Guide](https://www.getopenclaw.ai/how-to/enterprise-security-compliance) — Enterprise compliance guide covering SOC 2, HIPAA, and GDPR requirements.
- [2026 Enterprise Hardening](https://www.mintmcp.com/blog/secure-openclaw-enterprise) — Up-to-date enterprise hardening guidance for 2026.
- [CLAW-10 Evaluation Framework](https://onyx.app/insights/openclaw-enterprise-evaluation-framework) — Structured framework for evaluating OpenClaw enterprise readiness.
- [SOC 2 Audit Log Gap](https://www.clawctl.com/blog/soc2-ai-agent-no-audit-log) — Important finding: OpenClaw lacks the audit logging required for SOC 2 compliance.
- [Security Model Deep Dive](https://get-to-know-openclaw-security-model.vercel.app/) — Comprehensive deep dive into OpenClaw's underlying security model.
- [Official SECURITY.md](https://github.com/openclaw/openclaw/blob/main/SECURITY.md) — Official security policy and vulnerability reporting instructions.

### Enterprise Tool Integrations

- [Salesforce MCP](https://composio.dev/toolkits/salesforce/framework/openclaw) — Salesforce integration via MCP for OpenClaw agents.
- [Salesforce Service Cloud](https://composio.dev/toolkits/salesforce_service_cloud/framework/openclaw) — Salesforce Service Cloud integration for support automation.
- [Jira MCP](https://composio.dev/toolkits/jira/framework/openclaw) — Jira integration via MCP for project management automation.
- [ServiceNow MCP](https://composio.dev/toolkits/servicenow/framework/openclaw) — ServiceNow integration for IT service management workflows.
- [Jira Integration Guide](https://www.getopenclaw.ai/en/integrations/jira) — Step-by-step guide for connecting OpenClaw to Jira.
- [Expanso: Jira Automation](https://expanso.io/expanso-hearts-openclaw/jira/) — Expanso's guide for automating Jira workflows with OpenClaw.
- [ServiceNow Agent Skill](https://openclawskills.best/skills/thesethrose/servicenow-agent/) — Community-built ServiceNow agent skill for ClawHub.

---

## Ecosystem

A brief overview of notable OpenClaw forks and related frameworks.

| Project | Stars | Language | Highlight |
|---|---|---|---|
| [OpenClaw](https://github.com/openclaw/openclaw) | 331K+ | — | The original |
| [Nanobot](https://github.com/HKUDS/nanobot) | 34.6K | Python | Hong Kong University project |
| [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) | 28K | Rust | 3 MB single binary |
| [PicoClaw](https://github.com/sipeed/picoclaw) | 25K | Go | IoT and edge computing |
| [NanoClaw](https://github.com/qwibitai/nanoclaw) | 10K | TypeScript | 500 lines |
| [IronClaw](https://github.com/nearai/ironclaw) | — | Rust | WebAssembly sandbox security |
| [MicroClaw](https://github.com/gtanjil/MicroClaw) | — | Rust (no_std) | Bare-metal / chip-level |
| [ClawSwarm](https://github.com/The-Swarm-Corporation/ClawSwarm) | — | — | Native multi-agent orchestration |

---

## Contributing

Contributions are welcome. Please:

1. Check that the link is alive and directly relevant to OpenClaw security, self-hosting, or enterprise use.
2. Add a short, factual description (one sentence).
3. Place the entry in the most appropriate section.
4. Submit a pull request with a clear title.

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.
