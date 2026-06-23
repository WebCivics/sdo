# SDO Backlog Semantic Transition Plan

With the `sdo-app-design.md` architecture establishing the WebCivics Standards Documentation Engine, this document defines the roadmap for transitioning the existing text-based standards backlog into executable `nquin` semantic graphs.

## Transition Strategy

### Phase 1: Semantic Mapping & Nquin Extraction
Extracting normative rules from existing drafts (`q42-format-internal-draft.md`, `did-q42-method-draft.md`, etc.) and mapping them to nquin schemas.
- **Identification:** Isolate protocol syntax, constraints, and semantics.
- **Vocabulary Development:** Create the base RDF vocabularies (`q42:`, `hcai:`).

### Phase 2: Validation Boundary Definition
Translate text-based constraints into executable code:
- **ShEx Rules:** Develop shape expressions for data ingestion (e.g., `did:q42` parser constraints).
- **SHACL Audits:** Create SHACL shapes for multi-hop validation (e.g., cryptographic encumbrance states).

### Phase 3: Pipeline Bootstrapping
Bootstrap the RDF-to-ReSpec pipeline using one candidate standard to prove end-to-end functionality:
- Load extracted nquins into the Qualiadb test harness.
- Configure Jinja/OntoReSpec templates to render W3C/IETF-compliant output.

## Execution Priority

Based on the existing `standards-backlog.md`, semantic conversion will follow this sequence:

1. **`q42-format-internal-draft.md`**: Base container and sidecar semantic definitions.
2. **`qualia-vault-manifest.md`**: Model the human-facing entry layer and CBOR-LD projections.
3. **`did-q42-method-draft.md`**: Convert identifier syntax and dispatch rules into ShEx grammar.
4. **`hcai-agreement-negotiation-protocol.md`**: Implement agreement vocabulary as a test for Restorative Economics constraint mechanisms.
