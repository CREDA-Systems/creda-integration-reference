# CREDA Integration Reference

Implementation and integration infrastructure for deterministic governance across applications, agents, enterprise systems, and distributed networks.

## About CREDA®

CREDA® is an implementation and integration platform for deterministic governance.

CREDA provides the technical layer through which applications, agents, enterprise systems, and distributed networks can submit proposed actions for governance evaluation and consume machine-readable governance results.

This repository provides a limited public integration surface for developers, infrastructure providers, ecosystem partners, and grant reviewers evaluating CREDA interoperability.

## Purpose of This Repository

This repository is intended to demonstrate:

* clear integration boundaries around the CREDA® platform;
* implementation-neutral request and response interfaces;
* how external systems can submit proposed actions for governance evaluation;
* how machine-readable governance results can be returned to downstream systems;
* how blockchain, distributed-ledger, application, and enterprise adapters can integrate without becoming the source of governance authority; and
* a path toward open reference integrations and ecosystem-specific tooling.

This repository is intentionally limited.

It does not contain the complete CREDA runtime, production service architecture, proprietary orchestration logic, internal evaluation methods, or other separately maintained implementation technology.

It does not represent capabilities as implemented unless corresponding public code or documentation is present in this repository.

## Reference Integration Model

At a high level, the public integration model separates the requesting system from the governance implementation and from downstream infrastructure.

Application / Agent / Workflow
            │
            ▼
     Governance Request
            │
            ▼
          CREDA®
  Implementation Boundary
            │
            ▼
     Governance Response
            │
            ▼
 Application / Adapter / Chain

The requesting system identifies a proposed action and supplies the information required by the applicable implementation.

CREDA evaluates the request within the implementation boundary and returns a machine-readable governance response.

A downstream application, adapter, enterprise platform, or distributed network may then consume that response according to the applicable integration.

## Repository Contents

### Documentation

`docs/architecture.md`
Describes the public CREDA integration architecture and major component boundaries.

`docs/integration-model.md`
Explains the relationship between requesting systems, CREDA, governance responses, and downstream infrastructure.

`docs/trust-state-consumption.md`
Describes at a high level how CREDA implementations may consume or interact with externally defined governance-state information.

`docs/boundaries.md`
Defines the public/private implementation boundary for this repository.

### Reference Schemas

`schemas/governance-request.schema.json`
A draft, non-normative public interface for representing a governance request.

`schemas/governance-response.schema.json`
A draft, non-normative public interface for representing a governance response.

These schemas are integration aids only.

They do not disclose or define the complete CREDA runtime, proprietary evaluation logic, internal services, or separately maintained implementation methods.

### Examples

The `examples/` directory contains minimal example payloads corresponding to the public reference schemas.

Examples are illustrative and do not represent production transactions, certification test vectors, or complete governance implementations.

### Adapters

The `adapters/` directory documents the intended boundary for infrastructure-specific integrations.

Adapter implementations may target blockchains, distributed ledgers, APIs, applications, enterprise systems, or other execution environments.

No adapter should be represented as implemented until corresponding code exists.

## Infrastructure Neutrality

CREDA® is designed to support integration across different infrastructure environments.

Potential integrations may include:

* distributed ledgers and blockchain networks;
* smart-contract platforms;
* enterprise applications;
* APIs and workflow systems;
* identity and credential infrastructure;
* AI agents and autonomous systems; and
* legacy infrastructure.

A particular blockchain, network, application, or cloud provider does not become the source of governance authority merely because it records, transports, or executes a governance result.

## Relationship to VTI Foundation Inc.

CREDA Systems is separate from VTI Foundation Inc.

VTI Foundation Inc. develops and stewards standards, reference architectures, and governance frameworks for deterministic governance of consequential digital systems.

CREDA Systems may implement
