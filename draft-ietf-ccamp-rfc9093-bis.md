---
coding: utf-8

title: Common YANG Data Types for Layer 0 Networks

abbrev: L0 Common YANG Types
docname: draft-ietf-ccamp-rfc9093-bis-latest
obsoletes: 9093
submissiontype: IETF
workgroup: CCAMP Working Group
category: std
ipr: trust200902

stand_alone: yes
pi: [toc, sortrefs, symrefs, comments]

author:
  -
    name: Sergio Belotti
    org: Nokia
    role: editor
    email: sergio.belotti@nokia.com
  -
    name: Italo Busi
    org: Huawei
    role: editor
    email: italo.busi@huawei.com
  -
    name: Dieter Beller
    org: Nokia
    role: editor
    email: dieter.beller@nokia.com
  -
    name: Esther Le Rouzic
    ins: E. Le Rouzic
    org: Orange
    email: esther.lerouzic@orange.com
  -
    name: Aihua Guo
    org: Futurewei Technologies
    email: aihuaguo.ietf@gmail.com

contributor:
  -
    name: Haomian Zheng
    org: Huawei
    email: zhenghaomian@huawei.com
  -
    name: Daniel King
    org: University of Lancaster
    email: d.king@lancaster.ac.uk
  -
    name: Gabriele Galimberti
    org: Cisco
    email: ggalimbe@cisco.com
  -
    name: Enrico Griseri
    org: Nokia
    email: Enrico.Griseri@nokia.com
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
  -
    name: Young Lee
    org: Samsung
    email: younglee.tx@gmail.com
  -
    name: Victor Lopez
    org: Nokia
    email: victor.lopez@nokia.com

normative:
  ITU-T_G.666:
    title: >
      Characteristics of polarization mode dispersion compensators and of receivers that compensate for polarization mode dispersion"
    author:
      org: International Telecommunication Union
    date: February 2011
    seriesinfo: ITU-T Recommendation G.666
    target: https://www.itu.int/rec/T-REC-G.666
  ITU-T_G.694.1:
    title: "Spectral grids for WDM applications: DWDM frequency grid"
    author:
      org: International Telecommunication Union
    date: October 2020
    seriesinfo: ITU-T Recommendation G.694.1
    target: https://www.itu.int/rec/T-REC-G.694.1
  ITU-T_G.694.2:
    title: "Spectral grids for WDM applications: CWDM wavelength grid"
    author:
      org: International Telecommunication Union
    date: December 2003
    seriesinfo: ITU-T Recommendation G.694.2
    target: https://www.itu.int/rec/T-REC-G.694.2
  ITU-T_G.698.2:
    title: >
      Amplified multichannel dense wavelength division
      multiplexing applications with single channel optical
      interfaces
    author:
      org: International Telecommunication Union
    date: November 2018
    seriesinfo: ITU-T Recommendation G.698.2
    target: https://www.itu.int/rec/T-REC-G.698.2
  ITU-T_G.709:
    title: Interfaces for the optical transport network
    author:
      org: International Telecommunication Union
    date: June 2020
    seriesinfo: ITU-T Recommendation G.709
    target: https://www.itu.int/rec/T-REC-G.709
  ITU-T_G.709.2:
    title: OTU4 long-reach interface
    author:
      org: International Telecommunication Union
    date: September 2020
    seriesinfo: ITU-T Recommendation G.709.2, Corrigendum 1
    target: https://www.itu.int/rec/T-REC-G.709.2
  ITU-T_G.709.3:
    title: Flexible OTN B100G long-reach interfaces
    author:
      org: International Telecommunication Union
    date: November 2022
    seriesinfo: ITU-T Recommendation G.709.3, Amendment 1
    target: https://www.itu.int/rec/T-REC-G.709.3
  ITU-T_G.959.1:
    title: Optical transport network physical layer interfaces
    author:
      org: International Telecommunication Union
    date: July 2018
    seriesinfo: ITU-T Recommendation G.959.1
    target: https://www.itu.int/rec/T-REC-G.959.1
  ITU-T_G.975:
    title: Forward error correction for submarine systems
    author:
      org: International Telecommunication Union
    date: October 2000
    seriesinfo: ITU-T Recommendation G.975
    target: https://www.itu.int/rec/T-REC-G.975
  ITU-T_G.975.1:
    title: Forward error correction for high bit-rate DWDM submarine systems
    author:
      org: International Telecommunication Union
    date: July 2013
    seriesinfo: ITU-T Recommendation G.975.1, Corrigendum 2
    target: https://www.itu.int/rec/T-REC-G.975.1
  ITU-T_G.977.1:
    title: "Transverse compatible dense wavelength division multiplexing applications for repeatered optical fibre submarine cable systems"
    author:
      org: International Telecommunication Union
    date: February 2021
    seriesinfo: ITU-T Recommendation G.977.1
    target: https://www.itu.int/rec/T-REC-G.977.1
  ITU-T_G.9700:
    title: "Fast access to subscriber terminals (G.fast) - Power spectral density specification"
    author:
      org: International Telecommunication Union
    date: July 2019
    seriesinfo: ITU-T Recommendation G.9700
    target: https://www.itu.int/rec/T-REC-G.9700
  OIF_400ZR:
    title: Implementation Agreement 400ZR
    author:
      org:  Optical Internetworking Forum
    date: March 2020
    seriesinfo: OIF-400ZR-01.0 Implementation Agreement
    target: https://www.oiforum.com/wp-content/uploads/OIF-400ZR-01.0_reduced2.pdf

informative:
  ITU-T_G.Sup43:
    title: "Transport of IEEE 10GBASE-R in optical transport networks (OTN)"
    author:
      org: International Telecommunication Union
    date: December 2003
    seriesinfo: ITU-T Supplement G.Sup43
  ITU-T_G.Sup39:
    title: "Optical system design and engineering considerations"
    author:
      org: International Telecommunication Union
    date: February 2016
    seriesinfo: ITU-T Supplement G.Sup39

--- abstract

This document defines a collection of common data types, identities, and groupings
in the YANG data modeling language. 
These common types and groupings, derived from the built-in YANG data types, identities,
and groupings are intended to be imported by modules that model Layer 0
configuration and state capabilities, such as Wavelength Switched Optical Networks (WSONs) and
flexi-grid Dense Wavelength Division Multiplexing (DWDM) networks.

This document obsoletes RFC 9093 by replacing the YANG module it contained with a new revision that includes additional YANG data types, identities and groupings.

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
   Optical Networks (WSONs) {{?RFC6163}} {{ITU-T_G.694.1}} and {{ITU-T_G.694.2}}, and flexi-grid Dense
   Wavelength Division Multiplexing (DWDM) networks {{?RFC7698}}
   {{ITU-T_G.694.1}}.

   This document adds new type definitions to the YANG modules and
   obsoletes {{?RFC9093}}.  For further details, see the revision
   statements of the YANG module in {{yang-code}} or the summary in
   {{changes-bis}}.

This document obsoletes {{?RFC9093}} by replacing it in its entirety. It
provides a new revision of the YANG module contained in that RFC,
and retains the data types previously defined, but also adds new type
definitions to the YANG module.
For further details, see {{changes-bis}}.

   The YANG data model in this document conforms to the Network
   Management Datastore Architecture defined in {{!RFC8342}}.

## Terminology and Notations

   Refer to {{?RFC7446}} and {{?RFC7581}} for the key terms used in this
   document, and the terminology for describing YANG data models can be
   found in {{!RFC7950}}.

{::boilerplate bcp14}

## Prefix in Data Node Names

   In this document, names of data nodes and other data model objects
   are prefixed using the standard prefix associated with the
   corresponding YANG imported module.

| Prefix       | YANG module                      | Reference
| l0-types     | ietf-layer0-types                | RFC XXXX
{: #tab-prefixes title="Prefixes and corresponding YANG module"}

RFC Editor Note:
Please replace XXXX with the RFC number assigned to this document and remove this note.

# Layer 0 Types Module Contents

   This document defines a YANG module for common Layer 0 types, ietf-
   layer0-types.  This module is used for WSON and flexi-grid DWDM
   networks.  The "ietf-layer0-types" module contains the following YANG
   reusable YANG data types, identities and groupings:

l0-grid-type:
: A base YANG identity for the grid type as defined in {{!RFC6205}} and {{!RFC7699}}.

cwdm-ch-spc-type:
: A base YANG identity for the Coarse Wavelength Division
Multiplexing (CWDM) channel-spacing type as defined in {{!RFC6205}}.

dwdm-ch-spc-type:
: A base YANG identity for the DWDM channel-spacing type as defined
in {{!RFC6205}}.

flexi-ncfg-type:
: A base YANG identity for the DWDM flexi-grid Nominal Central Frequency Granularity (NCFG) 
  type as defined in {{!RFC7699}}.

> Note that the only value for NCFG standardized in {{ITU-T_G.694.1}} is 6.25GHz.

flexi-slot-width-granularity:
: A base YANG identity for the DWDM flexi-grid Slot Width Granularity (SWG) type, as defined in {{!RFC7699}}.
: Note that the only value for SWG standardized in {{ITU-T_G.694.1}} is 12.5GHz.

fec-type:
: A base YANG identity from which specific FEC (Forward Error Correction) type identities are derived.

line-coding:
: A base YANG identity from which specific identities defining the bit rate/line coding of optical tributary signals are derived.

wavelength-assignment:
: A base YANG identity from which for Wavelength selection method, as defined in {{!RFC7689}}.

otu-type:
: This specifies the type of OTU, including the types specified in {{ITU-T_G.709}}.
: Since {{ITU-T_G.Sup43}} does not guarantee interoperability in the data plane, the type of OTUk defined in {{ITU-T_G.Sup43}} can be defined in vendor-specific YANG modules using the otu-type identity, defined in this document, as the base.

operational-mode:
: A YANG data type used to identify an organization (e.g., vendor) specific mode for transceiver capability description, as defined in Section 2.5.2 of {{!I-D.ietf-ccamp-optical-impairment-topology-yang}}

wson-label-start-end:
: The WSON label range was defined in {{!RFC6205}}, and the generic
topology model defines the label-start/label-end in {{!RFC8795}}.
This grouping shows the WSON-specific label-start and label-end
information. See {{label-range}} for more details. 

wson-label-hop:
: The WSON label range was defined in {{!RFC6205}}, and the generic
topology model defines the label-hop in {{!RFC8795}}.  This grouping
shows the WSON-specific label-hop information. See {{label-range}} for more details.

l0-label-range-info:
: A YANG grouping that defines the Layer 0 label range information
applicable for WSON as defined in {{!RFC6205}}. The label range info is defined per priority {{!RFC4203}}.
: This grouping is used in the flexi-grid DWDM by adding more flexi-grid-specific
parameters. See {{label-range}} for more details.

wson-label-step:
: A YANG grouping that defines label steps for WSON as defined in
{{!I-D.ietf-teas-rfc8776-update}}. See {{label-range}} for more details.

flexi-grid-label-start-end:
: The flexi-grid label range was defined in {{!RFC7699}}, and the
generic topology model defines the label-start/label-end in
{{!RFC8795}}.
: This grouping shows the flexi-grid-specific label-
start and label-end information which is used to describe the range of available nominal central frequencies. See {{label-range}} for more details.
: As described in section 3.1 of {{!RFC8363}}, the range of available nominal central frequencies are advertised for m=1, which means that for an available central frequency n, the frequency slot from central frequency n-1 to central frequency n+1 is available.

flexi-grid-label-hop:
: The flexi-grid label range was defined in {{!RFC8363}}, and the
generic topology model defines the label-hop in {{!RFC8795}}.
: This grouping shows the WSON-specific label-hop information. See {{label-range}} for more details.

flexi-grid-label-range-info:
: A YANG grouping that defines flexi-grid label range information as
defined in {{!RFC8363}}. See {{label-range}} for more details. See {{label-range}} for more details.

flexi-grid-label-step:
: A YANG grouping that defines flexi-grid label steps as defined in
{{!I-D.ietf-teas-rfc8776-update}}. See {{label-range}} for more details.

wdm-label-start-end:
: A YANG grouping that combines the definition of label-start/label-end information
that was defined separately in wson-label-start-end and flexi-grid-label-start-end,
to support optical network scenarios that contain both fixed- and flexi-grid
links. See {{label-range}} for more details.

wdm-label-hop:
: A YANG grouping that combines the definition of label hop information
that was defined separately in wson-label-hop and flexi-grid-label-hop,
to support optical network scenarios that contain both fixed- and flexi-grid
links. See {{label-range}} for more details.

wdm-label-range-info:
: A YANG grouping that combines the definition of label range information
that was defined separately in wson-label-range-info and flexi-grid-label-range-info,
to support optical network scenarios that contain both fixed- and flexi-grid
links. See {{label-range}} for more details.

wdm-label-step:
: A YANG grouping that combines the definition of label step information
defined separately in wson-label-step and flexi-grid-label-step,
to support optical network scenarios that contain both fixed- and flexi-grid
links. See {{label-range}} for more details.

transceiver-capabilities:
: A YANG grouping to define the transceiver capabilities (also called
"modes") needed to determine optical signal compatibility.

standard-mode:
: A YANG grouping for the standard modes defined in {{ITU-T_G.698.2}}.

organizational-mode:
: A YANG grouping to define transponder operational mode supported by
organizations or vendors, as defined in {{!I-D.ietf-ccamp-optical-impairment-topology-yang}}.

explicit-mode:
: A YANG grouping to define the list of attributes related to optical
impairments limits in case of transceiver explicit mode, as defined in {{!I-D.ietf-ccamp-optical-impairment-topology-yang}}.
: Note that the the actual portion of the spectrum occupied by an OTSi is not explicitly reported within the explicit-mode parameters because it can be calculated using the available-baud-rate, the roll-off and the min-carrier-spacing attributes.

transmitter-tuning-range:
: A YANG grouping that defines the transmitter tuning range, which
includes the minimum and maximum tuning frequency, as well as the
frequency tuning steps.

common-organizational-explicit-mode:
: A YANG grouping to define the common capabilities attributes limit
range in case of operational mode and explicit mode.

modulation:
: A base YANG identity to define the different modulation types, as defined in {{ITU-T_G.Sup39}}

snr:
: A YANG data type used to represent an (Optical) Signal to Noise Ratio measured over 0.1 nm resolution bandwidth, as defined in {{ITU-T_G.977.1}}

psd:
: A YANG data type used to represent a Power Spectral Density (PSD), as defined in {{ITU-T_G.9700}}

penalty-value:
: A YANG grouping to define the penalty value for multiple penalty types, such as Chromatic Dispersion (CD), Polarization Mode Dispersion (PMD), as defined in {{ITU-T_G.666}} or Polarization Dependent Loss(PDL)

## WDM Label and Label Range {#label-range}

As described in {{!RFC6205}} and {{!RFC7699}}, the WDM label represents the frequency slot assigned to a WDM Label Switched Path (LSP) on a given WDM Link, which models an Optical Multiplex Section (OMS) Media Channel Group (MCG) as described in {{?I-D.ietf-ccamp-optical-impairment-topology-yang}}.

The same WDM label shall be assigned to the same WDM LSP on all the WDM Links on a regen-free LSP path or path segment.

A frequency slot is defined in {{ITU-T_G.694.1}} as a contiguous frequency range characterized by its nominal central frequency and slot width. The frequency range allocated to a frequency slot is unavailable to other frequency slots.

The definition of the frequency slot depends on the WDM grid type:

- In case of CWDM fixed-grid, defined in {{ITU-T_G.694.2}}, the frequency slot is defined by a fixed CWDM channel spacing (cwdm-ch-spc-type) and by the nominal central wavelength which is computed as described in {{?RFC6205}}. The formula in {{?RFC6205}} is copied here for reader convenience:

~~~~
      lambda = 1471 nm + n * channel spacing (measured in nm)
~~~~

> where 'n' is defined in {{?RFC6205}} as integer (positive, negative, or 0)

- In case of DWDM fixed-grid, defined in {{ITU-T_G.694.1}}, the frequency slot is defined by a fixed DWDM channel spacing (dwdm-ch-spc-type) and by the nominal central frequency, which is computed as described in {{?RFC6205}}. The formula in {{?RFC6205}} is copied here for reader convenience:

~~~~
      f = 193100.000 GHz + n * channel spacing (measured in GHz)
~~~~

> where 'n' is defined in {{?RFC6205}} as integer (positive, negative, or 0)

- In case of DWDM flexible-grid, defined in {{ITU-T_G.694.1}}, the frequency slot is defined by the slot width and by the nominal central frequency, which are computed, based on the slot width granularity (SWG, fixed at 12.5GHz in {{ITU-T_G.694.1}}), and of the nominal central frequency granularity (NCFG, fixed at 6.25GHz in {{ITU-T_G.694.1}}) respectively, as described in {{?RFC7698}} and {{?RFC7699}}. The formulas in {{?RFC7699}} can be generalized as follows:

~~~~
      SW = m * SWG (measured in GHz)
      f = 193100.000 GHz + N * NCFG (measured in GHz)
~~~~

> where 'n' is defined in {{?RFC7699}} as integer (positive, negative, or 0) and 'm' is defined in {{?RFC7698}} as an integer greater than or equal to 1.

The definition of the channel spacing, NCFG and SWG in the YANG model have been generalized to support modelling of vendor-specific values (e.g., finer vendor-specific granularity for NCFG and SWG).

The WDM Label Range represents the frequency slots that are available for WDM LSPs to be set up over a given WDM Link.

The WDM Label Range is defined by augmenting the label-restriction list, defined in {{!I-D.ietf-teas-rfc8776-update}}, with WDM technology-specific attributes, using the l0-label-range-info grouping (for WSON only models) or the flexi-grid-label-range-info grouping (for DWDM flexible-grid only models) or the wdm-label-range-info grouping (for models that supports both WSON and DWDM flexible-grid).

Each entry in the label-restriction list represents either the range of the available central wavelength values (in case of CWDM fixed-grid) or the range of the available nominal central frequencies values (in case of DWDM fixed or flexible grids): the grid-type attribute defines the type of grid for each entry of the list.

In case of DWDM flexible grid, each entry in the label-restriction
list represents also the range of the supported slot width values
based on the following attributes, defined based on concepts used in {{?RFC7699}}:

* slot-width-granularity, which represents the minimum space between slot widths;

* min-slot-width-factor: a multiplier of the slot width granularity, indicating the minimum slot width supported by each entry in the label-restriction list;

* max-slot-width-factor: a multiplier of the slot width granularity, indicating the maximum slot width supported by each entry in the label-restriction list.

Each entry of the label-restriction list, as defined in {{!I-D.ietf-teas-rfc8776-update}}, defines a label-start, a label-end, a label-step and a range-bitmap.

The label-start and label-end definitions, when used for representing WDM labe range, are augmented with WDM technology-specific attributes, using the wson-label-start-end grouping (for WSON only models) or the flexi-grid-label-start-end grouping (for DWDM flexible-grid only models) or the wdm-label-start-end grouping (for models that supports both WSON and DWDM flexible-grid).

The label-step definition, when used for representing WDM labe range, are augmented with WDM technology-specific attributes, using the wson-label-step grouping (for WSON only models) or the flexi-grid-label-step grouping (for DWDM flexible-grid only models) or the wdm-label-step grouping (for models that supports both WSON and DWDM flexible-grid). The label-step definition for WDM depends on the WDM grid type:

* For CWDM and DWDM fixed grids, it describes the channel spacing, as defined in {{?RFC6205}};

* For DWDM flexible grids, it describes the nominal central frequency granularity (e.g., 6,25 GHz) as well as the multiplier for the supported values of n, as defined in {{?RFC7699}}.
{: #yang-tree}

# YANG Tree for Layer 0 Types Groupings

~~~~ ascii-art
{::include ./ietf-layer0-types.folded.tree}
~~~~
{: #fig-yang-tree}

{: #yang-code}

# YANG Module for Layer 0 Types

This YANG module references {{!RFC6205}}, {{!RFC7689}}, {{!RFC7699}}, {{!RFC7698}}, {{!RFC8363}}, {{!RFC8363}}, {{!RFC9093}}, {{ITU-T_G.666}}, {{ITU-T_G.694.1}}, {{ITU-T_G.694.2}}, {{ITU-T_G.698.2}}, {{ITU-T_G.709}}, {{ITU-T_G.709.2}}, {{ITU-T_G.709.3}}, {{ITU-T_G.959.1}} {{ITU-T_G.975}}, {{ITU-T_G.975.1}}, {{ITU-T_G.977.1}}, {{ITU-T_G.9700}} and {{OIF_400ZR}}.

~~~~ yang
{::include ./ietf-layer0-types.yang}
~~~~
{: #fig-yang-code title="Layer 0 Types YANG module"
sourcecode-markers="true" sourcecode-name="ietf-layer0-types@2024-03-04.yang"}

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

For the following URI in the "IETF XML Registry" {{?RFC3688}}, IANA has updated the reference field to refer to this document:

~~~~
   URI:  urn:ietf:params:xml:ns:yang:ietf-layer0-types
   Registrant Contact:  The IESG
   XML:  N/A; the requested URI is an XML namespace.
~~~~

This document also adds an updated YANG module to the "YANG Module
Names" registry {{!RFC7950}}:

~~~~
   Name:  ietf-layer0-types
   Namespace:  urn:ietf:params:xml:ns:yang:ietf-layer0-types
   Prefix:  l0-types
   Reference:  RFC XXXX
~~~~

RFC Editor Note: Please replace XXXX with the RFC number assigned to this document.

--- back

{: #changes-bis}

# Changes from RFC 9093

This version adds new data types, identities, and groupings to the YANG modules.

The following new YANG data types have been added to the 'ietf-layer0-types' module:

- Standard-mode
- Organization-identifier
- Operational-mode
- frequency-thz
- frequency-ghz
- snr
- snr-or-null
- fiber-type
- decimal-2
- decimal-2-or-null
- power-gain
- power-gain-or-null
- power-loss
- power-loss-or-null
- power-ratio
- power-ratio-or-null
- power-dbm
- power-dbm-or-null
- decimal-5
- decimal-5-or-null
- psd
- psd-or-null

The following new YANG identities have been added to the 'ietf-layer0-types' module:

- identity cwdm-ch-spc-type
- identity flexi-ncfg-type
- identity flexi-ncfg-6p25gh
- identity modulation
- identity DPSK 
- identity QPSK
- identity DP-QPSK
- identity QAM8
- identity DP-QAM8
- identity QAM16
- identity DP-QAM16
- identity QAM32 
- identity DP-QAM32 
- identity QAM64
- identity DP-QAM64
- identity fec-type
- identity g-fec
- identity super-fec
- identity no-fec 
- identity sc-fec 
- identity o-fec 
- identity c-fec 
- identity line-coding 
- identity line-coding-NRZ-2p5G 
- identity line-coding-NRZ-OTU1 
- identity line-coding-NRZ-10G 
- identity line-coding-NRZ-OTU2 
- identity line-coding-OTL4.4-SC 
- identity line-coding-FOIC1.4-SC 
- identity wavelength-assignment 
- identity first-fit-wavelength-assignment
- identity random-wavelength-assignment 
- identity least-loaded-wavelength-assignment 
- identity lower-first-wavelength-assignment 
- identity upper-first-wavelength-assignment 
- identity otu-type 
- identity OTU1 
- identity OTU2 
- identity OTU3 
- identity OTU4 
- identity OTUCn 
- identity type-power-mode 
- identity power-spectral-density 
- identity carrier-power 

The following new YANG groupings have been added to the 'ietf-layer0-types' module:

- wdm-label-start-end
- wdm-label-step
- wdm-label-hop
- wdm-label-range-info
- transceiver-mode
- transceiver-capabilities
- standard-mode
- organizational-mode
- penalty-value
- explicit-mode
- common-standard-organizational-mode
- transmitter-tuning-range
- common-all-mode
- common-transceiver-param
- common-transceiver-configured-param
- common-transceiver-readonly-param
- l0-tunnel-attributes
- frequency-range
- l0-path-constraints
- l0-path-properties

{: numbered="false"}

# Acknowledgments

The authors and the working group give their sincere thanks to Robert
Wilton for the YANG doctor review and to Adrian Farrel and Tom Petch for their comments
during the model and document development.

This document was prepared using kramdown.
