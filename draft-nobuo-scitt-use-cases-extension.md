---
################################
# header
################################
v: 3

title: A YANG Data Model for Multi-Statements of SCITT
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

This document defines components, as represented by Software Bills of Materials (SBOMs); statements protecting the transparent lifecycle of those components; and alternative means for acquiring integrated Supply Chain information, including provenance and configuration details.

--- middle

# Introduction

A Software Bill of Materials (SBOM) describes the software contained within a device (including version management and dependencies), while a Hardware Bill of Materials (HBOM) describes the hardware contained within a device. Additionally, an XBOM exists.
Various formats exist for SBOMs, including Software Package Data Exchange [SPDX], Software Identity Tags [SWID], and CycloneDX [CycloneDX12].

SCITT ARCH provides supply chain information by issuing receipts for each stage of the software lifecycle.

A computer is an aggregate of hardware, software, and configuration. 
Providing supply chain information using the above method results in multiple statements.
This draft specifies the means by which integrated multi-statements can be advertised and retrieved.

The mechanisms specified in this document are meant to satisfy several use cases:

 - The hardware management system acquires integrated multi-statements from data center infrastructure devices and IoT devices as part of a continuous lifecycle.
 It evaluates whether the acquired integrated multi-statements can be used to correctly establish the Root of Trust.

 - The software layer management system acquires integrated multi-statements from the virtualization infrastructure as part of its continuous lifecycle. This multi-layer software is evaluated to determine whether it can be consistently delivered to consumers as a transparent, integrated product.

To fulfill these key use cases, integrated statements may be verified using one of the following methods. 


## Terminology {#terms}

{::boilerplate bcp14-tagged}

## Statement formats

As abstracted in SCITT Architecture　{{-SCITT-ARCH}}, this draft also does not refer to the internal format of XBOM or Provence, treating them entirely as statements.

## Discussion points
The following is discussion to be removed at time of RFC publication.

 - Is the model structure suitable for partially or comprehensively representing tree structures like computer systems?
 - Are there field names adopted in widely accepted models?


## The multi-statements schemer model extension

The following is discussion to be removed at time of after the SCITT WG adopted.

This draft does not affect the RFCization process of the SCITT Architecture and SCRAPI. While awaiting the two starter specifications' RFCization, we will progressively mature this draft. During this period, we will focus on use cases that can foster broad consensus and on the data model's scope.

TODO. 

# Privacy Considerations

The privacy considerations of the SCITT Architecture {{-SCITT-ARCH}} apply.

# Security Considerations

The privacy considerations of the SCITT Architecture {{-SCITT-ARCH}} apply.

--- back
