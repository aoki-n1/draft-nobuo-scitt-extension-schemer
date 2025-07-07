---
################################
# header
################################
v: 3

title: Supply Chain Use Cases to Design Secure Computing Systems for SCITT Extention
abbrev: SCITT Extension Supply Chain
docname: draft-nobuo-scitt-use-cases-extension-latest
#docname: draft-ietf-scitt-scrapi-latest
#nobuo-scitt-extension-use-cases-latest

stand_alone: true
area: Security
wg: SCITT
kw: Internet-Draft
cat: info
#consensus: no
#submissiontype: IETF
#ipr: trust200902
#pi:
#  toc: yes
#  sortrefs: yes
#  symrefs: yes

kramdown_options:
  auto_id_prefix: sec-

venue:
  group: SCITT
  mail: scitt@ietf.org
  github: aoki-n1/draft-nobuo-scitt-use-cases-extension ## check

################################
# author
################################
author:
- ins: N. Aoki
  name: Nobuo Aoki
  org: The Graduate University for Advanced　Studies (SOKENDAI)
  abbrev: SOKENDAI
  email: n_aoki@ieee.org
  #street: c/o, The Graduate School Office, National Institute of Informatics 2-1-2, Hitotsubashi
  #code: '1010003'
  #city: Tokyo
  country: Japan

################################
# reference
################################
normative:
  I-D.draft-ietf-scitt-architecture: SCITT-ARCH


informative:
  SoK-SW-SCS: DOI.10.1145/3560835.3564556
  RFC9472:

################################
# header
################################

--- abstract

This document includes a collection of representative Computational Supply Chain Use Cases.
These use cases aim to identify computational supply chain problems that the industry faces today and act as a guideline for developing a comprehensive security architecture  and solutions for these scenarios.

--- middle

# Introduction

Supply chain for components that make up a computer system consists of the entire lifecycle, including hardware selection, system design, development, build, integration, deployment, and maintenance.
In the software supply chain, SBOM and SCITT architecture are exemplary initiatives that enhance software transparency.
Discussions focusing on hardware and its interfaces are also beginning.
These supply chain security measures are expected to reduce the complexity of software and provide visibility into its lifecycle, thereby reducing the number of cyber threats that can cause harmful effects such as risks related to the system's attack surface, data leaks, business disruptions, damage to reputation, intellectual property, and financial assets.
On the other hand, thorough supply chain security for computer systems can only be achieved by integrating support from hardware to the software stack, enabling effective risk assessment and mitigation.
Modern computer systems are influenced by evolving computer architectures and increasingly complex software stacks, making the integrated management of components not always straightforward.
End users, such as consumers, need to be able to evaluate whether suppliers maintain appropriate security practices without requiring access to proprietary intellectual property, necessitating an evolutionary extension of the SCITT specification.
Post-SCITT compliant products support compliance management with legal, regulatory, and technical requirements (often differing but overlapping and interrelated), risk assessment, and detection of supply chain attacks throughout the entire lifecycle, prioritizing data privacy.

## Terminology {#terms}

{::boilerplate bcp14-tagged}

# Generic Proglem Statement

Supply chain security is a crucial requirement for ensuring the stable supply of materials that directly impact consumer survival and those widely used by the majority of consumers, while minimizing threats related to the economy, public health, and safety.
As an extension of discussions in the physical domain, the definition of software supply chain security in the cyber domain, {{SoK-SW-SCS}}, has been established.
This is due to the numerous supply chain attacks targeting vulnerabilities in the software supply chain that have been experienced globally, as well as the academic progress in analyzing these attack vectors.
This analysis can also be applied to the supply chains of computer systems, which include both hardware and software.
Supply chain attacks on computer systems typically involve attackers gaining initial access, making malicious changes upstream in the supply chain, and exploiting vulnerabilities in downstream systems that are already in operation.


The SCITT Architecture {{-SCITT-ARCH}} defines the core objects, identifiers and workflows necessary to interact with a SCITT Transparency Service:

- Signed Statements
- Receipts
- Transparent Statements
- Registration Policies


The extended YANG data model with transparency schemers {{RFC9472}} defines schemers for mapping SBOMs and vulnerability information.

- Access Control Lists
- SBOM Information
- Vulnerability Information

As described above, specifications for software supply chain security are maturing; however, it remains unclear whether exisiting standard specifications can be followed while also encompassing a scope that extends beyond software.

## Computational Supply Chain Use Cases

### Multi Software Stack and Computer Architecture

Software integration is an essential task in building computer systems.
The ecosystemization of software development is advancing, a process that involves procuring various software components from multiple suppliers at different layers and creating packages of varying sizes.
These include a considerable number of third-party components.
Furthermore, depending on the design, there may be cases where components are not strictly separated from one another.
Additionally, modern computer systems adopt a variety of architectures and infrastructures.
Similar to the increasing complexity of software stacks, computer architectures continue to evolve to keep pace with advancements in applications and hardware.

End-consummers want:

- all hardware and software components required to build a computer system are displayed
- the ability to identify and retrieve all components from a secure and tamper-proof location  - to receive an alert when a vulnerability scan detects a known security issue on a running component
- verifiable proofs on build process and build environment with all supplier tiers to ensure end to end build quality and security

SCITT provides a standardized way to:

- provide a tiered and transparent framework that allows for verification of integrity and authenticity of the integrated hardware and software at both component and product level before using
- notify hardware and software integrators of vulnerabilities identified during security scans of running components
- provide valid annotstions on build integrity to ensure conformance
- provide an interface that reconciles the division of responsibilities between the software and hardware sides


# Privacy Considerations

The privacy considerations of the SCITT Architecture {{-SCITT-ARCH}} apply.

# Security Considerations

The privacy considerations of the SCITT Architecture {{-SCITT-ARCH}} apply.

--- back
