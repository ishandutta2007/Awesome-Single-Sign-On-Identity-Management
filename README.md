# Awesome-Single-Sign-On-Identity-Management

# Top Single Sign-On & Identity Management Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on SSO Federation, Identity Providers & Self-Hosted IAM Platforms*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Single Sign-On (SSO) & Identity Management**. These tools enable organizations to centralize authentication, federate identities across applications, and enforce access policies—giving users one set of credentials while giving administrators a single point of control for who can access what.

**Examples** include Crowd, Okta, Microsoft Entra ID, Ping Identity, JumpCloud, OneLogin, Auth0, CyberArk, Keycloak, and ForgeRock (the category leaders).

**Open-source emphasis**: SSO & Identity Management is a domain where open-source tooling is **exceptionally mature and production-proven**, with clear leaders for different scales and philosophies. **Keycloak** remains the de facto standard—the most widely adopted open-source IAM platform with SSO, OAuth 2.0, OIDC, SAML, LDAP, and SCIM 2.0 server support . **Authentik** offers a modern, security-focused alternative with flexible flow-based authentication and a polished UI . **Casdoor** provides a UI-first experience where everything is editable in the console, backed by Casbin for policy-based authorization . **Burrow** targets small teams with a single-binary OIDC/SAML identity provider that includes mandatory TOTP and RBAC without the operational weight of Keycloak . The critical caveat: **commercial platforms differentiate on managed compliance, AI agent identity, and ecosystem breadth**—Okta's Agent SSO treats AI agents as first-class identities , and PingOne provides lifecycle automation and governance workflows that open-source tools require assembly to match .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Crowd (Atlassian)](https://www.atlassian.com/software/crowd)**  
  Atlassian's on-premises SSO and identity management platform for Data Center products; Crowd 7.1 adds **SAML and OpenID Connect support**, allowing integration with multiple identity providers as a bridge to Jira, Confluence, and Bitbucket . Centralizes user management across Active Directory, LDAP, Azure AD, and Novell eDirectory . **Best for organizations running Atlassian Data Center** needing a single integration point for IdPs.

- **[Okta](https://www.okta.com/)**  
  The leading independent identity platform; **Agent SSO** (GA August 2026) integrates the Cross App Access standard into Okta's Core SSO, treating AI agents as first-class identities in Universal Directory alongside human users . Agents receive short-lived, identity-governed tokens instead of static credentials, managed through the same console and workflows as employees . Included without additional cost in Core SSO subscriptions . **The benchmark for enterprise SSO with AI agent governance**.

- **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/microsoft-entra)**  
  Microsoft's cloud identity service with unlimited SSO, MFA, passwordless (Windows Hello, FIDO2), certificate-based authentication, Conditional Access, and automatic user provisioning to SaaS applications . **Microsoft Single Sign-On for Linux** (version 2.0.2+) enables Linux desktop SSO with Entra ID via the Microsoft Identity Broker, supporting Phish-Resistant MFA with SmartCard, CBA, or USB tokens . Deep integration with Microsoft 365 and Azure.

- **[Ping Identity](https://www.pingidentity.com/)**  
  Enterprise identity platform (merged with ForgeRock) with **Agent IAM Core** treating autonomous AI agents as governed identities with scoped tokens, least-privilege policies, and MCP/A2A support . PingOne Advanced Identity Cloud includes lifecycle automation (joiner/mover/leaver), access request workflows, and identity governance . PingFederate 13.1 adds private key JWT client assertions, ID-JAG flows, and Client ID Metadata Documents for AI agents . **The strongest option for organizations needing both workforce IAM and AI agent governance**.

- **[JumpCloud](https://jumpcloud.com/)**  
  Cloud directory platform unifying identity, access, and device management; manages macOS, Windows, Linux, iOS, and Android devices from one console with SSO, passwordless authentication (JumpCloud Go), Cloud RADIUS, Cloud LDAP, and conditional access for human, machine, and agent identities . Ranked #1 on G2 across Cloud Directory Services, PAM, and Password Policy Enforcement; 250,000+ organizations . **Best for organizations wanting directory, SSO, and device management in one platform**—especially tech companies and MSPs.

- **[OneLogin](https://www.onelogin.com/)**  
  Identity and access management platform (now part of One Identity) with SSO, MFA, cloud directory, and user provisioning/deprovisioning; risk-based SmartFactor Authentication uses machine learning to adjust requirements dynamically . **Best for enterprises wanting straightforward SSO with provisioning**—unlimited plan includes automated user management.

- **[Auth0](https://auth0.com/)**  
  Developer-focused identity platform for applications; **B2B plans now include free Self-Service SSO, SCIM, and one Enterprise Connection** on the Free Plan, with add-ons for Enterprise Connections, Enterprise MFA (WebAuthn, FIDO), and M2M tokens on Essentials . **Best for developers building SSO into their own products** (CIAM/B2B) rather than workforce IAM.

- **[CyberArk](https://www.cyberark.com/)**  
  Identity security platform with privileged access management and identity governance; CyberArk IGA adds Google Workspace SSO for verified secondary domain emails and TOTP MFA support for Microsoft SSO . **Best for organizations prioritizing privileged access security** alongside SSO.

- **[ForgeRock](https://www.forgerock.com/)**  
  Identity platform (now part of Ping Identity) with comprehensive IAM, access management, and identity gateway capabilities; Ping (ForgeRock) SDKs support social login with Apple, Facebook, and Google .

- **[Keycloak (Cloud)](https://www.keycloak.org/)**  
  The commercial cloud offering of Keycloak; while Keycloak itself is open-source, managed hosting removes operational burden.

## Open-Source GitHub Projects

### Full IAM Platforms (SSO + Federation)

- **[Keycloak](https://github.com/keycloak/keycloak)**  
  The **most widely adopted open-source IAM platform** (Apache-2.0) . Provides SSO, OAuth 2.0, OIDC, SAML 2.0, LDAP, Active Directory federation, identity brokering, and **SCIM 2.0 server support (since 26.8)** . Keycloak 26.8.0 includes identity provider redesign and OID4VP cross-device login improvements . **The default choice for self-hosted SSO**—mature, well-documented, and widely deployed. But it requires Java expertise and operational ownership.

- **[Authentik](https://github.com/goauthentik/authentik)**  
  Modern, security-focused **IdP and SSO platform** (open-source core with Enterprise edition) . Features: **flow-based authentication** (customizable login/authentication processes), support for **OAuth2, SAML, LDAP, and SCIM** providers, user and group management, application portal, and visual admin dashboards . **Best for teams wanting a modern UI and flexible authentication flows** with strong security defaults—Docker Compose and Kubernetes installation available .

- **[Casdoor](https://github.com/casdoor/casdoor)**  
  UI-first open-source **IAM/SSO platform** (Apache-2.0) with everything editable in the web console—organizations, applications, providers, sign-in methods, email/SMS templates, and login-page branding . Supports OAuth 2.0, OIDC, SAML, CAS, LDAP, SCIM, WebAuthn, TOTP, MFA, and RADIUS . **Policy-based authorization via Casbin** (ACL, RBAC, ABAC) rather than fixed permission schemes . Single Go binary + database; no JVM or cluster required . Docker, Helm, and configuration-as-code (JSON/YAML init data, Terraform provider) supported . **Best for teams wanting a clean UI-first IAM with flexible authorization**—inspired Burrow's design .

### Lightweight & Small-Team Options

- **[Burrow](https://github.com/ArkGravity/burrow)**  
  Lightweight, self-hosted **OIDC and SAML identity provider for small teams** (MIT, Go + React) . Ships as **one binary** with embedded UI or via Docker Compose with PostgreSQL; SQLite for dev. Features: shared SSO for web/SPA apps via OIDC Authorization Code with **PKCE S256 required by default**, SAML IdP with signed SP-initiated requests, password authentication with optional TOTP MFA (disabled by default), users/groups/custom roles/permissions with audited changes, and an application portal grouped by protocol . **Scope is deliberately limited**: no upstream identity federation, no Refresh Tokens, no cross-application logout—applications manage their own sessions . **Best for small teams wanting a simple, auditable SSO provider** without Keycloak's operational weight.

- **[VoidAuth](https://github.com/voidauth/voidauth)**  
  Open-source **SSO provider for self-hosted applications** (AGPL-3.0, v1.17.0) . Works as an **OIDC provider, ForwardAuth target, and LDAP directory server**; runs alongside Caddy, Traefik, or nginx so authentication stays on your infrastructure . Features: MFA, passkeys, passkey-only accounts, encryption at rest (Postgres/SQLite), invite or self-registration, and custom branding (logo, title, theme, email templates) . **Best for homelabs and small self-hosted deployments** wanting unified access control across apps.

### Modular / Composable Identity

- **[Ory (Kratos + Hydra)](https://github.com/ory)**  
  Open-source identity infrastructure (Apache-2.0) composed of modular services: **Ory Kratos** for identities and user management, **Ory Hydra** for certified OAuth 2.0 and OpenID Connect . **API-first and headless**—you build your own UI using the APIs (reference implementations available for React/Next.js, Node, and React Native) . **Best for teams wanting composable identity primitives** to embed in their own products rather than a turnkey IdP.

### Legacy Enterprise

- **[Apereo CAS](https://github.com/apereo/cas)**  
  Long-established **enterprise SSO and identity provider** (Apache-2.0, 11.4k stars, since 2011) . Supports SAML2, OIDC, OAuth, MFA, and a wide range of authentication backends (LDAP, RDBMS, X.509, Radius, JWT, MongoDB, Cassandra) with HA clustering via Hazelcast, JPA, Memcached, Redis, and more . **Widely used in higher education** and institutional contexts . **Best for organizations already in the Apereo ecosystem** or needing a battle-tested Java-based SSO platform—but development is concentrated in a single maintainer and growth is slow .

### Additional Strong Open-Source Options

- **WSO2 Identity Server** — Enterprise-grade open-source IAM (Apache-2.0) with SSO, OIDC, SAML, SCIM, and identity federation; manages over 1 billion identities across 1,500+ deployments . **Best for enterprises wanting a fully-featured IAM suite** with commercial support available.
- **Janssen** — Digital identity platform for centralized authentication and authorization (Linux Foundation project) . **Best for organizations wanting a scalable, standards-based identity service** with a governance foundation.
- **Authelia** — Authentication and authorization server with portal, 2FA, and SSO for self-hosted applications; lighter than Keycloak for simple reverse-proxy SSO . **Best for homelabs and small deployments** needing SSO in front of web apps.

**Frameworks for building custom systems**: For **enterprise SSO with federation and SCIM**, Keycloak is the default . For **modern UI and flexible flows**, Authentik . For **UI-first IAM with policy-based authorization**, Casdoor . For **small teams wanting minimal operational overhead**, Burrow or VoidAuth . For **composable identity primitives**, Ory Kratos + Hydra . For **AI agent identity governance**, Okta Agent SSO (commercial) or PingOne Agent IAM Core (commercial) —open-source has no equivalent yet.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- SSO and identity platforms handling authentication credentials and user data must comply with applicable security standards (SOC 2, ISO 27001) and privacy regulations; **self-hosted IdPs become critical infrastructure**—an outage or misconfiguration can lock users out of all connected applications.
- **Open-source SSO is mature and production-proven**—Keycloak, Authentik, and Casdoor provide enterprise-grade identity with SSO, federation, and SCIM . However, **commercial platforms differentiate on AI agent identity governance** (Okta Agent SSO, PingOne Agent IAM Core) and managed compliance workflows that open-source tools require assembly to match . For workforce SSO, open-source is a strong choice; for AI agent identity, commercial platforms currently lead.
- Verify license terms for commercial use; Keycloak uses Apache-2.0, Authentik is open-source with an Enterprise edition, Casdoor uses Apache-2.0, and Burrow uses MIT .

---

**Made for identity architects, IT administrators, and security engineers choosing their SSO and identity platform.**  
Let's make SSO and identity management more open, but with clear eyes about the AI agent identity governance that commercial platforms are currently pioneering.
