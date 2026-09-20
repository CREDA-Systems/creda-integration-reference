# CREDA Integration Model

## Purpose

This document describes the public integration model for CREDA®.

It explains how external systems may submit a governance request, receive a machine-readable governance response, and pass that result to downstream infrastructure without exposing the proprietary CREDA implementation layer.

## Integration Sequence

1. Requesting System
        │
        ▼
2. Governance Request
        │
        ▼
3. CREDA® Implementation Boundary
        │
        ▼
4. Governance Response
        │
        ▼
5. Infrastructure Adapter
        │
        ▼
6. External System / Network

## 1. Requesting System

A requesting system may be an application, agent, workflow, enterprise service, smart-contract integration, identity system, or other digital system proposing an action.

The requesting system remains responsible for constructing a request appropriate to its implementation context.

## 2. Governance Request

A governance request provides the information needed for evaluation.

A public reference request may include:

* a unique request identifier;
* the proposed action;
* the subject or actor;
* the target resource;
* scope information;
* governance-context references;
* authority-state references;
* timestamps; and
* implementation-specific metadata.

The public schema is intentionally limited and should not be treated as a complete production contract.

## 3. CREDA® Implementation Boundary

CREDA receives the governance request and performs implementation-specific processing.

The public integration model treats this processing layer as a defined boundary.

Internal methods may include separately maintained functionality relating to:

* authority-state processing;
* policy evaluation;
* evidence handling;
* integrity and provenance;
* deterministic decision processing;
* replay or reconstruction;
* orchestration; and
* implementation-specific security controls.

These internal methods are outside the scope of this repository unless expressly published.

## 4. Governance Response

CREDA returns a machine-readable governance response.

A public reference response may identify:

* the request evaluated;
* the resulting disposition;
* a decision or artifact reference;
* relevant authority-state references;
* an evaluation-context reference;
* evaluation timestamps;
* integrity or provenance references; and
* optional implementation metadata.

The response is intended to be consumed by downstream systems without requiring those systems to reproduce the full internal CREDA processing model.

## 5. Infrastructure Adapter

An adapter translates, transports, records, or enforces the governance response within an external environment.

Examples may include:

* blockchain transaction adapters;
* smart-contract interfaces;
* API connectors;
* enterprise workflow connectors;
* identity-system integrations; and
* legacy-system gateways.

The adapter should preserve the meaning of the governance response rather than redefine it.

## 6. External System or Network

The external system may use the governance response to:

* permit an action;
* deny an action;
* hold an action;
* request additional evidence;
* request additional approval;
* escalate a request;
* record a decision;
* anchor an integrity reference; or
* initiate another implementation-defined workflow.

## Separation of Responsibilities

The public integration model intentionally separates:

**Request construction**
Performed by the requesting system.

**Governance evaluation**
Performed within the CREDA implementation boundary.

**Infrastructure execution or recording**
Performed by the downstream adapter and external system.

This separation allows CREDA integrations to remain portable across infrastructure environments.

## Infrastructure Neutrality

A CREDA integration does not require a particular blockchain, distributed ledger, cloud provider, identity provider, or application platform.

Ecosystem-specific adapters may be developed independently while preserving the same public integration pattern.

## Non-Normative Status

This document is illustrative and non-normative.

It does not define the complete CREDA runtime, establish VTI conformance, create certification rights, or expand the scope of the repository license.

See `../NOTICE.md` for additional intellectual-property and platform-boundary information.
