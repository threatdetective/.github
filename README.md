# Threat Detective

**Cybersecurity and SBOM management, purpose-built for medical device manufacturers.**

Threat Detective helps medical device teams manage software supply chain risk and produce the cybersecurity evidence needed for FDA and EU regulatory submissions.

We bring SBOM management, vulnerability analysis and ongoing surveillance into a workflow designed around medical devices — rather than forcing regulatory teams to adapt generic application security tools.

## What Threat Detective does

- **SBOM management** — import and manage CycloneDX and SPDX software bills of materials across device and software versions.
- **Vulnerability analysis** — identify vulnerabilities using sources including NVD, GitHub Security Advisories and CISA's Known Exploited Vulnerabilities catalogue.
- **Risk prioritisation** — use CVSS, EPSS, KEV status and medical-device context to focus investigation where it matters.
- **Vulnerability management** — investigate findings, document decisions, mitigations and justifications, and maintain an auditable record.
- **Post-market surveillance** — continuously monitor supported device versions for newly disclosed vulnerabilities and changes in exploitation status.
- **Regulatory evidence** — produce cybersecurity documentation and evidence for FDA premarket submissions and EU MDR technical documentation.

## Developer tools

### Upload SBOM to Threat Detective

Our GitHub Action lets you send a CycloneDX SBOM directly from your CI/CD pipeline to Threat Detective using GitHub OIDC authentication — without storing long-lived API credentials.

```yaml
permissions:
  id-token: write
  contents: read

steps:
  - uses: actions/checkout@v4

  - name: Upload SBOM
    uses: threatdetective/upload-sbom-action@v1
    with:
      project-id: ${{ vars.TD_PROJECT_ID }}
      sbom-file: sbom.json
```

→ [View the GitHub Action](https://github.com/threatdetective/upload-sbom-action)

## Built for medical devices

Threat Detective is designed for teams developing **Software as a Medical Device (SaMD)**, software-controlled medical devices and connected medical devices.

Our workflows are informed by medical-device cybersecurity expectations including:

- FDA premarket cybersecurity requirements
- EU MDR
- IEC 81001-5-1
- IEC 62304
- CycloneDX and SPDX
- CISA Known Exploited Vulnerabilities
- CVSS and EPSS

## Learn more

🌐 **Website:** [threatdetectivehq.com](https://threatdetectivehq.com)  
📚 **Guides & resources:** [threatdetectivehq.com](https://threatdetectivehq.com/guides/medical-device-sbom)
🚀 **Try Threat Detective:** [threatdetectivehq.com](https://threatdetectivehq.com/trial?utm_source=github)

---

**Threat Detective — turn software supply chain data into medical-device cybersecurity evidence.**
