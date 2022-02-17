---
coding: utf-8

title: A YANG Data Model for Layer 0 Types

abbrev: Yang for Layer 0 Types
docname: draft-ietf-ccamp-rfc9093-bis-00
obsoletes: RFC9093
workgroup: CCAMP Working Group
category: std
ipr: trust200902

stand_alone: yes
pi: [toc, sortrefs, symrefs, comments]

author:
  -
    name: Haomian Zheng
    org: Huawei
    email: zhenghaomian@huawei.com
  -
    name: Young Lee
    org: Samsung
    email: younglee.tx@gmail.com
  -
    name: Aihua Guo
    org: Futurewei Technologies
    email: aihuaguo.ietf@gmail.com
  -
    name: Victor Lopez
    org: Nokia
    email: victor.lopez@nokia.com
  -
    name: Daniel King
    org: University of Lancaster
    email: d.king@lancaster.ac.uk
  -
    name: Dieter Beller
    org: Nokia
    email: dieter.beller@nokia.com
  -
    name: Sergio Belotti
    org: Nokia
    email: sergio.belotti@nokia.com
  -
    name: Italo Busi
    org: Huawei
    email: italo.busi@huawei.com
  -
    name: Esther Le Rouzic
    ins: E. Le Rouzic
    org: Orange
    email: esther.lerouzic@orange.com

contributor:
  -
    name: Dhruv Dhody
    org: Huawei
    email: dhruv.ietf@gmail.com
  -
    name: Bin Yeong Yoon
    org: ETRI
    email: byyun@etri.re.kr
  -
    name: Ricard Vilalta
    org: CTTC
    email: ricard.vilalta@cttc.es

normative:
  ITU-T_G.698.2:
    title: >
      Amplified multichannel dense wavelength division
      multiplexing applications with single channel optical
      interfaces
    author:
      org: ITU-T Recommendation G.698.2
    date: November 2018
    seriesinfo: ITU-T G.698.2

informative:
  ITU-T_G.694.1:
    title: "Spectral grids for WDM applications: DWDM frequency grid"
    author:
      org: ITU-T Recommendation G.694.1
    date: October 2020
    seriesinfo: ITU-T G.694.1
  ITU-T_G.694.2:
    title: "Spectral grids for WDM applications: CWDM wavelength grid"
    author:
      org: ITU-T Recommendation G.694.2
    date: December 2003
    seriesinfo: ITU-T G.694.2

--- abstract

   This document defines a collection of common data types and groupings
   in the YANG data modeling language.  These derived common types and
   groupings are intended to be imported by modules that model Layer 0
   optical Traffic Engineering (TE) configuration and state capabilities
   such as Wavelength Switched Optical Networks (WSONs) and flexi-grid
   Dense Wavelength Division Multiplexing (DWDM) networks.

   This document obsoletes RFC 9093.

--- middle

# Introduction

   YANG {{!RFC7950}} is a data modeling language used to model
   configuration data, state data, Remote Procedure Calls, and
   notifications for network management protocols such as the Network
   Configuration Protocol (NETCONF) {{!RFC6241}}.  The YANG language
   supports a small set of built-in data types and provides mechanisms
   to derive other types from the built-in types.

   This document introduces a collection of common data types derived
   from the built-in YANG data types.  The derived types and groupings
   are designed to be the common types applicable for modeling Traffic
   Engineering (TE) features as well as non-TE features (e.g., physical
   network configuration aspects) for Layer 0 optical networks in
   model(s) defined outside of this document.  The applicability of
   Layer 0 types specified in this document includes Wavelength Switched
   Optical Networks (WSONs) {{!RFC6163}} {{ITU-T_G.698.2}} and flexi-grid Dense
   Wavelength Division Multiplexing (DWDM) networks {{!RFC7698}}
   {{ITU-T_G.694.1}}.

\[Editors' Note]: This is the introduction from draft-ietf-ccamp-layer0-types-ext-01, to be reconciled with the introduction from RFC9093 above

   YANG {{!RFC7950}} is a data modeling language used to model
   configuration data, state data, Remote Procedure Calls, and
   notifications for network management protocols such as NETCONF
   {{!RFC6241}}.  The YANG language supports a small set of built-in data
   types and provides mechanisms to derive other types from the built-in
   types.

   This document introduces a collection of common data types derived
   from the built-in YANG data types.  The derived types and groupings
   are designed to be the common types applicable for modeling Traffic
   Engineering (TE) features as well as non-TE features (e.g., physical
   network configuration aspect) for Layer 0 optical networks in
   model(s) defined outside of this document.

## Requirements Language

   The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",
   "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this
   document are to be interpreted as described in RFC 2119 {{!RFC2119}}.

## Terminology and Notations

   Refer to {{?RFC7446}} and {{?RFC7581}} for the key terms used in this
   document, and the terminology for describing YANG data models can be
   found in {{!RFC7950}}.

   The YANG data model in this document conforms to the Network
   Management Datastore Architecture defined in {{!RFC8342}}.

## Prefix in Data Node Names

   In this document, names of data nodes and other data model objects
   are prefixed using the standard prefix associated with the
   corresponding YANG imported modules.

| Prefix       | YANG module                      | Reference
| l0-types     | ietf-layer0-types                | RFCXXXX
{: #tab-prefixes title="Prefixes and corresponding YANG modules"}

RFC Editor Note:
Please replace XXXX with the RFC number assigned to this document.

   The YANG module "ietf-layer0-types" (defined in {{yang-code}}) references
   {{!RFC4203}}, {{!RFC6163}}, {{!RFC6205}}, {{!RFC7698}}, {{!RFC7699}}, {{!RFC8363}},
   {{ITU-T_G.694.1}}, and {{ITU-T_G.694.2}}.

# Layer 0 Types Module Contents

   This document defines a YANG module for common Layer 0 types, ietf-
   layer0-types.  This module is used for WSON and flexi-grid DWDM
   networks.  The "ietf-layer0-types" module contains the following YANG
   reusable types and groupings:

   l0-grid-type
   : A base YANG identity for the grid type as defined in {{!RFC6163}} and
      {{!RFC7698}}.

   dwdm-ch-spc-type
   : A base YANG identity for the DWDM channel-spacing type as defined
      in {{!RFC6205}}.

   cwdm-ch-spc-type
   : A base YANG identity for the Coarse Wavelength Division
      Multiplexing (CWDM) channel-spacing type as defined in {{!RFC6205}}.

   wson-label-start-end
   : The WSON label range was defined in {{!RFC6205}}, and the generic
      topology model defines the label-start/label-end in {{!RFC8795}}.
      This grouping shows the WSON-specific label-start and label-end
      information.

   wson-label-hop
   : The WSON label range was defined in {{!RFC6205}}, and the generic
      topology model defines the label-hop in {{!RFC8795}}.  This grouping
      shows the WSON-specific label-hop information.

   l0-label-range-info
   : A YANG grouping that defines the Layer 0 label range information
      applicable for WSON as defined in {{!RFC6205}}.  This grouping is
      used in the flexi-grid DWDM by adding more flexi-grid-specific
      parameters.

   wson-label-step
   : A YANG grouping that defines label steps for WSON as defined in
      {{!RFC8776}}.

   flexi-grid-label-start-end
   : The flexi-grid label range was defined in {{!RFC7698}}, and the
      generic topology model defines the label-start/label-end in
      {{!RFC8795}}.  This grouping shows the flexi-grid-specific label-
      start and label-end information.

   flexi-grid-label-hop
   : The flexi-grid label range was defined in {{!RFC7698}}, and the
      generic topology model defines the label-hop in {{!RFC8795}}.  This
      grouping shows the WSON-specific label-hop information.

   flexi-grid-label-range-info
   : A YANG grouping that defines flexi-grid label range information as
      defined in {{!RFC7698}} and {{!RFC8363}}.

   flexi-grid-label-step
   : A YANG grouping that defines flexi-grid label steps as defined in
      {{!RFC8776}}.

   transceiver-capabilities
   : a YANG grouping to define the transceiver capabilities (also called
   "modes") needed to determine optical signal compatibility.

   standard-mode
   : a YANG grouping for ITU-T G.698.2 standard mode that guarantees
   interoperability.

   organizational-mode
   :a YANG grouping to define transponder operational mode supported by
   organizations or vendors.

   common-explicit-mode
   : a YANG grouping to define the list of attributes related to optical
   impairments limits in case of transceiver explicit mode.  This
   grouping should be the same used in
   {{?I-D.ietf-ccamp-dwdm-if-param-yang}}.

   common-organizational-explicit-mode
   : a YANG grouping to define the common capabilities attributes limit
   range in case of operational mode and explicit mode.  Also this
   grouping should be used in {{?I-D.ietf-ccamp-dwdm-if-param-yang}}.

   cd-pmd-penalty
   : a YANG grouping to define the triplet used as entries in the list
   optional penalty associated with a given accumulated CD and PMD.
   This list of triplet cd, pmd, penalty can be used to sample the
   function penalty = f(CD, PMD).

{: #yang-code}

# YANG Module for Layer 0 Types

~~~~
<CODE BEGINS> file "ietf-layer0-types-ext@2022-01-21.yang"
{::include ./ietf-layer0-types-ext.yang}
<CODE ENDS>
~~~~

# Security Considerations

   The YANG module specified in this document defines a schema for data
   that is designed to be accessed via network management protocols such
   as NETCONF {{!RFC6241}} or RESTCONF {{!RFC8040}}.  The lowest NETCONF layer
   is the secure transport layer, and the mandatory-to-implement secure
   transport is Secure Shell (SSH) {{!RFC6242}}.  The lowest RESTCONF layer
   is HTTPS, and the mandatory-to-implement secure transport is TLS
   {{!RFC8446}}.

   The Network Configuration Access Control Model (NACM) {{!RFC8341}}
   provides the means to restrict access for particular NETCONF or
   RESTCONF users to a preconfigured subset of all available NETCONF or
   RESTCONF protocol operations and content.  The NETCONF protocol over
   Secure Shell (SSH) specification {{!RFC6242}} describes a method for
   invoking and running NETCONF within a Secure Shell (SSH) session as
   an SSH subsystem.

   The objects in this YANG module are common data types and groupings.
   No object in this module can be read or written to.  These
   definitions can be imported and used by other Layer 0 specific
   modules.  It is critical to consider how imported definitions will be
   utilized and accessible via RPC operations, as the resultant schema
   will have data nodes that can be writable, or readable, and will have
   a significant effect on the network operations if used incorrectly or
   maliciously.  All of these considerations belong in the document that
   defines the modules that import from this YANG module.  Therefore, it
   is important to manage access to resultant data nodes that are
   considered sensitive or vulnerable in some network environments.

   The security considerations spelled out in the YANG 1.1 specification
   {{!RFC7950}} apply for this document as well.

# IANA Considerations

   IANA has assigned new URIs from the "IETF XML Registry" {{?RFC3688}} as
   follows:

~~~~
   URI:  urn:ietf:params:xml:ns:yang:ietf-layer0-types
   Registrant Contact:  The IESG
   XML:  N/A; the requested URI is an XML namespace.
~~~~

   This document registers the following YANG module in the "YANG Module
   Names" registry {{!RFC7950}}.

~~~~
   Name:  ietf-layer0-types
   Namespace:  urn:ietf:params:xml:ns:yang:ietf-layer0-types
   Prefix:  l0-types
   Reference:  RFC 9093
~~~~

\[Editors' Note] Check the IANA considerations in other bis documents

--- back

{: numbered="false"}

# Acknowledgements

   The authors and the working group give their sincere thanks to Robert
   Wilton for the YANG doctor review and Tom Petch for his comments
   during the model and document development.
