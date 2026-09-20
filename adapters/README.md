# Infrastructure Adapters

## Purpose

This directory defines the public boundary for ecosystem-specific and infrastructure-specific CREDA® adapters.

Adapters connect CREDA governance responses to external systems without changing the meaning of the governance outcome produced upstream.

## Adapter Role

An adapter may:

* validate required response fields;
* translate a governance response into an infrastructure-specific message or transaction;
* submit or record a result;
* invoke an application or smart-contract workflow;
* return an execution receipt or reference; and
* expose integration-specific status information.

An adapter should not silently reinterpret, expand, or replace the governance decision produced by the CREDA implementation.

## Potential Targets

Future adapters may target environments such as:

* Hedera;
* XRPL;
* Chainlink;
* XDC Network;
* Optimism / Superchain;
* Cardano;
* enterprise APIs;
* workflow platforms;
* identity infrastructure; and
* legacy systems.

No adapter is represented as implemented until corresponding public code exists.

## Adapter Boundary

CREDA Governance Response
          │
          ▼
 Infrastructure Adapter
          │
          ▼
External Network / System

The adapter sits downstream of the CREDA implementation boundary.

It does not become the source of governance authority merely because it transports, records, verifies, or executes a result.

## Repository Structure

When substantive adapter work exists, it may be placed in separate repositories or organized under clearly identified adapter directories.

Example future repository names may include:

creda-hedera-reference
creda-xrpl-reference
creda-chainlink-reference
creda-xdc-reference
creda-superchain-reference
creda-cardano-reference

Empty repositories should not be created merely to imply implementation readiness.

## Public / Private Boundary

Public adapters may expose:

* request and response mappings;
* transaction construction;
* event handling;
* verification helpers;
* receipts;
* integration tests; and
* developer documentation.

Adapters should not expose proprietary CREDA runtime internals unless expressly approved for public release.

## Licensing

Each adapter repository should clearly identify its applicable license.

Open-source adapter code does not change the ownership or licensing status of proprietary CREDA technology maintained outside that repository.

## Non-Normative Status

This document describes a public integration boundary only.

It does not define CREDA product requirements, VTI Foundation Inc. standards, certification criteria, or rights beyond those expressly provided by the applicable repository license.

See `../NOTICE.md` for additional intellectual-property and platform-boundary information.
