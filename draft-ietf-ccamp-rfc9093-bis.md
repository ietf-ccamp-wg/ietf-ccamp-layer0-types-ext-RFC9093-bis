---
coding: utf-8

title: Common YANG Data Types for Layer 0 Optical Networks

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
    org: Nokia
    email: gabriele.galimberti@nokia.com
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
  -
    name: Roberto Manzotti
    org: Cisco
    email: rmanzott@cisco.com
  -
    name: Gert Grammel
    org: Juniper
    email: ggrammel@juniper.net

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
  ITU-T_G.807:
    title: "Generic functional architecture of the optical media network"
    author:
      org: International Telecommunication Union
    date: January 2021
    seriesinfo: ITU-T Supplement G.807, Amendment 1
  ITU-T_G.872:
    title: "Architecture of optical transport networks"
    author:
      org: International Telecommunication Union
    date: January 2021
    seriesinfo: ITU-T Supplement G.872, Amendment 1
  ITU-T_G.Sup39:
    title: "Optical system design and engineering considerations"
    author:
      org: International Telecommunication Union
    date: February 2016
    seriesinfo: ITU-T Supplement G.Sup39

--- abstract

This document defines a collection of common data types, identities,
and groupings in the YANG data modeling language. These common types
and groupings, derived from the built-in YANG data types, identities,
and groupings are intended to be imported by modules that model Optical Layer 0 configuration and state
capabilities, such as Wavelength Switched Optical Networks (WSONs) and
flexi-grid Dense Wavelength Division Multiplexing (DWDM) networks.

This document obsoletes RFC 9093 by replacing the YANG module it contained with a new revision that includes additional YANG data types, identities and groupings.

--- middle

# Introduction

   This document introduces a collection of common data types derived
   from the built-in YANG data types.  The derived types and groupings
   are designed to be the common types applicable for modeling Traffic
   Engineering (TE) features as well as non-TE features (e.g., physical
   network configuration aspects) for Layer 0 optical networks in
   models defined outside of this document.  The applicability of
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

## Editorial Note (To be removed by RFC Editor)

> Note to the RFC Editor: This section is to be removed prior to publication.

This document contains placeholder values that need to be replaced with finalized values at the time of publication. This note summarizes all of the substitutions that are needed.

Please apply the following replacements:

- XXXX --> the assigned RFC number for this I-D

- YYYY --> the assigned RFC number for {{!I-D.ietf-teas-rfc8776-update}}

- ZZZZ --> the assigned RFC number for {{!I-D.ietf-ccamp-optical-impairment-topology-yang}}

Please replace the revision date of the latest revision of the 'ietf-layer0-types' module with the publication date of this I-D, using the the format (year-month-day).

Please manually fix the YANG trees in {{yang-tree}} which have been generated by pyang and have some bugs.

## Terminology and Notations

In the context of this document, the term "layer 0" refers to the
photonic layer or WDM layer network in the architecture of the
optical transport network (OTN) as defined in {{ITU-T_G.709}}, {{ITU-T_G.872}},
and {{ITU-T_G.807}} as opposed to the electrical switching
layers of the OTN, which are typically referred to as layer 1 (L1).

The term "layer 0" may also be used for other transport network
technologies (e.g., copper-based, radio-based, or free space optics-based, etc.), which are outside the scope of this document.

   Refer to {{?RFC7446}} and {{?RFC7581}} for other key terms used in this
   document, and the terminology for describing YANG data models can be
   found in {{!RFC7950}}.

{::boilerplate bcp14}

## Prefix in Data Node Names

   In this document, names of data nodes and other data model objects
   are prefixed using the standard prefix associated with the
   corresponding YANG imported module.

| Prefix       | YANG module                      | Reference
| te-types     | ietf-te-types                    | \[RFCYYYY]
| l0-types     | ietf-layer0-types                | RFC XXXX
{: #tab-prefixes title="Prefixes and corresponding YANG module"}

# Layer 0 Types Module Contents

This document defines a YANG module for common Layer 0 types, ietf-layer0-types.
This module is used for WSON and flexi-grid DWDM networks.

## Identities

The "ietf-layer0-types" module contains the following YANG reusable YANG identities:

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
: A base YANG identity from which specific identities defining the Wavelength selection methods, as defined in {{!RFC7689}}, are derived.

modulation:
: A base YANG identity to define the different modulation types, as defined in {{ITU-T_G.Sup39}}

switching-wson-lsc:
: A YANG identity for the Wavelength Switched Optical Network Lambda-Switch Capable (WSON-LSC) interface switching capability as defined in {{!RFC7688}}.

switching-flexi-grid-lsc:
: A YANG identity for the Flexi-Grid Lambda-Switch Capable (Flexi-Grid-LSC) interface switching capability as defined in {{!RFC8363}}.

It is worth noting that there is an inheritance relationship between the Lambda-Switch Capable (LSC) switching capability, defined in {{!RFC3471}}, and the WSON-LSC and Flexi-Grid-LSC, defined respectively in {{!RFC7688}} and {{!RFC8363}}. As a consequence, the 'switching-wson-lsc' and 'switching-flexi-grid-lsc' YANG identities are defined as derived identities from the 'switching-lsc', defined in {{!I-D.ietf-teas-rfc8776-update}}.

## Data Types

The "ietf-layer0-types" module contains the following YANG reusable YANG data types:

operational-mode:
: A YANG data type used to identify an organization (e.g., vendor) specific mode for transceiver capability description, as defined in {{Section 2.6.2 of !I-D.ietf-ccamp-optical-impairment-topology-yang}}

snr:
: A YANG data type used to represent an (Optical) Signal-to-noise ratio measured over 0.1 nm resolution bandwidth, as defined in {{ITU-T_G.977.1}}

psd:
: A YANG data type used to represent a Power Spectral Density (PSD), as defined in {{ITU-T_G.9700}}

### Reporting unknown values

Some data types, whose identifiers are suffixed as "-or-null", are defined as a union with an empty type (e.g., snr-or-null).

The empty data type is added to allow reporting the cases where the value is unknown and differentiating the case where an attribute is unknown from the case where an attribute is not applicable:

- if the value of a mandatory attribute is unknown, it MUST be reported using the empty type;
- if an optional attribute is applicable but its value is unknown, it MUST be reported using the empty type;
- if an optional attribute is not applicable to an entity, it MUST be omitted (not be present in the datastore).

## Groupings

The "ietf-layer0-types" module contains the following YANG reusable YANG groupings:

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
: This grouping shows the flexi-grid-specific label-start and label-end information which is used to describe the range of available nominal central frequencies. See {{label-range}} for more details.
: As described in {{Section 3.1 of !RFC8363}}, the range of available nominal central frequencies is advertised for m=1, which means that for an available central frequency n, the frequency slot from central frequency n-1 to central frequency n+1 is available.

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
: When this grouping is used, the explicit-mode container shall be augmented
with a leafref to an explicit mode template with the proper XPath, which
depends from where this grouping is actually used.

> Examples of how the transceiver-capabilities grouping can be used and augmented with a leafref
to an explicit mode template are provided in the YANG models defined in
{{?I-D.ietf-ccamp-optical-impairment-topology-yang}} and {{?I-D.ietf-ccamp-dwdm-if-param-yang}}.

standard-mode:
: A YANG grouping for the standard modes defined in {{ITU-T_G.698.2}}.

organizational-mode:
: A YANG grouping to define transponder operational mode supported by
organizations or vendors, as defined in {{!I-D.ietf-ccamp-optical-impairment-topology-yang}}.

explicit-mode:
: A YANG grouping to define the list of attributes related to the limits of the optical
impairments, in case of transceiver explicit mode, as defined in {{!I-D.ietf-ccamp-optical-impairment-topology-yang}}.
: Note that the actual portion of the spectrum occupied by an OTSi is not explicitly reported within the explicit-mode parameters because it can be calculated using the available-baud-rate, the roll-off and the min-carrier-spacing attributes.

transceiver-tuning-range:
: A YANG grouping that defines the transceiver tuning range, which
includes the minimum and maximum tuning frequency, as well as the
frequency tuning granularity.

common-all-modes:
: A YANG grouping used to define the common attributes used by all transceiver's modes.

penalty-value:
: A YANG grouping to define the penalty value for multiple penalty types, such as Chromatic Dispersion (CD), Polarization Mode Dispersion (PMD), as defined in {{ITU-T_G.666}} or Polarization Dependent Loss(PDL)

## WDM Label and Label Range {#label-range}

As described in {{!RFC6205}} and {{!RFC7699}}, the WDM label represents the frequency slots assigned to a WDM Label Switched Path (LSP) on a given WDM Link, which models an Optical Multiplex Section (OMS) Media Channel Group (MCG) as described in {{?I-D.ietf-ccamp-optical-impairment-topology-yang}}.

The same WDM label (which represents the frequency slots associated with the WDM LSP) will be assigned on all the
WDM Links along a regen-free LSP path or path segment (i.e., an LSP path or path segment which does not include any 3R regenerator). Depending on the 3R capabilities, the WDM label may or may not change at a 3R regenerator: see
{{Section 2.7 of ?I-D.ietf-ccamp-optical-impairment-topology-yang}} for more details on 3R regenerators.

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

The WDM Label Range is defined by augmenting the label-restriction list, defined in {{!I-D.ietf-teas-rfc8776-update}}, with WDM technology-specific attributes, using the l0-label-range-info grouping (for WSON only models) or the flexi-grid-label-range-info grouping (for DWDM flexible-grid only models) or the wdm-label-range-info grouping (for models that support both WSON and DWDM flexible-grid).

Each entry in the label-restriction list represents either the range of the available central wavelength values (in case of CWDM fixed-grid) or the range of the available nominal central frequencies values (in case of DWDM fixed or flexible grids): the grid-type attribute defines the type of grid for each entry of the list.

In case of DWDM flexible grid, each entry in the label-restriction list also represents the range of the supported slot width values
based on the following attributes, defined based on concepts used in {{?RFC7699}}:

* slot-width-granularity, which represents the minimum space between slot widths;

* min-slot-width-factor: a multiplier of the slot width granularity, indicating the minimum slot width supported by each entry in the label-restriction list;

* max-slot-width-factor: a multiplier of the slot width granularity, indicating the maximum slot width supported by each entry in the label-restriction list.

Each entry of the label-restriction list, as defined in {{!I-D.ietf-teas-rfc8776-update}}, defines a label-start, a label-end, a label-step and a range-bitmap.

The label-start and label-end definitions, when used for representing WDM label range, are augmented with WDM technology-specific attributes, using the wson-label-start-end grouping (for WSON only models) or the flexi-grid-label-start-end grouping (for DWDM flexible-grid only models) or the wdm-label-start-end grouping (for models that support both WSON and DWDM flexible-grid).

The label-step definition, when used for representing WDM label range, is augmented with WDM technology-specific attributes, using the wson-label-step grouping (for WSON only models) or the flexi-grid-label-step grouping (for DWDM flexible-grid only models) or the wdm-label-step grouping (for models that support both WSON and DWDM flexible-grid). The label-step definition for WDM depends on the WDM grid type:

* For CWDM and DWDM fixed grids, it describes the channel spacing, as defined in {{?RFC6205}};

* For DWDM flexible grids, it describes the nominal central frequency granularity (e.g., 6,25 GHz) as well as the multiplier for the supported values of n, as defined in {{?RFC7699}}.

# YANG Module for Layer 0 Types {#yang-code}

This YANG module references {{!RFC6205}}, {{!RFC7689}}, {{!RFC7699}}, {{!RFC8363}}, {{?RFC9093}}, {{ITU-T_G.666}}, {{ITU-T_G.694.1}}, {{ITU-T_G.694.2}}, {{ITU-T_G.698.2}}, {{ITU-T_G.709}}, {{ITU-T_G.709.2}}, {{ITU-T_G.709.3}}, {{ITU-T_G.959.1}} {{ITU-T_G.975}}, {{ITU-T_G.975.1}}, {{ITU-T_G.977.1}}, {{ITU-T_G.9700}} and {{OIF_400ZR}}.

~~~~ yang
{::include ./ietf-layer0-types.yang}
~~~~
{: #fig-yang-code title="Layer 0 Types YANG module"
sourcecode-markers="true" sourcecode-name="ietf-layer0-types@2025-10-02.yang"}

# Security Considerations

This section is modeled after the template described in {{Section 3.7
of ?I-D.ietf-netmod-rfc8407bis}}.

The "ietf-layer0-types" YANG module defines a data model that is
designed to be accessed via YANG-based management protocols, such as
NETCONF {{?RFC6241}} and RESTCONF {{?RFC8040}}. These YANG-based management
protocols (1) have to use a secure transport layer
(e.g., SSH {{?RFC4252}}, TLS {{?RFC8446}}, and
QUIC {{?RFC9000}}) and (2) have
to use mutual authentication.

The Network Configuration Access Control Model (NACM) {{!RFC8341}}
provides the means to restrict access for particular NETCONF or
RESTCONF users to a preconfigured subset of all available NETCONF or
RESTCONF protocol operations and content.

The YANG module defines a set of identities, types, and
groupings. These nodes are intended to be reused by other YANG
modules. The module by itself does not expose any data nodes that
are writable, data nodes that contain read-only state, or RPCs.
As such, there are no additional security issues related to
the YANG module that need to be considered.

Modules that use the groupings that are defined in this document
should identify the corresponding security considerations.

# IANA Considerations

IANA is requested to update the following registration in the "ns" registry
within the "IETF XML Registry" group {{?RFC3688}} to reference this document:

~~~~
      URI: urn:ietf:params:xml:ns:yang:ietf-layer0-types
      Registrant Contact:  The IESG.
      XML: N/A; the requested URI is an XML namespace.
~~~~

IANA is requested to register the following YANG module in the "YANG Module Names" registry {{?RFC6020}}
within the "YANG Parameters" registry group.

~~~~
      Name: ietf-layer0-types
      Maintained by IANA? N
      Namespace: urn:ietf:params:xml:ns:yang:ietf-layer0-types
      Prefix: l0-types
      Reference: RFC XXXX
~~~~

--- back

# The Complete Schema Trees {#yang-tree}

This appendix presents the complete tree of the Layer 0 Types data model. See {{?RFC8340}} for an explanation of the symbols used. The data type of every leaf node is shown near the right end of the corresponding line.

~~~~ ascii-art
{::include-fold ./ietf-layer0-types.tree}
~~~~
{: #fig-yang-tree}

# Changes from RFC 9093 {#changes-bis}

This version adds new identities, data types, and groupings to the 'ietf-layer0-types' YANG module. It also fixes few bugs in {{?RFC9093}}.

The following new YANG identities have been added to the 'ietf-layer0-types' module:

- cwdm-ch-spc-type;
- flexi-ncfg-type;
- flexi-ncfg-6p25gh;
- modulation;
- dpsk;
- qpsk;
- dp-qpsk;
- qam8;
- dp-qam8;
- qam16;
- dp-qam16;
- qam32;
- dp-qam32;
- qam64;
- dp-qam64;
- fec-type;
- g-fec;
- super-fec;
- no-fec;
- sc-fec;
- o-fec;
- c-fec;
- line-coding;
- nrz-2p5g;
- nrz-otu1;
- nrz-10g;
- nrz-otu2;
- otl4.4-sc;
- foic1.4-sc;
- wavelength-assignment;
- first-fit-wavelength-assignment;
- random-wavelength-assignment;
- least-loaded-wavelength-assignment;
- lower-first-wavelength-assignment;
- upper-first-wavelength-assignment;
- type-power-mode;
- power-spectral-density;
- carrier-power;
- switching-wson-lsc;
- switching-flexi-grid-lsc.

The following new YANG data types have been added to the 'ietf-layer0-types' module:

- standard-mode
- organization-identifier
- operational-mode
- frequency-thz
- frequency-ghz
- snr
- snr-or-null
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

The following new YANG groupings have been added to the 'ietf-layer0-types' module:

- wdm-label-start-end
- wdm-label-step
- wdm-label-hop
- wdm-label-range-info
- transceiver-capabilities
- standard-mode
- organizational-mode
- penalty-value
- explicit-mode
- common-standard-organizational-mode
- transceiver-tuning-range
- common-all-mode
- common-transceiver-param
- common-transceiver-configured-param
- common-transceiver-readonly-param
- tunnel-attributes
- frequency-range
- frequency-range-with-identifier
- path-constraints
- path-properties

The following YANG identities have been obsolted (bug fixing) in the 'ietf-layer0-types' module:

- flexi-ch-spc-type;
- flexi-ch-spc-6p25ghz.

The case super within the flexi-grid-label-hop has been obsolted (bug fixing).

The flexi-grid-channel-spacing data node in flexi-grid-label-step grouping has been obsoleted (bug fixing).

The default value of the min-slot-width-factor data node within flexi-grid-label-range-info grouping has been removed (bug fixing).

{: numbered="false"}

# Acknowledgments

The authors and the working group give their sincere thanks to Robert
Wilton for the YANG doctor review and to Adrian Farrel and Tom Petch for their comments
during the model and document development.

This document was prepared using kramdown.
