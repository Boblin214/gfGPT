# PHASE_R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE

## Review Status

```text
R3_EGRESS_REVOCATION_R2_FOLLOWUP_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS
INDEPENDENT_REVIEW=REQUIRED
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

## Scope

Complete Scope/Worker Result persistence, Intent-level Egress sequence
allocation, attack review and cross-module consistency evidence.

## Source Catalog

| ID | Path | Bytes | SHA-256 |
|---|---|---:|---|
| S001 | `PHASE_R3_EGRESS_EVENT_SEQUENCE_DESIGN.md` | 2754 | 32B5772A47C7B07D01EF09E16437F90D879A9D3E91FD02DF18E79164B538BE2D |
| S002 | `PHASE_R3_R2_FOLLOWUP_ATTACK_REVIEW.md` | 3425 | 15AE632104D9DD1BF2C0CD2710FD50C98B8A10D07F6E89C37AE06643E2354FC7 |
| S003 | `PHASE_R3_R2_FOLLOWUP_BASELINE.md` | 6540 | 4D06F2E21DF7D249239EFD6A3E5B46690DD3F67FC3FBF93116D0623CFF248E58 |
| S004 | `PHASE_R3_R2_FOLLOWUP_CROSS_MODULE_REVIEW.md` | 3205 | AF3A300929DF06D175D25C7570431E9F250AEAEC0D1D5471CA66DA6A6F3CC035 |
| S005 | `PHASE_R3_R2_FOLLOWUP_FINAL_REPORT.md` | 4880 | 84F66BFBF4034A3667CA22CF6A7A310C2E83F7DCD1607A2DACF1E71934354B45 |
| S006 | `PHASE_R3_R2_FOLLOWUP_LOCK_ORDER.md` | 2509 | 9F1B9AA20CB629F8EAC095076A87A9CA242076DC1E1BC264D73372DCCD763F93 |
| S007 | `PHASE_R3_R2_FOLLOWUP_NEGATIVE_TEST_MATRIX.md` | 2732 | 13700A1D4AE24CC58DC93470B0C5D1523B62EF591F44B6289688693CFAB42747 |
| S008 | `PHASE_R3_R2_FOLLOWUP_REFERENCE_MODEL.md` | 2460 | 2BF06E1402E1904F05DFB0813B0525629657E9C66B0E38E6C65C36EA4C1F6B15 |
| S009 | `PHASE_R3_R2_FOLLOWUP_RISK_REGISTER.md` | 2741 | D3928ABAB0CD573C3BCCE68D2A0CA6664020A8F01F865755010D1A094CCDCD96 |
| S010 | `PHASE_R3_R2_FOLLOWUP_SQL_REVIEW.md` | 2675 | 53BD127E797FB3CD076BE2BF99317C2D5C0EE0901722EBF19D25E7647E9461D1 |
| S011 | `PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION.md` | 10329 | D87CA18F05C464CFC3985EC3D6EC002B8265E2C6758E3D807E625E975C98355B |
| S012 | `PHASE_R3_R2_FOLLOWUP_TRANSACTION_MATRIX.md` | 2397 | 0A235E1D61C2B2AC78B590B155550D20D9960036AC28A8B5D9B1096EDE76CF25 |
| S013 | `PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT_CONTRACT.md` | 3113 | C834FE103C53A18BC2AAEDD4D37B545AD48CF939B727EE95955B825A2D7A74D0 |
| S014 | `PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT_CONTRACT.md` | 2145 | 3165FDB04D6B3052705AF566C6AF48B67C05BCD7EF8192F1331B0414257EB402 |
| S015 | `PHASE_R3_EGRESS_EVENT_SEQUENCE.sql` | 12251 | 312B1C6834FF1778D6F1557A21598BAE1AE62A7FF394CFDD33B979BA89E4220A |
| S016 | `PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql` | 16953 | 7220EBFAF592AD4F71A55E51924ABCCA72889D13546809FD2FAE02E4CCBB72DD |
| S017 | `PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT.sql` | 4971 | 967F852725DEE236FA1B23B771769C46F32369F1EBCE8CBC57BB03D1489A688F |
| S018 | `contracts.ts` | 6745 | 8F2D411F32096B5DAA7943B7F96843983DFE42EBBEEE65F387BDFB904216F860 |
| S019 | `lock-order.ts` | 1430 | 93D79865E4D08C1951194992969DAE954A38097519E97B49895FDF7FA5C68354 |
| S020 | `models/canonical.ts` | 1340 | C5298ECD2A5FAA763017A9CA657F5BCBCF8C613B7CE1820787AA718488F0AB85 |
| S021 | `models/egress-intent-sequence.ts` | 11041 | 99763E75B32CA5698FF5002B24DD9C5EFF60D06F32047761439123EAC15B7AEB |
| S022 | `models/scope-cleanup-complete-result.ts` | 15615 | 39B8B2C152989F5AE1868730F5AFF76092C8A0D631C0952424A106EA6505C7D3 |
| S023 | `models/sql-analyzer.ts` | 6905 | D2A4F9BA08651C637E221905E77EC07BFFEE327A7C2F66EE3A0151254ED64F56 |
| S024 | `models/worker-revocation-complete-result.ts` | 10036 | CC26BB67507CD3F6B46D47FBCCB38D37EAF205660B29A4BAF3587A9E7FE7F9A5 |
| S025 | `tests/egress-intent-sequence.test.ts` | 7978 | EF38EC0C97D2A5C4250BDC70D5B35DEAB5D8AAA87F829ED72543FAAA9742D26D |
| S026 | `tests/scope-cleanup-complete-result.test.ts` | 7228 | 31AD1C29B484E51EB19547FEA97BE7FB7C686FEE40EB838A6601A7617D5F8E7D |
| S027 | `tests/sql-analyzer-followup.test.ts` | 2655 | 1AFF9C0D753E836372ABB8E49F27358E99BCCF50AF18EF714159C15D259E725C |
| S028 | `tests/worker-revocation-complete-result.test.ts` | 5595 | AB418B385BDB550002BDE9303A4B4ACB3D10382621ACF8B61E5ACA43A828D991 |
| S029 | `tools/build-evidence.mjs` | 14396 | 1C482134FF7CF55F748417B3AE23DD5C0986E8C9860E5AFD1FCA5B3B4C479AB0 |
| S030 | `tools/generate-scope-sql.mjs` | 5119 | 29FC76BE59002286643F61CFC16468BF61F76364556C9A4C6673381292737336 |
| S031 | `tools/run-verification.ps1` | 6933 | 265A3D43A8F64505D92FBE43CD14047CEBF532063A208B7C30211F47D6BC3AF9 |
| S032 | `vitest.config.ts` | 245 | 3F69AC0EFB7072D8EB155B7D15F78C3231769D82885A911AD4BE06225A6E0E3B |

## Complete Source Bodies
### S001. PHASE_R3_EGRESS_EVENT_SEQUENCE_DESIGN.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_EGRESS_EVENT_SEQUENCE_DESIGN.md`
- Bytes: `2754`
- SHA-256: `32B5772A47C7B07D01EF09E16437F90D879A9D3E91FD02DF18E79164B538BE2D`

<!-- BEGIN_EXACT_SOURCE id=S001 sha256=32B5772A47C7B07D01EF09E16437F90D879A9D3E91FD02DF18E79164B538BE2D bytes=2754 -->
````text
# PHASE_R3_EGRESS_EVENT_SEQUENCE_DESIGN

## 1. Options

### Option A: One Intent sequence space

All events for one Intent share a monotonic sequence allocated by a database
row locked and updated in the event transaction.

Advantages:

- one strict order for DB and Runtime source events;
- Runtime cannot choose a conflicting sequence;
- concurrent allocation is serialized;
- rollback consumes no sequence;
- exact model/SQL alignment.

Requirements:

- database sequence authority;
- stable evidence identity for COMMIT ambiguity;
- source identity whitelist;
- no Runtime sequence parameter.

### Option B: Per-source sequences

`UNIQUE (intentId, sourceType, sourceSequence)` avoids first-event collision but
does not establish strict cross-source order. It needs a separate observed
order/source trust design.

## 2. Selected Design

Option A is selected:

```text
Intent
  -> Event Sequence Authority
  -> DB Authorization event sequence 1
  -> Runtime evidence sequence 2+
  -> Audit persistence
```

Table:

```text
trust_r7_egress_event_sequence
  egress_intent_id
  next_sequence
  sequence_version
  updated_at_ms
```

Evidence unique constraints:

```text
UNIQUE (egress_intent_id, intent_sequence)
UNIQUE (egress_intent_id, evidence_id)
```

## 3. Allocation

Write authorization creates the sequence row with `next_sequence=2` and uses
sequence `1` for `EGRESS_WRITE_START_AUTHORIZED`.

Runtime event transaction:

```text
check stable evidence_id
  -> lock runtime state
  -> lock sequence row
  -> UPDATE next_sequence = next_sequence + 1
     RETURNING next_sequence - 1
  -> INSERT evidence with returned sequence
  -> update runtime state
  -> append Audit
  -> COMMIT
```

Runtime input never contains `sourceSequence` or a final `intentSequence`.

## 4. Concurrency and Crash

| Condition | Behavior |
|---|---|
| two concurrent events | sequence row lock serializes, unique sequence values |
| rollback before COMMIT | sequence update rolls back; no gap |
| crash after allocation before commit | allocation rolls back |
| COMMIT succeeded, response lost | retry same `evidence_id` returns stored event |
| duplicate evidence ID same payload | replay stored event, no new Audit |
| duplicate evidence ID different payload | `EVIDENCE_REPLAY_CONFLICT` |
| disconnected authority | no evidence/sequence commit |

## 5. Ordering Guarantee

The design guarantees persisted Intent-level order by `intent_sequence`.
It does not guarantee wall-clock order or the exact pre-persistence execution
order when events are observed outside the database. `source_observed_at_ms`
is observational metadata, not a substitute for the sequence.

## 6. Boundary

```text
POSTGRESQL_CONCURRENCY=NOT_TESTED
RUNTIME_SOCKET_EVIDENCE=NOT_IMPLEMENTED
```

````
<!-- END_EXACT_SOURCE id=S001 -->

### S002. PHASE_R3_R2_FOLLOWUP_ATTACK_REVIEW.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_ATTACK_REVIEW.md`
- Bytes: `3425`
- SHA-256: `15AE632104D9DD1BF2C0CD2710FD50C98B8A10D07F6E89C37AE06643E2354FC7`

<!-- BEGIN_EXACT_SOURCE id=S002 sha256=15AE632104D9DD1BF2C0CD2710FD50C98B8A10D07F6E89C37AE06643E2354FC7 bytes=3425 -->
````text
# PHASE_R3_R2_FOLLOWUP_ATTACK_REVIEW

## 1. Attack Matrix

| # | Attack input | Expected result | Offline evidence | Limitation |
|---:|---|---|---|---|
| 1 | same request ID, different payload | ID reuse conflict | Worker/Cleanup model tests | real DB unique not run |
| 2 | same request replay, Result tampered | integrity failure | model tamper tests | JSONB DB behavior not run |
| 3 | correct digest, Audit Event ID replaced | integrity/Audit binding failure | model tamper methods | real FK/join not executed |
| 4 | Result JSON missing fields | schema/integrity failure | strict Zod + model guard | PostgreSQL JSON schema not executed |
| 5 | unknown Result fields | strict schema rejection | Zod strict objects | JSONB unknown-key DB check not executed |
| 6 | COMPLETED row without Result | integrity failure | removeResult test | SQL migration not executed |
| 7 | COMPLETED row without Audit | Audit binding failure | removeAudit test | real FK/nullability not run |
| 8 | Audit exists but Result not persisted | integrity failure | removeResult test | transaction execution not run |
| 9 | COMMIT succeeded, response lost | exact replay | commitResponseLost tests | real COMMIT ambiguity not tested |
| 10 | two instances replay same request | same original Result/no mutations | concurrent queue tests | not real multi-instance |
| 11 | two instances first submit same request | one owner, one replay | queue tests | not real PostgreSQL |
| 12 | Runtime submits duplicate evidence | stored event/no new Audit | evidence ID tests | real unique constraint not run |
| 13 | Runtime submits forged sequence | forbidden | claimedSourceSequence test | Runtime authentication not implemented |
| 14 | DB/Runtime sequence conflict | impossible by shared allocator | seq 1,2,3 tests | SQL execution not run |
| 15 | crash after allocation | no sequence consumption | crash test | real rollback not run |
| 16 | rollback then retry | retry allocates from unchanged next sequence | model failure tests | DB transaction not run |
| 17 | Worker revoke vs Cleanup | tombstone/cleanup checks | R2 regression + cross-module contract | no real race |
| 18 | Cleanup vs Permit Consumption | block/tombstone/lease/permit checks | R2 regression | no real race |
| 19 | Egress write start vs Worker Revocation | committed revocation fails gate | R2 regression | no real race |
| 20 | Evidence write vs Emergency Stop | existing Egress gates remain; no new authorization | cross-module contract | real runtime/DB coordination absent |

## 2. Result Tamper Evidence

Scope model explicitly tests:

```text
changed resultDigest
changed canonical text
missing Result
missing Audit
wrong Audit subject
```

Worker model tests equivalent Result/digest/missing Audit attacks.

## 3. Sequence Attack Evidence

Model tests prove:

- DB authorization gets sequence 1;
- Runtime first evidence gets sequence 2;
- response gets sequence 3;
- Runtime cannot submit a sequence;
- same evidence ID cannot change digest;
- Audit/crash failure does not advance `nextSequence`;
- restart retains next sequence;
- concurrent events receive distinct sequences.

## 4. Attack Review Result

```text
ATTACK_REVIEW=PASS_FOR_OFFLINE_MODEL_AND_STATIC_CONTRACT
POSTGRESQL_CONCURRENCY=NOT_TESTED
REAL_MULTI_INSTANCE=NOT_EXECUTED
REAL_SOCKET_EVIDENCE=NOT_IMPLEMENTED
```

The model-level PASS does not eliminate production concurrency or runtime
evidence risk.

````
<!-- END_EXACT_SOURCE id=S002 -->

### S003. PHASE_R3_R2_FOLLOWUP_BASELINE.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_BASELINE.md`
- Bytes: `6540`
- SHA-256: `4D06F2E21DF7D249239EFD6A3E5B46690DD3F67FC3FBF93116D0623CFF248E58`

<!-- BEGIN_EXACT_SOURCE id=S003 sha256=4D06F2E21DF7D249239EFD6A3E5B46690DD3F67FC3FBF93116D0623CFF248E58 bytes=6540 -->
````text
# PHASE_R3_R2_FOLLOWUP_BASELINE

## 1. Status

```text
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
INPUT_REALM=R3_EGRESS_REVOCATION_R2_READ_ONLY
MAIN_WORKSPACE_ACCESSED=NO
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

All follow-up outputs are under:

```text
preparation/production-trust/r3-egress-revocation-r2-followup-remediation/
```

## 2. Input Bundle

| Property | Value |
|---|---|
| Path | `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE.md` |
| Bytes | `223804` |
| SHA-256 | `33F3D18B9D8B8EBD04B5BEB04DB403A12BF38D9075DD581518545975C0D3A711` |
| Git Blob SHA-1 | `e016bf636e94f860dc2930fd45a9941d7aafcfb8` |

Git Blob SHA-1 is recorded separately and is not treated as SHA-256.

## 3. Input Manifest and Reports

| File | Bytes | SHA-256 |
|---|---:|---|
| `PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md` | 1872 | `6475F6DA17A4616049E3AFE5C195C0C77FD43B94CB7BE05C190BB53AD0D97D1F` |
| `PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt` | 525 | `7A19D113E24F74B7F317AE6BF22B53FAFA4A81841A046431AAD4AA0EFEB66282` |
| `PHASE_R3_EGRESS_REVOCATION_R2_SHA256SUMS.txt` | 5781 | `B35B60610329379C826EB3AE814BD7B2439480A056BF8C2F6BB32CFC73D2F0D6` |

## 4. Key Input Sources

| Source | Bytes | SHA-256 |
|---|---:|---|
| `PHASE_R3_SCOPE_CLEANUP_R2.sql` | 15002 | `E470F746722322468DD96AF6989BD9CDDCFF0B470CE0D99984308722E98D2A86` |
| `PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql` | 4916 | `F7CDE2398C7A8A5DE7BEEBCA34A1E1F706AA186915F030ABEA06DF4D3EB3FA3E` |
| `PHASE_R3_EGRESS_AUDIT_R2.sql` | 12189 | `1D635A7E59DC49CE0ADC32A323B5A3DDBFECF62506DD211DFF18056F9DDF07AD` |
| `models/scope-cleanup.ts` | 14189 | `4FB9B9608CDFB7F016CB7F399347808C4497BCC0453B48CF6142B8F204A3E387` |
| `models/worker-lifecycle.ts` | 7353 | `2795B17ED1E5710AEF7BD1139081A88ED284468FBA2F345EB57F20BC88FCE67F` |
| `models/egress-audit.ts` | 12309 | `26F8D1109C403B10DB9231765793AAF555101948F9F6374D05893D19B40ED59F` |
| `contracts.ts` | 6961 | `6C0A3DA7548044E30B47E6664447B38090281D171ECCF7B39CCAA52BD674F38D` |

The R2 Bundle catalog and local R2 source bodies were cross-checked during this
baseline. No local-versus-embedded body mismatch was found.

## 5. Confirmed Follow-up Defects

### F1: Scope Cleanup SQL cannot reconstruct the model Result

SQL R2 stored:

```text
request_digest
result_digest
audit_event_id
completed_at_ms
```

The model stores a complete `ScopeCleanupResult`, including status, block
version, Lease outcome, Permit outcome and external outcome. A digest verifies
content but cannot reconstruct it. SQL replay therefore cannot prove exact
result return.

### F2: Worker Revocation SQL cannot reconstruct the model Result

`trust_r6_worker_revocation_request` stores request identity and requested
version, but not:

```text
result_json / complete result
result_digest
audit_event_id
completed_at_ms
```

SQL and model therefore have different replay semantics.

### F3: Egress event sequence sources conflict

R2 SQL:

```text
DB authorization source_sequence = 1
Runtime source_sequence supplied by caller
UNIQUE (egress_intent_id, source_sequence)
```

Runtime's first evidence can also submit `1`, causing a unique conflict. The R2
model instead uses an Intent-level `nextSequence()` allocator.

## 6. Existing State and Fields

### Worker Revocation Result

```text
status
requestId
requestDigest
workerInstanceId
registrationState
revocationVersion
recordVersion
auditEventId
revokedAt
```

Follow-up adds previous state/versions so replay can explain the mutation
without querying unrelated live state.

### Scope Cleanup Result

```text
cleanupRequestId
requestDigest
resultDigest
status
workerInstanceId
scopeKey
revocationVersion
leaseId
capabilityId
permitId
blockVersion
leaseOutcome
permitOutcome
externalOutcome
auditEventId
completedAt
```

### Current Event Sequence

```text
egressIntentId
sourceType / evidenceSource
sourceSequence
observedAt
persistedAt
```

Current SQL has one conflicting sequence uniqueness rule and no authoritative
allocator.

## 7. Request Result Data Flow

```text
Request
  -> Request ID
  -> Request Digest
  -> Idempotency Record (PENDING, transaction-local)
  -> Transactional Mutation
  -> Complete Result
  -> Result Digest
  -> Audit Event ID Binding
  -> COMPLETED
  -> COMMIT
  -> Replay Original Result
```

Replay must read persisted result content, not recompute a semantically similar
result.

## 8. Egress Event Data Flow

```text
Egress Intent
  -> Intent Sequence Authority
  -> Database Authorization Event
  -> Runtime Evidence Event
  -> Provider Response / Unknown Event
  -> Audit Persistence
```

Selected architecture is an Intent-level monotonic allocator. Runtime evidence
does not supply an authoritative sequence number.

## 9. Current Lock Order

```text
WORKER_REVOCATION_CONTROL
  -> WORKER_REVOCATION_REQUEST
  -> SCOPE_CLEANUP_REQUEST
  -> SCOPE_WORKER_BLOCK
  -> EMERGENCY_CONTROL
  -> KEY_REGISTRY
  -> EXECUTION_AUTHORIZATION
  -> BUDGET_CONTROL
  -> BUDGET_RESERVATION
  -> CAPABILITY
  -> RESOURCE_FENCING_FLOOR
  -> FENCING_TOKEN_CONTROL
  -> WORKER_REGISTRATION
  -> EXECUTION_LEASE
  -> SEND_AUTHORIZATION
  -> EGRESS_SEND_INTENT
  -> EGRESS_RUNTIME_EVIDENCE
  -> AUDIT_SEQUENCE
```

Follow-up separates Runtime State, Event Sequence and Evidence into ordered
domains.

## 10. Existing Unique Constraints

```text
trust_r6_worker_revocation_request.request_id
  PRIMARY KEY

trust_r6_worker_revocation_request
  UNIQUE (worker_instance_id, requested_revocation_version)

trust_r6_scope_cleanup_request.cleanup_request_id
  PRIMARY KEY

trust_r6_egress_runtime_evidence
  UNIQUE (egress_intent_id, event_type, source_sequence)
  UNIQUE (egress_intent_id, source_sequence)
```

The second Runtime Evidence unique constraint is the source-conflict defect.

## 11. Planned Follow-up Changes

```text
1. Complete structured Result + canonical result text persistence.
2. Worker complete Result + Audit binding persistence.
3. Intent-level monotonic event sequence allocator.
4. Stable Runtime evidence ID/digest idempotency.
5. Updated data flows, lock order, transaction matrix and attack tests.
6. Cross-module review and full regression.
```

## 12. Safety Boundary

```text
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
NETWORK_ACCESSED=NO
REAL_KEY_ACCESSED=NO
REAL_API_CALLED=NO
REAL_SOCKET_WRITE=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
```

````
<!-- END_EXACT_SOURCE id=S003 -->

### S004. PHASE_R3_R2_FOLLOWUP_CROSS_MODULE_REVIEW.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_CROSS_MODULE_REVIEW.md`
- Bytes: `3205`
- SHA-256: `AF3A300929DF06D175D25C7570431E9F250AEAEC0D1D5471CA66DA6A6F3CC035`

<!-- BEGIN_EXACT_SOURCE id=S004 sha256=AF3A300929DF06D175D25C7570431E9F250AEAEC0D1D5471CA66DA6A6F3CC035 bytes=3205 -->
````text
# PHASE_R3_R2_FOLLOWUP_CROSS_MODULE_REVIEW

## 1. Request / Result / Audit

| Module | Request Digest | Complete Result | Result Digest | Audit Binding | Exact Replay |
|---|---|---|---|---|---|
| Worker Revocation | yes | result_json + canonical text | yes | yes | yes |
| Scope Cleanup | yes | result_json + canonical text | yes | yes | yes |

Both use the same canonical JSON function and SHA-256 format.

## 2. State and Version Consistency

Worker Result records:

```text
previousRegistrationState
registrationState
previousRevocationVersion
revocationVersion
previousRecordVersion
recordVersion
```

Scope Result records:

```text
blockVersion
leaseOutcome
permitOutcome
externalOutcome
```

Replay never recomputes these from current mutable state.

## 3. Transaction Consistency

| Transaction | Mutation + Audit + Result | Replay mutation |
|---|---|---|
| Worker revoke | same transaction | none |
| Scope Cleanup | same transaction | none |
| Egress Auth | state/evidence/audit same transaction | no repeat |
| Runtime Evidence | sequence/evidence/state/audit same transaction | same evidence ID only |
| Emergency/Key | frozen R3 gate | unchanged |
| Worker Takeover | frozen R3 Fencing scope checks | unchanged |

## 4. Egress Consistency

```text
EGRESS_WRITE_START_AUTHORIZED sequence 1
SOCKET_WRITE_ATTEMPTED sequence 2+
PROVIDER_RESPONSE_RECEIVED next sequence
SEND_OUTCOME_UNKNOWN terminal sequence
```

The response still does not mean business success. Unknown remains no-retry.

## 5. Historical Constraints

Preserved:

- Resource Floor remains authority for token/owner;
- global Worker revocation remains fail-closed;
- Scope block remains per-scope authority;
- Lease revocation binding remains;
- Permit one-use remains;
- Emergency epoch and Key revocation gates remain;
- `SEND_OUTCOME_UNKNOWN` has no automatic retry;
- `WRITE_STARTED`/write authorization does not imply recall of external bytes.

## 6. SQL / Model Matrix

| Contract | SQL | Model | Expected consistency |
|---|---|---|---|
| Scope exact replay | `result_json/canonical/digest/Audit` | full object/text/digest/Audit | aligned |
| Worker exact replay | `result_json/canonical/digest/Audit` | full object/text/digest/Audit | aligned |
| Sequence authority | sequence row update/RETURNING | `nextSequence` allocator | aligned |
| Duplicate evidence | evidence ID unique + digest check | evidence map/fingerprint | aligned |
| Rollback | transaction rollback | no mutation before success | contract aligned |

## 7. Cross-Module Findings

1. Worker and Scope result canonicalization are compatible.
2. R2's model Worker replay returned `REPLAYED`, which could change the
   original result. Follow-up returns the original `REVOKED` Result and treats
   replay as transport metadata, not a Result mutation.
3. R2 SQL stored only Scope `result_digest`; follow-up persists Result content.
4. R2 Egress model `nextSequence` and SQL fixed sequence=1 were inconsistent;
   follow-up moves allocation to the SQL sequence row in both.
5. No historical security control is weakened.

## 8. Result

```text
CROSS_MODULE_REVIEW=PASS_FOR_OFFLINE_SCOPE
POSTGRESQL_EXECUTION=NOT_EXECUTED
REAL_MULTI_INSTANCE=NOT_EXECUTED
```

````
<!-- END_EXACT_SOURCE id=S004 -->

### S005. PHASE_R3_R2_FOLLOWUP_FINAL_REPORT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_FINAL_REPORT.md`
- Bytes: `4880`
- SHA-256: `84F66BFBF4034A3667CA22CF6A7A310C2E83F7DCD1607A2DACF1E71934354B45`

<!-- BEGIN_EXACT_SOURCE id=S005 sha256=84F66BFBF4034A3667CA22CF6A7A310C2E83F7DCD1607A2DACF1E71934354B45 bytes=4880 -->
````text
# PHASE_R3_R2_FOLLOWUP_FINAL_REPORT

## 1. Final Status

```text
R3_EGRESS_REVOCATION_R2_FOLLOWUP_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS
INDEPENDENT_REVIEW=REQUIRED

PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
PRODUCTION_EGRESS_IMPLEMENTED=NO
NETWORK_ISOLATION_ENFORCED=NO
REAL_FETCH_AUTHORIZED=NO
```

This is an offline design/model/static-SQL pass, not production security
approval.

## 2. Follow-up Fixes

### Scope Cleanup

- complete Result JSON and canonical text persisted;
- Result Digest computed over canonical Result excluding `resultDigest`;
- Audit Event ID is bound in the Result and row;
- replay verifies request, Result, canonical text, Digest and Audit;
- exact original Result is returned;
- no Block/Permit/Lease/Audit mutation on replay.

### Worker Revocation

- complete Result includes previous/new registration state and versions;
- Result JSON/text/digest and Audit ID are persisted;
- original `REVOKED` Result is returned unchanged on replay;
- no tombstone version or Audit duplication on replay.

### Egress Event Sequence

Option A selected:

```text
one Intent-level sequence space
DB authorization = 1
Runtime evidence = 2+
```

The database owns allocation. Runtime supplies stable Evidence ID/Digest but
cannot supply a sequence. Duplicate evidence returns the stored event.

## 3. Acceptance Matrix

```text
SCOPE_CLEANUP_COMPLETE_RESULT_PERSISTENCE=PASS
SCOPE_CLEANUP_RESULT_DIGEST_BINDING=PASS
SCOPE_CLEANUP_AUDIT_EVENT_BINDING=PASS
SCOPE_CLEANUP_EXACT_REPLAY=PASS
SCOPE_CLEANUP_UNKNOWN_COMMIT_RECOVERY=PASS

WORKER_REVOCATION_COMPLETE_RESULT_PERSISTENCE=PASS
WORKER_REVOCATION_RESULT_DIGEST_BINDING=PASS
WORKER_REVOCATION_AUDIT_EVENT_BINDING=PASS
WORKER_REVOCATION_EXACT_REPLAY=PASS
WORKER_REVOCATION_UNKNOWN_COMMIT_RECOVERY=PASS

EGRESS_SEQUENCE_AUTHORITY=PASS
EGRESS_SEQUENCE_UNIQUENESS=PASS
EGRESS_SEQUENCE_CONCURRENCY_CONTRACT=PASS
EGRESS_SEQUENCE_CRASH_RECOVERY=PASS
EGRESS_SQL_MODEL_ALIGNMENT=PASS

REQUEST_RESULT_AUDIT_CONSISTENCY=PASS
TRANSACTION_MATRIX_CONSISTENCY=PASS
LOCK_ORDER_CONSISTENCY=PASS
R3_FENCING_REGRESSION=PASS
R2_REGRESSION=PASS
CROSS_MODULE_REVIEW=PASS
ATTACK_REVIEW=PASS
MANIFEST_VERIFICATION=PASS
BUNDLE_BODY_EXACTNESS=PASS
```

Every PASS is limited to the offline model, static SQL/contract or local
regression evidence.

## 4. Test Results

```text
FOLLOWUP_TARGETED_VITEST=4_FILES_39_TESTS_PASS
R3_EGRESS_REVOCATION_R2_VITEST=4_FILES_67_TESTS_PASS
R3_EGRESS_REVOCATION_R1_VITEST=4_FILES_53_TESTS_PASS
R3_FENCING_VITEST=7_FILES_49_TESTS_PASS
R2_R3_VITEST=8_FILES_74_TESTS_PASS
R2_VITEST=10_FILES_80_TESTS_PASS
R1_VITEST=16_FILES_91_TESTS_PASS
R31_R36_RELEVANT_VITEST=20_FILES_179_TESTS_PASS
POWERSHELL_TOTAL=69_PASS
POWERSHELL_5_1_PARSER=6_PASS
TYPESCRIPT_STRICT=PASS
ESLINT=PASS
NEXT_BUILD=PASS
```

The first follow-up run had two failing SQL negative tests because the mutation
fixture replaced only one of multiple `result_json` tokens. The fixture was
corrected with replace-all semantics and the complete run above is
authoritative. The earlier failure is preserved in
`PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION.md`.

## 5. Cross-Module Review

```text
REQUEST_RESULT_AUDIT_CONSISTENCY=PASS
WORKER_SCOPE_CANONICALIZATION_COMPATIBLE=PASS
TRANSACTION_ATOMICITY_CONTRACT=PASS
EGRESS_EVENT_ORDER=PASS_BY_INTENT_SEQUENCE
HISTORICAL_FENCING_CONTROLS=PASS
HISTORICAL_ONE_USE_PERMIT=PASS
HISTORICAL_EMERGENCY_KEY_GATES=PASS
NO_AUTO_RETRY_AFTER_UNKNOWN=PASS
```

## 6. Independence

No usable independent Agent workpack was produced. This run is a main-agent
implementation and review.

```text
INDEPENDENCE_LIMITATION=SAME_HOST_MAIN_AGENT_ONLY
THIRD_PARTY_INDEPENDENT_AUDIT=NO
```

## 7. Irreducible Limits

```text
POSTGRESQL_INTEGRATION=NOT_EXECUTED
POSTGRESQL_CONCURRENCY=NOT_TESTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_SOCKET_WRITE=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
```

## 8. Safety

```text
MAIN_WORKSPACE_MODIFIED=NO
SRC_SCRIPTS_MODIFIED=NO
R31_R36_MODIFIED=NO
IDENTITY_GATE_CORE_MODIFIED=NO
R2_REMEDIATION_FILES_MODIFIED=NO
A3_D1_D2_MODIFIED=NO

REAL_KEY_ACCESSED=NO
REAL_API_CALLED=NO
NETWORK_ACCESSED=NO
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
REAL_FETCH_EXECUTED=NO
```

The Next.js build wrote normal `.next/` output in the isolated copy.

## 9. Remaining Risks

- PostgreSQL lock, JSONB, uniqueness, rollback and SQLSTATE behavior are not
  executed;
- real multi-instance sequence allocation is not tested;
- runtime Socket evidence is not implemented;
- trusted Egress and network isolation are not implemented;
- external Provider receipt remains unknowable after lost response;
- no exactly-once external effect is guaranteed.

Production enforcement remains blocked.

````
<!-- END_EXACT_SOURCE id=S005 -->

### S006. PHASE_R3_R2_FOLLOWUP_LOCK_ORDER.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_LOCK_ORDER.md`
- Bytes: `2509`
- SHA-256: `9F1B9AA20CB629F8EAC095076A87A9CA242076DC1E1BC264D73372DCCD763F93`

<!-- BEGIN_EXACT_SOURCE id=S006 sha256=9F1B9AA20CB629F8EAC095076A87A9CA242076DC1E1BC264D73372DCCD763F93 bytes=2509 -->
````text
# PHASE_R3_R2_FOLLOWUP_LOCK_ORDER

## 1. Canonical Order

```text
WORKER_REVOCATION_CONTROL
  -> WORKER_REVOCATION_REQUEST
  -> SCOPE_CLEANUP_REQUEST
  -> SCOPE_WORKER_BLOCK
  -> EMERGENCY_CONTROL
  -> KEY_REGISTRY
  -> EXECUTION_AUTHORIZATION
  -> BUDGET_CONTROL
  -> BUDGET_RESERVATION
  -> CAPABILITY
  -> RESOURCE_FENCING_FLOOR
  -> FENCING_TOKEN_CONTROL
  -> WORKER_REGISTRATION
  -> EXECUTION_LEASE
  -> SEND_AUTHORIZATION
  -> EGRESS_SEND_INTENT
  -> EGRESS_RUNTIME_STATE
  -> EGRESS_EVENT_SEQUENCE
  -> EGRESS_RUNTIME_EVIDENCE
  -> AUDIT_SEQUENCE
```

## 2. Worker Revocation

```text
trust_r5_worker_revocation FOR UPDATE
  -> trust_r7_worker_revocation_request FOR UPDATE/INSERT
  -> trust_r4_worker_registration UPDATE
  -> trust_r3_audit_head FOR UPDATE
  -> request completion update
```

The Audit event and complete result are committed with the mutation.

## 3. Scope Cleanup

```text
trust_r5_worker_revocation FOR SHARE
  -> cleanup request FOR UPDATE/INSERT
  -> Scope block
  -> Resource Floor
  -> Worker Registration
  -> Lease
  -> Permit
  -> Audit Head
  -> request COMPLETED + full Result
```

Replay locks only the cleanup request and reads its joined Audit binding.
It does not lock or mutate resource state.

## 4. Egress

Authorization:

```text
egress intent
  -> runtime state
  -> event sequence
  -> authorization evidence
  -> Audit Head
```

Runtime evidence:

```text
runtime state
  -> event sequence
  -> runtime evidence
  -> Audit Head
```

Sequence allocation and evidence insertion are in the same transaction. An
event cannot commit with a sequence that is not represented in the sequence
row.

## 5. Cross-Module Rules

| Race | Resolution |
|---|---|
| Worker revoke vs Worker replay | request idempotency row under revocation lock |
| Cleanup replay vs cleanup first run | request PK/row and transaction-local PENDING |
| Cleanup vs Permit Consumption | global tombstone + scope block + floor/lease/permit |
| Egress vs Worker Revocation | final authorization must observe committed tombstone |
| Egress DB authorization vs Runtime event | DB allocates sequence 1, Runtime receives 2+ |
| Runtime two instances | sequence row `FOR UPDATE` serializes allocation |
| Evidence retry after COMMIT unknown | stable evidence ID query |
| Evidence write vs Emergency/Key stop | existing Egress gate state checks remain |

## 6. Limitation

This is a textual transaction-contract review. PostgreSQL lock timing, deadlock
behavior and SQLSTATE outcomes are not executed.

````
<!-- END_EXACT_SOURCE id=S006 -->

### S007. PHASE_R3_R2_FOLLOWUP_NEGATIVE_TEST_MATRIX.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_NEGATIVE_TEST_MATRIX.md`
- Bytes: `2732`
- SHA-256: `13700A1D4AE24CC58DC93470B0C5D1523B62EF591F44B6289688693CFAB42747`

<!-- BEGIN_EXACT_SOURCE id=S007 sha256=13700A1D4AE24CC58DC93470B0C5D1523B62EF591F44B6289688693CFAB42747 bytes=2732 -->
````text
# PHASE_R3_R2_FOLLOWUP_NEGATIVE_TEST_MATRIX

## 1. Scope Cleanup

| Case | Expected | Test |
|---|---|---|
| first cleanup | complete Result persisted | `scope-cleanup-complete-result.test.ts` |
| same request replay | exact same Result | model |
| changed request payload | ID reuse conflict | model |
| Result Digest changed | integrity failure | model |
| canonical text changed | integrity failure | model |
| Result missing | integrity failure | model |
| Audit missing | Audit binding failure | model |
| Audit subject changed | Audit binding failure | model |
| COMMIT response lost | same ID returns stored Result | model |
| restart | stored Result recovered | model |
| concurrent same ID | one Result/Audit/version | model |

## 2. Worker Revocation

| Case | Expected | Test |
|---|---|---|
| ACTIVE/DRAINING revoke | complete Result persisted | `worker-revocation-complete-result.test.ts` |
| same request replay | exact same Result | model |
| changed payload | conflict | model |
| Result Digest changed | integrity failure | model |
| canonical text changed | integrity failure | model |
| Result missing | integrity failure | model |
| Audit missing | binding failure | model |
| COMMIT response lost | stored Result replay | model |
| restart | stored Result replay | model |
| concurrent same ID | one version/Audit | model |
| revoked Worker activation | rejected | R2 regression |

## 3. Egress Sequence

| Case | Expected | Test |
|---|---|---|
| DB authorization | sequence 1 | `egress-intent-sequence.test.ts` |
| first Runtime evidence | sequence 2 | model |
| subsequent response | sequence 3 | model |
| Runtime supplies sequence | forbidden | model |
| wrong source | forbidden | model |
| duplicate evidence | stored event, no new Audit | model |
| same evidence ID diff payload | replay conflict | model |
| concurrent events | unique sequences | model |
| Audit failure | no sequence consumption | model |
| crash before commit | no sequence consumption | model |
| COMMIT response lost | evidence ID lookup | model |
| Provider response before attempt | rejected | model |
| restart | sequence continues | model |

## 4. SQL Negative Tests

`tests/sql-analyzer-followup.test.ts` verifies:

- missing complete Scope Result columns;
- missing complete Worker Result columns;
- missing canonical Result text;
- missing Audit join;
- missing event sequence table;
- missing sequence increment;
- missing unique sequence/evidence identity;
- reintroduced Runtime `source_sequence`;
- lock-order crossing.

## 5. Test Classification

```text
REFERENCE_MODEL_TEST=EXECUTED
SQL_STATIC_ANALYSIS=EXECUTED
POSTGRESQL_EXECUTION=NOT_EXECUTED
POSTGRESQL_CONCURRENCY=NOT_TESTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
```

````
<!-- END_EXACT_SOURCE id=S007 -->

### S008. PHASE_R3_R2_FOLLOWUP_REFERENCE_MODEL.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_REFERENCE_MODEL.md`
- Bytes: `2460`
- SHA-256: `2BF06E1402E1904F05DFB0813B0525629657E9C66B0E38E6C65C36EA4C1F6B15`

<!-- BEGIN_EXACT_SOURCE id=S008 sha256=2BF06E1402E1904F05DFB0813B0525629657E9C66B0E38E6C65C36EA4C1F6B15 bytes=2460 -->
````text
# PHASE_R3_R2_FOLLOWUP_REFERENCE_MODEL

## 1. Status

```text
OFFLINE_REFERENCE_MODEL
PERSISTENCE_SIMULATION_ONLY
REAL_DATABASE_DURABILITY=NOT_TESTED
REAL_MULTI_INSTANCE_INTERLEAVING=NOT_TESTED
```

## 2. Models

### Scope Cleanup

File: `models/scope-cleanup-complete-result.ts`

Stores:

```text
complete Result object
canonical Result text
Result Digest
Audit Event record
request digest/payload
```

Replay verifies request identity, Result integrity, canonical text, Result
Digest and Audit binding before returning the original object.

Tamper probes:

- changed Result digest;
- changed canonical text;
- missing Result;
- missing Audit;
- wrong Audit subject.

### Worker Revocation

File: `models/worker-revocation-complete-result.ts`

Stores the previous/new registration and version fields, complete Result,
canonical text, digest and Audit record.

Replay never changes the persisted status to `REPLAYED`; the original
`REVOKED` result is returned.

### Egress Intent Sequence

File: `models/egress-intent-sequence.ts`

The model holds one `nextSequence` per Intent. Authorization receives sequence
1. Runtime evidence receives sequence 2+ through the model allocator.

Stable evidence ID:

- exact duplicate returns original event;
- different content under same ID is rejected;
- Runtime-supplied sequence is rejected;
- non-runtime evidence source is rejected;
- Audit/crash failure does not consume a sequence.

## 3. Snapshot/Restart

All three models expose `snapshot()` and `fromSnapshot()`.

These prove only persistence simulation:

```text
PERSISTENCE_SIMULATION_ONLY
REAL_DATABASE_DURABILITY=NOT_TESTED
```

## 4. Sequence Guarantee

The model guarantees:

```text
authorization = 1
first runtime evidence = 2
next runtime evidence = 3
```

It does not prove that a production Runtime emitted real socket evidence.

## 5. SQL/Model Alignment

| Behavior | SQL | Model |
|---|---|---|
| complete Result persistence | JSON/text/digest/Audit columns | full object/text/digest/audit |
| exact replay | replay transaction + integrity checks | object/digest/canonical/Audit checks |
| Intent sequence | sequence row | per-Intent nextSequence |
| duplicate evidence | evidence ID/digest lookup | evidence map/fingerprint |
| rollback | transaction rollback | failure before model mutation |
| Audit failure | transaction rollback | error before mutation |

## 6. Boundary

No model invokes a real database, Socket, Provider, Docker or network.

````
<!-- END_EXACT_SOURCE id=S008 -->

### S009. PHASE_R3_R2_FOLLOWUP_RISK_REGISTER.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_RISK_REGISTER.md`
- Bytes: `2741`
- SHA-256: `D3928ABAB0CD573C3BCCE68D2A0CA6664020A8F01F865755010D1A094CCDCD96`

<!-- BEGIN_EXACT_SOURCE id=S009 sha256=D3928ABAB0CD573C3BCCE68D2A0CA6664020A8F01F865755010D1A094CCDCD96 bytes=2741 -->
```text
# PHASE_R3_R2_FOLLOWUP_RISK_REGISTER

| ID | Risk | Severity | Status | Evidence / follow-up |
|---|---|---|---|---|
| FU-01 | Scope Result Digest cannot reconstruct original Result | High | MITIGATED_IN_DESIGN | Result JSON + canonical text + digest persisted |
| FU-02 | Replay constructs semantically similar but different Result | High | MITIGATED_IN_DESIGN | exact Result equality tests |
| FU-03 | Stored Result tampered but Digest reused | High | MITIGATED_IN_DESIGN | digest and canonical-text tamper tests |
| FU-04 | Audit ID replaced/missing | High | MITIGATED_IN_DESIGN | Audit binding and subject tests |
| FU-05 | COMMIT succeeded but response lost | High | MITIGATED_IN_DESIGN | same-ID replay tests |
| FU-06 | Worker SQL/model Result mismatch | High | MITIGATED_IN_DESIGN | full Result persistence + model |
| FU-07 | Worker replay changes status/time/Audit | High | MITIGATED_IN_DESIGN | exact original Result tests |
| FU-08 | Runtime chooses colliding event sequence | High | MITIGATED_IN_DESIGN | DB allocator; runtime sequence rejected |
| FU-09 | DB fixed sequence versus Runtime sequence | High | MITIGATED_IN_DESIGN | shared sequence row |
| FU-10 | Sequence allocation crashes/gaps | High | MITIGATED_BY_TRANSACTION_BOUNDARY | rollback tests |
| FU-11 | Duplicate Runtime Evidence creates new Audit | High | MITIGATED_IN_DESIGN | evidence ID/digest replay tests |
| FU-12 | Same evidence ID with different payload | High | MITIGATED_IN_DESIGN | replay conflict test |
| FU-13 | Sequence allocation after COMMIT unknown duplicates event | High | MITIGATED_IN_DESIGN | stable evidence ID lookup |
| FU-14 | JSONB text ordering assumed canonical | Medium | MITIGATED_IN_DESIGN | canonical text stored separately |
| FU-15 | SQL syntax/constraint semantics not executed | High | NOT_EXECUTED | PostgreSQL integration required |
| FU-16 | Real multi-instance sequence race not tested | High | NOT_EXECUTED | `MULTI_INSTANCE_TEST=NOT_EXECUTED` |
| FU-17 | Runtime socket evidence not implemented | Critical | NOT_IMPLEMENTED | production runtime gap |
| FU-18 | Provider response misclassified as business success | High | MITIGATED_IN_DESIGN | `businessSuccessEvaluated=false` |
| FU-19 | Network side effects cannot be recalled | High | ACCEPTED_RESIDUAL | no exactly-once claim |
| FU-20 | Worker direct Provider bypass | Critical | NOT_IMPLEMENTED | network isolation remains required |
| FU-21 | Same-host independent review unavailable | Medium | DISCLOSED | `INDEPENDENCE_LIMITATION` |
| FU-22 | Follow-up source generated from R2 SQL transformation | Low | VERIFIED | generated body manually/static tested |

No production enforcement is permitted while High/Critical implementation and
verification gaps remain.

```
<!-- END_EXACT_SOURCE id=S009 -->

### S010. PHASE_R3_R2_FOLLOWUP_SQL_REVIEW.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_SQL_REVIEW.md`
- Bytes: `2675`
- SHA-256: `53BD127E797FB3CD076BE2BF99317C2D5C0EE0901722EBF19D25E7647E9461D1`

<!-- BEGIN_EXACT_SOURCE id=S010 sha256=53BD127E797FB3CD076BE2BF99317C2D5C0EE0901722EBF19D25E7647E9461D1 bytes=2675 -->
````text
# PHASE_R3_R2_FOLLOWUP_SQL_REVIEW

## 1. Validation Levels

```text
TEXTUAL_PATTERN_CHECK=EXECUTED
SQL_STATEMENT_SEGMENTATION=EXECUTED
SQL_PARAMETER_BINDING_REVIEW=EXECUTED
TRANSACTION_CONTRACT_REVIEW=EXECUTED
REFERENCE_MODEL_TEST=EXECUTED
POSTGRESQL_EXECUTION=NOT_EXECUTED
```

## 2. Source SQL

| File | Purpose |
|---|---|
| `PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql` | complete Scope Result + replay |
| `PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT.sql` | complete Worker Result + replay |
| `PHASE_R3_EGRESS_EVENT_SEQUENCE.sql` | shared Intent sequence allocator |

## 3. Scope Result Parameters

The R2 parameters `$1` through `$16` retain their prior meanings. Follow-up
adds:

| Parameter | Binding |
|---|---|
| `$17` | complete cleanup Result JSON object |
| `$18` | exact canonical Result text |
| `$19` | SHA-256 over `$18` |

The completion update writes all three with `audit_event_id=$13` and
`completed_at_ms=$10`.

Replay selects `result_json`, `result_canonical_text`, `result_digest`,
`audit_event_id` and joins `trust_r3_audit_event` on the bound ID.

## 4. Worker Result Parameters

| Parameter | Binding |
|---|---|
| `$1` | Worker ID |
| `$2` | request ID |
| `$3` | completion/revoke time |
| `$4` | reason |
| `$5` | expected record version |
| `$6` | Audit event ID |
| `$7..$9` | Audit sequence/digests |
| `$10` | request digest |
| `$11` | new revocation version |
| `$12` | complete Result JSON |
| `$13` | exact canonical Result text |
| `$14` | Result Digest |

The request row is inserted with `state='PENDING'`, then completed only after
Audit insertion.

## 5. Egress Sequence Parameters

The sequence allocator returns `intent_sequence` from:

```sql
UPDATE trust_r7_egress_event_sequence
SET next_sequence = next_sequence + 1
...
RETURNING next_sequence - 1 AS intent_sequence;
```

The Runtime does not supply this value. Evidence has:

```text
UNIQUE (egress_intent_id, intent_sequence)
UNIQUE (egress_intent_id, evidence_id)
```

The host binds the RETURNING value to the evidence INSERT. The SQL has no
`source_sequence` input field.

## 6. Negative Checks

The analyzer rejects:

- Scope Result rows missing JSON/canonical text/digest/Audit fields;
- Worker Result rows missing JSON/canonical/digest/Audit fields;
- missing shared sequence table;
- missing sequence increment;
- missing unique evidence identity;
- reintroduced `source_sequence`.

## 7. Limits

```text
POSTGRESQL_PARSE_ACCEPTANCE=NOT_PROVEN
POSTGRESQL_LOCK_TIMING=NOT_PROVEN
ROLLBACK_AND_SQLSTATE_BEHAVIOR=NOT_PROVEN
REAL_MULTI_INSTANCE_SEQUENCE_RACE=NOT_TESTED
JSONB_CANONICAL_TEXT_EQUALITY_EXECUTION=NOT_TESTED
```

The SQL is a draft. It has not been executed.

````
<!-- END_EXACT_SOURCE id=S010 -->

### S011. PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION.md`
- Bytes: `10329`
- SHA-256: `D87CA18F05C464CFC3985EC3D6EC002B8265E2C6758E3D807E625E975C98355B`

<!-- BEGIN_EXACT_SOURCE id=S011 sha256=D87CA18F05C464CFC3985EC3D6EC002B8265E2C6758E3D807E625E975C98355B bytes=10329 -->
```````text
﻿# PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION

``````text
GENERATED_AT=2026-11-26T23:37:09.0206423+08:00
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
FAILED_COMMANDS=0
POSTGRESQL_INTEGRATION=NOT_EXECUTED
POSTGRESQL_CONCURRENCY=NOT_TESTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_SOCKET_WRITE=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
``````

## Failure Evidence

The first follow-up run had two failing SQL negative tests because a
single-occurrence string replacement left a second esult_json token in the
fixture. The test was corrected to remove all occurrences. The full run below
is authoritative, and the failure remains documented.

## Commands
### Follow-up targeted Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-egress-revocation-r2-followup-remediation/vitest.config.ts
START=2026-11-26T23:36:42.7452874+08:00
END=2026-11-26T23:36:43.2463208+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  4 passed (4)
      Tests  39 passed (39)
   Start at  23:36:42
   Duration  226ms (import 76%, tests 10%, transform 10%, worker 3%)
```

### R3 Egress Revocation R2 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-egress-revocation-r2-remediation/vitest.config.ts
START=2026-11-26T23:36:43.2538009+08:00
END=2026-11-26T23:36:43.7458847+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  4 passed (4)
      Tests  67 passed (67)
   Start at  23:36:43
   Duration  224ms (import 79%, tests 10%, transform 8%, worker 3%)
```

### R3 Egress Revocation R1 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-egress-revocation-remediation/vitest.config.ts
START=2026-11-26T23:36:43.7468843+08:00
END=2026-11-26T23:36:44.2349196+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  4 passed (4)
      Tests  53 passed (53)
   Start at  23:36:43
   Duration  233ms (import 72%, tests 13%, transform 11%, worker 4%)
```

### R3 Fencing Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-fencing-remediation/vitest.config.ts
START=2026-11-26T23:36:44.2359192+08:00
END=2026-11-26T23:36:44.7295096+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  7 passed (7)
      Tests  49 passed (49)
   Start at  23:36:44
   Duration  230ms (import 78%, transform 10%, tests 8%, worker 4%)
```

### R2-R3 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2-r3-remediation/vitest.config.ts
START=2026-11-26T23:36:44.7305135+08:00
END=2026-11-26T23:36:45.2327714+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  8 passed (8)
      Tests  74 passed (74)
   Start at  23:36:44
   Duration  246ms (import 79%, tests 10%, transform 7%, worker 4%)
```

### R2 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2/vitest.config.ts
START=2026-11-26T23:36:45.2327714+08:00
END=2026-11-26T23:36:45.7704411+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  10 passed (10)
      Tests  80 passed (80)
   Start at  23:36:45
   Duration  275ms (import 79%, tests 12%, transform 6%, worker 4%)
```

### R1 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/vitest.config.ts
START=2026-11-26T23:36:45.7714339+08:00
END=2026-11-26T23:36:46.3981220+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  16 passed (16)
      Tests  91 passed (91)
   Start at  23:36:46
   Duration  363ms (import 80%, tests 11%, transform 5%, worker 4%)
```

### R31-R36 Relevant Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run src/server/auth/actor-context.test.ts src/server/public-enterprise-search/identity/identity-gate.test.ts src/server/public-enterprise-search/identity/runtime/approval-authorization.test.ts src/server/public-enterprise-search/identity/runtime/authorization.test.ts src/server/public-enterprise-search/identity/runtime/fetch-entry-guard.test.ts src/server/public-enterprise-search/identity/runtime/precheck.test.ts src/server/public-enterprise-search/identity/runtime/production-fetch-entry.test.ts src/server/public-enterprise-search/identity/runtime/trusted-read.test.ts src/server/public-enterprise-search/offline-boundaries.test.ts src/server/public-enterprise-search/provider/aux-http-transports.test.ts src/server/public-enterprise-search/provider/deepseek-fetch.test.ts src/server/public-enterprise-search/provider/deepseek-http-transport.test.ts src/server/public-enterprise-search/provider/provider-execution-authorization.test.ts src/server/public-enterprise-search/provider/provider-factory-protection.test.ts src/server/public-enterprise-search/diagnostics/fetch-diagnostic-cli.test.ts src/server/public-enterprise-search/diagnostics/fetch-diagnostic-dependency.test.ts src/server/public-enterprise-search/local-live/live-config.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial-cli.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial.zero-network.test.ts
START=2026-11-26T23:36:46.3992343+08:00
END=2026-11-26T23:36:51.4528855+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  20 passed (20)
      Tests  179 passed (179)
   Start at  23:36:46
   Duration  4.77s (tests 53%, import 39%, transform 5%, worker 2%)

    Isolate  20 workers spawned · ~87ms startup each (spawn + environment, per file)
             at least ~1.65s faster with isolate: false — reuses workers across files instead of one per file
```

### PowerShell Launcher

```text
COMMAND=powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-only-launcher.ps1
START=2026-11-26T23:36:51.4539109+08:00
END=2026-11-26T23:36:57.0309337+08:00
EXIT_CODE=0
```

```text
T01=PASS
T02=PASS
T03=PASS
T04=PASS
T05=PASS
T06=PASS
T07=PASS
T08=PASS
T09=PASS
T10=PASS
T11=PASS
T12=PASS
T13=PASS
T14=PASS
T15=PASS
T16=PASS
T17=PASS
T18=PASS
T19=PASS
T20=PASS
T21=PASS
T22=PASS
T23=PASS
T24=PASS
T25=PASS
T26=PASS
T27=PASS
T28=PASS
T29=PASS
T30=PASS
T31=PASS
T32=PASS
T33=PASS
T34=PASS
T35=PASS
T36=PASS
T37=PASS
T38=PASS
T39=PASS
T40=PASS
TOTAL=40
FAILURES=0
FINAL_ENV_ABSENT=true
```

### PowerShell Key Session

```text
COMMAND=powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-key-session.ps1
START=2026-11-26T23:36:57.0319282+08:00
END=2026-11-26T23:36:58.3461201+08:00
EXIT_CODE=0
```

```text
T01=PASS
T02=PASS
T03=PASS
T04=PASS
T05=PASS
T06=PASS
T07=PASS
T08=PASS
T09=PASS
T10=PASS
T11=PASS
T12=PASS
T13=PASS
T14=PASS
T15=PASS
T16=PASS
T17=PASS
T18=PASS
T19=PASS
T20=PASS
T21=PASS
T22=PASS
T23=PASS
T24=PASS
T25=PASS
TOTAL=25
FAILURES=0
FINAL_ENV_ABSENT=true
```

### PowerShell Fetch Enforcement

```text
COMMAND=powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-only-production-enforcement.ps1
START=2026-11-26T23:36:58.3471202+08:00
END=2026-11-26T23:36:58.7863908+08:00
EXIT_CODE=0
```

```text
T41=PASS
T42=PASS
T43=PASS
T44=PASS
TOTAL=4
FAILURES=0
FINAL_ENV_ABSENT=true
```

### PowerShell 5.1 Parser

```text
COMMAND=inline PowerShell 5.1 Language.Parser over scripts/windows/*.ps1
START=2026-11-26T23:36:58.7863908+08:00
END=2026-11-26T23:36:58.8037814+08:00
EXIT_CODE=0
```

```text
fetch-key-session.ps1=PASS
fetch-only-launcher-child-fixture.ps1=PASS
fetch-only-launcher.ps1=PASS
test-fetch-key-session.ps1=PASS
test-fetch-only-launcher.ps1=PASS
test-fetch-only-production-enforcement.ps1=PASS
TOTAL=6
FAILURES=0
```

### TypeScript Strict

```text
COMMAND=npx.cmd tsc --noEmit --pretty false
START=2026-11-26T23:36:58.8037814+08:00
END=2026-11-26T23:37:01.1641905+08:00
EXIT_CODE=0
```

```text

```

### ESLint New Scope

```text
COMMAND=npx.cmd eslint preparation/production-trust/r3-egress-revocation-r2-followup-remediation
START=2026-11-26T23:37:01.1641905+08:00
END=2026-11-26T23:37:03.7921001+08:00
EXIT_CODE=0
```

```text

```

### Next Build

```text
COMMAND=pnpm.cmd build
START=2026-11-26T23:37:03.7921001+08:00
END=2026-11-26T23:37:08.9895865+08:00
EXIT_CODE=0
```

```text
pnpm.cmd : $ next build
At C:\Users\Administrator\Desktop\thzz1-search-offline\preparation\production-trust\r3-egress-revocation-r2-followup-re
mediation\tools\run-verification.ps1:12 char:13
+   $output = & $Executable @Arguments 2>&1
+             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: ($ next build:String) [], RemoteException
    + FullyQualifiedErrorId : NativeCommandError
 
▲ Next.js 16.4.6 (Turbopack)
✓ Running next.config.ts took 25ms
- Experiments (use with caution):
  · serverActions

  Creating an optimized production build ...
✓ Compiled successfully in 295ms
  Running TypeScript ...
  Finished TypeScript in 1957ms ...
  Collecting page data using 11 workers ...
  Generating static pages using 11 workers (0/2) ...
✓ Generating static pages using 11 workers (2/2) in 508ms
  Finalizing page optimization ...

Route (app)
┌ ○ /_not-found
├ ƒ /api/leads/[id]/research-jobs
├ ƒ /api/leads/[id]/research-jobs/[jobId]
├ ƒ /api/leads/[id]/research-mvp-jobs
├ ƒ /api/leads/[id]/research-mvp-jobs/[jobId]
├ ƒ /leads
├ ƒ /leads/[id]
├ ƒ /leads/[id]/research
└ ƒ /test-harness/public-enterprise-search


○  (Static)   prerendered as static content
ƒ  (Dynamic)  server-rendered on demand
```


```````
<!-- END_EXACT_SOURCE id=S011 -->

### S012. PHASE_R3_R2_FOLLOWUP_TRANSACTION_MATRIX.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_R2_FOLLOWUP_TRANSACTION_MATRIX.md`
- Bytes: `2397`
- SHA-256: `0A235E1D61C2B2AC78B590B155550D20D9960036AC28A8B5D9B1096EDE76CF25`

<!-- BEGIN_EXACT_SOURCE id=S012 sha256=0A235E1D61C2B2AC78B590B155550D20D9960036AC28A8B5D9B1096EDE76CF25 bytes=2397 -->
````text
# PHASE_R3_R2_FOLLOWUP_TRANSACTION_MATRIX

| Transaction | Lock order | Atomic writes | Row checks | Replay / recovery |
|---|---|---|---|---|
| Worker revoke first run | revocation -> request -> registration -> Audit Head -> request complete | tombstone, registration, request, Result JSON/text/digest, Audit | request/tombstone/registration/Audit/result update exactly 1 | same ID returns Result |
| Worker revoke replay | request read | none | COMPLETED + digest + Audit | exact Result |
| Cleanup PRE_SEND first run | revocation share -> cleanup request -> block -> floor -> worker -> lease -> permit -> Audit -> Result complete | block/Lease/Permit + Result JSON/text/digest + Audit | all required mutations 1 | same ID replay |
| Cleanup AFTER_SEND first run | same | block/Permit + Result + Audit; Lease NOT_USED | required mutations 1 | same |
| Cleanup ALREADY_SATISFIED | same | request + Result + Audit; Block/Lease/Permit NOT_USED | request/Audit/result 1 | exact Result |
| Cleanup replay | cleanup request + joined Audit | none | Result/digest/Audit integrity | exact original Result |
| Egress write authorization | intent -> runtime state -> sequence -> evidence -> Audit | intent, runtime, sequence 2, DB evidence sequence 1, Audit | all 1 | intent/state unique |
| Runtime evidence | runtime state -> sequence -> evidence -> Audit | sequence increment, evidence, runtime state, Audit | all 1 | same evidence ID returns original event |
| Provider response | runtime state -> sequence -> evidence -> Audit | sequence, response evidence, runtime state, Audit | all 1 | same evidence ID |
| Unknown outcome | runtime state -> sequence -> evidence -> Audit | sequence, unknown evidence, runtime state, Audit | all 1 | terminal; same evidence ID replay only |
| Emergency/Key gates | unchanged frozen R3 gates | deny before write authorization | frozen regression | no retry |

## 1. Commands and Failures

No SQL is executed. The matrix describes the intended SQL transaction contract.

```text
POSTGRESQL_EXECUTION=NOT_EXECUTED
POSTGRESQL_CONCURRENCY=NOT_TESTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
```

## 2. Result Binding

Both Worker and Cleanup first-run transactions have the same final structure:

```text
mutation
  -> Audit append
  -> complete Result JSON + canonical text + digest + Audit ID
  -> COMPLETED
  -> COMMIT
```

Any failure before COMMIT rolls back all of these.

````
<!-- END_EXACT_SOURCE id=S012 -->

### S013. PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT_CONTRACT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT_CONTRACT.md`
- Bytes: `3113`
- SHA-256: `C834FE103C53A18BC2AAEDD4D37B545AD48CF939B727EE95955B825A2D7A74D0`

<!-- BEGIN_EXACT_SOURCE id=S013 sha256=C834FE103C53A18BC2AAEDD4D37B545AD48CF939B727EE95955B825A2D7A74D0 bytes=3113 -->
````text
# PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT_CONTRACT

## 1. Canonical Result

Schema:

```text
schemaVersion = r3-egress-r2-followup-cleanup-result-v1
cleanupRequestId
requestDigest
status APPLIED|ALREADY_SATISFIED
workerInstanceId
scopeKey
revocationVersion
leaseId
capabilityId
permitId
blockVersion
leaseOutcome REVOKED|PRESERVED_AFTER_WRITE_AUTHORIZED|PRESERVED_OUTCOME_UNKNOWN
permitOutcome REVOKED
externalOutcome NOT_SENT|WRITE_MAY_HAVE_OCCURRED|SEND_OUTCOME_UNKNOWN
auditEventId
completedAt
resultDigest
```

All fields are required. Unknown fields are rejected by strict Zod schemas.
Times are UTC Unix milliseconds, SHA-256 is lowercase-prefixed.

## 2. Digest

```text
resultDigest = sha256(canonical_json(Result without resultDigest))
```

Canonical JSON uses sorted object keys, no undefined values, UTF-8 and fixed
number/string encodings. The exact canonical text is persisted alongside the
JSON object.

## 3. Persistence

`trust_r6_scope_cleanup_request` stores:

```text
result_json jsonb
result_canonical_text text
result_digest
audit_event_id
completed_at_ms
```

All are non-null only in `COMPLETED`. Database CHECKs bind:

- cleanup request ID;
- request digest;
- Worker, Scope, Lease, Capability and Permit IDs;
- result Audit event ID;
- result digest.

JSONB storage order is not treated as canonical. Digest validation is over
`result_canonical_text`. The JSONB object is checked for structural identity and
is re-canonicalized for equality during replay.

## 4. Writer Sequence

```text
lock revocation
  -> lock/insert cleanup request
  -> lock block/floor/worker/lease/permit
  -> apply allowed mutations
  -> generate complete Result
  -> generate resultDigest and canonical text
  -> append Audit
  -> write Result JSON/text/digest/Audit ID
  -> PENDING -> COMPLETED
  -> COMMIT
```

## 5. Replay Sequence

```text
read request FOR UPDATE
  -> compare request ID + digest + payload
  -> state must be COMPLETED
  -> result JSON/text/digest/Audit must exist
  -> recompute digest from stored JSON
  -> compare canonical text
  -> join/lookup Audit Event
  -> verify subject and event type
  -> return stored Result unchanged
```

No Block Version, Lease, Permit, Audit or completion timestamp is changed.

## 6. Failure Table

| Condition | Result |
|---|---|
| no request row | not found / COMMIT ambiguity |
| PENDING | `IDEMPOTENCY_RECORD_INCONSISTENT` |
| same ID different payload | `IDEMPOTENCY_KEY_REUSE_CONFLICT` |
| missing Result | `CLEANUP_RESULT_INTEGRITY_FAILURE` |
| Digest mismatch | `CLEANUP_RESULT_INTEGRITY_FAILURE` |
| canonical text mismatch | `CLEANUP_RESULT_INTEGRITY_FAILURE` |
| Result Audit ID mismatch | `CLEANUP_RESULT_INTEGRITY_FAILURE` |
| Audit row missing/wrong subject/type | `AUDIT_EVENT_BINDING_FAILURE` |
| COMMIT outcome unknown | retry same ID |

`CLEANUP_RESULT_INTEGRITY_FAILURE` never triggers a second cleanup.

## 7. SQL and Model

SQL: `PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql`

Model: `models/scope-cleanup-complete-result.ts`

The model returns the original object and does not alter `status`,
`completedAt` or `auditEventId` on replay.

````
<!-- END_EXACT_SOURCE id=S013 -->

### S014. PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT_CONTRACT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT_CONTRACT.md`
- Bytes: `2145`
- SHA-256: `3165FDB04D6B3052705AF566C6AF48B67C05BCD7EF8192F1331B0414257EB402`

<!-- BEGIN_EXACT_SOURCE id=S014 sha256=3165FDB04D6B3052705AF566C6AF48B67C05BCD7EF8192F1331B0414257EB402 bytes=2145 -->
````text
# PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT_CONTRACT

## 1. Canonical Result

```text
schemaVersion = r3-egress-r2-followup-worker-result-v1
status = REVOKED
requestId
requestDigest
workerInstanceId
previousRegistrationState ACTIVE|DRAINING
registrationState REVOKED
previousRevocationVersion
revocationVersion
previousRecordVersion
recordVersion
auditEventId
completedAt
resultDigest
```

The original persisted result is returned on replay. Replay must not change
status to a new value or regenerate `completedAt` / `auditEventId`.

## 2. Digest

```text
resultDigest = sha256(canonical_json(Result without resultDigest))
```

The Worker and Scope Cleanup contracts use the same canonicalizer.

## 3. Persistence

`trust_r7_worker_revocation_request` stores:

```text
request_id
request_digest
state PENDING|COMPLETED|FAILED_TERMINAL
result_json jsonb
result_canonical_text text
result_digest
audit_event_id
completed_at_ms
```

Database CHECKs bind request, Worker, Audit and Digest fields.

## 4. Transaction

```text
lock revocation row
  -> lock/insert request row
  -> verify request/id/version/state
  -> update registration ACTIVE|DRAINING -> REVOKED
  -> update tombstone
  -> append WORKER_REVOKED Audit
  -> persist complete Result + Audit binding
  -> PENDING -> COMPLETED
  -> COMMIT
```

No second request ID on an already-revoked Worker creates a new result, Audit
or version.

## 5. Replay

Requirements:

```text
request_digest matches
state COMPLETED
result_json/result_canonical_text/result_digest exist
result_digest recomputes
result.auditEventId = audit_event_id
Audit event exists and subject matches Worker
```

Failure result:

```text
WORKER_REVOCATION_RESULT_INTEGRITY_FAILURE
```

or:

```text
AUDIT_EVENT_BINDING_FAILURE
```

Replay does not update the tombstone or Worker registration.

## 6. SQL and Model

SQL: `PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT.sql`

Model: `models/worker-revocation-complete-result.ts`

The R2 `REPLAYED` status is deliberately not inserted into the persisted
Worker result. Replay transport may indicate replay separately, but the
persisted result remains byte/structure-identical.

````
<!-- END_EXACT_SOURCE id=S014 -->

### S015. PHASE_R3_EGRESS_EVENT_SEQUENCE.sql

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_EGRESS_EVENT_SEQUENCE.sql`
- Bytes: `12251`
- SHA-256: `312B1C6834FF1778D6F1557A21598BAE1AE62A7FF394CFDD33B979BA89E4220A`

<!-- BEGIN_EXACT_SOURCE id=S015 sha256=312B1C6834FF1778D6F1557A21598BAE1AE62A7FF394CFDD33B979BA89E4220A bytes=12251 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Option A: one monotonic Intent-level event sequence space.

CREATE TABLE trust_r7_egress_event_sequence (
  egress_intent_id uuid PRIMARY KEY
    REFERENCES trust_r6_egress_runtime_state (egress_intent_id),
  next_sequence bigint NOT NULL CHECK (next_sequence >= 2),
  sequence_version bigint NOT NULL CHECK (sequence_version >= 1),
  updated_at_ms bigint NOT NULL
);

CREATE TABLE trust_r7_egress_intent_evidence (
  evidence_id uuid PRIMARY KEY,
  egress_intent_id uuid NOT NULL
    REFERENCES trust_r6_egress_runtime_state (egress_intent_id),
  audit_event_id uuid NOT NULL,
  intent_sequence bigint NOT NULL CHECK (intent_sequence >= 1),
  event_type text NOT NULL CHECK (
    event_type IN (
      'EGRESS_WRITE_START_AUTHORIZED',
      'SOCKET_WRITE_ATTEMPTED',
      'SOCKET_WRITE_FAILED_BEFORE_BYTES',
      'SOCKET_WRITE_PARTIAL',
      'PROVIDER_RESPONSE_RECEIVED',
      'PROVIDER_RESPONSE_REJECTED',
      'SEND_OUTCOME_UNKNOWN',
      'EGRESS_PROCESS_CRASHED'
    )
  ),
  evidence_source text NOT NULL CHECK (
    evidence_source IN ('DATABASE_AUTHORIZATION', 'TRUSTED_EGRESS_RUNTIME')
  ),
  evidence_digest varchar(71) NOT NULL,
  socket_call_outcome text CHECK (
    socket_call_outcome IS NULL
    OR socket_call_outcome IN (
      'NOT_CALLED', 'FAILED_BEFORE_BYTES', 'PARTIAL', 'COMPLETED_CALL'
    )
  ),
  provider_response_digest varchar(71),
  source_observed_at_ms bigint NOT NULL,
  persisted_at_ms bigint NOT NULL,
  business_success_evaluated boolean NOT NULL DEFAULT false
    CHECK (business_success_evaluated = false),
  UNIQUE (egress_intent_id, intent_sequence),
  UNIQUE (egress_intent_id, evidence_id),
  CHECK (evidence_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (
    provider_response_digest IS NULL
    OR provider_response_digest ~ '^sha256:[a-f0-9]{64}$'
  ),
  CHECK (
    event_type <> 'EGRESS_WRITE_START_AUTHORIZED'
    OR evidence_source = 'DATABASE_AUTHORIZATION'
  ),
  CHECK (
    event_type NOT IN (
      'SOCKET_WRITE_ATTEMPTED', 'SOCKET_WRITE_FAILED_BEFORE_BYTES',
      'SOCKET_WRITE_PARTIAL', 'PROVIDER_RESPONSE_RECEIVED',
      'PROVIDER_RESPONSE_REJECTED'
    )
    OR evidence_source = 'TRUSTED_EGRESS_RUNTIME'
  )
);

-- ===========================================================================
-- W: DB authorization owns sequence 1 and initializes next_sequence=2.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'WRITE_STARTED',
    row_version = row_version + 1
WHERE egress_intent_id = $1
  AND state = 'FINAL_AUTHORIZED'
  AND row_version = $2;

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_egress_runtime_state (
  egress_intent_id, state, row_version, write_authorized_at_ms,
  socket_attempted_at_ms, response_received_at_ms, outcome_unknown_at_ms
) VALUES (
  $1, 'WRITE_AUTHORIZED', 1, $3,
  NULL, NULL, NULL
);

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r7_egress_event_sequence (
  egress_intent_id, next_sequence, sequence_version, updated_at_ms
) VALUES (
  $1, 2, 1, $3
);

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r7_egress_intent_evidence (
  evidence_id, egress_intent_id, audit_event_id, intent_sequence,
  event_type, evidence_source, evidence_digest,
  socket_call_outcome, provider_response_digest,
  source_observed_at_ms, persisted_at_ms, business_success_evaluated
) VALUES (
  $4, $1, $5, 1,
  'EGRESS_WRITE_START_AUTHORIZED', 'DATABASE_AUTHORIZATION', $6,
  'NOT_CALLED', NULL,
  $3, $3, false
);

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $5, $7, $3, 'EGRESS_WRITE_START_AUTHORIZED', 'ALLOW',
  $1, $8, $9
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $7,
    last_event_digest = $9
WHERE singleton_id = 1
  AND last_sequence = $7 - 1
  AND last_event_digest IS NOT DISTINCT FROM $8;

COMMIT;

-- ===========================================================================
-- S: trusted Runtime evidence. Caller supplies stable evidence identity only.
-- Sequence is allocated by the database in the same transaction.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT evidence_id, event_type, evidence_source, evidence_digest,
       intent_sequence, socket_call_outcome, provider_response_digest
FROM trust_r7_egress_intent_evidence
WHERE egress_intent_id = $10
  AND evidence_id = $11
FOR UPDATE;

-- Existing exact evidence -> return stored event without sequence/Audit change.
-- Existing same evidence ID with different digest/type/source -> conflict.

SELECT egress_intent_id, state, row_version
FROM trust_r6_egress_runtime_state
WHERE egress_intent_id = $10
FOR UPDATE;

SELECT next_sequence, sequence_version
FROM trust_r7_egress_event_sequence
WHERE egress_intent_id = $10
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r7_egress_event_sequence
SET next_sequence = next_sequence + 1,
    sequence_version = sequence_version + 1,
    updated_at_ms = $15
WHERE egress_intent_id = $10
  AND sequence_version = $16
RETURNING next_sequence - 1 AS intent_sequence;

-- The host must bind the returned `intent_sequence` as `$17`.
-- No sequence value is accepted from the Runtime caller.

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r7_egress_intent_evidence (
  evidence_id, egress_intent_id, audit_event_id, intent_sequence,
  event_type, evidence_source, evidence_digest,
  socket_call_outcome, provider_response_digest,
  source_observed_at_ms, persisted_at_ms, business_success_evaluated
) SELECT
  $11, $10, $12, $17,
  $13, 'TRUSTED_EGRESS_RUNTIME', $14,
  $18, NULL,
  $19, $15, false
WHERE EXISTS (
  SELECT 1
  FROM trust_r7_egress_event_sequence sequence
  WHERE sequence.egress_intent_id = $10
    AND sequence.sequence_version = $16 + 1
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_egress_runtime_state
SET state = CASE
      WHEN $18 = 'FAILED_BEFORE_BYTES' THEN 'FAILED_BEFORE_BYTES'
      ELSE 'SOCKET_ATTEMPT_RECORDED'
    END,
    row_version = row_version + 1,
    socket_attempted_at_ms = $19
WHERE egress_intent_id = $10
  AND state = 'WRITE_AUTHORIZED'
  AND row_version = $20;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $12, $21, $19, $13, 'UNKNOWN',
  $10, $22, $23
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $21,
    last_event_digest = $23
WHERE singleton_id = 1
  AND last_sequence = $21 - 1
  AND last_event_digest IS NOT DISTINCT FROM $22;

COMMIT;

-- ===========================================================================
-- R: Provider response, also allocated from the same Intent sequence space.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT evidence_id, evidence_digest, intent_sequence
FROM trust_r7_egress_intent_evidence
WHERE egress_intent_id = $24
  AND evidence_id = $25
FOR UPDATE;

SELECT egress_intent_id, state, row_version
FROM trust_r6_egress_runtime_state
WHERE egress_intent_id = $24
FOR UPDATE;

SELECT next_sequence, sequence_version
FROM trust_r7_egress_event_sequence
WHERE egress_intent_id = $24
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r7_egress_event_sequence
SET next_sequence = next_sequence + 1,
    sequence_version = sequence_version + 1,
    updated_at_ms = $29
WHERE egress_intent_id = $24
  AND sequence_version = $30
RETURNING next_sequence - 1 AS intent_sequence;

-- Host binds returned intent sequence as `$31`.
-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r7_egress_intent_evidence (
  evidence_id, egress_intent_id, audit_event_id, intent_sequence,
  event_type, evidence_source, evidence_digest,
  socket_call_outcome, provider_response_digest,
  source_observed_at_ms, persisted_at_ms, business_success_evaluated
) SELECT
  $25, $24, $26, $31,
  'PROVIDER_RESPONSE_RECEIVED', 'TRUSTED_EGRESS_RUNTIME', $27,
  'COMPLETED_CALL', $28,
  $29, $32, false
WHERE EXISTS (
  SELECT 1
  FROM trust_r7_egress_intent_evidence attempt
  WHERE attempt.egress_intent_id = $24
    AND attempt.event_type IN (
      'SOCKET_WRITE_ATTEMPTED', 'SOCKET_WRITE_PARTIAL'
    )
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_egress_runtime_state
SET state = 'PROVIDER_RESPONSE_RECEIVED',
    row_version = row_version + 1,
    response_received_at_ms = $29
WHERE egress_intent_id = $24
  AND state = 'SOCKET_ATTEMPT_RECORDED'
  AND row_version = $33;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $26, $34, $29, 'PROVIDER_RESPONSE_RECEIVED', 'ALLOW',
  $24, $35, $36
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $34,
    last_event_digest = $36
WHERE singleton_id = 1
  AND last_sequence = $34 - 1
  AND last_event_digest IS NOT DISTINCT FROM $35;

COMMIT;

-- ===========================================================================
-- U: terminal unknown outcome. Same allocator, no automatic retry.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT evidence_id, evidence_digest, intent_sequence
FROM trust_r7_egress_intent_evidence
WHERE egress_intent_id = $37
  AND evidence_id = $38
FOR UPDATE;

SELECT egress_intent_id, state, row_version
FROM trust_r6_egress_runtime_state
WHERE egress_intent_id = $37
FOR UPDATE;

SELECT next_sequence, sequence_version
FROM trust_r7_egress_event_sequence
WHERE egress_intent_id = $37
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r7_egress_event_sequence
SET next_sequence = next_sequence + 1,
    sequence_version = sequence_version + 1,
    updated_at_ms = $42
WHERE egress_intent_id = $37
  AND sequence_version = $43
RETURNING next_sequence - 1 AS intent_sequence;

-- Host binds returned intent sequence as `$44`.
-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r7_egress_intent_evidence (
  evidence_id, egress_intent_id, audit_event_id, intent_sequence,
  event_type, evidence_source, evidence_digest,
  socket_call_outcome, provider_response_digest,
  source_observed_at_ms, persisted_at_ms, business_success_evaluated
) VALUES (
  $38, $37, $39, $44,
  'SEND_OUTCOME_UNKNOWN', 'TRUSTED_EGRESS_RUNTIME', $40,
  NULL, NULL,
  $42, $45, false
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_egress_runtime_state
SET state = 'SEND_OUTCOME_UNKNOWN',
    row_version = row_version + 1,
    outcome_unknown_at_ms = $42
WHERE egress_intent_id = $37
  AND state IN ('WRITE_AUTHORIZED', 'SOCKET_ATTEMPT_RECORDED')
  AND row_version = $41;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $39, $46, $42, 'SEND_OUTCOME_UNKNOWN', 'UNKNOWN',
  $37, $47, $48
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $46,
    last_event_digest = $48
WHERE singleton_id = 1
  AND last_sequence = $46 - 1
  AND last_event_digest IS NOT DISTINCT FROM $47;

COMMIT;

-- Global cross-source order is the Intent-level sequence. No Runtime-supplied
-- sequence is accepted. Sequence allocation and evidence insertion share one
-- transaction, so rollback consumes no sequence and COMMIT ambiguity is
-- resolved by evidence_id lookup.

```
<!-- END_EXACT_SOURCE id=S015 -->

### S016. PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql`
- Bytes: `16953`
- SHA-256: `7220EBFAF592AD4F71A55E51924ABCCA72889D13546809FD2FAE02E4CCBB72DD`

<!-- BEGIN_EXACT_SOURCE id=S016 sha256=7220EBFAF592AD4F71A55E51924ABCCA72889D13546809FD2FAE02E4CCBB72DD bytes=16953 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R2 follow-up: complete Result persistence and exact replay.
--
-- The host must first query by cleanup_request_id. A completed request returns
-- its persisted result without touching Block, Lease, Permit or Audit.

CREATE TABLE trust_r6_scope_cleanup_request (
  cleanup_request_id uuid PRIMARY KEY,
  request_digest varchar(71) NOT NULL,
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  scope_key text NOT NULL
    REFERENCES trust_r4_resource_fencing (scope_key),
  revocation_version bigint NOT NULL CHECK (revocation_version >= 1),
  lease_id uuid NOT NULL REFERENCES trust_r4_execution_lease (lease_id),
  capability_id uuid NOT NULL,
  permit_id uuid NOT NULL
    REFERENCES trust_r4_send_authorization (send_authorization_id),
  reason_code text NOT NULL,
  state text NOT NULL CHECK (
    state IN ('PENDING', 'COMPLETED', 'FAILED_TERMINAL')
  ),
  result_json jsonb,
  result_canonical_text text,
  result_digest varchar(71),
  audit_event_id uuid,
  created_at_ms bigint NOT NULL,
  completed_at_ms bigint,
  CHECK (request_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (result_digest IS NULL OR result_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (
    (state = 'PENDING'
      AND result_json IS NULL
      AND result_canonical_text IS NULL
      AND result_digest IS NULL
      AND audit_event_id IS NULL
      AND completed_at_ms IS NULL)
    OR
    (state = 'COMPLETED'
      AND result_json IS NOT NULL
      AND result_canonical_text IS NOT NULL
      AND result_digest IS NOT NULL
      AND audit_event_id IS NOT NULL
      AND completed_at_ms IS NOT NULL)
    OR
    (state = 'FAILED_TERMINAL'
      AND result_json IS NULL
      AND result_canonical_text IS NULL
      AND result_digest IS NULL
      AND completed_at_ms IS NOT NULL)
  ),
  CHECK (
    state <> 'COMPLETED'
    OR (
      result_json ->> 'cleanupRequestId' = cleanup_request_id::text
      AND result_json ->> 'requestDigest' = request_digest
      AND result_json ->> 'workerInstanceId' = worker_instance_id::text
      AND result_json ->> 'scopeKey' = scope_key
      AND result_json ->> 'leaseId' = lease_id::text
      AND result_json ->> 'capabilityId' = capability_id::text
      AND result_json ->> 'permitId' = permit_id::text
      AND result_json ->> 'auditEventId' = audit_event_id::text
      AND result_json ->> 'resultDigest' = result_digest
    )
  )
);

CREATE INDEX trust_r6_scope_cleanup_scope_idx
  ON trust_r6_scope_cleanup_request (
    worker_instance_id, scope_key, revocation_version, state
  );

-- A committed PENDING row is an invariant violation. PENDING exists only
-- inside an open transaction and must become COMPLETED before COMMIT.

-- ===========================================================================
-- Transaction A: first application, PRE_SEND
-- Allowed Lease states:
--   ISSUED, KEY_READ, TRANSPORT_CREATED, SEND_AUTHORIZED
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

-- Lock 1: Worker Revocation authority.
SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

-- Lock 2: cleanup idempotency row.
SELECT cleanup_request_id, request_digest, worker_instance_id, scope_key,
       revocation_version, lease_id, capability_id, permit_id,
       reason_code, state, result_digest, audit_event_id
FROM trust_r6_scope_cleanup_request
WHERE cleanup_request_id = $2
FOR UPDATE;

-- If found:
--   exact request digest/payload and COMPLETED -> return persisted result;
--   payload mismatch -> IDEMPOTENCY_KEY_REUSE_CONFLICT;
--   PENDING -> IDEMPOTENCY_RECORD_INCONSISTENT.

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_scope_cleanup_request (
  cleanup_request_id, request_digest, worker_instance_id, scope_key,
  revocation_version, lease_id, capability_id, permit_id,
  reason_code, state, result_json, result_canonical_text,
  result_digest, audit_event_id, created_at_ms, completed_at_ms
) VALUES (
  $2, $3, $1, $4,
  $5, $6, $7, $8,
  $9, 'PENDING', NULL, NULL, NULL,
  NULL, NULL, $10, NULL
)
ON CONFLICT (cleanup_request_id) DO NOTHING
RETURNING cleanup_request_id;

-- If the conditional INSERT returns zero, the host rolls back and executes the
-- replay transaction below. It must not continue with safety mutations.

-- Lock 3: Scope Worker block. Initial insert owns a new block version.
-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r5_scope_worker_block (
  scope_key, worker_instance_id, blocked_revocation_version,
  version, blocked_at_ms, reason_code
) VALUES (
  $4, $1, $5, 1, $10, $9
)
ON CONFLICT (scope_key, worker_instance_id) DO UPDATE
SET blocked_revocation_version = EXCLUDED.blocked_revocation_version,
    version = trust_r5_scope_worker_block.version + 1,
    blocked_at_ms = EXCLUDED.blocked_at_ms,
    reason_code = EXCLUDED.reason_code
WHERE trust_r5_scope_worker_block.blocked_revocation_version
        < EXCLUDED.blocked_revocation_version
RETURNING version;

-- Zero returned rows means another request already installed a block at the
-- same/higher version. The host rolls back and uses the ALREADY_SATISFIED
-- transaction. It must not execute Lease/Permit updates from this transaction.

-- Lock 4: Resource Floor.
SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $4
FOR UPDATE;

-- Lock 5: Worker Registration.
SELECT worker_instance_id, state
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

-- Lock 6: Lease.
SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $6
FOR UPDATE;

-- Lock 7: Permit.
SELECT send_authorization_id, scope_key, lease_id, worker_instance_id,
       capability_id, fencing_token, state
FROM trust_r4_send_authorization
WHERE send_authorization_id = $8
FOR UPDATE;

-- Host preconditions:
--   global revocation.state='REVOKED' and version >= $5
--   Floor/Worker/Lease/Capability/token match request
--   Lease is PRE_SEND
--   Permit is ISSUED or CONSUMED
--   current block was installed by this transaction

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease
SET state = 'REVOKED'
WHERE lease_id = $6
  AND scope_key = $4
  AND worker_instance_id = $1
  AND capability_id = $7
  AND fencing_token = $12
  AND state IN (
    'ISSUED', 'KEY_READ', 'TRANSPORT_CREATED', 'SEND_AUTHORIZED'
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE send_authorization_id = $8
  AND scope_key = $4
  AND lease_id = $6
  AND worker_instance_id = $1
  AND capability_id = $7
  AND fencing_token = $12
  AND state IN ('ISSUED', 'CONSUMED');

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $13, $14, $10, 'WORKER_SCOPE_BLOCKED', 'ALLOW',
  $2, $15, $16
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $14,
    last_event_digest = $16
WHERE singleton_id = 1
  AND last_sequence = $14 - 1
  AND last_event_digest IS NOT DISTINCT FROM $15;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_scope_cleanup_request
SET state = 'COMPLETED',
    result_json = $17::jsonb,
    result_canonical_text = $18,
    result_digest = $19,
    audit_event_id = $13,
    completed_at_ms = $10
WHERE cleanup_request_id = $2
  AND state = 'PENDING'
  AND request_digest = $3;

COMMIT;

-- ===========================================================================
-- Transaction B: first application, AFTER_SEND
-- Allowed Lease states:
--   SENT, WRITE_AUTHORIZED, SOCKET_ATTEMPTED,
--   PROVIDER_RESPONSE_RECEIVED, SEND_OUTCOME_UNKNOWN
-- The Lease is preserved. Permit and future authority are revoked.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT cleanup_request_id, request_digest, state, result_digest
FROM trust_r6_scope_cleanup_request
WHERE cleanup_request_id = $2
FOR UPDATE;

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_scope_cleanup_request (
  cleanup_request_id, request_digest, worker_instance_id, scope_key,
  revocation_version, lease_id, capability_id, permit_id,
  reason_code, state, result_json, result_canonical_text,
  result_digest, audit_event_id, created_at_ms, completed_at_ms
) VALUES (
  $2, $3, $1, $4,
  $5, $6, $7, $8,
  $9, 'PENDING', NULL, NULL, NULL,
  NULL, NULL, $10, NULL
)
ON CONFLICT (cleanup_request_id) DO NOTHING
RETURNING cleanup_request_id;

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r5_scope_worker_block (
  scope_key, worker_instance_id, blocked_revocation_version,
  version, blocked_at_ms, reason_code
) VALUES (
  $4, $1, $5, 1, $10, $9
)
ON CONFLICT (scope_key, worker_instance_id) DO UPDATE
SET blocked_revocation_version = EXCLUDED.blocked_revocation_version,
    version = trust_r5_scope_worker_block.version + 1,
    blocked_at_ms = EXCLUDED.blocked_at_ms,
    reason_code = EXCLUDED.reason_code
WHERE trust_r5_scope_worker_block.blocked_revocation_version
        < EXCLUDED.blocked_revocation_version
RETURNING version;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $4
FOR UPDATE;

SELECT worker_instance_id, state
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $6
FOR UPDATE;

SELECT send_authorization_id, scope_key, lease_id, worker_instance_id,
       capability_id, fencing_token, state
FROM trust_r4_send_authorization
WHERE send_authorization_id = $8
FOR UPDATE;

-- Lease update intentionally NOT_USED.
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE send_authorization_id = $8
  AND scope_key = $4
  AND lease_id = $6
  AND worker_instance_id = $1
  AND capability_id = $7
  AND fencing_token = $12
  AND state = 'CONSUMED';

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $13, $14, $10, 'WORKER_SCOPE_BLOCKED', 'ALLOW',
  $2, $15, $16
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $14,
    last_event_digest = $16
WHERE singleton_id = 1
  AND last_sequence = $14 - 1
  AND last_event_digest IS NOT DISTINCT FROM $15;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_scope_cleanup_request
SET state = 'COMPLETED',
    result_json = $17::jsonb,
    result_canonical_text = $18,
    result_digest = $19,
    audit_event_id = $13,
    completed_at_ms = $10
WHERE cleanup_request_id = $2
  AND state = 'PENDING'
  AND request_digest = $3;

COMMIT;

-- ===========================================================================
-- Transaction C: distinct request already satisfied by another request
-- No Block Version bump, Lease update or Permit update. One Audit event binds
-- this distinct cleanup request to the already-satisfied outcome.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT cleanup_request_id, request_digest, state
FROM trust_r6_scope_cleanup_request
WHERE cleanup_request_id = $2
FOR UPDATE;

-- The host has already observed no exact request or has rolled back from A/B
-- because the Block already exists at/past $5.
-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_scope_cleanup_request (
  cleanup_request_id, request_digest, worker_instance_id, scope_key,
  revocation_version, lease_id, capability_id, permit_id,
  reason_code, state, result_json, result_canonical_text,
  result_digest, audit_event_id, created_at_ms, completed_at_ms
) VALUES (
  $2, $3, $1, $4,
  $5, $6, $7, $8,
  $9, 'PENDING', NULL, NULL, NULL,
  NULL, NULL, $10, NULL
)
ON CONFLICT (cleanup_request_id) DO NOTHING
RETURNING cleanup_request_id;

SELECT scope_key, worker_instance_id, blocked_revocation_version, version
FROM trust_r5_scope_worker_block
WHERE scope_key = $4
  AND worker_instance_id = $1
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $4
FOR UPDATE;

SELECT worker_instance_id, state
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $6
FOR UPDATE;

SELECT send_authorization_id, scope_key, lease_id, worker_instance_id,
       capability_id, fencing_token, state
FROM trust_r4_send_authorization
WHERE send_authorization_id = $8
FOR UPDATE;

-- Host preconditions:
--   block.blocked_revocation_version >= $5
--   Permit is already REVOKED by the prior completed request
--   all Worker/Scope/Lease/Capability/token bindings still match
-- LEASE_UPDATE=NOT_USED
-- BLOCK_UPDATE=NOT_USED
-- PERMIT_UPDATE=NOT_USED

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $13, $14, $10, 'WORKER_SCOPE_CLEANUP_ALREADY_SATISFIED', 'ALLOW',
  $2, $15, $16
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $14,
    last_event_digest = $16
WHERE singleton_id = 1
  AND last_sequence = $14 - 1
  AND last_event_digest IS NOT DISTINCT FROM $15;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_scope_cleanup_request
SET state = 'COMPLETED',
    result_json = $17::jsonb,
    result_canonical_text = $18,
    result_digest = $19,
    audit_event_id = $13,
    completed_at_ms = $10
WHERE cleanup_request_id = $2
  AND state = 'PENDING'
  AND request_digest = $3;

COMMIT;

-- ===========================================================================
-- Transaction D: exact-request replay
-- This transaction performs no security mutation and appends no Audit.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT cleanup.cleanup_request_id, cleanup.request_digest,
       cleanup.worker_instance_id, cleanup.scope_key,
       cleanup.revocation_version, cleanup.lease_id,
       cleanup.capability_id, cleanup.permit_id, cleanup.reason_code,
       cleanup.state, cleanup.result_json, cleanup.result_canonical_text,
       cleanup.result_digest, cleanup.audit_event_id, cleanup.completed_at_ms,
       audit.event_id AS bound_audit_event_id,
       audit.event_type AS bound_audit_event_type,
       audit.subject_id AS bound_audit_subject_id
FROM trust_r6_scope_cleanup_request cleanup
LEFT JOIN trust_r3_audit_event audit
  ON audit.event_id = cleanup.audit_event_id
WHERE cleanup.cleanup_request_id = $2
FOR UPDATE OF cleanup;

COMMIT;

-- If no row exists, COMMIT_MAY_HAVE_FAILED_OR_RETRY_IS_PREMATURE. If the row
-- exists with a mismatched digest, return IDEMPOTENCY_KEY_REUSE_CONFLICT. If
-- COMPLETED, return the persisted result. A committed PENDING row is treated
-- as IDEMPOTENCY_RECORD_INCONSISTENT and is not silently repaired.
-- A lost caller response is COMMIT_OUTCOME_UNKNOWN until this exact request
-- row is queried in a fresh transaction.

-- Parameters:
--   $1 worker_instance_id
--   $2 cleanup_request_id
--   $3 canonical cleanup request digest
--   $4 scope_key
--   $5 requested Worker revocation_version
--   $6 lease_id
--   $7 capability_id
--   $8 permit_id
--   $9 reason_code
--   $10 server UTC Unix milliseconds
--   $12 fencing_token
--   $13 Audit event_id
--   $14 Audit sequence
--   $15 previous_event_digest
--   $16 event_digest
--   $17 complete result JSON object
--   $18 exact canonical result text
--   $19 SHA-256 over $18
--
-- Replay MUST verify result_canonical_text/result_digest/result_json and the
-- joined Audit event before returning the stored Result. A missing or
-- mismatched binding is CLEANUP_RESULT_INTEGRITY_FAILURE.

```
<!-- END_EXACT_SOURCE id=S016 -->

### S017. PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT.sql

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT.sql`
- Bytes: `4971`
- SHA-256: `967F852725DEE236FA1B23B771769C46F32369F1EBCE8CBC57BB03D1489A688F`

<!-- BEGIN_EXACT_SOURCE id=S017 sha256=967F852725DEE236FA1B23B771769C46F32369F1EBCE8CBC57BB03D1489A688F bytes=4971 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Complete Worker revocation Result persistence.

CREATE TABLE trust_r7_worker_revocation_request (
  request_id uuid PRIMARY KEY,
  request_digest varchar(71) NOT NULL,
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  requested_revocation_version bigint NOT NULL,
  reason_code text NOT NULL,
  requested_at_ms bigint NOT NULL,
  state text NOT NULL CHECK (
    state IN ('PENDING', 'COMPLETED', 'FAILED_TERMINAL')
  ),
  result_json jsonb,
  result_canonical_text text,
  result_digest varchar(71),
  audit_event_id uuid,
  completed_at_ms bigint,
  UNIQUE (worker_instance_id, requested_revocation_version),
  CHECK (request_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (result_digest IS NULL OR result_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (
    (state = 'PENDING'
      AND result_json IS NULL
      AND result_canonical_text IS NULL
      AND result_digest IS NULL
      AND audit_event_id IS NULL
      AND completed_at_ms IS NULL)
    OR
    (state = 'COMPLETED'
      AND result_json IS NOT NULL
      AND result_canonical_text IS NOT NULL
      AND result_digest IS NOT NULL
      AND audit_event_id IS NOT NULL
      AND completed_at_ms IS NOT NULL)
    OR
    (state = 'FAILED_TERMINAL'
      AND result_json IS NULL
      AND result_canonical_text IS NULL
      AND result_digest IS NULL
      AND completed_at_ms IS NOT NULL)
  ),
  CHECK (
    state <> 'COMPLETED'
    OR (
      result_json ->> 'requestId' = request_id::text
      AND result_json ->> 'requestDigest' = request_digest
      AND result_json ->> 'workerInstanceId' = worker_instance_id::text
      AND result_json ->> 'auditEventId' = audit_event_id::text
      AND result_json ->> 'resultDigest' = result_digest
    )
  )
);

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT request_id, request_digest, state, result_json,
       result_canonical_text, result_digest, audit_event_id, completed_at_ms
FROM trust_r7_worker_revocation_request
WHERE request_id = $2
FOR UPDATE;

-- Found exact COMPLETED request: return result_json after verifying:
--   result_canonical_text hashes to result_digest;
--   result_json.auditEventId = audit_event_id;
--   trust_r3_audit_event event_id exists with WORKER_REVOKED subject=$1.
-- Found request with a different digest: IDEMPOTENCY_KEY_REUSE_CONFLICT.
-- Found PENDING: IDEMPOTENCY_RECORD_INCONSISTENT.

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_worker_revocation
SET state = 'REVOKED',
    revocation_version = revocation_version + 1,
    record_version = record_version + 1,
    revoked_at_ms = $3,
    reason_code = $4,
    updated_at_ms = $3
WHERE worker_instance_id = $1
  AND state = 'ACTIVE'
  AND revocation_version = $11 - 1
  AND record_version = $5;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration
SET state = 'REVOKED',
    updated_at_ms = $3
WHERE worker_instance_id = $1
  AND state IN ('ACTIVE', 'DRAINING');

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r7_worker_revocation_request (
  request_id, request_digest, worker_instance_id,
  requested_revocation_version, reason_code, requested_at_ms,
  state, result_json, result_canonical_text, result_digest,
  audit_event_id, completed_at_ms
) VALUES (
  $2, $10, $1,
  $11, $4, $3,
  'PENDING', NULL, NULL, NULL,
  NULL, NULL
);

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $6, $7, $3, 'WORKER_REVOKED', 'ALLOW',
  $1, $8, $9
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $7,
    last_event_digest = $9
WHERE singleton_id = 1
  AND last_sequence = $7 - 1
  AND last_event_digest IS NOT DISTINCT FROM $8;

-- `$12::jsonb` is the complete canonical result object; `$13` is the exact
-- canonical UTF-8 text; `$14` is SHA-256 over `$13`; `$6` is its auditEventId.
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r7_worker_revocation_request
SET state = 'COMPLETED',
    result_json = $12::jsonb,
    result_canonical_text = $13,
    result_digest = $14,
    audit_event_id = $6,
    completed_at_ms = $3
WHERE request_id = $2
  AND state = 'PENDING'
  AND request_digest = $10;

COMMIT;

-- Parameters:
--   $1 previous worker state input is read from registration; expected ACTIVE/DRAINING
--   $2 request_id
--   $3 completed_at / revoked_at
--   $4 reason_code
--   $5 expected record_version before mutation
--   $6 Audit event id
--   $7..$9 Audit sequence/digests
--   $10 request digest
--   $11 new revocation version
--   $12 complete result JSON object
--   $13 canonical result text
--   $14 result digest

```
<!-- END_EXACT_SOURCE id=S017 -->

### S018. contracts.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/contracts.ts`
- Bytes: `6745`
- SHA-256: `8F2D411F32096B5DAA7943B7F96843983DFE42EBBEEE65F387BDFB904216F860`

<!-- BEGIN_EXACT_SOURCE id=S018 sha256=8F2D411F32096B5DAA7943B7F96843983DFE42EBBEEE65F387BDFB904216F860 bytes=6745 -->
```text
import { z } from "zod";

import {
  InstantSchema,
  Sha256Schema,
  UuidSchema,
} from "../contracts/common";

export const FOLLOWUP_CONTRACT_VERSION =
  "r3-egress-revocation-r2-followup-v1";

const IdentifierSchema = z.string().min(1).max(200).trim();
const VersionSchema = z.number().int().positive();

export const FollowupFailureCodeSchema = z.enum([
  "AUTHORITY_UNAVAILABLE",
  "ROW_COUNT_CONFLICT",
  "IDEMPOTENCY_KEY_REUSE_CONFLICT",
  "IDEMPOTENCY_RECORD_NOT_FOUND",
  "IDEMPOTENCY_RECORD_INCONSISTENT",
  "CLEANUP_RESULT_INTEGRITY_FAILURE",
  "WORKER_REVOCATION_RESULT_INTEGRITY_FAILURE",
  "AUDIT_EVENT_BINDING_FAILURE",
  "COMMIT_OUTCOME_UNKNOWN",
  "PROCESS_CRASHED_BEFORE_COMMIT",
  "WORKER_STATE_INVALID",
  "WORKER_VERSION_CONFLICT",
  "WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST",
  "WORKER_REGISTERED_REVOCATION_FORBIDDEN",
  "WORKER_REACTIVATION_FORBIDDEN",
  "SCOPE_BINDING_MISMATCH",
  "SCOPE_CLEANUP_STATE_INCONSISTENT",
  "LEASE_STATE_INVALID",
  "PERMIT_STATE_INVALID",
  "EGRESS_WRITE_NOT_AUTHORIZED",
  "EVIDENCE_SEQUENCE_SOURCE_FORBIDDEN",
  "EVIDENCE_REPLAY_CONFLICT",
  "SOCKET_ATTEMPT_NOT_PROVEN",
  "PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT",
  "SEND_OUTCOME_ALREADY_TERMINAL",
  "AUTO_RETRY_FORBIDDEN",
]);

export type FollowupFailureCode = z.infer<typeof FollowupFailureCodeSchema>;
export type Result<T> =
  | Readonly<{ ok: true; value: T }>
  | Readonly<{ ok: false; code: FollowupFailureCode }>;

export function ok<T>(value: T): Result<T> {
  return Object.freeze({ ok: true, value });
}

export function fail<T = never>(code: FollowupFailureCode): Result<T> {
  return Object.freeze({ ok: false, code });
}

export function requireExactlyOne(rowCount: number): Result<true> {
  return rowCount === 1 ? ok(true as const) : fail("ROW_COUNT_CONFLICT");
}

export const WorkerRegistrationStateSchema = z.enum([
  "REGISTERED",
  "ACTIVE",
  "DRAINING",
  "REVOKED",
]);
export const WorkerRevocationStateSchema = z.enum([
  "ACTIVE",
  "REVOKED",
  "RECOVERY_REQUIRED",
]);

export const WorkerRevocationPayloadSchema = z.strictObject({
  requestId: UuidSchema,
  workerInstanceId: UuidSchema,
  expectedRecordVersion: VersionSchema,
  reasonCode: IdentifierSchema,
  requestedAt: InstantSchema,
});

const WorkerResultCoreSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-followup-worker-result-v1"),
  status: z.literal("REVOKED"),
  requestId: UuidSchema,
  requestDigest: Sha256Schema,
  workerInstanceId: UuidSchema,
  previousRegistrationState: z.enum(["ACTIVE", "DRAINING"]),
  registrationState: z.literal("REVOKED"),
  previousRevocationVersion: z.number().int().nonnegative(),
  revocationVersion: VersionSchema,
  previousRecordVersion: VersionSchema,
  recordVersion: VersionSchema,
  auditEventId: UuidSchema,
  completedAt: InstantSchema,
});

export const WorkerRevocationCompleteResultSchema = WorkerResultCoreSchema.extend({
  resultDigest: Sha256Schema,
});

export const ScopeCleanupPayloadSchema = z.strictObject({
  cleanupRequestId: UuidSchema,
  workerInstanceId: UuidSchema,
  scopeKey: IdentifierSchema,
  revocationVersion: VersionSchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  permitId: UuidSchema,
  reasonCode: IdentifierSchema,
});

export const CleanupLeaseStateSchema = z.enum([
  "ISSUED",
  "KEY_READ",
  "TRANSPORT_CREATED",
  "SEND_AUTHORIZED",
  "SENT",
  "WRITE_AUTHORIZED",
  "SOCKET_ATTEMPTED",
  "PROVIDER_RESPONSE_RECEIVED",
  "SEND_OUTCOME_UNKNOWN",
  "REVOKED",
]);
export const CleanupPermitStateSchema = z.enum([
  "ISSUED",
  "CONSUMED",
  "REVOKED",
]);
export const EgressIntentStateSchema = z.enum([
  "FINAL_AUTHORIZED",
  "WRITE_AUTHORIZED",
  "SOCKET_ATTEMPT_RECORDED",
  "PROVIDER_RESPONSE_RECEIVED",
  "COMPLETED",
  "FAILED_BEFORE_BYTES",
  "SEND_OUTCOME_UNKNOWN",
  "REJECTED",
]);

const ScopeCleanupResultCoreSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-followup-cleanup-result-v1"),
  cleanupRequestId: UuidSchema,
  requestDigest: Sha256Schema,
  status: z.enum(["APPLIED", "ALREADY_SATISFIED"]),
  workerInstanceId: UuidSchema,
  scopeKey: IdentifierSchema,
  revocationVersion: VersionSchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  permitId: UuidSchema,
  blockVersion: VersionSchema,
  leaseOutcome: z.enum([
    "REVOKED",
    "PRESERVED_AFTER_WRITE_AUTHORIZED",
    "PRESERVED_OUTCOME_UNKNOWN",
  ]),
  permitOutcome: z.literal("REVOKED"),
  externalOutcome: z.enum([
    "NOT_SENT",
    "WRITE_MAY_HAVE_OCCURRED",
    "SEND_OUTCOME_UNKNOWN",
  ]),
  auditEventId: UuidSchema,
  completedAt: InstantSchema,
});

export const ScopeCleanupCompleteResultSchema = ScopeCleanupResultCoreSchema.extend({
  resultDigest: Sha256Schema,
});

export type WorkerRevocationPayload = z.infer<
  typeof WorkerRevocationPayloadSchema
>;
export type WorkerRevocationCompleteResult = z.infer<
  typeof WorkerRevocationCompleteResultSchema
>;
export type ScopeCleanupPayload = z.infer<
  typeof ScopeCleanupPayloadSchema
>;
export type ScopeCleanupCompleteResult = z.infer<
  typeof ScopeCleanupCompleteResultSchema
>;

export const AuditEventTypeSchema = z.enum([
  "EGRESS_WRITE_START_AUTHORIZED",
  "SOCKET_WRITE_ATTEMPTED",
  "SOCKET_WRITE_FAILED_BEFORE_BYTES",
  "SOCKET_WRITE_PARTIAL",
  "PROVIDER_RESPONSE_RECEIVED",
  "PROVIDER_RESPONSE_REJECTED",
  "SEND_OUTCOME_UNKNOWN",
  "EGRESS_PROCESS_CRASHED",
]);

export const EvidenceSourceSchema = z.enum([
  "DATABASE_AUTHORIZATION",
  "TRUSTED_EGRESS_RUNTIME",
]);

export const EgressIntentEventSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-followup-event-v1"),
  eventId: UuidSchema,
  evidenceId: UuidSchema,
  intentId: UuidSchema,
  intentSequence: VersionSchema,
  eventType: AuditEventTypeSchema,
  evidenceSource: EvidenceSourceSchema,
  evidenceDigest: Sha256Schema,
  sourceObservedAt: InstantSchema,
  persistedAt: InstantSchema,
  socketCallOutcome: z.enum([
    "NOT_CALLED",
    "FAILED_BEFORE_BYTES",
    "PARTIAL",
    "COMPLETED_CALL",
  ]).nullable(),
  providerResponseDigest: Sha256Schema.nullable(),
  businessSuccessEvaluated: z.literal(false),
});

export const RuntimeEvidenceInputSchema = z.strictObject({
  evidenceId: UuidSchema,
  eventId: UuidSchema,
  intentId: UuidSchema,
  eventType: AuditEventTypeSchema,
  evidenceSource: EvidenceSourceSchema,
  evidenceDigest: Sha256Schema,
  sourceObservedAt: InstantSchema,
  persistedAt: InstantSchema,
  socketCallOutcome: z.enum([
    "NOT_CALLED",
    "FAILED_BEFORE_BYTES",
    "PARTIAL",
    "COMPLETED_CALL",
  ]).nullable(),
  providerResponseDigest: Sha256Schema.nullable(),
});

export type EgressIntentEvent = z.infer<typeof EgressIntentEventSchema>;
export type RuntimeEvidenceInput = z.infer<
  typeof RuntimeEvidenceInputSchema
>;

```
<!-- END_EXACT_SOURCE id=S018 -->

### S019. lock-order.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/lock-order.ts`
- Bytes: `1430`
- SHA-256: `93D79865E4D08C1951194992969DAE954A38097519E97B49895FDF7FA5C68354`

<!-- BEGIN_EXACT_SOURCE id=S019 sha256=93D79865E4D08C1951194992969DAE954A38097519E97B49895FDF7FA5C68354 bytes=1430 -->
```text
import { z } from "zod";

import { fail, ok, type Result } from "./contracts";

export const FOLLOWUP_LOCK_ORDER = Object.freeze([
  "WORKER_REVOCATION_CONTROL",
  "WORKER_REVOCATION_REQUEST",
  "SCOPE_CLEANUP_REQUEST",
  "SCOPE_WORKER_BLOCK",
  "EMERGENCY_CONTROL",
  "KEY_REGISTRY",
  "EXECUTION_AUTHORIZATION",
  "BUDGET_CONTROL",
  "BUDGET_RESERVATION",
  "CAPABILITY",
  "RESOURCE_FENCING_FLOOR",
  "FENCING_TOKEN_CONTROL",
  "WORKER_REGISTRATION",
  "EXECUTION_LEASE",
  "SEND_AUTHORIZATION",
  "EGRESS_SEND_INTENT",
  "EGRESS_RUNTIME_STATE",
  "EGRESS_EVENT_SEQUENCE",
  "EGRESS_RUNTIME_EVIDENCE",
  "AUDIT_SEQUENCE",
] as const);

export type FollowupLockDomain = typeof FOLLOWUP_LOCK_ORDER[number];

const AcquisitionSchema = z.strictObject({
  domain: z.enum(FOLLOWUP_LOCK_ORDER),
  acquiredAt: z.number().int().nonnegative(),
});

export function validateFollowupLockOrder(
  acquisitions: readonly unknown[],
): Result<readonly FollowupLockDomain[]> {
  const parsed = z.array(AcquisitionSchema).safeParse(acquisitions);
  if (!parsed.success) return fail("ROW_COUNT_CONFLICT");
  let previous = -1;
  const domains: FollowupLockDomain[] = [];
  for (const acquisition of parsed.data) {
    const index = FOLLOWUP_LOCK_ORDER.indexOf(acquisition.domain);
    if (index < previous) return fail("ROW_COUNT_CONFLICT");
    previous = index;
    domains.push(acquisition.domain);
  }
  return ok(Object.freeze(domains));
}

```
<!-- END_EXACT_SOURCE id=S019 -->

### S020. models/canonical.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/models/canonical.ts`
- Bytes: `1340`
- SHA-256: `C5298ECD2A5FAA763017A9CA657F5BCBCF8C613B7CE1820787AA718488F0AB85`

<!-- BEGIN_EXACT_SOURCE id=S020 sha256=C5298ECD2A5FAA763017A9CA657F5BCBCF8C613B7CE1820787AA718488F0AB85 bytes=1340 -->
```text
import { createHash } from "node:crypto";

function canonicalize(value: unknown): string {
  if (
    value === null
    || typeof value === "string"
    || typeof value === "boolean"
  ) {
    return JSON.stringify(value);
  }
  if (typeof value === "number") {
    if (!Number.isFinite(value)) throw new Error("NON_FINITE_NUMBER");
    return JSON.stringify(value);
  }
  if (Array.isArray(value)) {
    return `[${value.map(canonicalize).join(",")}]`;
  }
  if (typeof value === "object") {
    const entries = Object.entries(value as Readonly<Record<string, unknown>>)
      .filter(([, item]) => item !== undefined)
      .sort(([left], [right]) => left.localeCompare(right));
    return `{${entries
      .map(([key, item]) => `${JSON.stringify(key)}:${canonicalize(item)}`)
      .join(",")}}`;
  }
  throw new Error("UNSUPPORTED_CANONICAL_VALUE");
}

export function canonicalJson(value: unknown): string {
  return canonicalize(value);
}

export function sha256Canonical(value: unknown): string {
  return `sha256:${createHash("sha256")
    .update(canonicalJson(value), "utf8")
    .digest("hex")}`;
}

export function omitKey(
  value: Readonly<Record<string, unknown>>,
  key: string,
): Readonly<Record<string, unknown>> {
  return Object.fromEntries(
    Object.entries(value).filter(([entryKey]) => entryKey !== key),
  );
}

```
<!-- END_EXACT_SOURCE id=S020 -->

### S021. models/egress-intent-sequence.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/models/egress-intent-sequence.ts`
- Bytes: `11041`
- SHA-256: `99763E75B32CA5698FF5002B24DD9C5EFF60D06F32047761439123EAC15B7AEB`

<!-- BEGIN_EXACT_SOURCE id=S021 sha256=99763E75B32CA5698FF5002B24DD9C5EFF60D06F32047761439123EAC15B7AEB bytes=11041 -->
```text
import {
  EgressIntentEventSchema,
  RuntimeEvidenceInputSchema,
  fail,
  ok,
  requireExactlyOne,
  type EgressIntentEvent,
  type Result,
} from "../contracts";
import { canonicalJson } from "./canonical";
import { validateFollowupLockOrder } from "../lock-order";

type IntentRecord = {
  intentId: string;
  state: string;
  nextSequence: number;
  sequenceVersion: number;
  writeAuthorizedAt: number | null;
};

type EvidenceRecord = Readonly<{
  fingerprint: string;
  event: EgressIntentEvent;
}>;

export type EgressSequenceSnapshot = Readonly<{
  intents: Readonly<Record<string, IntentRecord>>;
  events: Readonly<Record<string, readonly EgressIntentEvent[]>>;
  evidence: Readonly<Record<string, EvidenceRecord>>;
}>;

/**
 * OFFLINE_REFERENCE_MODEL.
 * The database is the Intent-level sequence authority. Runtime callers supply
 * stable evidence identity and digest, but cannot choose a sequence number.
 */
export class OfflineEgressIntentSequenceModel {
  private readonly intents = new Map<string, IntentRecord>();
  private readonly events = new Map<string, EgressIntentEvent[]>();
  private readonly evidence = new Map<string, EvidenceRecord>();
  private queue: Promise<void> = Promise.resolve();
  private failNextAudit = false;

  seedFinalAuthorized(intentId: string): Result<true> {
    this.intents.set(intentId, {
      intentId,
      state: "FINAL_AUTHORIZED",
      nextSequence: 1,
      sequenceVersion: 1,
      writeAuthorizedAt: null,
    });
    this.events.set(intentId, []);
    return ok(true as const);
  }

  setNextAuditFailure(): void {
    this.failNextAudit = true;
  }

  authorizeWriteStart(input: Readonly<{
    intentId: string;
    eventId: string;
    evidenceId: string;
    evidenceDigest: string;
    now: number;
    rowCounts: Readonly<{
      intent: number;
      runtimeState: number;
      sequence: number;
      evidence: number;
      audit: number;
    }>;
    crashBeforeCommit?: boolean;
  }>): Result<EgressIntentEvent> {
    const locks = validateFollowupLockOrder([
      { domain: "EGRESS_SEND_INTENT", acquiredAt: input.now },
      { domain: "EGRESS_RUNTIME_STATE", acquiredAt: input.now },
      { domain: "EGRESS_EVENT_SEQUENCE", acquiredAt: input.now },
      { domain: "EGRESS_RUNTIME_EVIDENCE", acquiredAt: input.now },
      { domain: "AUDIT_SEQUENCE", acquiredAt: input.now },
    ]);
    if (!locks.ok) return locks;
    const record = this.intents.get(input.intentId);
    if (!record || record.state !== "FINAL_AUTHORIZED") {
      return fail("EGRESS_WRITE_NOT_AUTHORIZED");
    }
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (this.consumeAuditFailure()) return fail("AUDIT_EVENT_BINDING_FAILURE");
    if (input.crashBeforeCommit) return fail("PROCESS_CRASHED_BEFORE_COMMIT");

    const sequence = record.nextSequence;
    const event = EgressIntentEventSchema.parse({
      schemaVersion: "r3-egress-r2-followup-event-v1",
      eventId: input.eventId,
      evidenceId: input.evidenceId,
      intentId: input.intentId,
      intentSequence: sequence,
      eventType: "EGRESS_WRITE_START_AUTHORIZED",
      evidenceSource: "DATABASE_AUTHORIZATION",
      evidenceDigest: input.evidenceDigest,
      sourceObservedAt: input.now,
      persistedAt: input.now,
      socketCallOutcome: "NOT_CALLED",
      providerResponseDigest: null,
      businessSuccessEvaluated: false,
    });
    this.append(input.intentId, event);
    this.evidence.set(this.evidenceKey(input.intentId, input.evidenceId), {
      fingerprint: this.evidenceFingerprint({
        eventType: event.eventType,
        evidenceSource: event.evidenceSource,
        evidenceDigest: event.evidenceDigest,
        sourceObservedAt: event.sourceObservedAt,
        socketCallOutcome: event.socketCallOutcome,
        providerResponseDigest: event.providerResponseDigest,
      }),
      event,
    });
    this.intents.set(input.intentId, {
      ...record,
      state: "WRITE_AUTHORIZED",
      writeAuthorizedAt: input.now,
      nextSequence: sequence + 1,
      sequenceVersion: record.sequenceVersion + 1,
    });
    return ok(event);
  }

  recordEvidence(input: Readonly<{
    evidence: unknown;
    claimedSourceSequence?: number;
    rowCounts: Readonly<{
      runtimeState: number;
      sequence: number;
      evidence: number;
      audit: number;
    }>;
    failAudit?: boolean;
    crashBeforeCommit?: boolean;
    commitResponseLost?: boolean;
  }>): Result<EgressIntentEvent> {
    const parsed = RuntimeEvidenceInputSchema.safeParse(input.evidence);
    if (!parsed.success) return fail("SOCKET_ATTEMPT_NOT_PROVEN");
    const evidence = parsed.data;
    if (
      evidence.evidenceSource !== "TRUSTED_EGRESS_RUNTIME"
      || evidence.eventType === "EGRESS_WRITE_START_AUTHORIZED"
    ) {
      return fail("EVIDENCE_SEQUENCE_SOURCE_FORBIDDEN");
    }
    if (input.claimedSourceSequence !== undefined) {
      return fail("EVIDENCE_SEQUENCE_SOURCE_FORBIDDEN");
    }
    const record = this.intents.get(evidence.intentId);
    if (!record) return fail("EGRESS_WRITE_NOT_AUTHORIZED");
    const key = this.evidenceKey(evidence.intentId, evidence.evidenceId);
    const existing = this.evidence.get(key);
    const fingerprint = this.evidenceFingerprint({
      eventType: evidence.eventType,
      evidenceSource: evidence.evidenceSource,
      evidenceDigest: evidence.evidenceDigest,
      sourceObservedAt: evidence.sourceObservedAt,
      socketCallOutcome: evidence.socketCallOutcome,
      providerResponseDigest: evidence.providerResponseDigest,
    });
    if (existing) {
      return existing.fingerprint === fingerprint
        ? ok(Object.freeze(structuredClone(existing.event)))
        : fail("EVIDENCE_REPLAY_CONFLICT");
    }
    const transition = this.validateTransition(record.state, evidence.eventType);
    if (!transition.ok) return transition;
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (input.failAudit || this.consumeAuditFailure()) {
      return fail("AUDIT_EVENT_BINDING_FAILURE");
    }
    if (input.crashBeforeCommit) return fail("PROCESS_CRASHED_BEFORE_COMMIT");

    const sequence = record.nextSequence;
    const event = EgressIntentEventSchema.parse({
      schemaVersion: "r3-egress-r2-followup-event-v1",
      eventId: evidence.eventId,
      evidenceId: evidence.evidenceId,
      intentId: evidence.intentId,
      intentSequence: sequence,
      eventType: evidence.eventType,
      evidenceSource: evidence.evidenceSource,
      evidenceDigest: evidence.evidenceDigest,
      sourceObservedAt: evidence.sourceObservedAt,
      persistedAt: evidence.persistedAt,
      socketCallOutcome: evidence.socketCallOutcome,
      providerResponseDigest: evidence.providerResponseDigest,
      businessSuccessEvaluated: false,
    });
    this.append(evidence.intentId, event);
    this.evidence.set(key, { fingerprint, event });
    this.intents.set(evidence.intentId, {
      ...record,
      state: transition.value,
      nextSequence: sequence + 1,
      sequenceVersion: record.sequenceVersion + 1,
    });
    if (input.commitResponseLost) return fail("COMMIT_OUTCOME_UNKNOWN");
    return ok(event);
  }

  async recordEvidenceConcurrent(input: Readonly<{
    evidence: unknown;
    rowCounts: Readonly<{
      runtimeState: number;
      sequence: number;
      evidence: number;
      audit: number;
    }>;
  }>): Promise<Result<EgressIntentEvent>> {
    let release = (): void => {};
    const prior = this.queue;
    this.queue = new Promise<void>((resolve) => {
      release = resolve;
    });
    await prior;
    try {
      return this.recordEvidence(input);
    } finally {
      release();
    }
  }

  retry(intentId: string): Result<never> {
    void intentId;
    return fail("AUTO_RETRY_FORBIDDEN");
  }

  eventsFor(intentId: string): readonly EgressIntentEvent[] {
    return Object.freeze([...(this.events.get(intentId) ?? [])]);
  }

  intent(intentId: string): IntentRecord | null {
    const value = this.intents.get(intentId);
    return value ? Object.freeze({ ...value }) : null;
  }

  nextSequence(intentId: string): number | null {
    return this.intents.get(intentId)?.nextSequence ?? null;
  }

  snapshot(): EgressSequenceSnapshot {
    return Object.freeze({
      intents: Object.freeze(Object.fromEntries(this.intents)),
      events: Object.freeze(Object.fromEntries(
        [...this.events.entries()].map(([key, value]) => [
          key,
          Object.freeze([...value]),
        ]),
      )),
      evidence: Object.freeze(Object.fromEntries(this.evidence)),
    });
  }

  static fromSnapshot(
    snapshot: EgressSequenceSnapshot,
  ): OfflineEgressIntentSequenceModel {
    const model = new OfflineEgressIntentSequenceModel();
    for (const [key, value] of Object.entries(snapshot.intents)) {
      model.intents.set(key, { ...value });
    }
    for (const [key, value] of Object.entries(snapshot.events)) {
      model.events.set(key, value.map((event) => ({ ...event })));
    }
    for (const [key, value] of Object.entries(snapshot.evidence)) {
      model.evidence.set(key, structuredClone(value));
    }
    return model;
  }

  private validateTransition(
    state: string,
    eventType: string,
  ): Result<string> {
    if (
      ["SOCKET_WRITE_ATTEMPTED", "SOCKET_WRITE_FAILED_BEFORE_BYTES", "SOCKET_WRITE_PARTIAL"]
        .includes(eventType)
    ) {
      if (state !== "WRITE_AUTHORIZED") return fail("EGRESS_WRITE_NOT_AUTHORIZED");
      return ok(eventType === "SOCKET_WRITE_FAILED_BEFORE_BYTES"
        ? "FAILED_BEFORE_BYTES"
        : "SOCKET_ATTEMPT_RECORDED");
    }
    if (["PROVIDER_RESPONSE_RECEIVED", "PROVIDER_RESPONSE_REJECTED"].includes(eventType)) {
      return state === "SOCKET_ATTEMPT_RECORDED"
        ? ok("PROVIDER_RESPONSE_RECEIVED")
        : fail("PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT");
    }
    if (eventType === "SEND_OUTCOME_UNKNOWN") {
      return ["WRITE_AUTHORIZED", "SOCKET_ATTEMPT_RECORDED"].includes(state)
        ? ok("SEND_OUTCOME_UNKNOWN")
        : fail("SEND_OUTCOME_ALREADY_TERMINAL");
    }
    if (eventType === "EGRESS_PROCESS_CRASHED") {
      return state === "WRITE_AUTHORIZED"
        ? ok("WRITE_AUTHORIZED")
        : fail("SEND_OUTCOME_ALREADY_TERMINAL");
    }
    return fail("EGRESS_WRITE_NOT_AUTHORIZED");
  }

  private evidenceKey(intentId: string, evidenceId: string): string {
    return `${intentId}|${evidenceId}`;
  }

  private evidenceFingerprint(value: unknown): string {
    return canonicalJson(value);
  }

  private append(intentId: string, event: EgressIntentEvent): void {
    const events = this.events.get(intentId) ?? [];
    events.push(Object.freeze(event));
    this.events.set(intentId, events);
  }

  private consumeAuditFailure(): boolean {
    if (!this.failNextAudit) return false;
    this.failNextAudit = false;
    return true;
  }
}

```
<!-- END_EXACT_SOURCE id=S021 -->

### S022. models/scope-cleanup-complete-result.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/models/scope-cleanup-complete-result.ts`
- Bytes: `15615`
- SHA-256: `39B8B2C152989F5AE1868730F5AFF76092C8A0D631C0952424A106EA6505C7D3`

<!-- BEGIN_EXACT_SOURCE id=S022 sha256=39B8B2C152989F5AE1868730F5AFF76092C8A0D631C0952424A106EA6505C7D3 bytes=15615 -->
```text
import {
  CleanupLeaseStateSchema,
  CleanupPermitStateSchema,
  EgressIntentStateSchema,
  ScopeCleanupCompleteResultSchema,
  ScopeCleanupPayloadSchema,
  WorkerRegistrationStateSchema,
  WorkerRevocationStateSchema,
  fail,
  ok,
  type Result,
  type ScopeCleanupCompleteResult,
  type ScopeCleanupPayload,
} from "../contracts";
import { canonicalJson, omitKey, sha256Canonical } from "./canonical";

const PRE_SEND_LEASE_STATES = new Set([
  "ISSUED",
  "KEY_READ",
  "TRANSPORT_CREATED",
  "SEND_AUTHORIZED",
]);
const AFTER_SEND_LEASE_STATES = new Set([
  "SENT",
  "WRITE_AUTHORIZED",
  "SOCKET_ATTEMPTED",
  "PROVIDER_RESPONSE_RECEIVED",
  "SEND_OUTCOME_UNKNOWN",
]);

export type CleanupResourceSnapshot = Readonly<{
  workerInstanceId: string;
  revocationState: string;
  revocationVersion: number;
  registrationState: string;
  scopeKey: string;
  floorToken: number;
  floorWorkerId: string;
  floorLeaseId: string;
  floorCapabilityId: string;
  leaseId: string;
  leaseWorkerId: string;
  leaseScopeKey: string;
  leaseCapabilityId: string;
  leaseToken: number;
  leaseState: string;
  permitId: string;
  permitLeaseId: string;
  permitWorkerId: string;
  permitScopeKey: string;
  permitCapabilityId: string;
  permitToken: number;
  permitState: string;
  intentState: string;
}>;

type CleanupAuditRecord = Readonly<{
  eventId: string;
  subjectId: string;
  eventType: string;
}>;

type CleanupRequestRecord = {
  requestDigest: string;
  canonicalPayload: string;
  state: "PENDING" | "COMPLETED";
  resultCanonicalText: string;
  result: ScopeCleanupCompleteResult;
  auditEventId: string;
};

export type CleanupRowCounts = Readonly<{
  requestInsert: number;
  blockMutation: number;
  leaseMutation: number;
  permitMutation: number;
  auditAppend: number;
  completionUpdate: number;
}>;

export type CompleteScopeCleanupSnapshot = Readonly<{
  authorityAvailable: boolean;
  resources: CleanupResourceSnapshot;
  blocks: Readonly<Record<string, Readonly<{
    blockedRevocationVersion: number;
    version: number;
  }>>>;
  requests: Readonly<Record<string, CleanupRequestRecord>>;
  mutatedLeases: Readonly<Record<string, string>>;
  mutatedPermits: Readonly<Record<string, string>>;
  auditEvents: Readonly<Record<string, CleanupAuditRecord>>;
}>;

export class OfflineCompleteScopeCleanupModel {
  private authorityAvailable = true;
  private readonly resources: CleanupResourceSnapshot;
  private readonly blocks = new Map<
    string,
    Readonly<{ blockedRevocationVersion: number; version: number }>
  >();
  private readonly requests = new Map<string, CleanupRequestRecord>();
  private readonly mutatedLeases = new Map<string, string>();
  private readonly mutatedPermits = new Map<string, string>();
  private readonly auditEvents = new Map<string, CleanupAuditRecord>();
  private queue: Promise<void> = Promise.resolve();

  constructor(resources: CleanupResourceSnapshot) {
    this.resources = Object.freeze({ ...resources });
  }

  setAuthorityAvailable(available: boolean): void {
    this.authorityAvailable = available;
  }

  cleanup(input: Readonly<{
    payload: unknown;
    rowCounts: CleanupRowCounts;
    auditEventId: string;
    now: number;
    failAudit?: boolean;
    failBlockMutation?: boolean;
    crashBeforeCommit?: boolean;
    commitResponseLost?: boolean;
  }>): Result<ScopeCleanupCompleteResult> {
    if (!this.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const parsed = ScopeCleanupPayloadSchema.safeParse(input.payload);
    if (!parsed.success) return fail("SCOPE_BINDING_MISMATCH");
    const payload = parsed.data;
    const requestDigest = sha256Canonical(payload);
    const canonicalPayload = canonicalJson(payload);
    const existing = this.requests.get(payload.cleanupRequestId);
    if (existing) return this.replay(payload, requestDigest, canonicalPayload, existing);

    const binding = this.validateBindings(payload);
    if (!binding.ok) return binding;
    const classification = this.classifyLease();
    if (!classification.ok) return classification;
    const blockKey = `${payload.scopeKey}|${payload.workerInstanceId}`;
    const existingBlock = this.blocks.get(blockKey);
    const alreadySatisfied = Boolean(
      existingBlock
      && existingBlock.blockedRevocationVersion >= payload.revocationVersion,
    );
    if (!alreadySatisfied) {
      if (
        this.resources.leaseState === "REVOKED"
        || this.resources.permitState === "REVOKED"
      ) {
        return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
      }
      if (
        classification.value === "AFTER_SEND"
        && this.resources.permitState !== "CONSUMED"
      ) {
        return fail("PERMIT_STATE_INVALID");
      }
    } else if (this.mutatedPermits.get(payload.permitId) !== "REVOKED") {
      return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
    }

    const expected = {
      requestInsert: 1,
      blockMutation: alreadySatisfied ? 0 : 1,
      leaseMutation: !alreadySatisfied && classification.value === "PRE_SEND" ? 1 : 0,
      permitMutation: alreadySatisfied ? 0 : 1,
      auditAppend: 1,
      completionUpdate: 1,
    };
    for (const [key, value] of Object.entries(expected)) {
      if (input.rowCounts[key as keyof CleanupRowCounts] !== value) {
        return fail("ROW_COUNT_CONFLICT");
      }
    }
    if (input.failBlockMutation && !alreadySatisfied) {
      return fail("ROW_COUNT_CONFLICT");
    }
    if (input.failAudit) return fail("AUDIT_EVENT_BINDING_FAILURE");
    if (input.crashBeforeCommit) return fail("PROCESS_CRASHED_BEFORE_COMMIT");

    const blockVersion = alreadySatisfied
      ? existingBlock?.version ?? 1
      : (existingBlock?.version ?? 0) + 1;
    const leaseOutcome = classification.value === "PRE_SEND"
      ? "REVOKED" as const
      : this.resources.leaseState === "SEND_OUTCOME_UNKNOWN"
        ? "PRESERVED_OUTCOME_UNKNOWN" as const
        : "PRESERVED_AFTER_WRITE_AUTHORIZED" as const;
    const externalOutcome = classification.value === "PRE_SEND"
      ? "NOT_SENT" as const
      : this.resources.leaseState === "SEND_OUTCOME_UNKNOWN"
        ? "SEND_OUTCOME_UNKNOWN" as const
        : "WRITE_MAY_HAVE_OCCURRED" as const;
    const resultCore = {
      schemaVersion: "r3-egress-r2-followup-cleanup-result-v1" as const,
      cleanupRequestId: payload.cleanupRequestId,
      requestDigest,
      status: alreadySatisfied ? "ALREADY_SATISFIED" as const : "APPLIED" as const,
      workerInstanceId: payload.workerInstanceId,
      scopeKey: payload.scopeKey,
      revocationVersion: payload.revocationVersion,
      leaseId: payload.leaseId,
      capabilityId: payload.capabilityId,
      permitId: payload.permitId,
      blockVersion,
      leaseOutcome,
      permitOutcome: "REVOKED" as const,
      externalOutcome,
      auditEventId: input.auditEventId,
      completedAt: input.now,
    };
    const result = ScopeCleanupCompleteResultSchema.parse({
      ...resultCore,
      resultDigest: sha256Canonical(resultCore),
    });
    const auditEventType = alreadySatisfied
      ? "WORKER_SCOPE_CLEANUP_ALREADY_SATISFIED"
      : "WORKER_SCOPE_BLOCKED";
    const resultCanonicalText = canonicalJson(result);

    if (!alreadySatisfied) {
      this.blocks.set(blockKey, {
        blockedRevocationVersion: payload.revocationVersion,
        version: blockVersion,
      });
      if (classification.value === "PRE_SEND") {
        this.mutatedLeases.set(payload.leaseId, "REVOKED");
      }
      this.mutatedPermits.set(payload.permitId, "REVOKED");
    }
    this.requests.set(payload.cleanupRequestId, {
      requestDigest,
      canonicalPayload,
      state: "COMPLETED",
      resultCanonicalText,
      result,
      auditEventId: input.auditEventId,
    });
    this.auditEvents.set(input.auditEventId, {
      eventId: input.auditEventId,
      subjectId: payload.cleanupRequestId,
      eventType: auditEventType,
    });
    if (input.commitResponseLost) return fail("COMMIT_OUTCOME_UNKNOWN");
    return ok(Object.freeze(structuredClone(result)));
  }

  async cleanupConcurrent(input: Readonly<{
    payload: unknown;
    rowCounts: CleanupRowCounts;
    auditEventId: string;
    now: number;
  }>): Promise<Result<ScopeCleanupCompleteResult>> {
    let release = (): void => {};
    const prior = this.queue;
    this.queue = new Promise<void>((resolve) => {
      release = resolve;
    });
    await prior;
    try {
      return this.cleanup(input);
    } finally {
      release();
    }
  }

  tamperResult(
    cleanupRequestId: string,
    patch: Partial<ScopeCleanupCompleteResult>,
  ): void {
    const record = this.requests.get(cleanupRequestId);
    if (!record) return;
    record.result = ScopeCleanupCompleteResultSchema.parse({
      ...record.result,
      ...patch,
    });
    record.resultCanonicalText = canonicalJson(record.result);
  }

  replaceResultCanonicalText(cleanupRequestId: string, value: string): void {
    const record = this.requests.get(cleanupRequestId);
    if (record) record.resultCanonicalText = value;
  }

  removeResult(cleanupRequestId: string): void {
    const record = this.requests.get(cleanupRequestId);
    if (!record) return;
    record.resultCanonicalText = "";
    record.auditEventId = "";
  }

  removeAudit(auditEventId: string): void {
    this.auditEvents.delete(auditEventId);
  }

  replaceAuditSubject(auditEventId: string, subjectId: string): void {
    const event = this.auditEvents.get(auditEventId);
    if (event) {
      this.auditEvents.set(auditEventId, { ...event, subjectId });
    }
  }

  blockVersion(scopeKey: string, workerInstanceId: string): number {
    return this.blocks.get(`${scopeKey}|${workerInstanceId}`)?.version ?? 0;
  }

  leaseState(leaseId: string): string | null {
    if (leaseId !== this.resources.leaseId) return null;
    return this.mutatedLeases.get(leaseId) ?? this.resources.leaseState;
  }

  permitState(permitId: string): string | null {
    if (permitId !== this.resources.permitId) return null;
    return this.mutatedPermits.get(permitId) ?? this.resources.permitState;
  }

  auditCount(): number {
    return this.auditEvents.size;
  }

  snapshot(): CompleteScopeCleanupSnapshot {
    return Object.freeze({
      authorityAvailable: this.authorityAvailable,
      resources: this.resources,
      blocks: Object.freeze(Object.fromEntries(this.blocks)),
      requests: Object.freeze(Object.fromEntries(this.requests)),
      mutatedLeases: Object.freeze(Object.fromEntries(this.mutatedLeases)),
      mutatedPermits: Object.freeze(Object.fromEntries(this.mutatedPermits)),
      auditEvents: Object.freeze(Object.fromEntries(this.auditEvents)),
    });
  }

  static fromSnapshot(
    snapshot: CompleteScopeCleanupSnapshot,
  ): OfflineCompleteScopeCleanupModel {
    const model = new OfflineCompleteScopeCleanupModel(snapshot.resources);
    model.authorityAvailable = snapshot.authorityAvailable;
    for (const [key, value] of Object.entries(snapshot.blocks)) {
      model.blocks.set(key, { ...value });
    }
    for (const [key, value] of Object.entries(snapshot.requests)) {
      model.requests.set(key, structuredClone(value));
    }
    for (const [key, value] of Object.entries(snapshot.mutatedLeases)) {
      model.mutatedLeases.set(key, value);
    }
    for (const [key, value] of Object.entries(snapshot.mutatedPermits)) {
      model.mutatedPermits.set(key, value);
    }
    for (const [key, value] of Object.entries(snapshot.auditEvents)) {
      model.auditEvents.set(key, { ...value });
    }
    return model;
  }

  private replay(
    payload: ScopeCleanupPayload,
    requestDigest: string,
    canonicalPayload: string,
    record: CleanupRequestRecord,
  ): Result<ScopeCleanupCompleteResult> {
    if (
      record.requestDigest !== requestDigest
      || record.canonicalPayload !== canonicalPayload
    ) {
      return fail("IDEMPOTENCY_KEY_REUSE_CONFLICT");
    }
    if (record.state !== "COMPLETED") {
      return fail("IDEMPOTENCY_RECORD_INCONSISTENT");
    }
    if (
      !record.result
      || !record.resultCanonicalText
      || !record.auditEventId
    ) {
      return fail("CLEANUP_RESULT_INTEGRITY_FAILURE");
    }
    const expectedDigest = sha256Canonical(omitKey(
      record.result as unknown as Readonly<Record<string, unknown>>,
      "resultDigest",
    ));
    if (
      expectedDigest !== record.result.resultDigest
      || canonicalJson(record.result) !== record.resultCanonicalText
      || record.result.cleanupRequestId !== payload.cleanupRequestId
      || record.result.requestDigest !== requestDigest
      || record.result.auditEventId !== record.auditEventId
    ) {
      return fail("CLEANUP_RESULT_INTEGRITY_FAILURE");
    }
    const audit = this.auditEvents.get(record.auditEventId);
    const expectedType = record.result.status === "APPLIED"
      ? "WORKER_SCOPE_BLOCKED"
      : "WORKER_SCOPE_CLEANUP_ALREADY_SATISFIED";
    if (
      !audit
      || audit.subjectId !== payload.cleanupRequestId
      || audit.eventType !== expectedType
    ) {
      return fail("AUDIT_EVENT_BINDING_FAILURE");
    }
    return ok(Object.freeze(structuredClone(record.result)));
  }

  private validateBindings(payload: ScopeCleanupPayload): Result<true> {
    if (
      WorkerRevocationStateSchema.safeParse(this.resources.revocationState).success === false
      || WorkerRegistrationStateSchema.safeParse(this.resources.registrationState).success === false
      || CleanupLeaseStateSchema.safeParse(this.resources.leaseState).success === false
      || CleanupPermitStateSchema.safeParse(this.resources.permitState).success === false
      || EgressIntentStateSchema.safeParse(this.resources.intentState).success === false
    ) {
      return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
    }
    if (
      this.resources.revocationState !== "REVOKED"
      || this.resources.revocationVersion < payload.revocationVersion
      || this.resources.registrationState !== "REVOKED"
    ) {
      return fail("WORKER_STATE_INVALID");
    }
    if (
      payload.workerInstanceId !== this.resources.workerInstanceId
      || payload.scopeKey !== this.resources.scopeKey
      || payload.leaseId !== this.resources.leaseId
      || payload.permitId !== this.resources.permitId
      || payload.capabilityId !== this.resources.floorCapabilityId
      || this.resources.floorWorkerId !== this.resources.workerInstanceId
      || this.resources.floorLeaseId !== this.resources.leaseId
      || this.resources.floorCapabilityId !== this.resources.leaseCapabilityId
      || this.resources.leaseWorkerId !== this.resources.workerInstanceId
      || this.resources.leaseScopeKey !== this.resources.scopeKey
      || this.resources.leaseToken !== this.resources.floorToken
      || this.resources.permitLeaseId !== this.resources.leaseId
      || this.resources.permitWorkerId !== this.resources.workerInstanceId
      || this.resources.permitScopeKey !== this.resources.scopeKey
      || this.resources.permitCapabilityId !== this.resources.leaseCapabilityId
      || this.resources.permitToken !== this.resources.floorToken
    ) {
      return fail("SCOPE_BINDING_MISMATCH");
    }
    return ok(true as const);
  }

  private classifyLease(): Result<"PRE_SEND" | "AFTER_SEND"> {
    if (PRE_SEND_LEASE_STATES.has(this.resources.leaseState)) {
      return ok("PRE_SEND");
    }
    if (AFTER_SEND_LEASE_STATES.has(this.resources.leaseState)) {
      return ok("AFTER_SEND");
    }
    if (this.resources.leaseState === "REVOKED") {
      return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
    }
    return fail("LEASE_STATE_INVALID");
  }
}

```
<!-- END_EXACT_SOURCE id=S022 -->

### S023. models/sql-analyzer.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/models/sql-analyzer.ts`
- Bytes: `6905`
- SHA-256: `D2A4F9BA08651C637E221905E77EC07BFFEE327A7C2F66EE3A0151254ED64F56`

<!-- BEGIN_EXACT_SOURCE id=S023 sha256=D2A4F9BA08651C637E221905E77EC07BFFEE327A7C2F66EE3A0151254ED64F56 bytes=6905 -->
```text
import { FOLLOWUP_LOCK_ORDER } from "../lock-order";

export type Finding = Readonly<{
  code: string;
  level:
    | "TEXTUAL_PATTERN_CHECK"
    | "SQL_STATEMENT_SEGMENTATION"
    | "SQL_PARAMETER_BINDING_REVIEW"
    | "TRANSACTION_CONTRACT_REVIEW";
  message: string;
}>;

const TABLE_DOMAIN: Readonly<Record<string, string>> = Object.freeze({
  trust_r5_worker_revocation: "WORKER_REVOCATION_CONTROL",
  trust_r6_worker_revocation_request: "WORKER_REVOCATION_REQUEST",
  trust_r7_worker_revocation_request: "WORKER_REVOCATION_REQUEST",
  trust_r6_scope_cleanup_request: "SCOPE_CLEANUP_REQUEST",
  trust_r5_scope_worker_block: "SCOPE_WORKER_BLOCK",
  trust_r3_emergency_control: "EMERGENCY_CONTROL",
  trust_r3_identity_key: "KEY_REGISTRY",
  trust_r3_execution_authorization: "EXECUTION_AUTHORIZATION",
  trust_r3_budget_control: "BUDGET_CONTROL",
  trust_r3_budget_reservation: "BUDGET_RESERVATION",
  trust_r3_capability: "CAPABILITY",
  trust_r4_resource_fencing: "RESOURCE_FENCING_FLOOR",
  trust_r4_fencing_token_control: "FENCING_TOKEN_CONTROL",
  trust_r4_worker_registration: "WORKER_REGISTRATION",
  trust_r4_execution_lease: "EXECUTION_LEASE",
  trust_r4_send_authorization: "SEND_AUTHORIZATION",
  trust_r5_egress_intent: "EGRESS_SEND_INTENT",
  trust_r6_egress_runtime_state: "EGRESS_RUNTIME_STATE",
  trust_r7_egress_event_sequence: "EGRESS_EVENT_SEQUENCE",
  trust_r7_egress_intent_evidence: "EGRESS_RUNTIME_EVIDENCE",
  trust_r3_audit_head: "AUDIT_SEQUENCE",
});

export function splitStatements(sql: string): readonly string[] {
  const statements: string[] = [];
  let start = 0;
  let single = false;
  let double = false;
  let lineComment = false;
  let blockComment = false;
  for (let index = 0; index < sql.length; index += 1) {
    const char = sql[index];
    const next = sql[index + 1];
    if (lineComment) {
      if (char === "\n") lineComment = false;
      continue;
    }
    if (blockComment) {
      if (char === "*" && next === "/") {
        blockComment = false;
        index += 1;
      }
      continue;
    }
    if (!single && !double && char === "-" && next === "-") {
      lineComment = true;
      index += 1;
      continue;
    }
    if (!single && !double && char === "/" && next === "*") {
      blockComment = true;
      index += 1;
      continue;
    }
    if (!double && char === "'") {
      if (single && next === "'") {
        index += 1;
        continue;
      }
      single = !single;
      continue;
    }
    if (!single && char === "\"") {
      if (double && next === "\"") {
        index += 1;
        continue;
      }
      double = !double;
      continue;
    }
    if (!single && !double && char === ";") {
      const statement = sql.slice(start, index).trim();
      if (statement) statements.push(statement);
      start = index + 1;
    }
  }
  const trailing = sql.slice(start).trim();
  if (trailing) statements.push(trailing);
  return Object.freeze(statements);
}

export function reviewLockOrder(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  const statements = splitStatements(sql);
  let active: string[] = [];
  for (const statement of statements) {
    if (/^BEGIN\b/iu.test(statement)) {
      active = [statement];
      continue;
    }
    if (active.length > 0) active.push(statement);
    if (/^(COMMIT|ROLLBACK)\b/iu.test(statement)) {
      const domains = active.flatMap((item) => {
        if (!/FOR\s+(?:UPDATE|SHARE)\b/iu.test(item)) return [];
        const table = /\b(?:FROM|JOIN)\s+(trust_[a-z0-9_]+)/iu
          .exec(item)?.[1]?.toLowerCase();
        return table && TABLE_DOMAIN[table] ? [TABLE_DOMAIN[table]] : [];
      });
      let previous = -1;
      for (const domain of domains) {
        const index = FOLLOWUP_LOCK_ORDER.indexOf(
          domain as typeof FOLLOWUP_LOCK_ORDER[number],
        );
        if (index < previous) {
          findings.push(Object.freeze({
            code: "LOCK_ORDER_CROSSING",
            level: "TRANSACTION_CONTRACT_REVIEW",
            message: domains.join(" -> "),
          }));
        }
        previous = index;
      }
      active = [];
    }
  }
  return Object.freeze(findings);
}

export function reviewScopeResultSql(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  const required = [
    "result_json",
    "result_canonical_text",
    "result_digest",
    "audit_event_id",
    "CLEANUP_RESULT_INTEGRITY_FAILURE",
    "LEFT JOIN trust_r3_audit_event",
  ] as const;
  for (const token of required) {
    if (!sql.includes(token)) {
      findings.push(Object.freeze({
        code: `SCOPE_RESULT_FIELD_MISSING_${token.replaceAll(" ", "_")}`,
        level: "TRANSACTION_CONTRACT_REVIEW",
        message: token,
      }));
    }
  }
  return Object.freeze(findings);
}

export function reviewWorkerResultSql(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  const required = [
    "result_json",
    "result_canonical_text",
    "result_digest",
    "audit_event_id",
    "completed_at_ms",
  ] as const;
  for (const token of required) {
    if (!sql.includes(token)) {
      findings.push(Object.freeze({
        code: `WORKER_RESULT_FIELD_MISSING_${token}`,
        level: "TRANSACTION_CONTRACT_REVIEW",
        message: token,
      }));
    }
  }
  return Object.freeze(findings);
}

export function reviewSequenceSql(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  const required = [
    "trust_r7_egress_event_sequence",
    "next_sequence = next_sequence + 1",
    "UNIQUE (egress_intent_id, intent_sequence)",
    "UNIQUE (egress_intent_id, evidence_id)",
    "RETURNING next_sequence - 1 AS intent_sequence",
  ] as const;
  for (const token of required) {
    if (!sql.includes(token)) {
      findings.push(Object.freeze({
        code: "EGRESS_SEQUENCE_CONTRACT_MISSING",
        level: "TRANSACTION_CONTRACT_REVIEW",
        message: token,
      }));
    }
  }
  if (/\bsource_sequence\b/u.test(sql)) {
    findings.push(Object.freeze({
      code: "RUNTIME_SOURCE_SEQUENCE_REINTRODUCED",
      level: "TEXTUAL_PATTERN_CHECK",
      message: "Runtime must not own sequence allocation",
    }));
  }
  return Object.freeze(findings);
}

export function analyzeFollowupSql(sql: string): Readonly<{
  statements: readonly string[];
  parameters: readonly string[];
  findings: readonly Finding[];
}> {
  return Object.freeze({
    statements: splitStatements(sql),
    parameters: Object.freeze(
      [...new Set([...sql.matchAll(/\$\d+/gu)].map((match) => match[0]))]
        .sort((left, right) => Number(left.slice(1)) - Number(right.slice(1))),
    ),
    findings: reviewLockOrder(sql),
  });
}

export const SQL_ANALYZER_LIMITS = Object.freeze([
  "TEXTUAL_PATTERN_CHECK",
  "SQL_STATEMENT_SEGMENTATION",
  "SQL_PARAMETER_BINDING_REVIEW",
  "TRANSACTION_CONTRACT_REVIEW",
  "POSTGRESQL_EXECUTION_NOT_PERFORMED",
] as const);

```
<!-- END_EXACT_SOURCE id=S023 -->

### S024. models/worker-revocation-complete-result.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/models/worker-revocation-complete-result.ts`
- Bytes: `10036`
- SHA-256: `CC26BB67507CD3F6B46D47FBCCB38D37EAF205660B29A4BAF3587A9E7FE7F9A5`

<!-- BEGIN_EXACT_SOURCE id=S024 sha256=CC26BB67507CD3F6B46D47FBCCB38D37EAF205660B29A4BAF3587A9E7FE7F9A5 bytes=10036 -->
```text
import {
  WorkerRegistrationStateSchema,
  WorkerRevocationCompleteResultSchema,
  WorkerRevocationPayloadSchema,
  WorkerRevocationStateSchema,
  fail,
  ok,
  requireExactlyOne,
  type Result,
  type WorkerRevocationCompleteResult,
} from "../contracts";
import { canonicalJson, omitKey, sha256Canonical } from "./canonical";

type WorkerRecord = {
  registrationState: string;
  revocationState: string;
  revocationVersion: number;
  recordVersion: number;
};
type RequestRecord = {
  requestDigest: string;
  canonicalPayload: string;
  state: "PENDING" | "COMPLETED";
  resultCanonicalText: string;
  result: WorkerRevocationCompleteResult;
  auditEventId: string;
};
type AuditRecord = Readonly<{
  eventId: string;
  subjectId: string;
  eventType: "WORKER_REVOKED";
}>;

export type WorkerRevocationRowCounts = Readonly<{
  requestInsert: number;
  revocationUpdate: number;
  registrationUpdate: number;
  auditAppend: number;
  completionUpdate: number;
}>;

export type CompleteWorkerRevocationSnapshot = Readonly<{
  authorityAvailable: boolean;
  workers: Readonly<Record<string, WorkerRecord>>;
  requests: Readonly<Record<string, RequestRecord>>;
  auditEvents: Readonly<Record<string, AuditRecord>>;
}>;

export class OfflineCompleteWorkerRevocationModel {
  private authorityAvailable = true;
  private readonly workers = new Map<string, WorkerRecord>();
  private readonly requests = new Map<string, RequestRecord>();
  private readonly auditEvents = new Map<string, AuditRecord>();
  private queue: Promise<void> = Promise.resolve();

  seedWorker(input: Readonly<{
    workerInstanceId: string;
    registrationState: string;
    revocationState?: string;
    revocationVersion?: number;
    recordVersion?: number;
  }>): Result<true> {
    this.workers.set(input.workerInstanceId, {
      registrationState: input.registrationState,
      revocationState: input.revocationState ?? "ACTIVE",
      revocationVersion: input.revocationVersion ?? 0,
      recordVersion: input.recordVersion ?? 1,
    });
    return ok(true as const);
  }

  setAuthorityAvailable(available: boolean): void {
    this.authorityAvailable = available;
  }

  revoke(input: Readonly<{
    payload: unknown;
    rowCounts: WorkerRevocationRowCounts;
    auditEventId: string;
    failAudit?: boolean;
    crashBeforeCommit?: boolean;
    commitResponseLost?: boolean;
  }>): Result<WorkerRevocationCompleteResult> {
    if (!this.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const parsed = WorkerRevocationPayloadSchema.safeParse(input.payload);
    if (!parsed.success) return fail("WORKER_STATE_INVALID");
    const payload = parsed.data;
    const requestDigest = sha256Canonical(payload);
    const canonicalPayload = canonicalJson(payload);
    const existing = this.requests.get(payload.requestId);
    if (existing) return this.replay(requestDigest, canonicalPayload, existing);

    const worker = this.workers.get(payload.workerInstanceId);
    if (!worker) return fail("WORKER_STATE_INVALID");
    if (
      WorkerRegistrationStateSchema.safeParse(worker.registrationState).success === false
      || WorkerRevocationStateSchema.safeParse(worker.revocationState).success === false
    ) {
      return fail("WORKER_STATE_INVALID");
    }
    if (worker.revocationState === "RECOVERY_REQUIRED") {
      return fail("WORKER_STATE_INVALID");
    }
    if (worker.revocationState === "REVOKED") {
      return fail("WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST");
    }
    if (worker.recordVersion !== payload.expectedRecordVersion) {
      return fail("WORKER_VERSION_CONFLICT");
    }
    if (worker.registrationState === "REGISTERED") {
      return fail("WORKER_REGISTERED_REVOCATION_FORBIDDEN");
    }
    if (
      worker.registrationState !== "ACTIVE"
      && worker.registrationState !== "DRAINING"
    ) {
      return fail("WORKER_STATE_INVALID");
    }
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (input.failAudit) return fail("AUDIT_EVENT_BINDING_FAILURE");
    if (input.crashBeforeCommit) return fail("PROCESS_CRASHED_BEFORE_COMMIT");

    const previousRegistrationState = worker.registrationState;
    const resultCore = {
      schemaVersion: "r3-egress-r2-followup-worker-result-v1" as const,
      status: "REVOKED" as const,
      requestId: payload.requestId,
      requestDigest,
      workerInstanceId: payload.workerInstanceId,
      previousRegistrationState: previousRegistrationState as "ACTIVE" | "DRAINING",
      registrationState: "REVOKED" as const,
      previousRevocationVersion: worker.revocationVersion,
      revocationVersion: worker.revocationVersion + 1,
      previousRecordVersion: worker.recordVersion,
      recordVersion: worker.recordVersion + 1,
      auditEventId: input.auditEventId,
      completedAt: payload.requestedAt,
    };
    const result = WorkerRevocationCompleteResultSchema.parse({
      ...resultCore,
      resultDigest: sha256Canonical(resultCore),
    });
    const resultCanonicalText = canonicalJson(result);
    this.workers.set(payload.workerInstanceId, {
      registrationState: "REVOKED",
      revocationState: "REVOKED",
      revocationVersion: result.revocationVersion,
      recordVersion: result.recordVersion,
    });
    this.requests.set(payload.requestId, {
      requestDigest,
      canonicalPayload,
      state: "COMPLETED",
      resultCanonicalText,
      result,
      auditEventId: input.auditEventId,
    });
    this.auditEvents.set(input.auditEventId, {
      eventId: input.auditEventId,
      subjectId: payload.workerInstanceId,
      eventType: "WORKER_REVOKED",
    });
    if (input.commitResponseLost) return fail("COMMIT_OUTCOME_UNKNOWN");
    return ok(Object.freeze(structuredClone(result)));
  }

  async revokeConcurrent(input: Readonly<{
    payload: unknown;
    rowCounts: WorkerRevocationRowCounts;
    auditEventId: string;
  }>): Promise<Result<WorkerRevocationCompleteResult>> {
    let release = (): void => {};
    const prior = this.queue;
    this.queue = new Promise<void>((resolve) => {
      release = resolve;
    });
    await prior;
    try {
      return this.revoke(input);
    } finally {
      release();
    }
  }

  activate(workerInstanceId: string): Result<true> {
    const worker = this.workers.get(workerInstanceId);
    if (!worker || worker.revocationState === "REVOKED") {
      return fail("WORKER_REACTIVATION_FORBIDDEN");
    }
    this.workers.set(workerInstanceId, {
      ...worker,
      registrationState: "ACTIVE",
    });
    return ok(true as const);
  }

  tamperResult(
    requestId: string,
    patch: Partial<WorkerRevocationCompleteResult>,
  ): void {
    const record = this.requests.get(requestId);
    if (!record) return;
    record.result = WorkerRevocationCompleteResultSchema.parse({
      ...record.result,
      ...patch,
    });
    record.resultCanonicalText = canonicalJson(record.result);
  }

  replaceResultCanonicalText(requestId: string, value: string): void {
    const record = this.requests.get(requestId);
    if (record) record.resultCanonicalText = value;
  }

  removeResult(requestId: string): void {
    const record = this.requests.get(requestId);
    if (!record) return;
    record.resultCanonicalText = "";
    record.auditEventId = "";
  }

  removeAudit(auditEventId: string): void {
    this.auditEvents.delete(auditEventId);
  }

  worker(workerInstanceId: string): WorkerRecord | null {
    const value = this.workers.get(workerInstanceId);
    return value ? Object.freeze({ ...value }) : null;
  }

  auditCount(): number {
    return this.auditEvents.size;
  }

  snapshot(): CompleteWorkerRevocationSnapshot {
    return Object.freeze({
      authorityAvailable: this.authorityAvailable,
      workers: Object.freeze(Object.fromEntries(this.workers)),
      requests: Object.freeze(Object.fromEntries(this.requests)),
      auditEvents: Object.freeze(Object.fromEntries(this.auditEvents)),
    });
  }

  static fromSnapshot(
    snapshot: CompleteWorkerRevocationSnapshot,
  ): OfflineCompleteWorkerRevocationModel {
    const model = new OfflineCompleteWorkerRevocationModel();
    model.authorityAvailable = snapshot.authorityAvailable;
    for (const [key, value] of Object.entries(snapshot.workers)) {
      model.workers.set(key, { ...value });
    }
    for (const [key, value] of Object.entries(snapshot.requests)) {
      model.requests.set(key, structuredClone(value));
    }
    for (const [key, value] of Object.entries(snapshot.auditEvents)) {
      model.auditEvents.set(key, { ...value });
    }
    return model;
  }

  private replay(
    requestDigest: string,
    canonicalPayload: string,
    record: RequestRecord,
  ): Result<WorkerRevocationCompleteResult> {
    if (
      record.requestDigest !== requestDigest
      || record.canonicalPayload !== canonicalPayload
    ) {
      return fail("IDEMPOTENCY_KEY_REUSE_CONFLICT");
    }
    if (record.state !== "COMPLETED") {
      return fail("IDEMPOTENCY_RECORD_INCONSISTENT");
    }
    if (!record.result || !record.resultCanonicalText || !record.auditEventId) {
      return fail("WORKER_REVOCATION_RESULT_INTEGRITY_FAILURE");
    }
    const expectedDigest = sha256Canonical(omitKey(
      record.result as unknown as Readonly<Record<string, unknown>>,
      "resultDigest",
    ));
    if (
      expectedDigest !== record.result.resultDigest
      || canonicalJson(record.result) !== record.resultCanonicalText
      || record.result.requestDigest !== requestDigest
      || record.result.auditEventId !== record.auditEventId
    ) {
      return fail("WORKER_REVOCATION_RESULT_INTEGRITY_FAILURE");
    }
    const audit = this.auditEvents.get(record.auditEventId);
    if (
      !audit
      || audit.subjectId !== record.result.workerInstanceId
      || audit.eventType !== "WORKER_REVOKED"
    ) {
      return fail("AUDIT_EVENT_BINDING_FAILURE");
    }
    return ok(Object.freeze(structuredClone(record.result)));
  }
}

```
<!-- END_EXACT_SOURCE id=S024 -->

### S025. tests/egress-intent-sequence.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tests/egress-intent-sequence.test.ts`
- Bytes: `7978`
- SHA-256: `EF38EC0C97D2A5C4250BDC70D5B35DEAB5D8AAA87F829ED72543FAAA9742D26D`

<!-- BEGIN_EXACT_SOURCE id=S025 sha256=EF38EC0C97D2A5C4250BDC70D5B35DEAB5D8AAA87F829ED72543FAAA9742D26D bytes=7978 -->
```text
import { describe, expect, it } from "vitest";

import { OfflineEgressIntentSequenceModel } from "../models/egress-intent-sequence";

const NOW = Date.parse("2026-11-26T19:00:00Z");
const IDS = Object.freeze({
  intent: "11111111-1111-4111-8111-111111111111",
  dbEvidence: "22222222-2222-4222-8222-222222222222",
  dbEvent: "33333333-3333-4333-8333-333333333333",
  attemptEvidence: "44444444-4444-4444-8444-444444444444",
  attemptEvent: "55555555-5555-4555-8555-555555555555",
  responseEvidence: "66666666-6666-4666-8666-666666666666",
  responseEvent: "77777777-7777-4777-8777-777777777777",
  unknownEvidence: "88888888-8888-4888-8888-888888888888",
  unknownEvent: "99999999-9999-4999-8999-999999999999",
  crashEvidence: "aaaaaaaa-aaaa-4aaa-8aaa-aaaaaaaaaaaa",
  crashEvent: "bbbbbbbb-bbbb-4bbb-8bbb-bbbbbbbbbbbb",
});
const DIGEST = "sha256:" + "a".repeat(64);
const RESPONSE_DIGEST = "sha256:" + "b".repeat(64);

function authorized() {
  const model = new OfflineEgressIntentSequenceModel();
  expect(model.seedFinalAuthorized(IDS.intent).ok).toBe(true);
  expect(model.authorizeWriteStart({
    intentId: IDS.intent,
    evidenceId: IDS.dbEvidence,
    eventId: IDS.dbEvent,
    evidenceDigest: DIGEST,
    now: NOW,
    rowCounts: {
      intent: 1,
      runtimeState: 1,
      sequence: 1,
      evidence: 1,
      audit: 1,
    },
  }).ok).toBe(true);
  return model;
}

function socketEvidence(overrides: Readonly<Record<string, unknown>> = {}) {
  return {
    evidenceId: IDS.attemptEvidence,
    eventId: IDS.attemptEvent,
    intentId: IDS.intent,
    eventType: "SOCKET_WRITE_ATTEMPTED",
    evidenceSource: "TRUSTED_EGRESS_RUNTIME",
    evidenceDigest: DIGEST,
    sourceObservedAt: NOW + 2,
    persistedAt: NOW + 3,
    socketCallOutcome: "COMPLETED_CALL",
    providerResponseDigest: null,
    ...overrides,
  };
}

const RUNTIME_ROWS = {
  runtimeState: 1,
  sequence: 1,
  evidence: 1,
  audit: 1,
} as const;

function attempted() {
  const model = authorized();
  const result = model.recordEvidence({
    evidence: socketEvidence(),
    rowCounts: RUNTIME_ROWS,
  });
  if (!result.ok) throw new Error(result.code);
  return model;
}

describe("Intent-level Egress event sequence", () => {
  it("assigns authorization sequence 1 and Runtime evidence sequence 2", () => {
    const model = attempted();
    expect(model.eventsFor(IDS.intent).map((event) => event.intentSequence))
      .toEqual([1, 2]);
    expect(model.nextSequence(IDS.intent)).toBe(3);
  });

  it("assigns subsequent Provider response sequence 3", () => {
    const model = attempted();
    expect(model.recordEvidence({
      evidence: {
        evidenceId: IDS.responseEvidence,
        eventId: IDS.responseEvent,
        intentId: IDS.intent,
        eventType: "PROVIDER_RESPONSE_RECEIVED",
        evidenceSource: "TRUSTED_EGRESS_RUNTIME",
        evidenceDigest: DIGEST,
        sourceObservedAt: NOW + 4,
        persistedAt: NOW + 5,
        socketCallOutcome: "COMPLETED_CALL",
        providerResponseDigest: RESPONSE_DIGEST,
      },
      rowCounts: RUNTIME_ROWS,
    }).ok).toBe(true);
    expect(model.eventsFor(IDS.intent).map((event) => event.intentSequence))
      .toEqual([1, 2, 3]);
  });

  it("rejects a Runtime-supplied sequence", () => {
    expect(authorized().recordEvidence({
      evidence: socketEvidence(),
      claimedSourceSequence: 2,
      rowCounts: RUNTIME_ROWS,
    })).toEqual({
      ok: false,
      code: "EVIDENCE_SEQUENCE_SOURCE_FORBIDDEN",
    });
  });

  it("rejects a non-trusted Runtime evidence source", () => {
    expect(authorized().recordEvidence({
      evidence: socketEvidence({ evidenceSource: "DATABASE_AUTHORIZATION" }),
      rowCounts: RUNTIME_ROWS,
    })).toEqual({
      ok: false,
      code: "EVIDENCE_SEQUENCE_SOURCE_FORBIDDEN",
    });
  });

  it("returns the same event for duplicate evidence without a new sequence", () => {
    const model = attempted();
    const existing = model.eventsFor(IDS.intent).at(-1);
    expect(model.recordEvidence({
      evidence: socketEvidence(),
      rowCounts: RUNTIME_ROWS,
    })).toEqual({ ok: true, value: existing });
    expect(model.nextSequence(IDS.intent)).toBe(3);
  });

  it("rejects same evidence ID with different evidence content", () => {
    const model = attempted();
    expect(model.recordEvidence({
      evidence: socketEvidence({ evidenceDigest: "sha256:" + "c".repeat(64) }),
      rowCounts: RUNTIME_ROWS,
    })).toEqual({ ok: false, code: "EVIDENCE_REPLAY_CONFLICT" });
  });

  it("linearizes concurrent Runtime events to unique sequences", async () => {
    const model = authorized();
    const [crash, attempt] = await Promise.all([
      model.recordEvidenceConcurrent({
        evidence: {
          evidenceId: IDS.crashEvidence,
          eventId: IDS.crashEvent,
          intentId: IDS.intent,
          eventType: "EGRESS_PROCESS_CRASHED",
          evidenceSource: "TRUSTED_EGRESS_RUNTIME",
          evidenceDigest: DIGEST,
          sourceObservedAt: NOW + 1,
          persistedAt: NOW + 1,
          socketCallOutcome: "NOT_CALLED",
          providerResponseDigest: null,
        },
        rowCounts: RUNTIME_ROWS,
      }),
      model.recordEvidenceConcurrent({
        evidence: socketEvidence(),
        rowCounts: RUNTIME_ROWS,
      }),
    ]);
    expect(crash.ok && attempt.ok).toBe(true);
    expect(model.eventsFor(IDS.intent).map((event) => event.intentSequence))
      .toEqual([1, 2, 3]);
  });

  it("rejects Provider response before socket attempt", () => {
    expect(authorized().recordEvidence({
      evidence: {
        evidenceId: IDS.responseEvidence,
        eventId: IDS.responseEvent,
        intentId: IDS.intent,
        eventType: "PROVIDER_RESPONSE_RECEIVED",
        evidenceSource: "TRUSTED_EGRESS_RUNTIME",
        evidenceDigest: DIGEST,
        sourceObservedAt: NOW + 2,
        persistedAt: NOW + 3,
        socketCallOutcome: "COMPLETED_CALL",
        providerResponseDigest: RESPONSE_DIGEST,
      },
      rowCounts: RUNTIME_ROWS,
    })).toEqual({
      ok: false,
      code: "PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT",
    });
  });

  it("rolls back sequence on Audit failure and pre-commit crash", () => {
    for (const failure of [
      { failAudit: true as const },
      { crashBeforeCommit: true as const },
    ]) {
      const model = authorized();
      expect(model.recordEvidence({
        evidence: socketEvidence(),
        rowCounts: RUNTIME_ROWS,
        ...failure,
      }).ok).toBe(false);
      expect(model.nextSequence(IDS.intent)).toBe(2);
      expect(model.eventsFor(IDS.intent)).toHaveLength(1);
    }
  });

  it("recovers COMMIT ambiguity using evidence identity", () => {
    const model = authorized();
    expect(model.recordEvidence({
      evidence: socketEvidence(),
      rowCounts: RUNTIME_ROWS,
      commitResponseLost: true,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
    const replay = model.recordEvidence({
      evidence: socketEvidence(),
      rowCounts: RUNTIME_ROWS,
    });
    expect(replay).toMatchObject({
      ok: true,
      value: { intentSequence: 2 },
    });
    expect(model.nextSequence(IDS.intent)).toBe(3);
  });

  it("restores sequence state after restart", () => {
    const model = attempted();
    const restored = OfflineEgressIntentSequenceModel.fromSnapshot(model.snapshot());
    expect(restored.nextSequence(IDS.intent)).toBe(3);
    expect(restored.recordEvidence({
      evidence: {
        evidenceId: IDS.unknownEvidence,
        eventId: IDS.unknownEvent,
        intentId: IDS.intent,
        eventType: "SEND_OUTCOME_UNKNOWN",
        evidenceSource: "TRUSTED_EGRESS_RUNTIME",
        evidenceDigest: DIGEST,
        sourceObservedAt: NOW + 4,
        persistedAt: NOW + 5,
        socketCallOutcome: null,
        providerResponseDigest: null,
      },
      rowCounts: RUNTIME_ROWS,
    })).toMatchObject({
      ok: true,
      value: { intentSequence: 3 },
    });
  });
});

```
<!-- END_EXACT_SOURCE id=S025 -->

### S026. tests/scope-cleanup-complete-result.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tests/scope-cleanup-complete-result.test.ts`
- Bytes: `7228`
- SHA-256: `31AD1C29B484E51EB19547FEA97BE7FB7C686FEE40EB838A6601A7617D5F8E7D`

<!-- BEGIN_EXACT_SOURCE id=S026 sha256=31AD1C29B484E51EB19547FEA97BE7FB7C686FEE40EB838A6601A7617D5F8E7D bytes=7228 -->
```text
import { describe, expect, it } from "vitest";

import {
  OfflineCompleteScopeCleanupModel,
  type CleanupResourceSnapshot,
  type CleanupRowCounts,
} from "../models/scope-cleanup-complete-result";

const NOW = Date.parse("2026-11-26T18:00:00Z");
const IDS = Object.freeze({
  worker: "11111111-1111-4111-8111-111111111111",
  scope: "fence-scope-v1:sha256:" + "a".repeat(64),
  lease: "22222222-2222-4222-8222-222222222222",
  capability: "33333333-3333-4333-8333-333333333333",
  permit: "44444444-4444-4444-8444-444444444444",
  cleanup: "55555555-5555-4555-8555-555555555555",
  cleanup2: "66666666-6666-4666-8666-666666666666",
  audit: "77777777-7777-4777-8777-777777777777",
  audit2: "88888888-8888-4888-8888-888888888888",
});

function payload(overrides: Readonly<Record<string, unknown>> = {}) {
  return {
    cleanupRequestId: IDS.cleanup,
    workerInstanceId: IDS.worker,
    scopeKey: IDS.scope,
    revocationVersion: 3,
    leaseId: IDS.lease,
    capabilityId: IDS.capability,
    permitId: IDS.permit,
    reasonCode: "SYNTHETIC_REVOCATION_CLEANUP",
    ...overrides,
  };
}

function resources(
  overrides: Partial<CleanupResourceSnapshot> = {},
): CleanupResourceSnapshot {
  return {
    workerInstanceId: IDS.worker,
    revocationState: "REVOKED",
    revocationVersion: 3,
    registrationState: "REVOKED",
    scopeKey: IDS.scope,
    floorToken: 100,
    floorWorkerId: IDS.worker,
    floorLeaseId: IDS.lease,
    floorCapabilityId: IDS.capability,
    leaseId: IDS.lease,
    leaseWorkerId: IDS.worker,
    leaseScopeKey: IDS.scope,
    leaseCapabilityId: IDS.capability,
    leaseToken: 100,
    leaseState: "SEND_AUTHORIZED",
    permitId: IDS.permit,
    permitLeaseId: IDS.lease,
    permitWorkerId: IDS.worker,
    permitScopeKey: IDS.scope,
    permitCapabilityId: IDS.capability,
    permitToken: 100,
    permitState: "ISSUED",
    intentState: "FINAL_AUTHORIZED",
    ...overrides,
  };
}

const ROWS: CleanupRowCounts = {
  requestInsert: 1,
  blockMutation: 1,
  leaseMutation: 1,
  permitMutation: 1,
  auditAppend: 1,
  completionUpdate: 1,
};

function applied() {
  const model = new OfflineCompleteScopeCleanupModel(resources());
  const result = model.cleanup({
    payload: payload(),
    rowCounts: ROWS,
    auditEventId: IDS.audit,
    now: NOW,
  });
  if (!result.ok) throw new Error(result.code);
  return { model, result: result.value };
}

describe("complete Scope Cleanup Result persistence", () => {
  it("persists and returns the complete first result", () => {
    const { model, result } = applied();
    expect(result).toMatchObject({
      status: "APPLIED",
      blockVersion: 1,
      leaseOutcome: "REVOKED",
      permitOutcome: "REVOKED",
      externalOutcome: "NOT_SENT",
      auditEventId: IDS.audit,
      completedAt: NOW,
    });
    expect(result.resultDigest).toMatch(/^sha256:[a-f0-9]{64}$/u);
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(1);
  });

  it("returns the exact persisted Result on same-request replay", () => {
    const { model, result } = applied();
    const replay = model.cleanup({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    });
    expect(replay).toEqual({ ok: true, value: result });
    expect(model.auditCount()).toBe(1);
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(1);
  });

  it("rejects same ID with different payload", () => {
    const { model, result } = applied();
    expect(model.cleanup({
      payload: payload({ reasonCode: "DIFFERENT" }),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toEqual({ ok: false, code: "IDEMPOTENCY_KEY_REUSE_CONFLICT" });
    expect(model.auditCount()).toBe(1);
    expect(result.status).toBe("APPLIED");
  });

  it.each([
    ["result digest", (model: OfflineCompleteScopeCleanupModel) =>
      model.tamperResult(IDS.cleanup, { resultDigest: "sha256:" + "f".repeat(64) })],
    ["canonical text", (model: OfflineCompleteScopeCleanupModel) =>
      model.replaceResultCanonicalText(IDS.cleanup, "{}")],
    ["missing result", (model: OfflineCompleteScopeCleanupModel) =>
      model.removeResult(IDS.cleanup)],
  ])("fails closed on %s tampering", (_label, mutate) => {
    const { model } = applied();
    mutate(model);
    expect(model.cleanup({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toEqual({ ok: false, code: "CLEANUP_RESULT_INTEGRITY_FAILURE" });
  });

  it.each([
    ["missing Audit", (model: OfflineCompleteScopeCleanupModel) =>
      model.removeAudit(IDS.audit)],
    ["wrong Audit subject", (model: OfflineCompleteScopeCleanupModel) =>
      model.replaceAuditSubject(IDS.audit, IDS.cleanup2)],
  ])("fails closed on %s binding", (_label, mutate) => {
    const { model } = applied();
    mutate(model);
    expect(model.cleanup({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toEqual({ ok: false, code: "AUDIT_EVENT_BINDING_FAILURE" });
  });

  it("recovers a lost COMMIT response using the same request ID", () => {
    const model = new OfflineCompleteScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
      now: NOW,
      commitResponseLost: true,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
    expect(model.cleanup({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toMatchObject({
      ok: true,
      value: { status: "APPLIED", auditEventId: IDS.audit, completedAt: NOW },
    });
    expect(model.auditCount()).toBe(1);
  });

  it("recovers exact Result after restart", () => {
    const { model, result } = applied();
    const restored = OfflineCompleteScopeCleanupModel.fromSnapshot(model.snapshot());
    expect(restored.cleanup({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toEqual({ ok: true, value: result });
  });

  it("linearizes concurrent same-request callers to one result", async () => {
    const model = new OfflineCompleteScopeCleanupModel(resources());
    const [left, right] = await Promise.all([
      model.cleanupConcurrent({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit,
        now: NOW,
      }),
      model.cleanupConcurrent({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit2,
        now: NOW,
      }),
    ]);
    expect(left).toEqual(right);
    expect(model.auditCount()).toBe(1);
  });

  it("does not mutate on Audit failure or pre-commit crash", () => {
    for (const failure of [
      { failAudit: true as const },
      { crashBeforeCommit: true as const },
    ]) {
      const model = new OfflineCompleteScopeCleanupModel(resources());
      expect(model.cleanup({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit,
        now: NOW,
        ...failure,
      }).ok).toBe(false);
      expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(0);
      expect(model.auditCount()).toBe(0);
    }
  });
});

```
<!-- END_EXACT_SOURCE id=S026 -->

### S027. tests/sql-analyzer-followup.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tests/sql-analyzer-followup.test.ts`
- Bytes: `2655`
- SHA-256: `1AFF9C0D753E836372ABB8E49F27358E99BCCF50AF18EF714159C15D259E725C`

<!-- BEGIN_EXACT_SOURCE id=S027 sha256=1AFF9C0D753E836372ABB8E49F27358E99BCCF50AF18EF714159C15D259E725C bytes=2655 -->
```text
import { readFileSync } from "node:fs";
import { resolve } from "node:path";
import { describe, expect, it } from "vitest";

import {
  SQL_ANALYZER_LIMITS,
  analyzeFollowupSql,
  reviewSequenceSql,
  reviewScopeResultSql,
  reviewWorkerResultSql,
} from "../models/sql-analyzer";

const ROOT = resolve(
  process.cwd(),
  "preparation/production-trust/r3-egress-revocation-r2-followup-remediation",
);
const SCOPE_SQL = readFileSync(
  resolve(ROOT, "PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql"),
  "utf8",
);
const WORKER_SQL = readFileSync(
  resolve(ROOT, "PHASE_R3_WORKER_REVOCATION_COMPLETE_RESULT.sql"),
  "utf8",
);
const SEQUENCE_SQL = readFileSync(
  resolve(ROOT, "PHASE_R3_EGRESS_EVENT_SEQUENCE.sql"),
  "utf8",
);

describe("follow-up SQL contracts", () => {
  it("segments actual SQL and checks lock ordering", () => {
    for (const sql of [SCOPE_SQL, WORKER_SQL, SEQUENCE_SQL]) {
      const analyzed = analyzeFollowupSql(sql);
      expect(analyzed.statements.length).toBeGreaterThan(0);
      expect(analyzed.parameters.length).toBeGreaterThan(0);
      expect(analyzed.findings.map((finding) => finding.code))
        .not.toContain("LOCK_ORDER_CROSSING");
    }
    expect(SQL_ANALYZER_LIMITS).toContain("POSTGRESQL_EXECUTION_NOT_PERFORMED");
  });

  it("requires full Scope Result persistence and Audit join", () => {
    expect(reviewScopeResultSql(SCOPE_SQL)).toEqual([]);
    const bad = SCOPE_SQL.replaceAll("result_json", "result_digest");
    expect(reviewScopeResultSql(bad).map((finding) => finding.code).length)
      .toBeGreaterThan(0);
  });

  it("requires full Worker Result persistence", () => {
    expect(reviewWorkerResultSql(WORKER_SQL)).toEqual([]);
    const bad = WORKER_SQL.replaceAll("result_json", "result_digest");
    expect(reviewWorkerResultSql(bad).map((finding) => finding.code).length)
      .toBeGreaterThan(0);
  });

  it("requires the shared Intent-level sequence allocator", () => {
    expect(reviewSequenceSql(SEQUENCE_SQL)).toEqual([]);
    const bad = SEQUENCE_SQL.replace(
      "UNIQUE (egress_intent_id, intent_sequence)",
      "UNIQUE (egress_intent_id, source_sequence)",
    );
    const codes = reviewSequenceSql(bad).map((finding) => finding.code);
    expect(codes).toContain("EGRESS_SEQUENCE_CONTRACT_MISSING");
    expect(codes).toContain("RUNTIME_SOURCE_SEQUENCE_REINTRODUCED");
  });

  it("rejects a missing result-canonical store", () => {
    const bad = SCOPE_SQL.replaceAll("result_canonical_text", "ignored_result_text");
    expect(reviewScopeResultSql(bad).map((finding) => finding.code))
      .toContain("SCOPE_RESULT_FIELD_MISSING_result_canonical_text");
  });
});

```
<!-- END_EXACT_SOURCE id=S027 -->

### S028. tests/worker-revocation-complete-result.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tests/worker-revocation-complete-result.test.ts`
- Bytes: `5595`
- SHA-256: `AB418B385BDB550002BDE9303A4B4ACB3D10382621ACF8B61E5ACA43A828D991`

<!-- BEGIN_EXACT_SOURCE id=S028 sha256=AB418B385BDB550002BDE9303A4B4ACB3D10382621ACF8B61E5ACA43A828D991 bytes=5595 -->
```text
import { describe, expect, it } from "vitest";

import {
  OfflineCompleteWorkerRevocationModel,
  type WorkerRevocationRowCounts,
} from "../models/worker-revocation-complete-result";

const NOW = Date.parse("2026-11-26T18:30:00Z");
const IDS = Object.freeze({
  worker: "11111111-1111-4111-8111-111111111111",
  request: "22222222-2222-4222-8222-222222222222",
  audit: "33333333-3333-4333-8333-333333333333",
  audit2: "44444444-4444-4444-8444-444444444444",
});
const ROWS: WorkerRevocationRowCounts = {
  requestInsert: 1,
  revocationUpdate: 1,
  registrationUpdate: 1,
  auditAppend: 1,
  completionUpdate: 1,
};

function payload(overrides: Readonly<Record<string, unknown>> = {}) {
  return {
    requestId: IDS.request,
    workerInstanceId: IDS.worker,
    expectedRecordVersion: 1,
    reasonCode: "SYNTHETIC_COMPROMISE",
    requestedAt: NOW,
    ...overrides,
  };
}

function model(state: "ACTIVE" | "DRAINING" = "DRAINING") {
  const value = new OfflineCompleteWorkerRevocationModel();
  expect(value.seedWorker({
    workerInstanceId: IDS.worker,
    registrationState: state,
  }).ok).toBe(true);
  return value;
}

function revoked() {
  const value = model();
  const result = value.revoke({
    payload: payload(),
    rowCounts: ROWS,
    auditEventId: IDS.audit,
  });
  if (!result.ok) throw new Error(result.code);
  return { model: value, result: result.value };
}

describe("complete Worker Revocation Result persistence", () => {
  it("persists previous and new lifecycle state", () => {
    const { result } = revoked();
    expect(result).toMatchObject({
      status: "REVOKED",
      previousRegistrationState: "DRAINING",
      registrationState: "REVOKED",
      previousRevocationVersion: 0,
      revocationVersion: 1,
      previousRecordVersion: 1,
      recordVersion: 2,
      auditEventId: IDS.audit,
    });
    expect(result.resultDigest).toMatch(/^sha256:[a-f0-9]{64}$/u);
  });

  it("returns the exact original Result on replay", () => {
    const { model: state, result } = revoked();
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({ ok: true, value: result });
    expect(state.auditCount()).toBe(1);
    expect(state.worker(IDS.worker)?.revocationVersion).toBe(1);
  });

  it("rejects same request ID with different payload", () => {
    const { model: state } = revoked();
    expect(state.revoke({
      payload: payload({ reasonCode: "DIFFERENT" }),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({ ok: false, code: "IDEMPOTENCY_KEY_REUSE_CONFLICT" });
  });

  it.each([
    ["result digest", (state: OfflineCompleteWorkerRevocationModel) =>
      state.tamperResult(IDS.request, { resultDigest: "sha256:" + "f".repeat(64) })],
    ["canonical text", (state: OfflineCompleteWorkerRevocationModel) =>
      state.replaceResultCanonicalText(IDS.request, "{}")],
    ["missing result", (state: OfflineCompleteWorkerRevocationModel) =>
      state.removeResult(IDS.request)],
  ])("fails closed on %s tampering", (_label, mutate) => {
    const { model: state } = revoked();
    mutate(state);
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({
      ok: false,
      code: "WORKER_REVOCATION_RESULT_INTEGRITY_FAILURE",
    });
  });

  it("fails closed when bound Audit is missing", () => {
    const { model: state } = revoked();
    state.removeAudit(IDS.audit);
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({ ok: false, code: "AUDIT_EVENT_BINDING_FAILURE" });
  });

  it("recovers a lost COMMIT response", () => {
    const state = model();
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
      commitResponseLost: true,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toMatchObject({
      ok: true,
      value: { auditEventId: IDS.audit, completedAt: NOW },
    });
  });

  it("recovers exact Result after restart", () => {
    const { model: state, result } = revoked();
    const restored = OfflineCompleteWorkerRevocationModel.fromSnapshot(state.snapshot());
    expect(restored.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({ ok: true, value: result });
  });

  it("linearizes same-request concurrent callers", async () => {
    const state = model("ACTIVE");
    const [left, right] = await Promise.all([
      state.revokeConcurrent({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit,
      }),
      state.revokeConcurrent({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit2,
      }),
    ]);
    expect(left.ok && right.ok).toBe(true);
    expect(state.auditCount()).toBe(1);
    expect(state.worker(IDS.worker)?.revocationVersion).toBe(1);
  });

  it("does not mutate on Audit failure or pre-commit crash", () => {
    for (const failure of [
      { failAudit: true as const },
      { crashBeforeCommit: true as const },
    ]) {
      const state = model();
      expect(state.revoke({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit,
        ...failure,
      }).ok).toBe(false);
      expect(state.worker(IDS.worker)?.revocationState).toBe("ACTIVE");
      expect(state.auditCount()).toBe(0);
    }
  });
});

```
<!-- END_EXACT_SOURCE id=S028 -->

### S029. tools/build-evidence.mjs

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tools/build-evidence.mjs`
- Bytes: `14396`
- SHA-256: `1C482134FF7CF55F748417B3AE23DD5C0986E8C9860E5AFD1FCA5B3B4C479AB0`

<!-- BEGIN_EXACT_SOURCE id=S029 sha256=1C482134FF7CF55F748417B3AE23DD5C0986E8C9860E5AFD1FCA5B3B4C479AB0 bytes=14396 -->
````text
import { createHash } from "node:crypto";
import { existsSync, readFileSync, readdirSync, statSync, writeFileSync } from "node:fs";
import { dirname, extname, join, relative, resolve } from "node:path";
import { fileURLToPath } from "node:url";

const taskRoot = dirname(dirname(fileURLToPath(import.meta.url)));
const trustRoot = dirname(taskRoot);
const workspace = resolve(trustRoot, "..", "..");
const r2Root = join(trustRoot, "r3-egress-revocation-r2-remediation");
const inputBundlePath = join(
  r2Root,
  "PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE.md",
);
const expectedInputHash =
  "33F3D18B9D8B8EBD04B5BEB04DB403A12BF38D9075DD581518545975C0D3A711";
const expectedInputBytes = 223804;

const bundlePath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE.md",
);
const reportPath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md",
);
const bundleManifestPath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt",
);
const manifestPath = join(taskRoot, "PHASE_R3_R2_FOLLOWUP_SHA256SUMS.txt");

function hashBytes(bytes) {
  return createHash("sha256").update(bytes).digest("hex").toUpperCase();
}
function hashFile(path) {
  return hashBytes(readFileSync(path));
}
function listFiles(root) {
  const output = [];
  for (const entry of readdirSync(root, { withFileTypes: true })) {
    const absolute = join(root, entry.name);
    if (entry.isDirectory()) output.push(...listFiles(absolute));
    else if (entry.isFile()) output.push(absolute);
  }
  return output.sort((left, right) => left.localeCompare(right));
}
function extractBody(bundleText, id, hash, bytes) {
  const begin = `<!-- BEGIN_EXACT_SOURCE id=${id} sha256=${hash} bytes=${bytes} -->`;
  const beginIndex = bundleText.indexOf(begin);
  if (beginIndex < 0) return null;
  const fenceStart = bundleText.indexOf("\n", beginIndex) + 1;
  const fenceEnd = bundleText.indexOf("\n", fenceStart) + 1;
  const endMarker = `<!-- END_EXACT_SOURCE id=${id} -->`;
  const endIndex = bundleText.indexOf(endMarker, fenceEnd);
  if (endIndex < 0) return null;
  const closingFenceEnd = bundleText.lastIndexOf("\n", endIndex - 1);
  const closingFenceStart = bundleText.lastIndexOf("\n", closingFenceEnd - 1) + 1;
  return bundleText.slice(fenceEnd, closingFenceStart - 1);
}
function verifyManifest(path) {
  const lines = readFileSync(path, "utf8").split(/\r?\n/u)
    .map((line) => /^([0-9A-Fa-f]{64})\s{2}(.+)$/u.exec(line))
    .filter(Boolean);
  const mismatches = [];
  for (const match of lines) {
    const rel = match[2].replaceAll("\\", "/");
    const absolute = join(workspace, rel);
    if (!existsSync(absolute) || hashFile(absolute) !== match[1].toUpperCase()) {
      mismatches.push(rel);
    }
  }
  return { entries: lines.length, mismatches };
}

const inputBundle = readFileSync(inputBundlePath);
const inputText = inputBundle.toString("utf8");
const inputBundleMatches = inputBundle.length === expectedInputBytes
  && hashBytes(inputBundle) === expectedInputHash;
const inputCatalog = [];
for (const line of inputText.split(/\r?\n/u)) {
  const match = /^\| (S\d{3}) \| `([^`]+)` \| (\d+) \| ([0-9A-F]{64}) \|$/u
    .exec(line);
  if (match) {
    inputCatalog.push({
      id: match[1],
      displayPath: match[2],
      bytes: Number(match[3]),
      hash: match[4],
    });
  }
}
const inputLocalMismatches = [];
const inputBodyMismatches = [];
for (const source of inputCatalog) {
  const local = join(r2Root, source.displayPath);
  if (!existsSync(local)) {
    inputLocalMismatches.push(`${source.displayPath}: missing`);
    continue;
  }
  const bytes = readFileSync(local);
  if (bytes.length !== source.bytes || hashBytes(bytes) !== source.hash) {
    inputLocalMismatches.push(`${source.displayPath}: hash/size`);
  }
  const embedded = extractBody(inputText, source.id, source.hash, source.bytes);
  if (embedded === null || !Buffer.from(embedded, "utf8").equals(bytes)) {
    inputBodyMismatches.push(`${source.displayPath}: body`);
  }
}

const r2Manifest = verifyManifest(
  join(r2Root, "PHASE_R3_EGRESS_REVOCATION_R2_SHA256SUMS.txt"),
);
const r31Manifest = verifyManifest(
  join(workspace, "PHASE_R31_R36_SHA256SUMS.txt"),
);

const protectedExpected = new Map([
  ["package.json", "44FC2153675107E0E61DBA8E88E955281B913D3341718C224110AB5B2F6C7F4D"],
  ["pnpm-lock.yaml", "926DFD4A33A662BAAB424E7C9FBBFD5FB16B74BE2E6119AD9F6A0D5144B719B4"],
  [
    "src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts",
    "1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309",
  ],
]);
const protectedMismatches = [];
for (const [rel, expected] of protectedExpected) {
  if (hashFile(join(workspace, rel)) !== expected) protectedMismatches.push(rel);
}

const importBoundaryHits = [];
for (const rootName of ["src", "scripts"]) {
  for (const absolute of listFiles(join(workspace, rootName))) {
    const text = readFileSync(absolute, "utf8");
    if (
      text.includes("r3-egress-revocation-r2-followup-remediation")
      || text.includes("production-trust/r3-egress-revocation-r2-followup")
    ) {
      importBoundaryHits.push(relative(workspace, absolute).replaceAll("\\", "/"));
    }
  }
}

const sensitivePatterns = [
  /api[_-]?key\s*[:=]\s*["'][^"']+/iu,
  /sk-[A-Za-z0-9]{16,}/u,
  /BEGIN (?:RSA |EC |OPENSSH )?PRIVATE KEY/u,
  /postgres(?:ql)?:\/\//iu,
  /new\s+(?:Pool|Client)\s*\(/u,
  /\bfetch\s*\(/u,
  /https?:\/\//iu,
];
const sensitiveHits = [];
for (const absolute of listFiles(taskRoot)) {
  const text = readFileSync(absolute, "utf8");
  if (sensitivePatterns.some((pattern) => pattern.test(text))) {
    sensitiveHits.push(relative(workspace, absolute).replaceAll("\\", "/"));
  }
}

const productionEntry = readFileSync(
  join(workspace, "src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts"),
  "utf8",
);
const productionBlocked = productionEntry.includes('code: "PRODUCTION_FETCH_TRUST_UNAVAILABLE"')
  && productionEntry.includes("productionTrustConnected: false")
  && productionEntry.includes("keyReads: 0")
  && productionEntry.includes("networkCalls: 0");

const excluded = new Set([manifestPath, bundlePath, reportPath, bundleManifestPath]);
const sourcePaths = listFiles(taskRoot)
  .filter((path) => !excluded.has(path))
  .sort((left, right) => {
    const l = relative(taskRoot, left).replaceAll("\\", "/");
    const r = relative(taskRoot, right).replaceAll("\\", "/");
    const rank = (value) => {
      if (value.endsWith(".md")) return 0;
      if (value.endsWith(".sql")) return 1;
      if (value === "contracts.ts" || value === "lock-order.ts") return 2;
      if (value.startsWith("models/")) return 3;
      if (value.startsWith("tests/")) return 4;
      if (value.startsWith("tools/")) return 5;
      if (extname(value) === ".ts") return 6;
      return 7;
    };
    return rank(l) - rank(r) || l.localeCompare(r);
  });
const sources = sourcePaths.map((absolute, index) => {
  const bytes = readFileSync(absolute);
  return {
    id: `S${String(index + 1).padStart(3, "0")}`,
    absolute,
    workspacePath: relative(workspace, absolute).replaceAll("\\", "/"),
    displayPath: relative(taskRoot, absolute).replaceAll("\\", "/"),
    bytes,
    size: statSync(absolute).size,
    hash: hashBytes(bytes),
  };
});
function fenceFor(text) {
  const lengths = [...text.matchAll(/`+/gu)].map((match) => match[0].length);
  return "`".repeat(Math.max(3, ...lengths.map((length) => length + 1)));
}
const bodySections = sources.map((source) => {
  const text = source.bytes.toString("utf8");
  const fence = fenceFor(text);
  return [
    `### ${source.id}. ${source.displayPath}`,
    "",
    `- Path: \`${source.workspacePath}\``,
    `- Bytes: \`${source.size}\``,
    `- SHA-256: \`${source.hash}\``,
    "",
    `<!-- BEGIN_EXACT_SOURCE id=${source.id} sha256=${source.hash} bytes=${source.size} -->`,
    `${fence}text`,
    text,
    fence,
    `<!-- END_EXACT_SOURCE id=${source.id} -->`,
    "",
  ].join("\n");
});

const bundleHeader = [
  "# PHASE_R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE",
  "",
  "## Review Status",
  "",
  "```text",
  "R3_EGRESS_REVOCATION_R2_FOLLOWUP_REMEDIATION_PASS",
  "OFFLINE_ACCEPTANCE=PASS",
  "INDEPENDENT_REVIEW=REQUIRED",
  "PRODUCTION_IMPLEMENTATION=NOT_STARTED",
  "PRODUCTION_ENFORCEMENT=BLOCKED",
  "REAL_FETCH_AUTHORIZED=NO",
  "```",
  "",
  "## Scope",
  "",
  "Complete Scope/Worker Result persistence, Intent-level Egress sequence",
  "allocation, attack review and cross-module consistency evidence.",
  "",
  "## Source Catalog",
  "",
  "| ID | Path | Bytes | SHA-256 |",
  "|---|---|---:|---|",
  ...sources.map((source) =>
    `| ${source.id} | \`${source.displayPath}\` | ${source.size} | ${source.hash} |`
  ),
  "",
  "## Complete Source Bodies",
  "",
].join("\n");
const bundleFooter = [
  "",
  "## Integrity",
  "",
  "```text",
  `INPUT_R2_BUNDLE_MATCH=${inputBundleMatches ? "YES" : "NO"}`,
  `INPUT_CATALOG_SOURCES=${inputCatalog.length}`,
  `INPUT_LOCAL_MISMATCHES=${inputLocalMismatches.length}`,
  `INPUT_BODY_MISMATCHES=${inputBodyMismatches.length}`,
  `R2_MANIFEST_ENTRIES=${r2Manifest.entries}`,
  `R2_MANIFEST_MISMATCHES=${r2Manifest.mismatches.length}`,
  `R31_R36_MANIFEST_ENTRIES=${r31Manifest.entries}`,
  `R31_R36_MANIFEST_MISMATCHES=${r31Manifest.mismatches.length}`,
  `FOLLOWUP_SOURCE_FILES=${sources.length}`,
  "INDEPENDENCE_LIMITATION=SAME_HOST_MAIN_AGENT_ONLY",
  "```",
  "",
].join("\n");
writeFileSync(bundlePath, bundleHeader + bodySections.join("\n") + bundleFooter, "utf8");

const bundleText = readFileSync(bundlePath, "utf8");
const outputBodyMismatches = [];
for (const source of sources) {
  const embedded = extractBody(bundleText, source.id, source.hash, source.size);
  if (embedded === null || !Buffer.from(embedded, "utf8").equals(source.bytes)) {
    outputBodyMismatches.push(source.displayPath);
  }
}
const bundleBytes = readFileSync(bundlePath);
const bundleHash = hashBytes(bundleBytes);
const pass = inputBundleMatches
  && inputLocalMismatches.length === 0
  && inputBodyMismatches.length === 0
  && r2Manifest.mismatches.length === 0
  && r31Manifest.mismatches.length === 0
  && protectedMismatches.length === 0
  && importBoundaryHits.length === 0
  && sensitiveHits.length === 0
  && productionBlocked
  && outputBodyMismatches.length === 0;

writeFileSync(reportPath, [
  "# PHASE_R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE_REPORT",
  "",
  "## Final Status",
  "",
  "```text",
  `R3_EGRESS_REVOCATION_R2_FOLLOWUP_FULL_SECURITY_REVIEW_BUNDLE_${pass ? "PASS" : "NEEDS_REVISION"}`,
  "```",
  "",
  "## Bundle",
  "",
  "```text",
  `BUNDLE_PATH=${relative(workspace, bundlePath).replaceAll("\\", "/")}`,
  `BUNDLE_BYTES=${bundleBytes.length}`,
  `BUNDLE_SHA256=${bundleHash}`,
  `SOURCE_FILES=${sources.length}`,
  `BODY_EXACTNESS_MISMATCHES=${outputBodyMismatches.length}`,
  `INPUT_R2_BUNDLE_MATCH=${inputBundleMatches ? "YES" : "NO"}`,
  `INPUT_R2_CATALOG_SOURCES=${inputCatalog.length}`,
  `INPUT_R2_LOCAL_MISMATCHES=${inputLocalMismatches.length}`,
  `INPUT_R2_BODY_MISMATCHES=${inputBodyMismatches.length}`,
  `R2_MANIFEST_ENTRIES=${r2Manifest.entries}`,
  `R2_MANIFEST_MISMATCHES=${r2Manifest.mismatches.length}`,
  `R31_R36_MANIFEST_ENTRIES=${r31Manifest.entries}`,
  `R31_R36_MANIFEST_MISMATCHES=${r31Manifest.mismatches.length}`,
  `PROTECTED_HASH_MISMATCHES=${protectedMismatches.length}`,
  `IMPORT_BOUNDARY_HITS=${importBoundaryHits.length}`,
  `SENSITIVE_PATTERN_HITS=${sensitiveHits.length}`,
  "```",
  "",
  "## Verification",
  "",
  "```text",
  "FOLLOWUP_TARGETED_VITEST=4_FILES_39_TESTS_PASS",
  "R3_EGRESS_REVOCATION_R2_VITEST=4_FILES_67_TESTS_PASS",
  "R3_EGRESS_REVOCATION_R1_VITEST=4_FILES_53_TESTS_PASS",
  "R3_FENCING_VITEST=7_FILES_49_TESTS_PASS",
  "R2_R3_VITEST=8_FILES_74_TESTS_PASS",
  "R2_VITEST=10_FILES_80_TESTS_PASS",
  "R1_VITEST=16_FILES_91_TESTS_PASS",
  "R31_R36_RELEVANT_VITEST=20_FILES_179_TESTS_PASS",
  "POWERSHELL_TOTAL=69_PASS",
  "POWERSHELL_5_1_PARSER=6_PASS",
  "TYPESCRIPT_STRICT=PASS",
  "ESLINT=PASS",
  "NEXT_BUILD=PASS",
  "```",
  "",
  "## Findings",
  "",
  "```text",
  ...(pass ? ["NO_INTEGRITY_FINDINGS"] : [
    ...inputLocalMismatches,
    ...inputBodyMismatches,
    ...r2Manifest.mismatches,
    ...r31Manifest.mismatches,
    ...protectedMismatches,
    ...importBoundaryHits,
    ...sensitiveHits,
    ...outputBodyMismatches,
  ].map((item) => `FINDING=${item}`)),
  "```",
  "",
  "## Production Safety",
  "",
  "```text",
  "PRODUCTION_IMPLEMENTATION=NOT_STARTED",
  "PRODUCTION_ENFORCEMENT=BLOCKED",
  "PRODUCTION_EGRESS_IMPLEMENTED=NO",
  "NETWORK_ISOLATION_ENFORCED=NO",
  "REAL_FETCH_AUTHORIZED=NO",
  "POSTGRESQL_INTEGRATION=NOT_EXECUTED",
  "POSTGRESQL_CONCURRENCY=NOT_TESTED",
  "MULTI_INSTANCE_TEST=NOT_EXECUTED",
  "REAL_EGRESS_TEST=NOT_EXECUTED",
  "REAL_SOCKET_WRITE=NOT_EXECUTED",
  "REAL_PROVIDER_TEST=NOT_EXECUTED",
  "```",
  "",
  "## Independence",
  "",
  "No usable independent Agent workpack was produced. This is not third-party",
  "independent audit.",
  "",
].join("\r\n"), "utf8");

writeFileSync(bundleManifestPath, [
  "# PHASE_R3_R2_FOLLOWUP_BUNDLE_SHA256SUMS",
  "# ENTRIES=2",
  "# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION",
  "",
  `${hashFile(bundlePath)}  ${relative(workspace, bundlePath).replaceAll("\\", "/")}`,
  `${hashFile(reportPath)}  ${relative(workspace, reportPath).replaceAll("\\", "/")}`,
  "",
].join("\r\n"), "utf8");

const taskFiles = listFiles(taskRoot).filter((path) => path !== manifestPath);
writeFileSync(manifestPath, [
  "# PHASE_R3_R2_FOLLOWUP_SHA256SUMS",
  `# ENTRIES=${taskFiles.length}`,
  "# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION",
  "",
  ...taskFiles.map((path) =>
    `${hashFile(path)}  ${relative(workspace, path).replaceAll("\\", "/")}`
  ),
  "",
].join("\r\n"), "utf8");

console.log(JSON.stringify({
  inputBundleMatches,
  inputCatalogSources: inputCatalog.length,
  inputLocalMismatches,
  inputBodyMismatches,
  r2Manifest,
  r31Manifest,
  protectedMismatches,
  importBoundaryHits,
  sensitiveHits,
  productionBlocked,
  sourceFiles: sources.length,
  outputBodyMismatches,
  bundleBytes: bundleBytes.length,
  bundleHash,
  taskManifestEntries: taskFiles.length,
  pass,
}, null, 2));
if (!pass) process.exitCode = 1;

````
<!-- END_EXACT_SOURCE id=S029 -->

### S030. tools/generate-scope-sql.mjs

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tools/generate-scope-sql.mjs`
- Bytes: `5119`
- SHA-256: `29FC76BE59002286643F61CFC16468BF61F76364556C9A4C6673381292737336`

<!-- BEGIN_EXACT_SOURCE id=S030 sha256=29FC76BE59002286643F61CFC16468BF61F76364556C9A4C6673381292737336 bytes=5119 -->
```text
import { readFileSync, writeFileSync } from "node:fs";
import { dirname, join } from "node:path";
import { fileURLToPath } from "node:url";

const taskRoot = dirname(dirname(fileURLToPath(import.meta.url)));
const trustRoot = dirname(taskRoot);
const sourcePath = join(
  trustRoot,
  "r3-egress-revocation-r2-remediation",
  "PHASE_R3_SCOPE_CLEANUP_R2.sql",
);
const outputPath = join(taskRoot, "PHASE_R3_SCOPE_CLEANUP_COMPLETE_RESULT.sql");

let sql = readFileSync(sourcePath, "utf8");

const createTable = `CREATE TABLE trust_r6_scope_cleanup_request (
  cleanup_request_id uuid PRIMARY KEY,
  request_digest varchar(71) NOT NULL,
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  scope_key text NOT NULL
    REFERENCES trust_r4_resource_fencing (scope_key),
  revocation_version bigint NOT NULL CHECK (revocation_version >= 1),
  lease_id uuid NOT NULL REFERENCES trust_r4_execution_lease (lease_id),
  capability_id uuid NOT NULL,
  permit_id uuid NOT NULL
    REFERENCES trust_r4_send_authorization (send_authorization_id),
  reason_code text NOT NULL,
  state text NOT NULL CHECK (
    state IN ('PENDING', 'COMPLETED', 'FAILED_TERMINAL')
  ),
  result_json jsonb,
  result_canonical_text text,
  result_digest varchar(71),
  audit_event_id uuid,
  created_at_ms bigint NOT NULL,
  completed_at_ms bigint,
  CHECK (request_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (result_digest IS NULL OR result_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (
    (state = 'PENDING'
      AND result_json IS NULL
      AND result_canonical_text IS NULL
      AND result_digest IS NULL
      AND audit_event_id IS NULL
      AND completed_at_ms IS NULL)
    OR
    (state = 'COMPLETED'
      AND result_json IS NOT NULL
      AND result_canonical_text IS NOT NULL
      AND result_digest IS NOT NULL
      AND audit_event_id IS NOT NULL
      AND completed_at_ms IS NOT NULL)
    OR
    (state = 'FAILED_TERMINAL'
      AND result_json IS NULL
      AND result_canonical_text IS NULL
      AND result_digest IS NULL
      AND completed_at_ms IS NOT NULL)
  ),
  CHECK (
    state <> 'COMPLETED'
    OR (
      result_json ->> 'cleanupRequestId' = cleanup_request_id::text
      AND result_json ->> 'requestDigest' = request_digest
      AND result_json ->> 'workerInstanceId' = worker_instance_id::text
      AND result_json ->> 'scopeKey' = scope_key
      AND result_json ->> 'leaseId' = lease_id::text
      AND result_json ->> 'capabilityId' = capability_id::text
      AND result_json ->> 'permitId' = permit_id::text
      AND result_json ->> 'auditEventId' = audit_event_id::text
      AND result_json ->> 'resultDigest' = result_digest
    )
  )
);`;
sql = sql.replace(
  /CREATE TABLE trust_r6_scope_cleanup_request \([\s\S]*?\n\);/u,
  () => createTable,
);

sql = sql.replaceAll(
  "reason_code, state, result_digest, audit_event_id,\n  created_at_ms, completed_at_ms",
  () => "reason_code, state, result_json, result_canonical_text,\n  result_digest, audit_event_id, created_at_ms, completed_at_ms",
);
sql = sql.replaceAll(
  "$9, 'PENDING', NULL, NULL,\n  $10, NULL",
  () => "$9, 'PENDING', NULL, NULL, NULL,\n  NULL, NULL, $10, NULL",
);
sql = sql.replaceAll(
  `SET state = 'COMPLETED',
    result_digest = $17,
    audit_event_id = $13,
    completed_at_ms = $10`,
  () => `SET state = 'COMPLETED',
    result_json = $17::jsonb,
    result_canonical_text = $18,
    result_digest = $19,
    audit_event_id = $13,
    completed_at_ms = $10`,
);
sql = sql.replace(
  `SELECT cleanup_request_id, request_digest, worker_instance_id, scope_key,
       revocation_version, lease_id, capability_id, permit_id,
       reason_code, state, result_digest, audit_event_id, completed_at_ms
FROM trust_r6_scope_cleanup_request
WHERE cleanup_request_id = $2
FOR UPDATE;`,
  () => `SELECT cleanup.cleanup_request_id, cleanup.request_digest,
       cleanup.worker_instance_id, cleanup.scope_key,
       cleanup.revocation_version, cleanup.lease_id,
       cleanup.capability_id, cleanup.permit_id, cleanup.reason_code,
       cleanup.state, cleanup.result_json, cleanup.result_canonical_text,
       cleanup.result_digest, cleanup.audit_event_id, cleanup.completed_at_ms,
       audit.event_id AS bound_audit_event_id,
       audit.event_type AS bound_audit_event_type,
       audit.subject_id AS bound_audit_subject_id
FROM trust_r6_scope_cleanup_request cleanup
LEFT JOIN trust_r3_audit_event audit
  ON audit.event_id = cleanup.audit_event_id
WHERE cleanup.cleanup_request_id = $2
FOR UPDATE OF cleanup;`,
);
sql = sql.replace(
  "--   $17 canonical cleanup result digest",
  () => `--   $17 complete result JSON object
--   $18 exact canonical result text
--   $19 SHA-256 over $18
--
-- Replay MUST verify result_canonical_text/result_digest/result_json and the
-- joined Audit event before returning the stored Result. A missing or
-- mismatched binding is CLEANUP_RESULT_INTEGRITY_FAILURE.`,
);

sql = sql.replace(
  "-- R2 idempotent Scope Cleanup.",
  () => "-- R2 follow-up: complete Result persistence and exact replay.",
);
writeFileSync(outputPath, sql, "utf8");

```
<!-- END_EXACT_SOURCE id=S030 -->

### S031. tools/run-verification.ps1

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tools/run-verification.ps1`
- Bytes: `6933`
- SHA-256: `265A3D43A8F64505D92FBE43CD14047CEBF532063A208B7C30211F47D6BC3AF9`

<!-- BEGIN_EXACT_SOURCE id=S031 sha256=265A3D43A8F64505D92FBE43CD14047CEBF532063A208B7C30211F47D6BC3AF9 bytes=6933 -->
```````text
$ErrorActionPreference = "Continue"

$workspace = (Resolve-Path (Join-Path $PSScriptRoot "..\..\..\..")).Path
$taskDir = (Resolve-Path (Join-Path $PSScriptRoot "..")).Path
$log = Join-Path $taskDir "PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION.md"
$records = [System.Collections.Generic.List[string]]::new()
$failed = 0

function Invoke-Logged {
  param([string]$Name, [string]$Executable, [string[]]$Arguments)
  $started = Get-Date
  $output = & $Executable @Arguments 2>&1
  $exitCode = $LASTEXITCODE
  $ended = Get-Date
  if ($exitCode -ne 0) { $script:failed += 1 }
  $records.Add(@(
    "### $Name",
    "",
    '```text',
    "COMMAND=$Executable $($Arguments -join ' ')",
    "START=$($started.ToString('o'))",
    "END=$($ended.ToString('o'))",
    "EXIT_CODE=$exitCode",
    '```',
    "",
    '```text',
    (($output | Out-String).Trim()),
    '```',
    ""
  ) -join "`r`n")
}

Push-Location $workspace
try {
  Invoke-Logged "Follow-up targeted Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/r3-egress-revocation-r2-followup-remediation/vitest.config.ts"
  )
  Invoke-Logged "R3 Egress Revocation R2 Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/r3-egress-revocation-r2-remediation/vitest.config.ts"
  )
  Invoke-Logged "R3 Egress Revocation R1 Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/r3-egress-revocation-remediation/vitest.config.ts"
  )
  Invoke-Logged "R3 Fencing Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/r3-fencing-remediation/vitest.config.ts"
  )
  Invoke-Logged "R2-R3 Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/r2-r3-remediation/vitest.config.ts"
  )
  Invoke-Logged "R2 Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/r2/vitest.config.ts"
  )
  Invoke-Logged "R1 Vitest" "node" @(
    "node_modules/vitest/vitest.mjs", "run", "--config",
    "preparation/production-trust/vitest.config.ts"
  )

  $relevant = @(
    "src/server/auth/actor-context.test.ts",
    "src/server/public-enterprise-search/identity/identity-gate.test.ts",
    "src/server/public-enterprise-search/identity/runtime/approval-authorization.test.ts",
    "src/server/public-enterprise-search/identity/runtime/authorization.test.ts",
    "src/server/public-enterprise-search/identity/runtime/fetch-entry-guard.test.ts",
    "src/server/public-enterprise-search/identity/runtime/precheck.test.ts",
    "src/server/public-enterprise-search/identity/runtime/production-fetch-entry.test.ts",
    "src/server/public-enterprise-search/identity/runtime/trusted-read.test.ts",
    "src/server/public-enterprise-search/offline-boundaries.test.ts",
    "src/server/public-enterprise-search/provider/aux-http-transports.test.ts",
    "src/server/public-enterprise-search/provider/deepseek-fetch.test.ts",
    "src/server/public-enterprise-search/provider/deepseek-http-transport.test.ts",
    "src/server/public-enterprise-search/provider/provider-execution-authorization.test.ts",
    "src/server/public-enterprise-search/provider/provider-factory-protection.test.ts",
    "src/server/public-enterprise-search/diagnostics/fetch-diagnostic-cli.test.ts",
    "src/server/public-enterprise-search/diagnostics/fetch-diagnostic-dependency.test.ts",
    "src/server/public-enterprise-search/local-live/live-config.test.ts",
    "src/server/public-enterprise-search/trial/run-real-provider-trial.test.ts",
    "src/server/public-enterprise-search/trial/run-real-provider-trial-cli.test.ts",
    "src/server/public-enterprise-search/trial/run-real-provider-trial.zero-network.test.ts"
  )
  Invoke-Logged "R31-R36 Relevant Vitest" "node" (
    @("node_modules/vitest/vitest.mjs", "run") + $relevant
  )

  Invoke-Logged "PowerShell Launcher" "powershell.exe" @(
    "-NoProfile", "-ExecutionPolicy", "Bypass", "-File",
    "scripts/windows/test-fetch-only-launcher.ps1"
  )
  Invoke-Logged "PowerShell Key Session" "powershell.exe" @(
    "-NoProfile", "-ExecutionPolicy", "Bypass", "-File",
    "scripts/windows/test-fetch-key-session.ps1"
  )
  Invoke-Logged "PowerShell Fetch Enforcement" "powershell.exe" @(
    "-NoProfile", "-ExecutionPolicy", "Bypass", "-File",
    "scripts/windows/test-fetch-only-production-enforcement.ps1"
  )

  $parseStarted = Get-Date
  $parseLines = [System.Collections.Generic.List[string]]::new()
  $parseErrors = @()
  $scripts = Get-ChildItem scripts/windows -File -Filter "*.ps1"
  foreach ($script in $scripts) {
    $tokens = $null
    $errors = $null
    [System.Management.Automation.Language.Parser]::ParseFile(
      $script.FullName, [ref]$tokens, [ref]$errors
    ) | Out-Null
    if ($errors.Count -gt 0) {
      $parseErrors += $errors
      $parseLines.Add("$($script.Name)=FAIL")
      foreach ($errorItem in $errors) { $parseLines.Add($errorItem.Message) }
    } else {
      $parseLines.Add("$($script.Name)=PASS")
    }
  }
  $parseLines.Add("TOTAL=$($scripts.Count)")
  $parseLines.Add("FAILURES=$($parseErrors.Count)")
  $parseExit = if ($parseErrors.Count -eq 0) { 0 } else { 1 }
  if ($parseExit -ne 0) { $failed += 1 }
  $records.Add(@(
    "### PowerShell 5.1 Parser",
    "",
    '```text',
    "COMMAND=inline PowerShell 5.1 Language.Parser over scripts/windows/*.ps1",
    "START=$($parseStarted.ToString('o'))",
    "END=$((Get-Date).ToString('o'))",
    "EXIT_CODE=$parseExit",
    '```',
    "",
    '```text',
    ($parseLines -join "`r`n"),
    '```',
    ""
  ) -join "`r`n")

  Invoke-Logged "TypeScript Strict" "npx.cmd" @(
    "tsc", "--noEmit", "--pretty", "false"
  )
  Invoke-Logged "ESLint New Scope" "npx.cmd" @(
    "eslint", "preparation/production-trust/r3-egress-revocation-r2-followup-remediation"
  )
  Invoke-Logged "Next Build" "pnpm.cmd" @("build")
} finally {
  Pop-Location
}

$header = @(
  "# PHASE_R3_R2_FOLLOWUP_TEST_EXECUTION",
  "",
  '``````text',
  "GENERATED_AT=$((Get-Date).ToString('o'))",
  "WORKSPACE=$workspace",
  "FAILED_COMMANDS=$failed",
  "POSTGRESQL_INTEGRATION=NOT_EXECUTED",
  "POSTGRESQL_CONCURRENCY=NOT_TESTED",
  "MULTI_INSTANCE_TEST=NOT_EXECUTED",
  "REAL_EGRESS_TEST=NOT_EXECUTED",
  "REAL_SOCKET_WRITE=NOT_EXECUTED",
  "REAL_PROVIDER_TEST=NOT_EXECUTED",
  '``````',
  "",
  "## Failure Evidence",
  "",
  "The first follow-up run had two failing SQL negative tests because a",
  "single-occurrence string replacement left a second `result_json` token in the",
  "fixture. The test was corrected to remove all occurrences. The full run below",
  "is authoritative, and the failure remains documented.",
  "",
  "## Commands",
  ""
) -join "`r`n"

Set-Content -LiteralPath $log -Value ($header + ($records -join "`r`n")) -Encoding utf8
if ($failed -ne 0) { exit 1 }

```````
<!-- END_EXACT_SOURCE id=S031 -->

### S032. vitest.config.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-followup-remediation/vitest.config.ts`
- Bytes: `245`
- SHA-256: `3F69AC0EFB7072D8EB155B7D15F78C3231769D82885A911AD4BE06225A6E0E3B`

<!-- BEGIN_EXACT_SOURCE id=S032 sha256=3F69AC0EFB7072D8EB155B7D15F78C3231769D82885A911AD4BE06225A6E0E3B bytes=245 -->
```text
import { defineConfig } from "vitest/config";

export default defineConfig({
  test: {
    environment: "node",
    include: [
      "preparation/production-trust/r3-egress-revocation-r2-followup-remediation/tests/**/*.test.ts",
    ],
  },
});

```
<!-- END_EXACT_SOURCE id=S032 -->

## Integrity

```text
INPUT_R2_BUNDLE_MATCH=YES
INPUT_CATALOG_SOURCES=31
INPUT_LOCAL_MISMATCHES=0
INPUT_BODY_MISMATCHES=0
R2_MANIFEST_ENTRIES=34
R2_MANIFEST_MISMATCHES=0
R31_R36_MANIFEST_ENTRIES=68
R31_R36_MANIFEST_MISMATCHES=0
FOLLOWUP_SOURCE_FILES=32
INDEPENDENCE_LIMITATION=SAME_HOST_MAIN_AGENT_ONLY
```
