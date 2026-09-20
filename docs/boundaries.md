# Public / Private Boundaries

## Purpose

This document defines the intended boundary between material that may be published in the CREDA® Integration Reference repository and CREDA Systems technology that remains separately maintained.

The purpose of this boundary is to support technical transparency and interoperability without unintentionally publishing proprietary implementation methods, patent-sensitive material, or other protected technology.

## Public Reference Surface

Material appropriate for this repository may include:

* public interface definitions;
* request and response schemas;
* implementation-neutral documentation;
* sample payloads;
* adapter patterns;
* validation examples;
* interoperability guidance;
* public test fixtures;
* developer documentation; and
* ecosystem-specific reference integrations that have been intentionally approved for public release.

Public material should be sufficient to help an external developer understand how to integrate with CREDA without requiring access to proprietary internal implementation details.

## Separately Maintained Technology

The following material should remain outside this repository unless expressly approved for public release:

* proprietary orchestration logic;
* internal service topology;
* protected authority-resolution methods;
* internal rule-resolution mechanisms;
* canonicalization methods;
* replay and reconstruction internals;
* integrity-value generation methods;
* policy-evaluation internals;
* security-sensitive implementation details;
* production credentials or configuration;
* unpublished patent-sensitive implementation material;
* internal certification or conformity-assessment logic; and
* confidential third-party integration information.

## Interface Does Not Equal Implementation

Publication of a public interface does not require publication of the internal implementation that satisfies that interface.

For example, CREDA may publish:

Governance Request
        │
        ▼
[ CREDA Implementation Boundary ]
        │
        ▼
Governance Response

without publishing the proprietary processes operating inside the implementation boundary.

This distinction is intentional.

## Pre-Existing Intellectual Property

Public integration work may rely conceptually on pre-existing CREDA Systems technology.

Publication of a reference implementation, adapter, schema, or example does not change the ownership or licensing status of separately maintained pre-existing technology.

Where grant-funded or partner-funded work is performed, project documentation should distinguish between:

* pre-existing technology;
* previously published reference material;
* newly created funded deliverables; and
* third-party components.

## Relationship to VTI Foundation Inc.

CREDA Systems and VTI Foundation Inc. perform different roles.

VTI Foundation Inc. develops and stewards standards, reference architectures, and related governance frameworks.

CREDA Systems develops implementation and integration technology.

The publication of CREDA integration material does not publish, amend, or license VTI Foundation Inc. standards or certification materials.

## Patent-Sensitive Review

Before publishing new technical material, particular care should be given to content that may describe:

* claimed or potentially claimed system behavior;
* claim-sensitive execution sequences;
* protected state-transition logic;
* enforcement-gateway behavior;
* integrity or replay mechanisms;
* deterministic reconstruction methods; or
* other implementation details relevant to pending or future patent rights.

Where uncertainty exists, publication should occur only after appropriate intellectual-property review.

## Repository Discipline

This repository should remain intentionally small.

Material should not be added merely to make the project appear larger or more mature.

Public artifacts should be:

* accurate;
* technically useful;
* internally consistent;
* supportable by existing or clearly identified planned work; and
* appropriate for public disclosure.

Placeholder code that implies unsupported capability should not be published.

## Non-Normative Status

This document describes repository publication boundaries only.

It does not define CREDA product requirements, VTI Foundation Inc. standards, certification criteria, or rights beyond those expressly provided by the applicable repository license.

See `../NOTICE.md` for additional intellectual-property and platform-boundary information.
