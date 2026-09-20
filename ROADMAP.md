# Roadmap

## Purpose

This roadmap describes the intended development path for the CREDA® Integration Reference repository.

It applies only to public reference and integration work.

It does not commit CREDA Systems to publish proprietary runtime technology, internal services, patent-sensitive methods, or other separately maintained implementation details.

## Current Stage

**Stage 0 — Public Integration Surface**

Current work includes:

* repository governance and licensing;
* public integration architecture;
* request and response boundaries;
* Trust-State® consumption guidance;
* public/private implementation boundaries; and
* preparation for limited schemas and examples.

This stage is focused on making the integration surface understandable without exposing the proprietary CREDA implementation layer.

## Stage 1 — Reference Interfaces

Planned work may include:

* a draft governance-request schema;
* a draft governance-response schema;
* validated example payloads;
* identifier conventions;
* versioning conventions;
* error-handling guidance; and
* implementation-neutral interoperability notes.

## Stage 2 — Validation and Developer Tooling

Future public work may include:

* schema validation utilities;
* example test fixtures;
* request/response validation examples;
* developer setup guidance;
* integration test helpers; and
* reproducible reference flows.

No capability should be represented as implemented until corresponding public code or documentation exists.

## Stage 3 — Adapter Implementations

Subject to technical review, funding, partnerships, and ecosystem requirements, CREDA Systems may develop public reference adapters for environments such as:

* Hedera;
* XRPL;
* Chainlink;
* XDC Network;
* Optimism / Superchain;
* Cardano;
* enterprise APIs; and
* other suitable infrastructure.

Each adapter should remain separable from the proprietary CREDA runtime.

## Stage 4 — SDK and API Surface

Where appropriate, future public work may include:

* SDKs;
* API client libraries;
* adapter libraries;
* developer tooling;
* test harnesses; and
* integration demonstrations.

Publication of client-side tooling does not imply publication of the underlying CREDA runtime.

## Repository Principles

Development of this repository should follow several principles:

* publish interfaces before internals;
* do not expose proprietary implementation methods merely to demonstrate maturity;
* do not publish placeholder code that implies unsupported capability;
* keep ecosystem-specific code separate from the infrastructure-neutral reference model;
* maintain clear intellectual-property boundaries;
* validate examples before publication;
* prefer small, testable interfaces over speculative breadth; and
* accurately distinguish current capability from planned work.

## Versioning

Early releases may use pre-1.0 semantic versioning, for example:

`v0.1.0-reference`

A `v1.0.0` designation should be reserved for a stable public integration surface with defined interfaces, documentation, examples, and validation behavior.

## Scope Changes

This roadmap may evolve based on:

* implementation experience;
* grant-funded work;
* customer or partner integration requirements;
* ecosystem requirements;
* security review;
* intellectual-property review; and
* changes in the public integration strategy.

Roadmap items are directional and are not guarantees of delivery.

## Related Notice

See `NOTICE.md` for intellectual-property, trademark, and platform-boundary information.
