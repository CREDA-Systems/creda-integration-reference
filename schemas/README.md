# Reference Schemas

## Purpose

The schemas in this directory define a limited, non-normative public integration surface for CREDA®.

They are intended to support interoperability, implementation planning, developer integration, grant review, and future open-source reference work.

They do not define the complete CREDA runtime, proprietary processing model, internal services, or VTI Foundation Inc. standards.

## Current Schemas

### `governance-request.schema.json`

Provides a minimal public representation of a governance request submitted by an external application, agent, workflow, or other requesting system.

### `governance-response.schema.json`

Provides a minimal public representation of a machine-readable governance response returned by a CREDA implementation.

## Non-Normative Status

These schemas are public integration interfaces only.

They do not:

* define the complete CREDA® implementation;
* define Trust-State® conformance;
* define complete ASL or PAL semantics;
* establish certification requirements;
* disclose proprietary evaluation, replay, integrity, or authority-resolution logic;
* replace any official VTI Foundation Inc. specification; or
* grant rights beyond those provided by the repository license.

## Versioning

Early schemas may use pre-1.0 interface versions such as:

`0.1`

A schema version identifies the version of the public interface only.

It should not be interpreted as a version number for the CREDA platform, any VTI Foundation Inc. standard, or any certification program.

## Extension Guidance

Implementations may require additional fields.

Extensions should avoid changing the meaning of defined public fields and should not imply VTI conformance, CREDA endorsement, or certification merely because they are structurally compatible with these schemas.

## Intellectual Property

See `../NOTICE.md` for additional information concerning proprietary CREDA technology, standards, certification, trademarks, patents, and pre-existing intellectual property.
