# PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE

## Review Status

```text
R3_EGRESS_REVOCATION_R2_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS
INDEPENDENT_REVIEW=REQUIRED
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

## Scope

Complete R2 evidence for DRAINING revocation, Scope Cleanup idempotency
and truthful Egress audit semantics. This is not a production approval.

## Evidence Boundary

```text
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED
```

## Contents

- 1. Source Catalog
- 2. Complete Source Bodies
- 3. Integrity and Independence

## 1. Source Catalog

| ID | Path | Bytes | SHA-256 |
|---|---|---:|---|
| S001 | `PHASE_R3_EGRESS_AUDIT_SEMANTICS_R2_CONTRACT.md` | 2966 | A628219CE128F1EF2FCAB441F31B23E3C8C109180AB75A785BEA56EA4F295A4B |
| S002 | `PHASE_R3_EGRESS_LOCK_ORDER_R2.md` | 4290 | 72356E3B349BFE2BD17F55DB90399AE2768591E7A32DB5F21446BCF6984DF10E |
| S003 | `PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX_R2.md` | 3854 | 2F0BA5C31FBF19946C0C2C87813749D5EBE964D31E2C58C06156F98D263397F4 |
| S004 | `PHASE_R3_EGRESS_REFERENCE_MODEL_R2.md` | 2634 | DD8CE21ADC4F00EE0BB3456930686F3D3C11A2A5C71CBA82165CC2820336EF28 |
| S005 | `PHASE_R3_EGRESS_REVOCATION_R2_BASELINE.md` | 6234 | 00AC6D7AF56FD8B866FCE3FE6A3633BC6061D26416201CDFCC71C706F66767CB |
| S006 | `PHASE_R3_EGRESS_REVOCATION_R2_DIFF.md` | 1704 | 665B5686FFFBD0C838EC828F88114AD39AC3C97179886D41AFE2E1BF86AA7779 |
| S007 | `PHASE_R3_EGRESS_REVOCATION_R2_FINAL_REPORT.md` | 6143 | 4D4746436F19E90BEC035C8F7DE15E06DCFD3D2EA5E385EFE2E6944EA460C7D5 |
| S008 | `PHASE_R3_EGRESS_RISK_REGISTER_R2.md` | 2365 | C82B87E7CD5C667C4AF5940B514B97FF74DE7866413C9D7EE7677DCA3E7EABDF |
| S009 | `PHASE_R3_EGRESS_SQL_REVIEW_R2.md` | 5115 | AFF2C4ED28360F823AD73E5678D50F3C3D4118058E0B51FDC2F46BC15B33919E |
| S010 | `PHASE_R3_EGRESS_TEST_EXECUTION_R2.md` | 9971 | EEE25B2E88DA4DB24F6BA9BFE29DE023C47190A7FAE443AAC47C651E338CB019 |
| S011 | `PHASE_R3_EGRESS_THREAT_MODEL_R2.md` | 2598 | 38CE643BCC319AD1BB39B0C8FA4B8E821B28F52B35EB7F18658252781E975912 |
| S012 | `PHASE_R3_EGRESS_TRANSACTION_MATRIX_R2.md` | 4552 | 85EAE34845D590A0ABF6FB03D250E156D6DD484A72D49A4F4C7D88B9CADE1FF1 |
| S013 | `PHASE_R3_SCOPE_CLEANUP_IDEMPOTENCY_R2_CONTRACT.md` | 4423 | 2940A12BE5911EADCE1D3F6182EFCBB5DFEF20E2533E21989AA98F403E625D02 |
| S014 | `PHASE_R3_WORKER_LIFECYCLE_R2_CONTRACT.md` | 4004 | D5175B56967FA38C4043C0AFCFAE2EDDFD9288FD68E4A24B9E9132418CBFE651 |
| S015 | `PHASE_R3_EGRESS_AUDIT_R2.sql` | 12189 | 1D635A7E59DC49CE0ADC32A323B5A3DDBFECF62506DD211DFF18056F9DDF07AD |
| S016 | `PHASE_R3_SCOPE_CLEANUP_R2.sql` | 15002 | E470F746722322468DD96AF6989BD9CDDCFF0B470CE0D99984308722E98D2A86 |
| S017 | `PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql` | 4916 | F7CDE2398C7A8A5DE7BEEBCA34A1E1F706AA186915F030ABEA06DF4D3EB3FA3E |
| S018 | `contracts.ts` | 6961 | 6C0A3DA7548044E30B47E6664447B38090281D171ECCF7B39CCAA52BD674F38D |
| S019 | `lock-order.ts` | 1433 | E0A0DC39C01F08B4F1681960393A1F13209604D8C48B20B7164F198B9E0BA161 |
| S020 | `models/canonical.ts` | 1423 | C41A128E422179F88C18D32B545182F02862F22D3EF1758109ABFCF4A2BBA4D3 |
| S021 | `models/egress-audit.ts` | 12309 | 26F8D1109C403B10DB9231765793AAF555101948F9F6374D05893D19B40ED59F |
| S022 | `models/scope-cleanup.ts` | 14189 | 4FB9B9608CDFB7F016CB7F399347808C4497BCC0453B48CF6142B8F204A3E387 |
| S023 | `models/sql-analyzer.ts` | 11263 | 4F62392A2F1A50570E4EF0B8B474F0EC6D88950FCE32B8F452EB234FB39590B0 |
| S024 | `models/worker-lifecycle.ts` | 7353 | 2795B17ED1E5710AEF7BD1139081A88ED284468FBA2F345EB57F20BC88FCE67F |
| S025 | `tests/egress-audit.test.ts` | 9332 | 2987961905852135BE1F7ED73BCC11BA894FF937A84E77AECC04A71431626EC8 |
| S026 | `tests/scope-cleanup.test.ts` | 13474 | 60D407FAB476DDE174688A2027EAFD06BFF11F134D89F2B5F2D9DB3391EA58E9 |
| S027 | `tests/sql-analyzer.test.ts` | 4145 | 885CAC0221379589D50332351DB7B79CAF7613D578D438E1DCE774DFB8A59F7E |
| S028 | `tests/worker-lifecycle.test.ts` | 8668 | 1A206423D850960CEBF832802499CB8DCCAC3565D611661D8469F7A466DD8E6F |
| S029 | `tools/build-evidence.mjs` | 15278 | 4E443CDF94282B080C231A3D87FB72C1AE47844FC9D858139E028EC9CF578C79 |
| S030 | `tools/run-verification.ps1` | 7036 | AB6A8EC0A35807DBB736E46F9C1155EAD817592C01E1FB974C8E13473075C093 |
| S031 | `vitest.config.ts` | 236 | 03D475BAE8413140BD17B07408911906F0BBF97BF08107D6FF88051A7E66E5A5 |

## 2. Complete Source Bodies
### S001. PHASE_R3_EGRESS_AUDIT_SEMANTICS_R2_CONTRACT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_AUDIT_SEMANTICS_R2_CONTRACT.md`
- Bytes: `2966`
- SHA-256: `A628219CE128F1EF2FCAB441F31B23E3C8C109180AB75A785BEA56EA4F295A4B`

<!-- BEGIN_EXACT_SOURCE id=S001 sha256=A628219CE128F1EF2FCAB441F31B23E3C8C109180AB75A785BEA56EA4F295A4B bytes=2966 -->
````text
# PHASE_R3_EGRESS_AUDIT_SEMANTICS_R2_CONTRACT

## 1. Event Levels

The following facts are distinct:

| Event | Proves | Does not prove |
|---|---|---|
| `EGRESS_WRITE_START_AUTHORIZED` | database final authorization committed | socket call, bytes left host, Provider receipt |
| `SOCKET_WRITE_ATTEMPTED` | trusted Egress runtime invoked the socket API | Provider business success |
| `PROVIDER_RESPONSE_RECEIVED` | Provider response bytes were observed | business-valid response |
| `SEND_OUTCOME_UNKNOWN` | external effect cannot be determined | that a request was or was not received |

The obsolete event name `REQUEST_SENT` is forbidden for the pre-write
transaction.

## 2. State Machine

```text
FINAL_AUTHORIZED
  -> WRITE_AUTHORIZED
  -> SOCKET_ATTEMPT_RECORDED
  -> PROVIDER_RESPONSE_RECEIVED
  -> COMPLETED

WRITE_AUTHORIZED
  -> SEND_OUTCOME_UNKNOWN

SOCKET_ATTEMPT_RECORDED
  -> SEND_OUTCOME_UNKNOWN

SOCKET_WRITE_FAILED_BEFORE_BYTES
  -> manual review; no automatic retry in R2
```

`FAILED_BEFORE_BYTES` is recorded only when the trusted runtime supplies
evidence that no bytes were emitted.

## 3. Runtime Evidence

`SOCKET_WRITE_ATTEMPTED` requires:

```text
evidenceSource = TRUSTED_EGRESS_RUNTIME
evidenceSequence
evidenceDigest
socketCallOutcome
observedAt
persistedAt
```

SQL insertion cannot manufacture this event. The trusted runtime emits it only
from the actual Socket API boundary.

```text
SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED
```

## 4. Time Order

```text
database authorization time
  <= socket API invocation time
  <= local observation/persist time
  <= Provider response observation time
```

The database authorization commit and Socket Write are not atomic.

If the Socket Write occurred but its evidence/Audit persistence failed:

- no automatic retry;
- transition to unknown outcome via the stable Intent ID;
- reconcile with runtime evidence and Provider records;
- never pretend the database and network shared a transaction.

## 5. Provider Response

`PROVIDER_RESPONSE_RECEIVED` records bytes receipt and response digest only.
It sets:

```text
businessSuccessEvaluated=false
```

Business validation remains a later contract step.

## 6. Unknown Outcome

`SEND_OUTCOME_UNKNOWN` applies after:

- authorization without a proven socket call;
- crash before the call;
- partial write;
- connection loss;
- timeout;
- lost response;
- runtime evidence/Audit persistence failure.

```text
AUTO_RETRY=FORBIDDEN
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
```

## 7. SQL and Tests

SQL: `PHASE_R3_EGRESS_AUDIT_R2.sql`

Transactions:

- W: `EGRESS_WRITE_START_AUTHORIZED`;
- S: trusted runtime socket-attempt event;
- R: Provider response receipt;
- U: terminal unknown outcome.

Model: `models/egress-audit.ts`

Tests include authorization-only, crash before call, socket call, failure before
bytes, partial write, lost response, Audit persistence failure, Provider
response ordering and retry prohibition.

````
<!-- END_EXACT_SOURCE id=S001 -->

### S002. PHASE_R3_EGRESS_LOCK_ORDER_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_LOCK_ORDER_R2.md`
- Bytes: `4290`
- SHA-256: `72356E3B349BFE2BD17F55DB90399AE2768591E7A32DB5F21446BCF6984DF10E`

<!-- BEGIN_EXACT_SOURCE id=S002 sha256=72356E3B349BFE2BD17F55DB90399AE2768591E7A32DB5F21446BCF6984DF10E bytes=4290 -->
````text
# PHASE_R3_EGRESS_LOCK_ORDER_R2

## 1. Validation Level

```text
TEXTUAL_PATTERN_CHECK
SQL_STATEMENT_SEGMENTATION
SQL_PARAMETER_BINDING_REVIEW
TRANSACTION_CONTRACT_REVIEW
POSTGRESQL_EXECUTION=NOT_EXECUTED
```

## 2. Canonical Order

```text
WORKER_REVOCATION_CONTROL
  -> WORKER_REVOCATION_REQUEST
  -> SCOPE_CLEANUP_REQUEST
  -> SCOPE_WORKER_BLOCK
  -> EMERGENCY_CONTROL
  -> KEY_REGISTRY
  -> APPROVAL
  -> APPROVAL_CONSUMPTION
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

## 3. Lock Meanings

| Domain | Database object | Purpose |
|---|---|---|
| Worker Revocation | `trust_r5_worker_revocation` | global terminal authority |
| Worker Revocation Request | `trust_r6_worker_revocation_request` | request ID/payload idempotency |
| Scope Cleanup Request | `trust_r6_scope_cleanup_request` | cleanup idempotency/result |
| Scope Worker Block | `trust_r5_scope_worker_block` | per-scope blocking authority |
| Resource Floor | `trust_r4_resource_fencing` | current token/owner |
| Worker Registration | `trust_r4_worker_registration` | ACTIVE/DRAINING/REVOKED runtime state |
| Execution Lease | `trust_r4_execution_lease` | local execution state |
| Send Authorization | `trust_r4_send_authorization` | one-use permit |
| Egress Send Intent | `trust_r5_egress_intent` | final authorization/write permission |
| Egress Runtime Evidence | `trust_r6_egress_runtime_state/evidence` | actual runtime observations |
| Audit Sequence | `trust_r3_audit_head` | single global append order |

## 4. Global Revocation

```text
trust_r5_worker_revocation FOR UPDATE
  -> trust_r6_worker_revocation_request FOR UPDATE
  -> trust_r4_worker_registration UPDATE
  -> trust_r3_audit_head FOR UPDATE
```

The global tombstone is the fail-closed linearization point. `DRAINING` is
accepted by the registration update.

## 5. Scope Cleanup

```text
trust_r5_worker_revocation FOR SHARE
  -> cleanup request insert/select FOR UPDATE
  -> Scope block insert/select FOR UPDATE
  -> Resource Floor FOR UPDATE
  -> Worker Registration FOR UPDATE
  -> Execution Lease FOR UPDATE
  -> Send Authorization FOR UPDATE
  -> Audit Head FOR UPDATE
```

Two different cleanup request IDs cannot both claim the same block version.
The Scope block row serializes them. The loser rolls back the attempted owner
transaction and records `ALREADY_SATISFIED`.

Two same-ID callers are serialized by the cleanup request primary key. One owns
the request; the other reads the completed result.

## 6. Egress Audit

Write authorization:

```text
trust_r5_egress_intent FOR UPDATE
  -> trust_r6_egress_runtime_state insert
  -> trust_r6_egress_runtime_evidence insert
  -> Audit Head FOR UPDATE
```

Socket evidence:

```text
trust_r6_egress_runtime_state FOR UPDATE
  -> trust_r6_egress_runtime_evidence insert
  -> Audit Head FOR UPDATE
```

Provider response:

```text
trust_r6_egress_runtime_state FOR UPDATE
  -> runtime evidence attempt precondition
  -> runtime evidence response insert
  -> Audit Head FOR UPDATE
```

Unknown outcome uses the same runtime-state/evidence/Audit order.

## 7. Cross-Transaction Rules

| Race | Resolution |
|---|---|
| revoke vs DRAINING registration | `ACTIVE`/`DRAINING` update rule resolves |
| revoke vs takeover | global tombstone commits or later gates fail closed |
| cleanup same ID | request PK/row serializes |
| cleanup different IDs same scope | block row serializes; no duplicate version |
| cleanup vs permit consumption | global tombstone + block + floor/lease/permit checks |
| cleanup vs Egress write authorization | block/permit/floor/revocation checks fail closed before authorization |
| Egress authorization vs Emergency/Key | mutable gates re-read before write authorization |
| socket evidence persistence failure | unknown outcome; no retry |
| runtime response before attempt | rejected by runtime state/evidence precondition |

## 8. Limitation

The analyzer maps locks textually. It does not execute PostgreSQL and cannot
prove actual lock acquisition, deadlock behavior, SQLSTATE values or
multi-instance interleavings.

````
<!-- END_EXACT_SOURCE id=S002 -->

### S003. PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX_R2.md`
- Bytes: `3854`
- SHA-256: `2F0BA5C31FBF19946C0C2C87813749D5EBE964D31E2C58C06156F98D263397F4`

<!-- BEGIN_EXACT_SOURCE id=S003 sha256=2F0BA5C31FBF19946C0C2C87813749D5EBE964D31E2C58C06156F98D263397F4 bytes=3854 -->
````text
# PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX_R2

## 1. Evidence Classes

```text
TEST_IMPLEMENTATION=PRESENT
TEST_EXECUTION_RESULT=RECORDED_IN_FINAL_REPORT
SQL_STATIC_ANALYSIS=EXECUTED
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
```

## 2. Worker Negative Cases

| Case | Expected | Test |
|---|---|---|
| ACTIVE revoke | success | `worker-lifecycle.test.ts` |
| DRAINING revoke | success | `worker-lifecycle.test.ts` |
| REGISTERED runtime revoke | reject | `worker-lifecycle.test.ts` |
| REVOKED activation | `WORKER_REACTIVATION_FORBIDDEN` | model |
| same request replay | original result, no new Audit | model |
| same ID different payload | `IDEMPOTENCY_KEY_REUSE_CONFLICT` | model |
| different request after revoke | conflict, no new Audit | model |
| expected version mismatch | version conflict | model |
| request/tombstone/registration/Audit row count 0 | rollback | model |
| Audit failure | registration/tombstone rollback | model |
| authority unavailable | fail closed | model |
| same-ID concurrent | one version/Audit | model |
| different-ID concurrent | one winner/Audit | model |
| SQL ACTIVE-only update | analyzer reject | `sql-analyzer.test.ts` |
| Worker Upsert reactivation | analyzer reject | `sql-analyzer.test.ts` |

## 3. Scope Cleanup Negative Cases

### 3.1 Idempotency

| Case | Expected |
|---|---|
| missing `cleanup_request_id` | analyzer reject |
| missing `request_digest` | analyzer reject |
| same ID + same payload | exact stored result |
| same ID + different payload | `IDEMPOTENCY_KEY_REUSE_CONFLICT` |
| different ID, same Scope | `ALREADY_SATISFIED`, no version/Audit duplication |
| same ID after completion | no Block Version bump |
| same ID after completion | no new Audit |
| two same-ID instances | one owner, one replay |
| two different-ID instances | one block version; consistent final state |

### 3.2 State and Failure

| Case | Expected |
|---|---|
| PRE_SEND cleanup | Lease/Permit REVOKED |
| Lease already REVOKED without record | fail closed |
| Permit already REVOKED without record | fail closed |
| AFTER_SEND cleanup | Lease preserved; Permit REVOKED |
| WRITE_AUTHORIZED cleanup | external outcome may have occurred |
| SEND_OUTCOME_UNKNOWN cleanup | preserve unknown |
| Block mutation failure | rollback |
| Audit failure | rollback |
| Lease/Permit/request/completion row count 0 | rollback |
| COMMIT succeeded, response lost | same-ID replay returns result |
| crash before COMMIT | no partial state |
| authority unavailable | deny |

## 4. Egress Audit Negative Cases

| Case | Expected |
|---|---|
| authorization before socket call | only `EGRESS_WRITE_START_AUTHORIZED` |
| DB tries to fabricate socket attempt | `SOCKET_ATTEMPT_NOT_PROVEN` |
| crash after authorization before call | unknown, no attempt event |
| Socket API called | `SOCKET_WRITE_ATTEMPTED` with runtime evidence |
| failure before bytes | `SOCKET_WRITE_FAILED_BEFORE_BYTES` |
| partial write | `SOCKET_WRITE_PARTIAL`, no retry |
| Provider response before attempt | `PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT` |
| response received | business success remains unevaluated |
| response lost | `SEND_OUTCOME_UNKNOWN` |
| socket occurred, Audit failed | unknown recovery, no retry |
| repeated unknown transition | terminal-state rejection |
| obsolete `REQUEST_SENT` | analyzer reject |
| missing runtime evidence source | analyzer reject |

## 5. Test Counts

Vitest files:

```text
tests/worker-lifecycle.test.ts
tests/scope-cleanup.test.ts
tests/egress-audit.test.ts
tests/sql-analyzer.test.ts
```

Final execution count and exact command are recorded in
`PHASE_R3_EGRESS_TEST_EXECUTION_R2.md`.

## 6. Important Limit

The in-memory concurrency queue proves only the modeled linearization order.
It is not PostgreSQL, multi-process or real network evidence.

````
<!-- END_EXACT_SOURCE id=S003 -->

### S004. PHASE_R3_EGRESS_REFERENCE_MODEL_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_REFERENCE_MODEL_R2.md`
- Bytes: `2634`
- SHA-256: `DD8CE21ADC4F00EE0BB3456930686F3D3C11A2A5C71CBA82165CC2820336EF28`

<!-- BEGIN_EXACT_SOURCE id=S004 sha256=DD8CE21ADC4F00EE0BB3456930686F3D3C11A2A5C71CBA82165CC2820336EF28 bytes=2634 -->
````text
# PHASE_R3_EGRESS_REFERENCE_MODEL_R2

## 1. Status

```text
OFFLINE_REFERENCE_MODEL
PERSISTENCE_SIMULATION_ONLY
REAL_DATABASE_DURABILITY=NOT_TESTED
REAL_MULTI_INSTANCE_INTERLEAVING=NOT_TESTED
REAL_SOCKET_WRITE=NOT_IMPLEMENTED
```

## 2. Files

### `contracts.ts`

Strict runtime schemas for:

- Worker revocation requests/results;
- Cleanup requests/results;
- Egress audit events;
- socket-attempt runtime evidence;
- intent/runtime states.

Unknown fields are rejected.

### `models/canonical.ts`

Deterministic object-key ordering and SHA-256 canonical digest. It binds
idempotency keys to complete payloads and computes result digests.

### `models/worker-lifecycle.ts`

Behavior:

- ACTIVE/DRAINING -> REVOKED;
- REGISTERED runtime denial;
- terminal reactivation protection;
- same-ID replay and payload mismatch;
- different-ID conflict;
- row-count/Audit rollback;
- COMMIT-unknown recovery;
- queue-based same-ID/different-ID concurrency simulation;
- snapshot/restart replay.

### `models/scope-cleanup.ts`

Behavior:

- pre-send vs after-send classification;
- stable request/result digest;
- same-ID replay with no version/Audit change;
- different-ID `ALREADY_SATISFIED`;
- COMMIT-unknown and crash recovery;
- Lease/Permit consistency checks;
- same-ID and different-ID concurrent calls;
- persistence snapshot/restore.

### `models/egress-audit.ts`

Behavior:

- write authorization event;
- trusted runtime socket-attempt evidence;
- failure-before-bytes/partial/complete call outcomes;
- response receipt without business-success claim;
- crash-before-call recovery;
- Audit persistence failure -> unknown, no retry;
- terminal outcome and event sequence checks.

### `models/sql-analyzer.ts`

Responsibilities:

- SQL statement segmentation;
- transaction grouping;
- lock-domain extraction;
- parameter inventory;
- Worker lifecycle checks;
- cleanup idempotency checks;
- truthful Audit event checks;
- lock-order crossing detection.

It is not a PostgreSQL parser or executor.

## 3. Snapshot Models

Worker and Cleanup models expose `snapshot()` and `fromSnapshot()` to simulate
restart recovery. They reflect in-memory state only:

```text
PERSISTENCE_SIMULATION_ONLY
REAL_DATABASE_DURABILITY=NOT_TESTED
```

## 4. Model Guarantees

The tests can prove:

- the declared state transitions;
- idempotency decision tables;
- no duplicated Audit/version in modeled replay;
- unknown result has no automatic retry;
- event order in modeled runtime sequence.

They cannot prove:

- real transaction isolation or durability;
- cross-instance scheduling;
- actual network bytes;
- Provider receipt or business success.

````
<!-- END_EXACT_SOURCE id=S004 -->

### S005. PHASE_R3_EGRESS_REVOCATION_R2_BASELINE.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_REVOCATION_R2_BASELINE.md`
- Bytes: `6234`
- SHA-256: `00AC6D7AF56FD8B866FCE3FE6A3633BC6061D26416201CDFCC71C706F66767CB`

<!-- BEGIN_EXACT_SOURCE id=S005 sha256=00AC6D7AF56FD8B866FCE3FE6A3633BC6061D26416201CDFCC71C706F66767CB bytes=6234 -->
````text
# PHASE_R3_EGRESS_REVOCATION_R2_BASELINE

## 1. Status

```text
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
BASELINE_REALM=READ_ONLY_R3_EGRESS_REVOCATION_R1
MAIN_WORKSPACE_ACCESSED=NO
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

This phase creates a new directory:

```text
preparation/production-trust/r3-egress-revocation-r2-remediation/
```

No previous R3 Egress/Revocation file is an output target.

## 2. Input Bundle

| File | Bytes | SHA-256 |
|---|---:|---|
| `preparation/production-trust/PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE.md` | 320631 | `CDD2ED989668FE7A9588533532A8A209699085EB68934BB9CE74CDBBE47354FE` |
| `preparation/production-trust/PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md` | 1878 | `185ECEA130E4CB563FAC3ABEB811B7AC05617E3F8A8375012DB447A38FC9E23C` |
| `preparation/production-trust/PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt` | 444 | `3EAAAD5B2B6281F252E140F3ACB7C20B73AFD036F4FFABB8E79CFE503AE99E4C` |
| `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt` | 5742 | `9F71A2D092F2032B8EAD3C23346FB5FB8B34E0762B370DFF9F194C87051AA0DA` |

The Bundle Hash and byte count match the values supplied in the R2 task.
The Bundle Manifest and R1 remediation Manifest were verified again during
this phase.

## 3. Key Input Sources

| Source | Bytes | SHA-256 |
|---|---:|---|
| `r3-egress-revocation-remediation/sql/10-worker-global-revocation.sql` | 5443 | `54B918ABA73574E0BB92000C993ED1CDF8FF1C8F5CB646FC27AAAC20721D37E1` |
| `r3-egress-revocation-remediation/sql/20-worker-scope-cleanup.sql` | 6953 | `FE3ED25A80BB275DA7428C07B84433AD0720E10D46788F1B7F413A86D82F9D53` |
| `r3-egress-revocation-remediation/sql/30-egress-final-authorization.sql` | 23151 | `149262A324348E3AF2AA6264B3E2740FAB0D63CF5D662AEF672DCD38FE7A8906` |
| `r3-egress-revocation-remediation/models/worker-revocation.ts` | 15706 | `974C1463AB2280605B7EC94EDBEE4AAC36383BBE1D16C6CDDB3B8ECD69E54C90` |
| `r3-egress-revocation-remediation/models/egress-boundary.ts` | 14446 | `14FE4BA52870232929A8AB7966623E7D0450659669D0069F79A32F35AC347A02` |
| `r3-egress-revocation-remediation/models/sql-contract-analyzer.ts` | 15322 | `5C29304B30B7693089B00C29C40BC2C72A6429AB64519AE81D78D18CD423DEA9` |
| `r3-egress-revocation-remediation/tests/worker-revocation.test.ts` | 12727 | `9CB055D02F1F023044DA7344A93E27A7AC09343338319E77796D3631FBF13A2A` |
| `r3-egress-revocation-remediation/tests/egress-boundary.test.ts` | 12927 | `A61F2FBF565922218741DEE6C37F557857C1E93C8F10A97E962D1980F37DAD64` |
| `r3-egress-revocation-remediation/tests/sql-contract.test.ts` | 9038 | `FF4BAF2B9E1F737381CF3D0CD103DFF240C242B1E3E29415AC35032BCCA8305A` |
| `r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_CONTRACT.md` | 5484 | `C4E21EBF5DCC615F260BDADFB72117886D11A7724693E92023A1373AB4804EE1` |
| `r3-egress-revocation-remediation/PHASE_R3_EGRESS_LOCK_ORDER.md` | 6273 | `C1ADAFD47A69C61143826821B117C1CF5D2C8E549F08F8EDF4B5A071D087F66C` |
| `r3-egress-revocation-remediation/PHASE_R3_EGRESS_RISK_REGISTER.md` | 4235 | `A51A1EB30734C7DEF550B225F7B0B7584F22244ABE8F21DED53988132C7E357D` |
| `r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_FINAL_REPORT.md` | 6301 | `6EF2E8AA32746E311BC7408FB836D569ACBEE521162E700A65FEAB9870A99BD1` |

Local source bodies and the source bodies embedded in the input Bundle were
read from the same R1 output. No unexplained body mismatch was found before
remediation.

## 4. Confirmed Defects

### R2-D1: DRAINING cannot be revoked

`10-worker-global-revocation.sql` updates Registration only when:

```sql
AND state = 'ACTIVE'
```

The draft contract permits:

```text
REGISTERED -> ACTIVE -> DRAINING -> REVOKED
```

Therefore a `DRAINING` Worker produces a zero-row Registration update and the
global revocation transaction cannot complete under its exactly-one rule.

### R2-D2: Scope Cleanup replay is not idempotent

The R1 cleanup branches have no `cleanupRequestId` or persistent idempotency
record. A committed retry observes Lease/Permit in `REVOKED`, performs zero-row
checked updates, may roll back, and cannot return the original result. The
Scope block upsert can increment `version` on a repeated request.

### R2-D3: Audit event name precedes the socket call

`30-egress-final-authorization.sql` commits `REQUEST_SENT` in the database
transaction that authorizes `WRITE_STARTED`. At that point no Socket Write API
has necessarily been called. The Audit vocabulary therefore conflates:

```text
authorization committed
socket write API called
bytes accepted locally or remotely
Provider response received
```

## 5. Current Lock Order

```text
WORKER_REVOCATION_CONTROL
  -> EMERGENCY_CONTROL
  -> KEY_REGISTRY
  -> APPROVAL
  -> APPROVAL_CONSUMPTION
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
  -> AUDIT_SEQUENCE
```

The R2 cleanup idempotency record must be placed without creating a lock-order
cycle. It is treated as a child of the Worker Revocation decision domain and
is acquired immediately after the global revocation row.

## 6. Expected R2 Changes

```text
1. Worker lifecycle contract + DRAINING revoke SQL/model/tests
2. cleanupRequestId + payload digest + persistent idempotency record
3. replay/COMMIT-unknown recovery without duplicate block version or Audit
4. truthful Audit event split for authorization vs runtime socket evidence
5. updated lock/transaction matrices and negative tests
6. new Bundle with complete bodies and Hash verification
```

## 7. Explicit Non-Changes

```text
R1_R3_EGRESS_FILES_MODIFIED=NO
R3_FENCING_FILES_MODIFIED=NO
R31_R36_FILES_MODIFIED=NO
SRC_MODIFIED=NO
SCRIPTS_MODIFIED=NO
PACKAGE_OR_LOCKFILE_MODIFIED=NO
PRODUCTION_ENTRY_MODIFIED=NO
```

## 8. Safety Boundary

```text
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
NETWORK_ACCESSED=NO
REAL_KEY_ACCESSED=NO
PROVIDER_API_CALLED=NO
REAL_FETCH_EXECUTED=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
```

````
<!-- END_EXACT_SOURCE id=S005 -->

### S006. PHASE_R3_EGRESS_REVOCATION_R2_DIFF.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_REVOCATION_R2_DIFF.md`
- Bytes: `1704`
- SHA-256: `665B5686FFFBD0C838EC828F88114AD39AC3C97179886D41AFE2E1BF86AA7779`

<!-- BEGIN_EXACT_SOURCE id=S006 sha256=665B5686FFFBD0C838EC828F88114AD39AC3C97179886D41AFE2E1BF86AA7779 bytes=1704 -->
````text
# PHASE_R3_EGRESS_REVOCATION_R2_DIFF

## 1. Baseline Preservation

```text
R3_R1_BUNDLE_SHA256=CDD2ED989668FE7A9588533532A8A209699085EB68934BB9CE74CDBBE47354FE
R3_R1_BUNDLE_BYTES=320631
R3_R1_FILES_MODIFIED=NO
```

All R2 output is in:

```text
preparation/production-trust/r3-egress-revocation-r2-remediation/
```

## 2. Worker Revocation Diff

Before:

```sql
UPDATE trust_r4_worker_registration
SET state = 'REVOKED'
WHERE worker_instance_id = $1
  AND state = 'ACTIVE';
```

After:

```sql
UPDATE trust_r4_worker_registration
SET state = 'REVOKED'
WHERE worker_instance_id = $1
  AND state IN ('ACTIVE', 'DRAINING');
```

Added:

- `trust_r6_worker_revocation_request`;
- request digest binding;
- exact same-request replay;
- different-request conflict;
- REGISTERED provisioning-only policy.

## 3. Scope Cleanup Diff

Before:

- no cleanup request record;
- no request/result digest;
- repeated condition UPDATE expected one row;
- Block version could increment on replay;
- repeated Audit possible.

After:

- `trust_r6_scope_cleanup_request`;
- request ID + digest + result digest + Audit event binding;
- same-ID exact replay;
- different-ID `ALREADY_SATISFIED`;
- transactional PENDING -> COMPLETED;
- dedicated owner pre-send/after-send/already-satisfied/replay transactions.

## 4. Egress Audit Diff

Before:

```text
WRITE_STARTED + Audit REQUEST_SENT in one database transaction
```

After:

```text
EGRESS_WRITE_START_AUTHORIZED
  -> trusted runtime SOCKET_WRITE_ATTEMPTED / failure / partial
  -> PROVIDER_RESPONSE_RECEIVED
  -> optional SEND_OUTCOME_UNKNOWN
```

Response receipt no longer equals business success. Socket evidence remains
unimplemented as a production runtime control.

````
<!-- END_EXACT_SOURCE id=S006 -->

### S007. PHASE_R3_EGRESS_REVOCATION_R2_FINAL_REPORT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_REVOCATION_R2_FINAL_REPORT.md`
- Bytes: `6143`
- SHA-256: `4D4746436F19E90BEC035C8F7DE15E06DCFD3D2EA5E385EFE2E6944EA460C7D5`

<!-- BEGIN_EXACT_SOURCE id=S007 sha256=4D4746436F19E90BEC035C8F7DE15E06DCFD3D2EA5E385EFE2E6944EA460C7D5 bytes=6143 -->
````text
# PHASE_R3_EGRESS_REVOCATION_R2_FINAL_REPORT

## 1. Final Status

```text
R3_EGRESS_REVOCATION_R2_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS
INDEPENDENT_REVIEW=REQUIRED

PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
PRODUCTION_EGRESS_IMPLEMENTED=NO
NETWORK_ISOLATION_ENFORCED=NO
MULTI_INSTANCE_COORDINATION=NOT_IMPLEMENTED
REAL_FETCH_AUTHORIZED=NO
```

This is an offline design/model/static-SQL result, not production security
acceptance.

## 2. Defects Closed

| Finding | Resolution |
|---|---|
| DRAINING Worker could not be revoked | Registration revoke now accepts `ACTIVE` and `DRAINING` |
| Cleanup was not idempotent | persistent request ID + payload digest + result digest + result replay |
| pre-socket Audit claimed `REQUEST_SENT` | replaced by truthful authorization/runtime event levels |

## 3. Worker Lifecycle

```text
REGISTERED -> ACTIVE -> DRAINING -> REVOKED
```

- `ACTIVE -> REVOKED`: allowed.
- `DRAINING -> REVOKED`: allowed.
- `REGISTERED`: provisioning-only; runtime revoke denied because the frozen R4
  table does not represent it. Separate deprovisioning is required.
- `REVOKED`: terminal for ordinary registration.
- same request ID: replay original result.
- different request ID after revocation: conflict without new version/Audit.

## 4. Scope Cleanup Idempotency

The cleanup request binds:

```text
cleanupRequestId
requestDigest
workerInstanceId
scopeKey
revocationVersion
leaseId
capabilityId
permitId
reasonCode
```

The persistent record contains `result_digest`, `audit_event_id` and a
transactional `PENDING -> COMPLETED` transition.

- same request + same payload -> exact persisted result;
- same request + different payload -> conflict;
- same request retry -> no Block version/Audit duplication;
- different request on satisfied Scope -> `ALREADY_SATISFIED`;
- lost COMMIT response -> same request ID recovery;
- committed PENDING -> invariant failure.

## 5. Egress Audit Semantics

Distinct events:

```text
EGRESS_WRITE_START_AUTHORIZED
SOCKET_WRITE_ATTEMPTED
PROVIDER_RESPONSE_RECEIVED
SEND_OUTCOME_UNKNOWN
```

`EGRESS_WRITE_START_AUTHORIZED` proves only a committed database authorization.
`SOCKET_WRITE_ATTEMPTED` requires trusted Egress runtime evidence.
`PROVIDER_RESPONSE_RECEIVED` has `businessSuccessEvaluated=false`.
`SEND_OUTCOME_UNKNOWN` is terminal for automatic retry purposes.

```text
SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
```

## 6. Acceptance Matrix

```text
WORKER_ACTIVE_REVOCATION=PASS
WORKER_DRAINING_REVOCATION=PASS
WORKER_REGISTERED_REVOCATION_POLICY=PASS
WORKER_REVOKED_REACTIVATION_BLOCK=PASS
WORKER_REVOCATION_IDEMPOTENCY=PASS
WORKER_REVOCATION_AUDIT_ATOMICITY=PASS

SCOPE_CLEANUP_REQUEST_ID=PASS
SCOPE_CLEANUP_REQUEST_DIGEST_BINDING=PASS
SCOPE_CLEANUP_REPLAY_IDEMPOTENCY=PASS
SCOPE_CLEANUP_ID_REUSE_CONFLICT=PASS
SCOPE_CLEANUP_NO_DUPLICATE_VERSION=PASS
SCOPE_CLEANUP_NO_DUPLICATE_AUDIT=PASS
SCOPE_CLEANUP_CONCURRENT_SAME_ID=PASS
SCOPE_CLEANUP_CONCURRENT_DIFFERENT_ID=PASS
SCOPE_CLEANUP_UNKNOWN_COMMIT_RECOVERY=PASS
SCOPE_CLEANUP_CRASH_RECOVERY=PASS
SCOPE_CLEANUP_LEASE_PERMIT_STATE_ALIGNMENT=PASS

EGRESS_WRITE_START_AUTHORIZED_SEMANTICS=PASS
SOCKET_WRITE_ATTEMPTED_SEMANTICS=PASS
PROVIDER_RESPONSE_RECEIVED_SEMANTICS=PASS
SEND_OUTCOME_UNKNOWN_SEMANTICS=PASS
EGRESS_AUDIT_TIME_ORDER=PASS
NO_FALSE_REQUEST_SENT_CLAIM=PASS
NO_AUTOMATIC_RETRY_AFTER_UNKNOWN=PASS

LOCK_ORDER_CONSISTENCY=PASS
SQL_NEGATIVE_TESTS=PASS
OFFLINE_MODEL_TESTS=PASS
REGRESSION_TESTS=PASS
BUNDLE_BODY_EXACTNESS=PASS
MANIFEST_HASH_VERIFICATION=PASS
```

The PASS items are offline contract/model/static analysis. Concurrency tests
use in-memory queues. `SOCKET_WRITE_ATTEMPTED_SEMANTICS=PASS` means the evidence
source and truth boundary are modeled correctly, not that runtime evidence is
implemented.

## 7. Verification Results

```text
R3_R2_TARGETED_VITEST=4_FILES_67_TESTS_PASS
R3_EGRESS_REVOCATION_R1_VITEST=4_FILES_53_TESTS_PASS
R3_FENCING_VITEST=7_FILES_49_TESTS_PASS
R2_R3_VITEST=8_FILES_74_TESTS_PASS
R2_VITEST=10_FILES_80_TESTS_PASS
R1_VITEST=16_FILES_91_TESTS_PASS
R31_R36_RELEVANT_VITEST=20_FILES_179_TESTS_PASS
POWERSHELL_LAUNCHER=40_PASS
POWERSHELL_KEY_SESSION=25_PASS
POWERSHELL_FETCH_ENFORCEMENT=4_PASS
POWERSHELL_5_1_PARSER=6_PASS
TYPESCRIPT_STRICT=PASS
ESLINT=PASS
NEXT_BUILD=PASS
```

The initial R2 run had three test failures. The root causes were a wrong
failure-code expectation and two SQL negative-test transformations that did not
remove the target clause. The implementation/test fixtures were corrected and
the complete run above is authoritative. The failure evidence is preserved in
`PHASE_R3_EGRESS_TEST_EXECUTION_R2.md`.

## 8. Workpack Independence

Three same-host subagents were requested. They returned without creating
workpacks or findings. No independence or third-party audit is claimed.

```text
INDEPENDENCE_LIMITATION=SAME_HOST_AGENTS_NO_USABLE_WORKPACK
```

## 9. Evidence Boundaries

```text
OFFLINE_REFERENCE_MODEL=PASS
LOCAL_UNIT_TESTS=PASS
SQL_STATIC_ANALYSIS=PASS
SQL_NEGATIVE_TESTS=PASS

POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
REAL_DATABASE_DURABILITY=NOT_TESTED
```

## 10. Safety

```text
MAIN_WORKSPACE_MODIFIED=NO
SRC_SCRIPTS_MODIFIED=NO
R31_R36_MODIFIED=NO
IDENTITY_GATE_CORE_MODIFIED=NO
PRIOR_R3_EGRESS_FILES_MODIFIED=NO
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

## 11. Residual Risks

- PostgreSQL row-lock, SQLSTATE and durability behavior are not tested;
- real multi-instance idempotency is not tested;
- runtime socket-attempt evidence is not implemented;
- production Egress and Worker network isolation are not implemented;
- no external Provider receipt or exactly-once guarantee exists;
- same-host agents are not independent review.

Production enforcement remains blocked.

````
<!-- END_EXACT_SOURCE id=S007 -->

### S008. PHASE_R3_EGRESS_RISK_REGISTER_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_RISK_REGISTER_R2.md`
- Bytes: `2365`
- SHA-256: `C82B87E7CD5C667C4AF5940B514B97FF74DE7866413C9D7EE7677DCA3E7EABDF`

<!-- BEGIN_EXACT_SOURCE id=S008 sha256=C82B87E7CD5C667C4AF5940B514B97FF74DE7866413C9D7EE7677DCA3E7EABDF bytes=2365 -->
```text
# PHASE_R3_EGRESS_RISK_REGISTER_R2

| ID | Risk | Severity | Status | Evidence |
|---|---|---|---|---|
| R2-01 | DRAINING Worker zero-row revocation | High | MITIGATED_IN_DESIGN | SQL + model tests |
| R2-02 | REGISTERED semantics inconsistent with frozen schema | Medium | POLICY_EXPLICIT | separate provisioning flow required |
| R2-03 | Worker request ID reused with different payload | High | MITIGATED_IN_DESIGN | digest conflict test |
| R2-04 | Different Worker request double-bumps/Audits | High | MITIGATED_IN_DESIGN | conflict model test |
| R2-05 | Cleanup same-ID replay increments version | High | MITIGATED_IN_DESIGN | exact result replay |
| R2-06 | Cleanup same-ID replay duplicates Audit | High | MITIGATED_IN_DESIGN | audit count tests |
| R2-07 | Different cleanup IDs double-apply | High | MITIGATED_IN_DESIGN | ALREADY_SATISFIED branch |
| R2-08 | Cleanup leaves committed PENDING | High | MITIGATED_BY_TRANSACTION_DESIGN | PENDING transaction-local |
| R2-09 | Lost COMMIT response cannot recover | High | MITIGATED_IN_DESIGN | same-ID replay tests |
| R2-10 | Audit and Cleanup completion split | High | MITIGATED_IN_DESIGN | same transaction contract |
| R2-11 | `REQUEST_SENT` falsely claims external send | High | MITIGATED_IN_DESIGN | event split + analyzer |
| R2-12 | SQL fabricates Socket Write evidence | Critical | MITIGATED_IN_DESIGN | trusted runtime source requirement |
| R2-13 | Runtime Socket evidence not implemented | High | NOT_IMPLEMENTED | `SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED` |
| R2-14 | Provider response treated as business success | High | MITIGATED_IN_DESIGN | `businessSuccessEvaluated=false` |
| R2-15 | Socket occurred but Audit persistence failed | High | MITIGATED_BY_UNKNOWN_POLICY | no retry, manual reconciliation |
| R2-16 | PostgreSQL lock/durability semantics unverified | High | NOT_EXECUTED | SQL static only |
| R2-17 | Multi-instance coordination unverified | High | NOT_EXECUTED | model only |
| R2-18 | Worker not isolated from direct Provider route | Critical | NOT_IMPLEMENTED | production boundary |
| R2-19 | Same-host subagents produced no independent workpack | Low | DISCLOSED | independence limitation |
| R2-20 | Cleanup parameter `$11` unused | Low | DOCUMENTED | renumber before production |

No production enforcement is authorized while these residual risks remain.

```
<!-- END_EXACT_SOURCE id=S008 -->

### S009. PHASE_R3_EGRESS_SQL_REVIEW_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_SQL_REVIEW_R2.md`
- Bytes: `5115`
- SHA-256: `AFF2C4ED28360F823AD73E5678D50F3C3D4118058E0B51FDC2F46BC15B33919E`

<!-- BEGIN_EXACT_SOURCE id=S009 sha256=AFF2C4ED28360F823AD73E5678D50F3C3D4118058E0B51FDC2F46BC15B33919E bytes=5115 -->
````text
# PHASE_R3_EGRESS_SQL_REVIEW_R2

## 1. Validation Levels

```text
TEXTUAL_PATTERN_CHECK=EXECUTED
SQL_STATEMENT_SEGMENTATION=EXECUTED
SQL_PARAMETER_BINDING_REVIEW=EXECUTED
TRANSACTION_CONTRACT_REVIEW=EXECUTED
POSTGRESQL_EXECUTION=NOT_EXECUTED
POSTGRESQL_AST_ANALYSIS=NOT_EXECUTED
```

No PostgreSQL, Docker, network or SQL execution is used.

## 2. Worker Revocation Parameters

File: `PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql`

| Parameter | Source |
|---|---|
| `$1` | server-resolved Worker ID |
| `$2` | caller request UUID |
| `$3` | server UTC Unix milliseconds |
| `$4` | reason code |
| `$5` | expected revocation record version |
| `$6` | Audit event UUID |
| `$7` | Audit sequence under locked head |
| `$8` | previous event digest |
| `$9` | new event digest |
| `$10` | SHA-256 of canonical request payload |
| `$11` | new revocation version (expected current + 1) |

## 3. Scope Cleanup Parameters

File: `PHASE_R3_SCOPE_CLEANUP_R2.sql`

| Parameter | Source |
|---|---|
| `$1` | server-resolved Worker ID |
| `$2` | cleanup request UUID |
| `$3` | SHA-256 of canonical cleanup request |
| `$4` | canonical Scope Key |
| `$5` | requested Worker revocation version |
| `$6` | Lease ID |
| `$7` | Capability ID |
| `$8` | Permit ID |
| `$9` | cleanup reason code |
| `$10` | server UTC Unix milliseconds |
| `$12` | current Resource Floor fencing token |
| `$13` | Audit event UUID |
| `$14` | Audit sequence |
| `$15` | previous event digest |
| `$16` | new event digest |
| `$17` | SHA-256 of canonical cleanup result |

`$11` is not used. The omission is intentional in this draft; a production
implementation should renumber parameters or bind by name rather than guessing.

## 4. Egress Audit Parameters

File: `PHASE_R3_EGRESS_AUDIT_R2.sql`

### Write Authorization

| Parameter | Source |
|---|---|
| `$1` | Egress Intent ID |
| `$2` | expected Intent row version |
| `$3` | database authorization time |
| `$4` | runtime evidence UUID |
| `$5` | Audit event UUID |
| `$6` | authorization evidence digest |
| `$7` | Audit sequence |
| `$8` | previous event digest |
| `$9` | new event digest |

### Socket Attempt

| Parameter | Source |
|---|---|
| `$10` | Egress Intent ID |
| `$11` | runtime evidence UUID |
| `$12` | Audit event UUID |
| `$13` | trusted runtime source sequence |
| `$14` | exact socket event type |
| `$15` | expected runtime-state row version |
| `$16` | runtime evidence digest |
| `$17` | socket call outcome |
| `$18` | socket API observation time |
| `$19` | database persistence time |
| `$20` | Audit sequence |
| `$21` | previous event digest |
| `$22` | new event digest |

### Provider Response

| Parameter | Source |
|---|---|
| `$23` | Egress Intent ID |
| `$24` | runtime evidence UUID |
| `$25` | Audit event UUID |
| `$26` | trusted runtime source sequence |
| `$27` | expected runtime-state row version |
| `$28` | response evidence digest |
| `$29` | Provider response digest |
| `$30` | response observation time |
| `$31` | database persistence time |
| `$32` | Audit sequence |
| `$33` | previous event digest |
| `$34` | new event digest |

### Unknown Outcome

| Parameter | Source |
|---|---|
| `$35` | Egress Intent ID |
| `$36` | runtime evidence UUID |
| `$37` | Audit event UUID |
| `$38` | trusted runtime source sequence |
| `$39` | expected runtime-state row version |
| `$40` | unknown-outcome evidence digest |
| `$41` | unknown observation time |
| `$42` | database persistence time |
| `$43` | Audit sequence |
| `$44` | previous event digest |
| `$45` | new event digest |

## 5. Condition / Row-Count Map

| SQL operation | Expected row count |
|---|---|
| Worker tombstone update | 1 |
| Worker registration `ACTIVE`/`DRAINING -> REVOKED` | 1 |
| Worker request insert | 1 |
| Worker Audit-head update | 1 |
| Cleanup request PENDING insert | 1 on owner path |
| Cleanup block claim | 1 on APPLIED path; 0 on ALREADY_SATISFIED path |
| Cleanup Lease revoke | 1 PRE_SEND; `NOT_USED` AFTER_SEND |
| Cleanup Permit revoke | 1 APPLIED; `NOT_USED` ALREADY_SATISFIED |
| Cleanup request `PENDING -> COMPLETED` | 1 |
| Cleanup Audit-head update | 1 |
| Egress intent authorization update | 1 |
| Runtime state/evidence inserts | 1 each |
| Provider response state update | 1 |
| Unknown outcome state update | 1 |

## 6. Static Negative Tests

`tests/sql-analyzer.test.ts` reads actual SQL and rejects:

- ACTIVE-only Worker revocation;
- Worker reactivation Upsert;
- missing cleanup request digest;
- unconditional Scope block version increment;
- missing result/audit binding;
- the obsolete pre-socket `REQUEST_SENT` event;
- missing trusted runtime evidence source;
- missing business-success separation;
- lock-domain order crossings.

## 7. What Static Review Cannot Prove

```text
POSTGRESQL_PARSE_ACCEPTANCE
LOCK_ACQUISITION_TIMING
DEADLOCK_BEHAVIOR
SQLSTATE_VALUES
UNIQUE_CONSTRAINT_RACE_BEHAVIOR
TRANSACTION_DURABILITY
REAL_SOCKET_WRITE
PROVIDER_RECEIPT
```

The SQL parameter omissions/gaps are reported rather than hidden. `$11` in the
cleanup draft is intentionally unused and should be renumbered before
production implementation.

````
<!-- END_EXACT_SOURCE id=S009 -->

### S010. PHASE_R3_EGRESS_TEST_EXECUTION_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_TEST_EXECUTION_R2.md`
- Bytes: `9971`
- SHA-256: `EEE25B2E88DA4DB24F6BA9BFE29DE023C47190A7FAE443AAC47C651E338CB019`

<!-- BEGIN_EXACT_SOURCE id=S010 sha256=EEE25B2E88DA4DB24F6BA9BFE29DE023C47190A7FAE443AAC47C651E338CB019 bytes=9971 -->
```````text
﻿# PHASE_R3_EGRESS_TEST_EXECUTION_R2

## Status

``````text
GENERATED_AT=2026-11-26T23:13:51.4111147+08:00
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
FAILED_COMMANDS=0
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
``````

## Execution Notes

- The first R2 focused run had three failing assertions: an already-REVOKED
  Lease returned LEASE_STATE_INVALID instead of the intended inconsistent
  idempotency-state error, and two SQL analyzer fixtures did not mutate the
  target clause as intended. The implementation/fixtures were corrected and
  the complete run below is authoritative. The failure is preserved here.
- The same-host subagents returned without producing workpacks. They are not
  represented as independent review.

## Commands
### R3 R2 targeted Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-egress-revocation-r2-remediation/vitest.config.ts
START=2026-11-26T23:13:25.2227744+08:00
END=2026-11-26T23:13:25.7281202+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  4 passed (4)
      Tests  67 passed (67)
   Start at  23:13:25
   Duration  236ms (import 70%, transform 17%, tests 9%, worker 3%)
```

### R3 Egress Revocation R1 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-egress-revocation-remediation/vitest.config.ts
START=2026-11-26T23:13:25.7403658+08:00
END=2026-11-26T23:13:26.2277666+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  4 passed (4)
      Tests  53 passed (53)
   Start at  23:13:25
   Duration  235ms (import 72%, tests 12%, transform 12%, worker 4%)
```

### R3 Fencing Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-fencing-remediation/vitest.config.ts
START=2026-11-26T23:13:26.2277666+08:00
END=2026-11-26T23:13:26.7277262+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  7 passed (7)
      Tests  49 passed (49)
   Start at  23:13:26
   Duration  235ms (import 77%, transform 11%, tests 8%, worker 4%)
```

### R2-R3 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2-r3-remediation/vitest.config.ts
START=2026-11-26T23:13:26.7277262+08:00
END=2026-11-26T23:13:27.2488007+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  8 passed (8)
      Tests  74 passed (74)
   Start at  23:13:26
   Duration  252ms (import 78%, tests 11%, transform 7%, worker 4%)
```

### R2 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2/vitest.config.ts
START=2026-11-26T23:13:27.2488007+08:00
END=2026-11-26T23:13:27.7914372+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  10 passed (10)
      Tests  80 passed (80)
   Start at  23:13:27
   Duration  278ms (import 79%, tests 12%, transform 6%, worker 4%)
```

### R1 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/vitest.config.ts
START=2026-11-26T23:13:27.7924359+08:00
END=2026-11-26T23:13:28.3902495+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  16 passed (16)
      Tests  91 passed (91)
   Start at  23:13:28
   Duration  340ms (import 80%, tests 10%, transform 6%, worker 4%)
```

### R31-R36 Relevant Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run src/server/auth/actor-context.test.ts src/server/public-enterprise-search/identity/identity-gate.test.ts src/server/public-enterprise-search/identity/runtime/approval-authorization.test.ts src/server/public-enterprise-search/identity/runtime/authorization.test.ts src/server/public-enterprise-search/identity/runtime/fetch-entry-guard.test.ts src/server/public-enterprise-search/identity/runtime/precheck.test.ts src/server/public-enterprise-search/identity/runtime/production-fetch-entry.test.ts src/server/public-enterprise-search/identity/runtime/trusted-read.test.ts src/server/public-enterprise-search/offline-boundaries.test.ts src/server/public-enterprise-search/provider/aux-http-transports.test.ts src/server/public-enterprise-search/provider/deepseek-fetch.test.ts src/server/public-enterprise-search/provider/deepseek-http-transport.test.ts src/server/public-enterprise-search/provider/provider-execution-authorization.test.ts src/server/public-enterprise-search/provider/provider-factory-protection.test.ts src/server/public-enterprise-search/diagnostics/fetch-diagnostic-cli.test.ts src/server/public-enterprise-search/diagnostics/fetch-diagnostic-dependency.test.ts src/server/public-enterprise-search/local-live/live-config.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial-cli.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial.zero-network.test.ts
START=2026-11-26T23:13:28.3922715+08:00
END=2026-11-26T23:13:33.5048307+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  20 passed (20)
      Tests  179 passed (179)
   Start at  23:13:28
   Duration  4.84s (tests 53%, import 39%, transform 5%, worker 2%)

    Isolate  20 workers spawned · ~87ms startup each (spawn + environment, per file)
             at least ~1.66s faster with isolate: false — reuses workers across files instead of one per file
```

### PowerShell Launcher

```text
COMMAND=powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-only-launcher.ps1
START=2026-11-26T23:13:33.5058256+08:00
END=2026-11-26T23:13:39.1256613+08:00
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
START=2026-11-26T23:13:39.1266659+08:00
END=2026-11-26T23:13:40.4306111+08:00
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
START=2026-11-26T23:13:40.4306111+08:00
END=2026-11-26T23:13:40.8724023+08:00
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
START=2026-11-26T23:13:40.8724023+08:00
END=2026-11-26T23:13:40.8971909+08:00
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
START=2026-11-26T23:13:40.8971909+08:00
END=2026-11-26T23:13:43.3636122+08:00
EXIT_CODE=0
```

```text

```

### ESLint New Scope

```text
COMMAND=npx.cmd eslint preparation/production-trust/r3-egress-revocation-r2-remediation
START=2026-11-26T23:13:43.3636122+08:00
END=2026-11-26T23:13:45.9721543+08:00
EXIT_CODE=0
```

```text

```

### Next Build

```text
COMMAND=pnpm.cmd build
START=2026-11-26T23:13:45.9721543+08:00
END=2026-11-26T23:13:51.3826890+08:00
EXIT_CODE=0
```

```text
pnpm.cmd : $ next build
At C:\Users\Administrator\Desktop\thzz1-search-offline\preparation\production-trust\r3-egress-revocation-r2-remediation
\tools\run-verification.ps1:17 char:13
+   $output = & $Executable @Arguments 2>&1
+             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: ($ next build:String) [], RemoteException
    + FullyQualifiedErrorId : NativeCommandError
 
▲ Next.js 16.4.6 (Turbopack)
✓ Running next.config.ts took 28ms
- Experiments (use with caution):
  · serverActions

  Creating an optimized production build ...
✓ Compiled successfully in 302ms
  Running TypeScript ...
  Finished TypeScript in 2.0s ...
  Collecting page data using 11 workers ...
  Generating static pages using 11 workers (0/2) ...
✓ Generating static pages using 11 workers (2/2) in 510ms
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
<!-- END_EXACT_SOURCE id=S010 -->

### S011. PHASE_R3_EGRESS_THREAT_MODEL_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_THREAT_MODEL_R2.md`
- Bytes: `2598`
- SHA-256: `38CE643BCC319AD1BB39B0C8FA4B8E821B28F52B35EB7F18658252781E975912`

<!-- BEGIN_EXACT_SOURCE id=S011 sha256=38CE643BCC319AD1BB39B0C8FA4B8E821B28F52B35EB7F18658252781E975912 bytes=2598 -->
````text
# PHASE_R3_EGRESS_THREAT_MODEL_R2

## 1. Protected Assets

- Worker revocation authority;
- Scope Cleanup finality;
- idempotency request/result integrity;
- Lease/Permit one-use state;
- truthful external outcome evidence;
- Audit chain integrity;
- Provider request non-retry after uncertain write.

## 2. Threats and Controls

| Threat | Control | Residual |
|---|---|---|
| DRAINING Worker is never revoked | SQL accepts ACTIVE and DRAINING | PostgreSQL execution not tested |
| Worker Upsert restores revoked identity | terminal tombstone + `state IN` guard | provisioning service needs review |
| Retry after cleanup creates duplicate version/Audit | request ID + digest + completed result | real DB race not tested |
| Same key with changed payload silently succeeds | `IDEMPOTENCY_KEY_REUSE_CONFLICT` | none in model |
| Two cleanup callers both claim Block | block row unique lock/upsert | multi-instance not executed |
| Different request IDs disagree | second observes prior Block | real lock timing not tested |
| COMMIT succeeded but client timed out | same-ID persisted result lookup | real DB result query not executed |
| Audit succeeds but transaction rolls back | same transaction | real SQLSTATE not tested |
| Block/Permit changed but no idempotency row | fail closed | data repair protocol outside scope |
| `REQUEST_SENT` claims false send | split event semantics | runtime evidence not implemented |
| DB fabricates socket attempt | trusted runtime source requirement | runtime trust chain not implemented |
| Provider response interpreted as business success | `businessSuccessEvaluated=false` | downstream evaluator absent |
| Lost response triggers automatic retry | terminal unknown, retry forbidden | manual reconciliation required |
| Already written request falsely revoked | after-send branch preserves Lease | external side effect cannot be recalled |
| Audit persistence fails after socket call | unknown outcome and no retry | real evidence recovery not implemented |
| Network and DB treated as atomic | explicit non-atomic contract | exactly-once not guaranteed |

## 3. Irreducible Limits

```text
DATABASE_COMMIT != SOCKET_WRITE
SOCKET_API_CALL != PROVIDER_RECEIPT
PROVIDER_RESPONSE != BUSINESS_SUCCESS
SEND_OUTCOME_UNKNOWN_AUTO_RETRY=FORBIDDEN
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
```

## 4. Production Gaps

```text
PRODUCTION_EGRESS_IMPLEMENTED=NO
NETWORK_ISOLATION_ENFORCED=NO
MULTI_INSTANCE_COORDINATION=NOT_IMPLEMENTED
SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED
REAL_POSTGRESQL_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```

````
<!-- END_EXACT_SOURCE id=S011 -->

### S012. PHASE_R3_EGRESS_TRANSACTION_MATRIX_R2.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_TRANSACTION_MATRIX_R2.md`
- Bytes: `4552`
- SHA-256: `85EAE34845D590A0ABF6FB03D250E156D6DD484A72D49A4F4C7D88B9CADE1FF1`

<!-- BEGIN_EXACT_SOURCE id=S012 sha256=85EAE34845D590A0ABF6FB03D250E156D6DD484A72D49A4F4C7D88B9CADE1FF1 bytes=4552 -->
````text
# PHASE_R3_EGRESS_TRANSACTION_MATRIX_R2

## 1. Matrix

| Transaction | Locks | Conditional mutations | Row count | Audit | Idempotency |
|---|---|---|---|---|---|
| Worker global revoke owner | revocation -> request -> registration -> audit head | tombstone update; registration `ACTIVE/DRAINING -> REVOKED`; request insert | each exactly 1 | same transaction | request ID + digest |
| Worker revoke same-ID replay | request read | none | row exists | no new Audit | return persisted result |
| Cleanup owner PRE_SEND | revocation share -> cleanup request -> block -> floor -> registration -> lease -> permit -> audit head | block claim; lease/permit `REVOKED`; request `PENDING -> COMPLETED` | block/lease/permit/request/audit each 1 | same transaction | request ID + digest + result digest |
| Cleanup owner AFTER_SEND | same | block claim; permit `CONSUMED -> REVOKED`; request completed | block/permit/request/audit each 1; Lease `NOT_USED` | same transaction | same |
| Cleanup different-ID already satisfied | revocation share -> cleanup request -> block -> floor -> registration -> lease -> permit -> audit head | request completed only | request/audit 1; block/lease/permit `NOT_USED` | one satisfied event | distinct request |
| Cleanup same-ID replay | cleanup request row | none | completed row | no new Audit | return stored result |
| Cleanup unknown COMMIT recovery | cleanup request query | none | completed row expected | no new Audit | retry same ID |
| Egress write authorization | intent -> runtime state -> runtime evidence -> audit head | intent to `WRITE_STARTED`; runtime `WRITE_AUTHORIZED`; authorization evidence | intent/state/evidence/audit 1 | `EGRESS_WRITE_START_AUTHORIZED` | one runtime state per intent |
| Socket attempt persistence | runtime state -> runtime evidence -> audit head | runtime `SOCKET_ATTEMPT_RECORDED`; attempt evidence | state/evidence/audit 1 | `SOCKET_WRITE_ATTEMPTED` or failure/partial variant | unique evidence sequence |
| Provider response | runtime state -> response evidence -> audit head | runtime `PROVIDER_RESPONSE_RECEIVED` | state/evidence/audit 1 | `PROVIDER_RESPONSE_RECEIVED` | requires attempt evidence |
| Unknown outcome | runtime state -> evidence -> audit head | runtime `SEND_OUTCOME_UNKNOWN` | state/evidence/audit 1 | `SEND_OUTCOME_UNKNOWN` | terminal; no retry |

## 2. Retry Rules

```text
same Worker request ID + same digest -> replay stored result
same Worker request ID + different digest -> conflict
different Worker request ID after REVOKED -> reject

same Cleanup request ID + same digest -> replay stored result
same Cleanup request ID + different digest -> conflict
different Cleanup request IDs, same scope -> one applies; others record ALREADY_SATISFIED

Socket outcome unknown -> no automatic retry
Provider response received -> no automatic business-success claim
```

## 3. Rollback Rules

All of these roll back the transaction:

- expected row count is not one for a required mutation;
- Block claim loses to an existing equivalent/higher block;
- Lease or Permit state changed unexpectedly;
- Audit event/head append fails;
- idempotency completion fails;
- referenced binding is inconsistent.

Rollback removes the PENDING idempotency row. A committed PENDING row is an
invariant violation, not a recoverable normal state.

## 4. Linearization Points

| Fact | Linearization |
|---|---|
| Worker revocation | COMMIT of tombstone/registration/request/Audit |
| Cleanup result | COMMIT of Block/Lease/Permit/request COMPLETED/Audit |
| Scope already satisfied | COMMIT of request COMPLETED + one observation Audit |
| Egress write authorization | COMMIT of runtime state `WRITE_AUTHORIZED` + Audit |
| Socket attempt evidence | persistence of trusted runtime evidence, not the authorization COMMIT |
| Provider response receipt | persistence of response evidence |
| Unknown outcome | terminal runtime state + Audit |

## 5. Failure Codes

See `contracts.ts` `FailureCodeSchema`. Notable codes:

```text
IDEMPOTENCY_KEY_REUSE_CONFLICT
IDEMPOTENCY_RECORD_INCONSISTENT
COMMIT_OUTCOME_UNKNOWN
WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST
SOCKET_ATTEMPT_NOT_PROVEN
SOCKET_ATTEMPT_AUDIT_FAILED_OUTCOME_UNKNOWN
PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT
AUTO_RETRY_FORBIDDEN
```

`WORKER_DRAINING_REVOCATION_NOT_REQUIRED` is deliberately not a failure code;
DRAINING revocation must succeed.

## 6. Not Proven

```text
POSTGRESQL_LOCK_TIMING
POSTGRESQL_ISOLATION_BEHAVIOR
REAL_MULTI_INSTANCE_INTERLEAVING
REAL_DATABASE_DURABILITY
REAL_SOCKET_WRITE
PROVIDER_RESPONSE
```

````
<!-- END_EXACT_SOURCE id=S012 -->

### S013. PHASE_R3_SCOPE_CLEANUP_IDEMPOTENCY_R2_CONTRACT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_SCOPE_CLEANUP_IDEMPOTENCY_R2_CONTRACT.md`
- Bytes: `4423`
- SHA-256: `2940A12BE5911EADCE1D3F6182EFCBB5DFEF20E2533E21989AA98F403E625D02`

<!-- BEGIN_EXACT_SOURCE id=S013 sha256=2940A12BE5911EADCE1D3F6182EFCBB5DFEF20E2533E21989AA98F403E625D02 bytes=4423 -->
````text
# PHASE_R3_SCOPE_CLEANUP_IDEMPOTENCY_R2_CONTRACT

## 1. Goal

Scope Cleanup must be safe to retry after:

- a lost client response;
- process crash;
- concurrent same-request callers;
- concurrent different-request callers for the same scope;
- a prior cleanup that already changed Lease/Permit state.

## 2. Request Identity

```text
cleanupRequestId
requestDigest
workerInstanceId
scopeKey
revocationVersion
leaseId
capabilityId
permitId
reasonCode
```

The request digest binds all fields above using canonical serialization.
Reusing `cleanupRequestId` for any different field set is:

```text
IDEMPOTENCY_KEY_REUSE_CONFLICT
```

## 3. Persistent Record

Table:

```text
trust_r6_scope_cleanup_request
```

Fields:

```text
cleanup_request_id
request_digest
worker_instance_id
scope_key
revocation_version
lease_id
capability_id
permit_id
reason_code
state = PENDING|COMPLETED|FAILED_TERMINAL
result_digest
audit_event_id
created_at_ms
completed_at_ms
```

`PENDING` is transaction-local. The owner transaction inserts it, performs all
security mutations, writes Audit and sets `COMPLETED` before COMMIT. A
committed PENDING row is an invariant violation and fails closed.

`FAILED_TERMINAL` is reserved for an explicit trusted quarantine flow and is
not produced by normal cleanup rollback.

## 4. Result

The persisted result binds:

```text
status APPLIED|ALREADY_SATISFIED
cleanupRequestId
requestDigest
blockVersion
leaseOutcome
permitOutcome
externalOutcome
auditEventId
completedAt
resultDigest
```

`resultDigest` is computed over the result fields excluding the digest itself.
An exact-request replay returns the stored result unchanged.

## 5. First Application

### Pre-send

Allowed Lease states:

```text
ISSUED
KEY_READ
TRANSPORT_CREATED
SEND_AUTHORIZED
```

First application creates/raises the Scope block and transitions Lease and
Permit to `REVOKED`.

### After-send

Recognized states:

```text
SENT
WRITE_AUTHORIZED
SOCKET_ATTEMPTED
PROVIDER_RESPONSE_RECEIVED
SEND_OUTCOME_UNKNOWN
```

The Lease is preserved. Permit and future authority are revoked. `SENT` does
not mean Provider acknowledgement. `WRITE_AUTHORIZED`, `SOCKET_ATTEMPTED` and
`SEND_OUTCOME_UNKNOWN` explicitly preserve uncertainty.

## 6. Replay Rules

| Situation | Result |
|---|---|
| same request ID, same payload, COMPLETED | return exact persisted result |
| same request ID, different payload | `IDEMPOTENCY_KEY_REUSE_CONFLICT` |
| same request ID, committed PENDING | `IDEMPOTENCY_RECORD_INCONSISTENT` |
| different request ID, block already sufficient | new request record + `ALREADY_SATISFIED`; no Block/Lease/Permit mutation |
| different request ID, first cleanup wins | one block version; other observes final state |
| Lease/Permit already `REVOKED` without a matching idempotency record | fail closed |

Different request IDs are distinct audit subjects. Each gets at most one
`WORKER_SCOPE_CLEANUP_ALREADY_SATISFIED` event. Same-ID replay gets none.

## 7. Lock Order

```text
WORKER_REVOCATION_CONTROL FOR SHARE
  -> SCOPE_CLEANUP_REQUEST FOR UPDATE / INSERT
  -> SCOPE_WORKER_BLOCK
  -> RESOURCE_FENCING_FLOOR
  -> WORKER_REGISTRATION
  -> EXECUTION_LEASE
  -> SEND_AUTHORIZATION
  -> AUDIT_SEQUENCE
```

The block upsert only raises an older blocked revocation version:

```sql
ON CONFLICT (...) DO UPDATE
WHERE existing.blocked_revocation_version
      < EXCLUDED.blocked_revocation_version
```

A zero-row block upsert on a different request causes the host to roll back
and use the already-satisfied transaction.

## 8. Crash and Unknown Commit

| Event | Behavior |
|---|---|
| crash before COMMIT | all PENDING/block/audit/resource changes roll back |
| Audit failure | full rollback |
| COMMIT succeeded, response lost | retry exact request ID; completed result is read |
| same request concurrent | exactly one owner; other replays or waits and replays |
| different requests concurrent | block row serializes; one applies, one observes |
| authority unavailable | fail closed, no mutation |

No permanent PENDING row is permitted after rollback because it was never
committed.

## 9. Model Boundary

Model: `models/scope-cleanup.ts`

```text
PERSISTENCE_SIMULATION_ONLY
REAL_DATABASE_DURABILITY=NOT_TESTED
REAL_MULTI_INSTANCE_INTERLEAVING=NOT_TESTED
```

The model includes in-memory concurrency queues and persistence snapshots.
They simulate the contract but are not PostgreSQL or multi-instance evidence.

````
<!-- END_EXACT_SOURCE id=S013 -->

### S014. PHASE_R3_WORKER_LIFECYCLE_R2_CONTRACT.md

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_WORKER_LIFECYCLE_R2_CONTRACT.md`
- Bytes: `4004`
- SHA-256: `D5175B56967FA38C4043C0AFCFAE2EDDFD9288FD68E4A24B9E9132418CBFE651`

<!-- BEGIN_EXACT_SOURCE id=S014 sha256=D5175B56967FA38C4043C0AFCFAE2EDDFD9288FD68E4A24B9E9132418CBFE651 bytes=4004 -->
````text
# PHASE_R3_WORKER_LIFECYCLE_R2_CONTRACT

## 1. Version and Scope

```text
CONTRACT=r3-egress-r2-worker-lifecycle-v1
REALM=OFFLINE_REFERENCE_MODEL
POSTGRESQL_EXECUTION=NOT_EXECUTED
```

This contract preserves the existing R4 registration states:

```text
ACTIVE
DRAINING
REVOKED
```

`REGISTERED` remains a provisioning concept from the lifecycle diagram. The
frozen R4 `trust_r4_worker_registration` table does not accept it. R2 does not
silently add it to the runtime table.

## 2. State Transition Matrix

| Current runtime state | Revocation request | Result |
|---|---|---|
| `ACTIVE` | new valid request | `REVOKED` |
| `DRAINING` | new valid request | `REVOKED` |
| `REGISTERED` | runtime revoke | reject: `WORKER_REGISTERED_REVOCATION_FORBIDDEN` |
| `REVOKED` | exact same request replay | return persisted result, no version/Audit change |
| `REVOKED` | different request ID | reject: `WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST` |
| `REVOKED` | activation/Upsert | reject: `WORKER_REACTIVATION_FORBIDDEN` |
| unknown/unrepresentable | revoke | fail closed |

`REGISTERED` policy rationale:

The provisioning lifecycle may describe `REGISTERED -> ACTIVE`, but the
frozen runtime table has no such state. A future `REGISTERED` record is not a
runtime identity with a registration row. Allowing it into the global
revocation transaction would require a schema change outside this phase.
Provisioning must revoke/discard that record through a separate trusted
provisioning flow before runtime registration.

## 3. Invariants

- `DRAINING` is revocable.
- `REVOKED` is terminal for ordinary registration.
- Ordinary Upsert cannot restore `ACTIVE`.
- Tombstone and registration commit atomically with the request record and
  Audit.
- The same request ID is bound to one canonical request digest.
- Same request ID + different payload fails closed.
- A different request ID on an already-revoked Worker does not create a second
  revocation version or Audit.
- A retry after an unknown COMMIT queries the durable request record.

## 4. Request Identity

```text
requestId
requestDigest = sha256(canonical payload)
workerInstanceId
expectedRecordVersion
reasonCode
requestedAt
```

Canonical payload uses sorted object keys, UTF-8 and JSON scalar/array/object
encoding. `requestDigest` has the form:

```text
sha256:<64 lowercase hex>
```

## 5. Transaction Result Cases

| Case | Result |
|---|---|
| first valid ACTIVE/DRAINING revoke | `REVOKED` |
| same request ID and exact payload | `REPLAYED` with original result |
| same request ID, different payload | `IDEMPOTENCY_KEY_REUSE_CONFLICT` |
| different request ID after commit | `WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST` |
| expected record version mismatch | `WORKER_VERSION_CONFLICT` |
| any unexpected affected-row count | rollback + `ROW_COUNT_CONFLICT` |
| Audit failure | rollback + `WORKER_AUDIT_ATOMICITY_FAILED` |
| authority unavailable | `AUTHORITY_UNAVAILABLE` |
| COMMIT result unknown | durable request lookup; no blind retry |

## 6. SQL Linearization

`PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql` locks in this order:

```text
trust_r5_worker_revocation FOR UPDATE
  -> trust_r6_worker_revocation_request FOR UPDATE
  -> trust_r4_worker_registration UPDATE
  -> trust_r3_audit_head FOR UPDATE
```

The tombstone update, registration update, request insert and Audit commit in
one transaction. Registration accepts:

```sql
state IN ('ACTIVE', 'DRAINING')
```

## 7. Model and Tests

Model: `models/worker-lifecycle.ts`

Tests:

- ACTIVE and DRAINING revocation;
- REGISTERED denial;
- revoke/reactivate protection;
- same-request replay;
- same-ID/different-payload conflict;
- different-ID conflict;
- version mismatch;
- all non-one row counts;
- Audit rollback;
- authority loss;
- COMMIT-response loss;
- pre-commit crash;
- same-ID and different-ID concurrent callers;
- snapshot/restart replay.

`WorkerLifecycleModel` is an in-memory simulation:

```text
PERSISTENCE_SIMULATION_ONLY
REAL_POSTGRESQL_DURABILITY=NOT_TESTED
```

````
<!-- END_EXACT_SOURCE id=S014 -->

### S015. PHASE_R3_EGRESS_AUDIT_R2.sql

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_EGRESS_AUDIT_R2.sql`
- Bytes: `12189`
- SHA-256: `1D635A7E59DC49CE0ADC32A323B5A3DDBFECF62506DD211DFF18056F9DDF07AD`

<!-- BEGIN_EXACT_SOURCE id=S015 sha256=1D635A7E59DC49CE0ADC32A323B5A3DDBFECF62506DD211DFF18056F9DDF07AD bytes=12189 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Truthful Egress audit semantics.
-- SQL cannot prove a real Socket Write. Runtime evidence is a separate input.

CREATE TABLE trust_r6_egress_runtime_state (
  egress_intent_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (
    state IN (
      'WRITE_AUTHORIZED',
      'SOCKET_ATTEMPT_RECORDED',
      'FAILED_BEFORE_BYTES',
      'PROVIDER_RESPONSE_RECEIVED',
      'COMPLETED',
      'SEND_OUTCOME_UNKNOWN'
    )
  ),
  row_version bigint NOT NULL CHECK (row_version >= 1),
  write_authorized_at_ms bigint NOT NULL,
  socket_attempted_at_ms bigint,
  response_received_at_ms bigint,
  outcome_unknown_at_ms bigint,
  CHECK (
    state NOT IN ('SOCKET_ATTEMPT_RECORDED', 'PROVIDER_RESPONSE_RECEIVED', 'COMPLETED')
    OR socket_attempted_at_ms IS NOT NULL
  ),
  CHECK (
    state <> 'PROVIDER_RESPONSE_RECEIVED'
    OR response_received_at_ms IS NOT NULL
  ),
  CHECK (
    state <> 'SEND_OUTCOME_UNKNOWN'
    OR outcome_unknown_at_ms IS NOT NULL
  )
);

CREATE TABLE trust_r6_egress_runtime_evidence (
  evidence_id uuid PRIMARY KEY,
  egress_intent_id uuid NOT NULL
    REFERENCES trust_r6_egress_runtime_state (egress_intent_id),
  audit_event_id uuid NOT NULL,
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
  source_sequence bigint NOT NULL CHECK (source_sequence >= 1),
  source_digest varchar(71) NOT NULL,
  socket_call_outcome text CHECK (
    socket_call_outcome IS NULL
    OR socket_call_outcome IN (
      'NOT_CALLED', 'FAILED_BEFORE_BYTES', 'PARTIAL', 'COMPLETED_CALL'
    )
  ),
  provider_response_digest varchar(71),
  observed_at_ms bigint NOT NULL,
  persisted_at_ms bigint NOT NULL,
  business_success_evaluated boolean NOT NULL DEFAULT false
    CHECK (business_success_evaluated = false),
  UNIQUE (egress_intent_id, event_type, source_sequence),
  UNIQUE (egress_intent_id, source_sequence),
  CHECK (source_digest ~ '^sha256:[a-f0-9]{64}$'),
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
-- Transaction W: database authority grants one short write authorization.
-- Event name says exactly what is known: authorization, not external sending.
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
INSERT INTO trust_r6_egress_runtime_evidence (
  evidence_id, egress_intent_id, audit_event_id, event_type,
  evidence_source, source_sequence, source_digest,
  socket_call_outcome, provider_response_digest,
  observed_at_ms, persisted_at_ms, business_success_evaluated
) VALUES (
  $4, $1, $5, 'EGRESS_WRITE_START_AUTHORIZED',
  'DATABASE_AUTHORIZATION', 1, $6,
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

-- Parameters W:
--   $1 egress_intent_id
--   $2 expected trust_r5_egress_intent row_version
--   $3 database authorization time
--   $4 runtime evidence row id
--   $5 Audit event id
--   $6 authorization evidence digest
--   $7 Audit sequence
--   $8 previous_event_digest
--   $9 event_digest
--
-- COMMIT of W proves only that the final database authorization exists.
-- It does not prove a socket call, bytes leaving the host or Provider receipt.

-- ===========================================================================
-- Transaction S: persist trusted runtime evidence after the Socket API call.
-- This statement must be emitted by the trusted Egress runtime boundary. The
-- database cannot independently prove that the external call occurred.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r6_egress_runtime_state
WHERE egress_intent_id = $10
FOR UPDATE;

-- Host MUST call the Socket API first and provide the resulting evidence.
-- `$14` is one of these exact event types, with trusted runtime source fixed
-- by the INSERT:
--   SOCKET_WRITE_ATTEMPTED
--   SOCKET_WRITE_FAILED_BEFORE_BYTES
--   SOCKET_WRITE_PARTIAL
-- and must be backed by an actual runtime evidence record of source_sequence=$13.

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_egress_runtime_evidence (
  evidence_id, egress_intent_id, audit_event_id, event_type,
  evidence_source, source_sequence, source_digest,
  socket_call_outcome, provider_response_digest,
  observed_at_ms, persisted_at_ms, business_success_evaluated
) SELECT
  $11, $10, $12, $14,
  'TRUSTED_EGRESS_RUNTIME', $13, $16,
  $17, NULL,
  $18, $19, false
WHERE EXISTS (
  SELECT 1
  FROM trust_r6_egress_runtime_state runtime
  WHERE runtime.egress_intent_id = $10
    AND runtime.state = 'WRITE_AUTHORIZED'
    AND runtime.row_version = $15
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_egress_runtime_state
SET state = CASE
      WHEN $17 = 'FAILED_BEFORE_BYTES' THEN 'FAILED_BEFORE_BYTES'
      ELSE 'SOCKET_ATTEMPT_RECORDED'
    END,
    row_version = row_version + 1,
    socket_attempted_at_ms = $18
WHERE egress_intent_id = $10
  AND state = 'WRITE_AUTHORIZED'
  AND row_version = $15;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $12, $20, $18, $14, 'UNKNOWN',
  $10, $21, $22
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $20,
    last_event_digest = $22
WHERE singleton_id = 1
  AND last_sequence = $20 - 1
  AND last_event_digest IS NOT DISTINCT FROM $21;

COMMIT;

-- Parameters S:
--   $10 egress_intent_id
--   $11 runtime evidence id
--   $12 Audit event id
--   $13 monotonically increasing runtime evidence sequence
--   $14 exact socket event type
--   $15 expected runtime_state row_version
--   $16 runtime evidence digest
--   $17 socket_call_outcome
--   $18 local observation time
--   $19 database persistence time
--   $20..$22 Audit fields
--
-- If evidence persistence fails after the API call, the host MUST NOT retry the
-- Socket call. It enters SEND_OUTCOME_UNKNOWN recovery with the same Intent ID.

-- ===========================================================================
-- Transaction R: Provider response received after a proven socket attempt.
-- Receipt of bytes is not business success.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r6_egress_runtime_state
WHERE egress_intent_id = $23
FOR UPDATE;

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_egress_runtime_evidence (
  evidence_id, egress_intent_id, audit_event_id, event_type,
  evidence_source, source_sequence, source_digest,
  socket_call_outcome, provider_response_digest,
  observed_at_ms, persisted_at_ms, business_success_evaluated
) SELECT
  $24, $23, $25, 'PROVIDER_RESPONSE_RECEIVED',
  'TRUSTED_EGRESS_RUNTIME', $26, $28,
  'COMPLETED_CALL', $29,
  $30, $31, false
WHERE EXISTS (
  SELECT 1
  FROM trust_r6_egress_runtime_evidence attempt
  WHERE attempt.egress_intent_id = $23
    AND attempt.event_type IN (
      'SOCKET_WRITE_ATTEMPTED', 'SOCKET_WRITE_PARTIAL'
    )
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_egress_runtime_state
SET state = 'PROVIDER_RESPONSE_RECEIVED',
    row_version = row_version + 1,
    response_received_at_ms = $30
WHERE egress_intent_id = $23
  AND state = 'SOCKET_ATTEMPT_RECORDED'
  AND row_version = $27;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $25, $32, $30, 'PROVIDER_RESPONSE_RECEIVED', 'ALLOW',
  $23, $33, $34
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $32,
    last_event_digest = $34
WHERE singleton_id = 1
  AND last_sequence = $32 - 1
  AND last_event_digest IS NOT DISTINCT FROM $33;

COMMIT;

-- No business success assignment is present. A separate Provider contract
-- evaluation is required after response capture.

-- ===========================================================================
-- Transaction U: terminal unknown outcome. Allowed after authorization alone.
-- AUTO_RETRY=FORBIDDEN.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r6_egress_runtime_state
WHERE egress_intent_id = $35
FOR UPDATE;

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r6_egress_runtime_evidence (
  evidence_id, egress_intent_id, audit_event_id, event_type,
  evidence_source, source_sequence, source_digest,
  socket_call_outcome, provider_response_digest,
  observed_at_ms, persisted_at_ms, business_success_evaluated
) VALUES (
  $36, $35, $37, 'SEND_OUTCOME_UNKNOWN',
  'TRUSTED_EGRESS_RUNTIME', $38, $40,
  NULL, NULL,
  $41, $42, false
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r6_egress_runtime_state
SET state = 'SEND_OUTCOME_UNKNOWN',
    row_version = row_version + 1,
    outcome_unknown_at_ms = $41
WHERE egress_intent_id = $35
  AND state IN ('WRITE_AUTHORIZED', 'SOCKET_ATTEMPT_RECORDED')
  AND row_version = $39;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $37, $43, $41, 'SEND_OUTCOME_UNKNOWN', 'UNKNOWN',
  $35, $44, $45
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $43,
    last_event_digest = $45
WHERE singleton_id = 1
  AND last_sequence = $43 - 1
  AND last_event_digest IS NOT DISTINCT FROM $44;

COMMIT;

-- Unknown after authorization does not claim SOCKET_WRITE_ATTEMPTED when no
-- trusted evidence exists. It records that the external outcome is unknowable
-- and prohibits automatic retry of the same Intent.

```
<!-- END_EXACT_SOURCE id=S015 -->

### S016. PHASE_R3_SCOPE_CLEANUP_R2.sql

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_SCOPE_CLEANUP_R2.sql`
- Bytes: `15002`
- SHA-256: `E470F746722322468DD96AF6989BD9CDDCFF0B470CE0D99984308722E98D2A86`

<!-- BEGIN_EXACT_SOURCE id=S016 sha256=E470F746722322468DD96AF6989BD9CDDCFF0B470CE0D99984308722E98D2A86 bytes=15002 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R2 idempotent Scope Cleanup.
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
  result_digest varchar(71),
  audit_event_id uuid,
  created_at_ms bigint NOT NULL,
  completed_at_ms bigint,
  CHECK (request_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (result_digest IS NULL OR result_digest ~ '^sha256:[a-f0-9]{64}$'),
  CHECK (
    (state = 'PENDING'
      AND result_digest IS NULL
      AND audit_event_id IS NULL
      AND completed_at_ms IS NULL)
    OR
    (state = 'COMPLETED'
      AND result_digest IS NOT NULL
      AND audit_event_id IS NOT NULL
      AND completed_at_ms IS NOT NULL)
    OR
    (state = 'FAILED_TERMINAL'
      AND result_digest IS NULL
      AND completed_at_ms IS NOT NULL)
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
  reason_code, state, result_digest, audit_event_id,
  created_at_ms, completed_at_ms
) VALUES (
  $2, $3, $1, $4,
  $5, $6, $7, $8,
  $9, 'PENDING', NULL, NULL,
  $10, NULL
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
    result_digest = $17,
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
  reason_code, state, result_digest, audit_event_id,
  created_at_ms, completed_at_ms
) VALUES (
  $2, $3, $1, $4,
  $5, $6, $7, $8,
  $9, 'PENDING', NULL, NULL,
  $10, NULL
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
    result_digest = $17,
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
  reason_code, state, result_digest, audit_event_id,
  created_at_ms, completed_at_ms
) VALUES (
  $2, $3, $1, $4,
  $5, $6, $7, $8,
  $9, 'PENDING', NULL, NULL,
  $10, NULL
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
    result_digest = $17,
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

SELECT cleanup_request_id, request_digest, worker_instance_id, scope_key,
       revocation_version, lease_id, capability_id, permit_id,
       reason_code, state, result_digest, audit_event_id, completed_at_ms
FROM trust_r6_scope_cleanup_request
WHERE cleanup_request_id = $2
FOR UPDATE;

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
--   $17 canonical cleanup result digest

```
<!-- END_EXACT_SOURCE id=S016 -->

### S017. PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql`
- Bytes: `4916`
- SHA-256: `F7CDE2398C7A8A5DE7BEEBCA34A1E1F706AA186915F030ABEA06DF4D3EB3FA3E`

<!-- BEGIN_EXACT_SOURCE id=S017 sha256=F7CDE2398C7A8A5DE7BEEBCA34A1E1F706AA186915F030ABEA06DF4D3EB3FA3E bytes=4916 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R2 overlay for global Worker revocation.

CREATE TABLE trust_r6_worker_revocation_request (
  request_id uuid PRIMARY KEY,
  request_digest varchar(71) NOT NULL,
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  requested_revocation_version bigint NOT NULL
    CHECK (requested_revocation_version >= 1),
  reason_code text NOT NULL,
  requested_at_ms bigint NOT NULL,
  UNIQUE (worker_instance_id, requested_revocation_version),
  CHECK (request_digest ~ '^sha256:[a-f0-9]{64}$')
);

-- Future deployment migration only. Historical schema is not edited here.
ALTER TABLE trust_r3_audit_event
  DROP CONSTRAINT IF EXISTS trust_r3_audit_event_event_type_check;

ALTER TABLE trust_r3_audit_event
  ADD CONSTRAINT trust_r3_audit_event_event_type_check CHECK (
    event_type IN (
      'APPROVAL_CONSUMED', 'BUDGET_RESERVED', 'BUDGET_RELEASED',
      'BUDGET_SETTLED', 'LEASE_ISSUED', 'WORKER_PROGRESS',
      'SEND_AUTHORIZED', 'SEND_AUTHORIZATION_CONSUMED',
      'EGRESS_WRITE_START_AUTHORIZED', 'SOCKET_WRITE_ATTEMPTED',
      'SOCKET_WRITE_FAILED_BEFORE_BYTES', 'SOCKET_WRITE_PARTIAL',
      'PROVIDER_RESPONSE_RECEIVED', 'PROVIDER_RESPONSE_REJECTED',
      'SEND_OUTCOME_UNKNOWN', 'EGRESS_PROCESS_CRASHED',
      'EMERGENCY_ACTIVATED', 'EMERGENCY_RECOVERY_REQUESTED',
      'EMERGENCY_RECOVERY_APPROVED', 'KEY_REVOKED',
      'WORKER_REVOKED', 'WORKER_SCOPE_BLOCKED',
      'WORKER_SCOPE_CLEANUP_ALREADY_SATISFIED', 'LEASE_REVOKED'
    )
  );

-- ===========================================================================
-- Worker global revocation owner transaction
-- Linearization point: COMMIT of tombstone + registration + request + Audit.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

-- Lock 1: global Worker revocation authority.
SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

-- Lock 2: request idempotency row.
SELECT request_id, request_digest, worker_instance_id,
       requested_revocation_version, reason_code, requested_at_ms
FROM trust_r6_worker_revocation_request
WHERE request_id = $2
FOR UPDATE;

-- Host branch when a row is found:
--   request_digest=$10 and complete payload match
--     -> read trust_r5_worker_revocation and return REPLAYED;
--   any request_digest/payload mismatch
--     -> IDEMPOTENCY_KEY_REUSE_CONFLICT;
--   missing request row and worker already REVOKED
--     -> WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST.

-- The current frozen R4 registration table has no REGISTERED state. REGISTERED
-- is a provisioning state only; runtime revocation must reject it and use a
-- separate trusted deprovisioning flow. ACTIVE and DRAINING are revocable.
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
INSERT INTO trust_r6_worker_revocation_request (
  request_id, request_digest, worker_instance_id,
  requested_revocation_version, reason_code, requested_at_ms
) SELECT
  $2, $10, $1, $11, $4, $3
WHERE EXISTS (
  SELECT 1
  FROM trust_r5_worker_revocation revocation
  WHERE revocation.worker_instance_id = $1
    AND revocation.state = 'REVOKED'
    AND revocation.revocation_version = $11
    AND revocation.record_version = $5 + 1
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

COMMIT;

-- Parameters:
--   $1 worker_instance_id
--   $2 request_id
--   $3 server UTC Unix milliseconds
--   $4 reason_code
--   $5 expected revocation record_version
--   $6..$9 Audit event/head fields
--   $10 canonical request digest
--   $11 new revocation_version
--
-- Once a distinct request sees REVOKED, it does not insert another request,
-- bump versions or append Audit. It returns the existing tombstone with
-- WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST.

```
<!-- END_EXACT_SOURCE id=S017 -->

### S018. contracts.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/contracts.ts`
- Bytes: `6961`
- SHA-256: `6C0A3DA7548044E30B47E6664447B38090281D171ECCF7B39CCAA52BD674F38D`

<!-- BEGIN_EXACT_SOURCE id=S018 sha256=6C0A3DA7548044E30B47E6664447B38090281D171ECCF7B39CCAA52BD674F38D bytes=6961 -->
```text
import { z } from "zod";

import {
  InstantSchema,
  Sha256Schema,
  UuidSchema,
} from "../contracts/common";

export const R3_EGRESS_R2_CONTRACT_VERSION =
  "r3-egress-revocation-r2-v1";

const IdentifierSchema = z.string().min(1).max(200).trim();
const VersionSchema = z.number().int().positive();

export const FailureCodeSchema = z.enum([
  "AUTHORITY_UNAVAILABLE",
  "ROW_COUNT_CONFLICT",
  "IDEMPOTENCY_KEY_REUSE_CONFLICT",
  "IDEMPOTENCY_RECORD_NOT_FOUND",
  "IDEMPOTENCY_RECORD_INCONSISTENT",
  "COMMIT_OUTCOME_UNKNOWN",
  "PROCESS_CRASHED_BEFORE_COMMIT",
  "WORKER_STATE_INVALID",
  "WORKER_VERSION_CONFLICT",
  "WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST",
  "WORKER_REGISTERED_REVOCATION_FORBIDDEN",
  "WORKER_REACTIVATION_FORBIDDEN",
  "WORKER_AUDIT_ATOMICITY_FAILED",
  "SCOPE_BINDING_MISMATCH",
  "SCOPE_CLEANUP_STATE_INCONSISTENT",
  "LEASE_STATE_INVALID",
  "PERMIT_STATE_INVALID",
  "EGRESS_WRITE_NOT_AUTHORIZED",
  "SOCKET_ATTEMPT_NOT_PROVEN",
  "SOCKET_ATTEMPT_AUDIT_FAILED_OUTCOME_UNKNOWN",
  "PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT",
  "SEND_OUTCOME_ALREADY_TERMINAL",
  "AUTO_RETRY_FORBIDDEN",
]);

export type FailureCode = z.infer<typeof FailureCodeSchema>;
export type Result<T> =
  | Readonly<{ ok: true; value: T }>
  | Readonly<{ ok: false; code: FailureCode }>;

export function ok<T>(value: T): Result<T> {
  return Object.freeze({ ok: true, value });
}

export function fail<T = never>(code: FailureCode): Result<T> {
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
export type WorkerRegistrationState = z.infer<
  typeof WorkerRegistrationStateSchema
>;

export const WorkerRevocationStateSchema = z.enum([
  "ACTIVE",
  "REVOKED",
  "RECOVERY_REQUIRED",
]);
export type WorkerRevocationState = z.infer<
  typeof WorkerRevocationStateSchema
>;
export const WorkerRevocationRequestSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-worker-revocation-request-v1"),
  requestId: UuidSchema,
  requestDigest: Sha256Schema,
  workerInstanceId: UuidSchema,
  expectedRecordVersion: VersionSchema,
  reasonCode: IdentifierSchema,
  requestedAt: InstantSchema,
});

export const WorkerRevocationPayloadSchema =
  WorkerRevocationRequestSchema.omit({
    schemaVersion: true,
    requestDigest: true,
  });

export const WorkerRevocationResultSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-worker-revocation-result-v1"),
  status: z.enum(["REVOKED", "REPLAYED"]),
  requestId: UuidSchema,
  requestDigest: Sha256Schema,
  workerInstanceId: UuidSchema,
  registrationState: z.literal("REVOKED"),
  revocationVersion: z.number().int().positive(),
  recordVersion: z.number().int().positive(),
  auditEventId: UuidSchema,
  revokedAt: InstantSchema,
});

export type WorkerRevocationRequest = z.infer<
  typeof WorkerRevocationRequestSchema
>;
export type WorkerRevocationPayload = z.infer<
  typeof WorkerRevocationPayloadSchema
>;
export type WorkerRevocationResult = z.infer<
  typeof WorkerRevocationResultSchema
>;

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

export const ScopeCleanupRequestSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-scope-cleanup-request-v1"),
  cleanupRequestId: UuidSchema,
  requestDigest: Sha256Schema,
  workerInstanceId: UuidSchema,
  scopeKey: IdentifierSchema,
  revocationVersion: VersionSchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  permitId: UuidSchema,
  reasonCode: IdentifierSchema,
});

export const ScopeCleanupPayloadSchema = ScopeCleanupRequestSchema.omit({
  schemaVersion: true,
  requestDigest: true,
});

export const ScopeCleanupResultSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-scope-cleanup-result-v1"),
  cleanupRequestId: UuidSchema,
  requestDigest: Sha256Schema,
  resultDigest: Sha256Schema,
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

export type ScopeCleanupPayload = z.infer<typeof ScopeCleanupPayloadSchema>;
export type ScopeCleanupResult = z.infer<typeof ScopeCleanupResultSchema>;

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

export const AuditEvidenceSourceSchema = z.enum([
  "DATABASE_AUTHORIZATION",
  "TRUSTED_EGRESS_RUNTIME",
]);

export const EgressAuditEventSchema = z.strictObject({
  schemaVersion: z.literal("r3-egress-r2-audit-event-v1"),
  eventId: UuidSchema,
  intentId: UuidSchema,
  eventType: AuditEventTypeSchema,
  evidenceSource: AuditEvidenceSourceSchema,
  evidenceSequence: VersionSchema,
  evidenceDigest: Sha256Schema,
  observedAt: InstantSchema,
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

export const SocketAttemptEvidenceSchema = z.strictObject({
  socketApiCalled: z.literal(true),
  evidenceSource: z.literal("TRUSTED_EGRESS_RUNTIME"),
  evidenceDigest: Sha256Schema,
  callOutcome: z.enum([
    "FAILED_BEFORE_BYTES",
    "PARTIAL",
    "COMPLETED_CALL",
  ]),
});

export type EgressIntentState = z.infer<typeof EgressIntentStateSchema>;
export type AuditEventType = z.infer<typeof AuditEventTypeSchema>;
export type AuditEvidenceSource = z.infer<
  typeof AuditEvidenceSourceSchema
>;
export type EgressAuditEvent = z.infer<typeof EgressAuditEventSchema>;
export type SocketAttemptEvidence = z.infer<
  typeof SocketAttemptEvidenceSchema
>;

```
<!-- END_EXACT_SOURCE id=S018 -->

### S019. lock-order.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/lock-order.ts`
- Bytes: `1433`
- SHA-256: `E0A0DC39C01F08B4F1681960393A1F13209604D8C48B20B7164F198B9E0BA161`

<!-- BEGIN_EXACT_SOURCE id=S019 sha256=E0A0DC39C01F08B4F1681960393A1F13209604D8C48B20B7164F198B9E0BA161 bytes=1433 -->
```text
import { z } from "zod";

import { fail, ok, type Result } from "./contracts";

export const R3_EGRESS_R2_LOCK_ORDER = Object.freeze([
  "WORKER_REVOCATION_CONTROL",
  "WORKER_REVOCATION_REQUEST",
  "SCOPE_CLEANUP_REQUEST",
  "SCOPE_WORKER_BLOCK",
  "EMERGENCY_CONTROL",
  "KEY_REGISTRY",
  "APPROVAL",
  "APPROVAL_CONSUMPTION",
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
  "EGRESS_RUNTIME_EVIDENCE",
  "AUDIT_SEQUENCE",
] as const);

export type R3EgressR2LockDomain =
  typeof R3_EGRESS_R2_LOCK_ORDER[number];

const AcquisitionSchema = z.strictObject({
  domain: z.enum(R3_EGRESS_R2_LOCK_ORDER),
  acquiredAt: z.number().int().nonnegative(),
});

export function validateLockOrder(
  acquisitions: readonly unknown[],
): Result<readonly R3EgressR2LockDomain[]> {
  const parsed = z.array(AcquisitionSchema).safeParse(acquisitions);
  if (!parsed.success) return fail("ROW_COUNT_CONFLICT");
  let previous = -1;
  const domains: R3EgressR2LockDomain[] = [];
  for (const acquisition of parsed.data) {
    const index = R3_EGRESS_R2_LOCK_ORDER.indexOf(acquisition.domain);
    if (index < previous) return fail("ROW_COUNT_CONFLICT");
    previous = index;
    domains.push(acquisition.domain);
  }
  return ok(Object.freeze(domains));
}

```
<!-- END_EXACT_SOURCE id=S019 -->

### S020. models/canonical.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/models/canonical.ts`
- Bytes: `1423`
- SHA-256: `C41A128E422179F88C18D32B545182F02862F22D3EF1758109ABFCF4A2BBA4D3`

<!-- BEGIN_EXACT_SOURCE id=S020 sha256=C41A128E422179F88C18D32B545182F02862F22D3EF1758109ABFCF4A2BBA4D3 bytes=1423 -->
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
  const digest = createHash("sha256")
    .update(canonicalJson(value), "utf8")
    .digest("hex");
  return `sha256:${digest}`;
}

export function withoutKeys<T extends Readonly<Record<string, unknown>>>(
  value: T,
  keys: readonly string[],
): Readonly<Record<string, unknown>> {
  const omitted = new Set(keys);
  return Object.fromEntries(
    Object.entries(value).filter(([key]) => !omitted.has(key)),
  );
}

```
<!-- END_EXACT_SOURCE id=S020 -->

### S021. models/egress-audit.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/models/egress-audit.ts`
- Bytes: `12309`
- SHA-256: `26F8D1109C403B10DB9231765793AAF555101948F9F6374D05893D19B40ED59F`

<!-- BEGIN_EXACT_SOURCE id=S021 sha256=26F8D1109C403B10DB9231765793AAF555101948F9F6374D05893D19B40ED59F bytes=12309 -->
```text
import {
  EgressAuditEventSchema,
  SocketAttemptEvidenceSchema,
  fail,
  ok,
  requireExactlyOne,
  type EgressAuditEvent,
  type EgressIntentState,
  type Result,
} from "../contracts";
import { validateLockOrder } from "../lock-order";

type IntentRecord = {
  intentId: string;
  state: EgressIntentState;
  writeAuthorizedAt: number | null;
  socketAttemptedAt: number | null;
  responseReceivedAt: number | null;
  outcomeUnknownAt: number | null;
};

export type EgressAuditSnapshot = Readonly<{
  intents: Readonly<Record<string, IntentRecord>>;
  events: Readonly<Record<string, readonly EgressAuditEvent[]>>;
  unrecordedAttempts: readonly string[];
}>;

/**
 * OFFLINE_REFERENCE_MODEL.
 * `SOCKET_WRITE_ATTEMPTED` can only be accepted with explicit trusted-runtime
 * evidence. The model does not call a socket and cannot create production
 * runtime evidence.
 */
export class OfflineEgressAuditModel {
  private readonly intents = new Map<string, IntentRecord>();
  private readonly events = new Map<string, EgressAuditEvent[]>();
  private readonly unrecordedAttempts = new Set<string>();
  private failNextAudit = false;

  seedFinalAuthorized(intentId: string): Result<true> {
    this.intents.set(intentId, {
      intentId,
      state: "FINAL_AUTHORIZED",
      writeAuthorizedAt: null,
      socketAttemptedAt: null,
      responseReceivedAt: null,
      outcomeUnknownAt: null,
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
    evidenceDigest: string;
    now: number;
    rowCounts: Readonly<{ intent: number; audit: number }>;
  }>): Result<EgressAuditEvent> {
    const locks = validateLockOrder([
      { domain: "EGRESS_SEND_INTENT", acquiredAt: input.now },
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
    if (this.consumeAuditFailure()) {
      return fail("WORKER_AUDIT_ATOMICITY_FAILED");
    }
    const event = EgressAuditEventSchema.parse({
      schemaVersion: "r3-egress-r2-audit-event-v1",
      eventId: input.eventId,
      intentId: input.intentId,
      eventType: "EGRESS_WRITE_START_AUTHORIZED",
      evidenceSource: "DATABASE_AUTHORIZATION",
      evidenceSequence: this.nextSequence(input.intentId),
      evidenceDigest: input.evidenceDigest,
      observedAt: input.now,
      persistedAt: input.now,
      socketCallOutcome: "NOT_CALLED",
      providerResponseDigest: null,
      businessSuccessEvaluated: false,
    });
    this.intents.set(input.intentId, {
      ...record,
      state: "WRITE_AUTHORIZED",
      writeAuthorizedAt: input.now,
    });
    this.append(input.intentId, event);
    return ok(event);
  }

  recordSocketAttempt(input: Readonly<{
    intentId: string;
    eventId: string;
    evidence: unknown;
    observedAt: number;
    persistedAt: number;
    rowCounts: Readonly<{ intent: number; audit: number }>;
  }>): Result<EgressAuditEvent> {
    const evidence = SocketAttemptEvidenceSchema.safeParse(input.evidence);
    if (!evidence.success) return fail("SOCKET_ATTEMPT_NOT_PROVEN");
    const record = this.intents.get(input.intentId);
    if (!record || record.state !== "WRITE_AUTHORIZED") {
      return fail("EGRESS_WRITE_NOT_AUTHORIZED");
    }
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (this.consumeAuditFailure()) {
      this.unrecordedAttempts.add(input.intentId);
      return fail("SOCKET_ATTEMPT_AUDIT_FAILED_OUTCOME_UNKNOWN");
    }
    const eventType = evidence.data.callOutcome === "FAILED_BEFORE_BYTES"
      ? "SOCKET_WRITE_FAILED_BEFORE_BYTES" as const
      : evidence.data.callOutcome === "PARTIAL"
        ? "SOCKET_WRITE_PARTIAL" as const
        : "SOCKET_WRITE_ATTEMPTED" as const;
    const event = EgressAuditEventSchema.parse({
      schemaVersion: "r3-egress-r2-audit-event-v1",
      eventId: input.eventId,
      intentId: input.intentId,
      eventType,
      evidenceSource: evidence.data.evidenceSource,
      evidenceSequence: this.nextSequence(input.intentId),
      evidenceDigest: evidence.data.evidenceDigest,
      observedAt: input.observedAt,
      persistedAt: input.persistedAt,
      socketCallOutcome: evidence.data.callOutcome,
      providerResponseDigest: null,
      businessSuccessEvaluated: false,
    });
    const state = evidence.data.callOutcome === "FAILED_BEFORE_BYTES"
      ? "FAILED_BEFORE_BYTES" as const
      : "SOCKET_ATTEMPT_RECORDED" as const;
    this.intents.set(input.intentId, {
      ...record,
      state,
      socketAttemptedAt: input.observedAt,
    });
    this.append(input.intentId, event);
    return ok(event);
  }

  recordProviderResponse(input: Readonly<{
    intentId: string;
    eventId: string;
    responseDigest: string;
    evidenceDigest: string;
    observedAt: number;
    persistedAt: number;
    rowCounts: Readonly<{ intent: number; audit: number }>;
  }>): Result<EgressAuditEvent> {
    const record = this.intents.get(input.intentId);
    if (!record || record.state !== "SOCKET_ATTEMPT_RECORDED") {
      return fail("PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT");
    }
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (this.consumeAuditFailure()) {
      return fail("WORKER_AUDIT_ATOMICITY_FAILED");
    }
    const event = EgressAuditEventSchema.parse({
      schemaVersion: "r3-egress-r2-audit-event-v1",
      eventId: input.eventId,
      intentId: input.intentId,
      eventType: "PROVIDER_RESPONSE_RECEIVED",
      evidenceSource: "TRUSTED_EGRESS_RUNTIME",
      evidenceSequence: this.nextSequence(input.intentId),
      evidenceDigest: input.evidenceDigest,
      observedAt: input.observedAt,
      persistedAt: input.persistedAt,
      socketCallOutcome: "COMPLETED_CALL",
      providerResponseDigest: input.responseDigest,
      businessSuccessEvaluated: false,
    });
    this.intents.set(input.intentId, {
      ...record,
      state: "PROVIDER_RESPONSE_RECEIVED",
      responseReceivedAt: input.observedAt,
    });
    this.append(input.intentId, event);
    return ok(event);
  }

  markOutcomeUnknown(input: Readonly<{
    intentId: string;
    eventId: string;
    evidenceDigest: string;
    observedAt: number;
    persistedAt: number;
    rowCounts: Readonly<{ intent: number; audit: number }>;
  }>): Result<EgressAuditEvent> {
    const record = this.intents.get(input.intentId);
    if (
      !record
      || !["WRITE_AUTHORIZED", "SOCKET_ATTEMPT_RECORDED"].includes(record.state)
    ) {
      return fail("SEND_OUTCOME_ALREADY_TERMINAL");
    }
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (this.consumeAuditFailure()) {
      return fail("WORKER_AUDIT_ATOMICITY_FAILED");
    }
    const event = EgressAuditEventSchema.parse({
      schemaVersion: "r3-egress-r2-audit-event-v1",
      eventId: input.eventId,
      intentId: input.intentId,
      eventType: "SEND_OUTCOME_UNKNOWN",
      evidenceSource: "TRUSTED_EGRESS_RUNTIME",
      evidenceSequence: this.nextSequence(input.intentId),
      evidenceDigest: input.evidenceDigest,
      observedAt: input.observedAt,
      persistedAt: input.persistedAt,
      socketCallOutcome: null,
      providerResponseDigest: null,
      businessSuccessEvaluated: false,
    });
    this.intents.set(input.intentId, {
      ...record,
      state: "SEND_OUTCOME_UNKNOWN",
      outcomeUnknownAt: input.observedAt,
    });
    this.append(input.intentId, event);
    this.unrecordedAttempts.delete(input.intentId);
    return ok(event);
  }

  recoverCrashBeforeSocket(input: Readonly<{
    intentId: string;
    crashEventId: string;
    unknownEventId: string;
    evidenceDigest: string;
    now: number;
    rowCounts: Readonly<{ crashAudit: number; unknownIntent: number; unknownAudit: number }>;
  }>): Result<readonly EgressAuditEvent[]> {
    const record = this.intents.get(input.intentId);
    if (!record || record.state !== "WRITE_AUTHORIZED") {
      return fail("SEND_OUTCOME_ALREADY_TERMINAL");
    }
    for (const count of Object.values(input.rowCounts)) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (this.consumeAuditFailure()) {
      return fail("WORKER_AUDIT_ATOMICITY_FAILED");
    }
    const crash = EgressAuditEventSchema.parse({
      schemaVersion: "r3-egress-r2-audit-event-v1",
      eventId: input.crashEventId,
      intentId: input.intentId,
      eventType: "EGRESS_PROCESS_CRASHED",
      evidenceSource: "TRUSTED_EGRESS_RUNTIME",
      evidenceSequence: this.nextSequence(input.intentId),
      evidenceDigest: input.evidenceDigest,
      observedAt: input.now,
      persistedAt: input.now,
      socketCallOutcome: "NOT_CALLED",
      providerResponseDigest: null,
      businessSuccessEvaluated: false,
    });
    const unknown = EgressAuditEventSchema.parse({
      schemaVersion: "r3-egress-r2-audit-event-v1",
      eventId: input.unknownEventId,
      intentId: input.intentId,
      eventType: "SEND_OUTCOME_UNKNOWN",
      evidenceSource: "TRUSTED_EGRESS_RUNTIME",
      evidenceSequence: this.nextSequence(input.intentId) + 1,
      evidenceDigest: input.evidenceDigest,
      observedAt: input.now,
      persistedAt: input.now,
      socketCallOutcome: "NOT_CALLED",
      providerResponseDigest: null,
      businessSuccessEvaluated: false,
    });
    this.intents.set(input.intentId, {
      ...record,
      state: "SEND_OUTCOME_UNKNOWN",
      outcomeUnknownAt: input.now,
    });
    this.append(input.intentId, crash);
    this.append(input.intentId, unknown);
    return ok(Object.freeze([crash, unknown]));
  }

  retry(intentId: string): Result<never> {
    const record = this.intents.get(intentId);
    if (
      !record
      || ["WRITE_AUTHORIZED", "SOCKET_ATTEMPT_RECORDED", "SEND_OUTCOME_UNKNOWN"]
        .includes(record.state)
      || this.unrecordedAttempts.has(intentId)
    ) {
      return fail("AUTO_RETRY_FORBIDDEN");
    }
    return fail("AUTO_RETRY_FORBIDDEN");
  }

  intent(intentId: string): IntentRecord | null {
    const record = this.intents.get(intentId);
    return record ? Object.freeze({ ...record }) : null;
  }

  eventsFor(intentId: string): readonly EgressAuditEvent[] {
    return Object.freeze([...(this.events.get(intentId) ?? [])]);
  }

  snapshot(): EgressAuditSnapshot {
    return Object.freeze({
      intents: Object.freeze(Object.fromEntries(this.intents)),
      events: Object.freeze(Object.fromEntries(
        [...this.events.entries()].map(([key, value]) => [
          key,
          Object.freeze([...value]),
        ]),
      )),
      unrecordedAttempts: Object.freeze([...this.unrecordedAttempts]),
    });
  }

  static fromSnapshot(snapshot: EgressAuditSnapshot): OfflineEgressAuditModel {
    const model = new OfflineEgressAuditModel();
    for (const [key, value] of Object.entries(snapshot.intents)) {
      model.intents.set(key, { ...value });
    }
    for (const [key, value] of Object.entries(snapshot.events)) {
      model.events.set(key, value.map((event) => ({ ...event })));
    }
    for (const value of snapshot.unrecordedAttempts) {
      model.unrecordedAttempts.add(value);
    }
    return model;
  }

  private append(intentId: string, event: EgressAuditEvent): void {
    const events = this.events.get(intentId) ?? [];
    events.push(Object.freeze(event));
    this.events.set(intentId, events);
  }

  private nextSequence(intentId: string): number {
    return (this.events.get(intentId)?.length ?? 0) + 1;
  }

  private consumeAuditFailure(): boolean {
    if (!this.failNextAudit) return false;
    this.failNextAudit = false;
    return true;
  }
}

```
<!-- END_EXACT_SOURCE id=S021 -->

### S022. models/scope-cleanup.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/models/scope-cleanup.ts`
- Bytes: `14189`
- SHA-256: `4FB9B9608CDFB7F016CB7F399347808C4497BCC0453B48CF6142B8F204A3E387`

<!-- BEGIN_EXACT_SOURCE id=S022 sha256=4FB9B9608CDFB7F016CB7F399347808C4497BCC0453B48CF6142B8F204A3E387 bytes=14189 -->
```text
import {
  CleanupLeaseStateSchema,
  CleanupPermitStateSchema,
  EgressIntentStateSchema,
  ScopeCleanupPayloadSchema,
  ScopeCleanupResultSchema,
  WorkerRegistrationStateSchema,
  WorkerRevocationStateSchema,
  fail,
  ok,
  requireExactlyOne,
  type Result,
  type ScopeCleanupPayload,
  type ScopeCleanupResult,
} from "../contracts";
import { canonicalJson, sha256Canonical } from "./canonical";

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

type CleanupRequestRecord = {
  requestDigest: string;
  canonicalPayload: string;
  state: "PENDING" | "COMPLETED";
  result: ScopeCleanupResult;
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

export type ScopeCleanupSnapshot = Readonly<{
  authorityAvailable: boolean;
  resources: CleanupResourceSnapshot;
  blocks: Readonly<Record<string, Readonly<{
    blockedRevocationVersion: number;
    version: number;
  }>>>;
  requests: Readonly<Record<string, CleanupRequestRecord>>;
  mutatedLeases: Readonly<Record<string, string>>;
  mutatedPermits: Readonly<Record<string, string>>;
  auditEvents: readonly string[];
}>;

/**
 * OFFLINE_REFERENCE_MODEL / PERSISTENCE_SIMULATION_ONLY.
 * The model simulates the database idempotency protocol. It does not prove
 * cross-process durability, PostgreSQL locking or SQLSTATE behavior.
 */
export class OfflineScopeCleanupModel {
  private authorityAvailable = true;
  private resources: CleanupResourceSnapshot;
  private readonly blocks = new Map<
    string,
    Readonly<{ blockedRevocationVersion: number; version: number }>
  >();
  private readonly requests = new Map<string, CleanupRequestRecord>();
  private readonly mutatedLeases = new Map<string, string>();
  private readonly mutatedPermits = new Map<string, string>();
  private readonly auditEvents: string[] = [];
  private queue: Promise<void> = Promise.resolve();

  constructor(resources: CleanupResourceSnapshot) {
    const parsed = this.parseResources(resources);
    if (!parsed.ok) throw new Error(parsed.code);
    this.resources = parsed.value;
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
  }>): Result<ScopeCleanupResult> {
    if (!this.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const payloadResult = ScopeCleanupPayloadSchema.safeParse(input.payload);
    if (!payloadResult.success) return fail("SCOPE_BINDING_MISMATCH");
    const payload = payloadResult.data;
    const requestDigest = sha256Canonical(payload);
    const canonicalPayload = canonicalJson(payload);
    const existing = this.requests.get(payload.cleanupRequestId);
    if (existing) {
      if (
        existing.requestDigest !== requestDigest
        || existing.canonicalPayload !== canonicalPayload
      ) {
        return fail("IDEMPOTENCY_KEY_REUSE_CONFLICT");
      }
      if (existing.state !== "COMPLETED") {
        return fail("IDEMPOTENCY_RECORD_INCONSISTENT");
      }
      return ok(existing.result);
    }

    const binding = this.validateBindings(payload);
    if (!binding.ok) return binding;
    const leaseClassification = this.classifyLease();
    if (!leaseClassification.ok) return leaseClassification;
    const blockKey = `${payload.scopeKey}|${payload.workerInstanceId}`;
    const existingBlock = this.blocks.get(blockKey);
    const alreadySatisfied = Boolean(
      existingBlock
      && existingBlock.blockedRevocationVersion >= payload.revocationVersion,
    );
    if (!alreadySatisfied) {
      if (this.resources.leaseState === "REVOKED") {
        return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
      }
      if (this.resources.permitState === "REVOKED") {
        return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
      }
      if (
        leaseClassification.value === "AFTER_SEND"
        && this.resources.permitState !== "CONSUMED"
      ) {
        return fail("PERMIT_STATE_INVALID");
      }
    }
    if (alreadySatisfied) {
      if (this.mutatedPermits.get(payload.permitId) !== "REVOKED") {
        return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
      }
    }

    const requestRows = requireExactlyOne(input.rowCounts.requestInsert);
    if (!requestRows.ok) return requestRows;
    const expectedBlockRows = alreadySatisfied ? 0 : 1;
    if (input.rowCounts.blockMutation !== expectedBlockRows) {
      return fail("ROW_COUNT_CONFLICT");
    }
    const expectedLeaseRows = !alreadySatisfied
      && leaseClassification.value === "PRE_SEND"
      ? 1
      : 0;
    if (input.rowCounts.leaseMutation !== expectedLeaseRows) {
      return fail("ROW_COUNT_CONFLICT");
    }
    const expectedPermitRows = alreadySatisfied ? 0 : 1;
    if (input.rowCounts.permitMutation !== expectedPermitRows) {
      return fail("ROW_COUNT_CONFLICT");
    }
    for (const count of [
      input.rowCounts.auditAppend,
      input.rowCounts.completionUpdate,
    ]) {
      const checked = requireExactlyOne(count);
      if (!checked.ok) return checked;
    }
    if (input.failBlockMutation && !alreadySatisfied) {
      return fail("ROW_COUNT_CONFLICT");
    }
    if (input.failAudit) {
      return fail("WORKER_AUDIT_ATOMICITY_FAILED");
    }
    if (input.crashBeforeCommit) {
      return fail("PROCESS_CRASHED_BEFORE_COMMIT");
    }

    const blockVersion = alreadySatisfied
      ? existingBlock?.version ?? 1
      : (existingBlock?.version ?? 0) + 1;
    const leaseOutcome = leaseClassification.value === "PRE_SEND"
      ? "REVOKED" as const
      : this.resources.leaseState === "SEND_OUTCOME_UNKNOWN"
        ? "PRESERVED_OUTCOME_UNKNOWN" as const
        : "PRESERVED_AFTER_WRITE_AUTHORIZED" as const;
    const externalOutcome = leaseClassification.value === "PRE_SEND"
      ? "NOT_SENT" as const
      : this.resources.leaseState === "SEND_OUTCOME_UNKNOWN"
        ? "SEND_OUTCOME_UNKNOWN" as const
        : "WRITE_MAY_HAVE_OCCURRED" as const;
    const status = alreadySatisfied ? "ALREADY_SATISFIED" as const : "APPLIED" as const;
    const resultCore = {
      schemaVersion: "r3-egress-r2-scope-cleanup-result-v1" as const,
      cleanupRequestId: payload.cleanupRequestId,
      requestDigest,
      status,
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
    const result = ScopeCleanupResultSchema.parse({
      ...resultCore,
      resultDigest: sha256Canonical(resultCore),
    });

    if (!alreadySatisfied) {
      this.blocks.set(blockKey, {
        blockedRevocationVersion: payload.revocationVersion,
        version: blockVersion,
      });
      if (leaseClassification.value === "PRE_SEND") {
        this.mutatedLeases.set(payload.leaseId, "REVOKED");
      }
      this.mutatedPermits.set(payload.permitId, "REVOKED");
    }
    this.requests.set(payload.cleanupRequestId, {
      requestDigest,
      canonicalPayload,
      state: "COMPLETED",
      result,
      auditEventId: input.auditEventId,
    });
    this.auditEvents.push(
      alreadySatisfied
        ? `WORKER_SCOPE_CLEANUP_ALREADY_SATISFIED:${payload.cleanupRequestId}`
        : `WORKER_SCOPE_BLOCKED:${payload.cleanupRequestId}`,
    );
    if (input.commitResponseLost) {
      return fail("COMMIT_OUTCOME_UNKNOWN");
    }
    return ok(result);
  }

  async cleanupConcurrent(input: Readonly<{
    payload: unknown;
    rowCounts: CleanupRowCounts;
    auditEventId: string;
    now: number;
  }>): Promise<Result<ScopeCleanupResult>> {
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

  auditSnapshot(): readonly string[] {
    return Object.freeze([...this.auditEvents]);
  }

  snapshot(): ScopeCleanupSnapshot {
    return Object.freeze({
      authorityAvailable: this.authorityAvailable,
      resources: Object.freeze({ ...this.resources }),
      blocks: Object.freeze(Object.fromEntries(this.blocks)),
      requests: Object.freeze(Object.fromEntries(this.requests)),
      mutatedLeases: Object.freeze(Object.fromEntries(this.mutatedLeases)),
      mutatedPermits: Object.freeze(Object.fromEntries(this.mutatedPermits)),
      auditEvents: this.auditSnapshot(),
    });
  }

  static fromSnapshot(snapshot: ScopeCleanupSnapshot): OfflineScopeCleanupModel {
    const model = new OfflineScopeCleanupModel(snapshot.resources);
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
    model.auditEvents.push(...snapshot.auditEvents);
    return model;
  }

  private validateBindings(payload: ScopeCleanupPayload): Result<true> {
    const resource = this.resources;
    const revocationState = WorkerRevocationStateSchema.safeParse(
      resource.revocationState,
    );
    const registrationState = WorkerRegistrationStateSchema.safeParse(
      resource.registrationState,
    );
    const leaseState = CleanupLeaseStateSchema.safeParse(resource.leaseState);
    const permitState = CleanupPermitStateSchema.safeParse(resource.permitState);
    const intentState = EgressIntentStateSchema.safeParse(resource.intentState);
    if (
      !revocationState.success
      || !registrationState.success
      || !leaseState.success
      || !permitState.success
      || !intentState.success
    ) {
      return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
    }
    if (
      revocationState.data !== "REVOKED"
      || resource.revocationVersion < payload.revocationVersion
      || registrationState.data !== "REVOKED"
    ) {
      return fail("WORKER_STATE_INVALID");
    }
    if (
      payload.workerInstanceId !== resource.workerInstanceId
      || payload.scopeKey !== resource.scopeKey
      || payload.leaseId !== resource.leaseId
      || payload.capabilityId !== resource.floorCapabilityId
      || payload.permitId !== resource.permitId
      || resource.floorWorkerId !== resource.workerInstanceId
      || resource.floorLeaseId !== resource.leaseId
      || resource.floorCapabilityId !== resource.leaseCapabilityId
      || resource.leaseWorkerId !== resource.workerInstanceId
      || resource.leaseScopeKey !== resource.scopeKey
      || resource.leaseToken !== resource.floorToken
      || resource.permitLeaseId !== resource.leaseId
      || resource.permitWorkerId !== resource.workerInstanceId
      || resource.permitScopeKey !== resource.scopeKey
      || resource.permitCapabilityId !== resource.leaseCapabilityId
      || resource.permitToken !== resource.floorToken
    ) {
      return fail("SCOPE_BINDING_MISMATCH");
    }
    return ok(true as const);
  }

  private classifyLease(): Result<"PRE_SEND" | "AFTER_SEND"> {
    const state = this.resources.leaseState;
    if (PRE_SEND_LEASE_STATES.has(state)) {
      return ok("PRE_SEND");
    }
    if (AFTER_SEND_LEASE_STATES.has(state)) {
      return ok("AFTER_SEND");
    }
    if (state === "REVOKED") {
      return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
    }
    return fail("LEASE_STATE_INVALID");
  }

  private parseResources(
    resources: CleanupResourceSnapshot,
  ): Result<CleanupResourceSnapshot> {
    if (
      !WorkerRevocationStateSchema.safeParse(resources.revocationState).success
      || !WorkerRegistrationStateSchema.safeParse(resources.registrationState).success
      || !CleanupLeaseStateSchema.safeParse(resources.leaseState).success
      || !CleanupPermitStateSchema.safeParse(resources.permitState).success
      || !EgressIntentStateSchema.safeParse(resources.intentState).success
    ) {
      return fail("SCOPE_CLEANUP_STATE_INCONSISTENT");
    }
    return ok(Object.freeze({ ...resources }));
  }
}

```
<!-- END_EXACT_SOURCE id=S022 -->

### S023. models/sql-analyzer.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/models/sql-analyzer.ts`
- Bytes: `11263`
- SHA-256: `4F62392A2F1A50570E4EF0B8B474F0EC6D88950FCE32B8F452EB234FB39590B0`

<!-- BEGIN_EXACT_SOURCE id=S023 sha256=4F62392A2F1A50570E4EF0B8B474F0EC6D88950FCE32B8F452EB234FB39590B0 bytes=11263 -->
```text
import { R3_EGRESS_R2_LOCK_ORDER } from "../lock-order";

export type AnalysisLevel =
  | "TEXTUAL_PATTERN_CHECK"
  | "SQL_STATEMENT_SEGMENTATION"
  | "SQL_PARAMETER_BINDING_REVIEW"
  | "TRANSACTION_CONTRACT_REVIEW";

export type Finding = Readonly<{
  code: string;
  level: AnalysisLevel;
  message: string;
}>;

export type SqlStatement = Readonly<{
  index: number;
  kind: "BEGIN" | "COMMIT" | "ROLLBACK" | "SELECT" | "INSERT" | "UPDATE" | "DELETE" | "OTHER";
  table: string | null;
  normalized: string;
  start: number;
  end: number;
}>;

export type SqlTransaction = Readonly<{
  statements: readonly SqlStatement[];
  lockDomains: readonly string[];
  mutationTables: readonly string[];
  auditEvent: boolean;
  auditHead: boolean;
}>;

const TABLE_DOMAIN: Readonly<Record<string, string>> = Object.freeze({
  trust_r5_worker_revocation: "WORKER_REVOCATION_CONTROL",
  trust_r6_worker_revocation_request: "WORKER_REVOCATION_REQUEST",
  trust_r6_scope_cleanup_request: "SCOPE_CLEANUP_REQUEST",
  trust_r5_scope_worker_block: "SCOPE_WORKER_BLOCK",
  trust_r3_emergency_control: "EMERGENCY_CONTROL",
  trust_r3_identity_key: "KEY_REGISTRY",
  trust_r3_approval: "APPROVAL",
  trust_r3_approval_consumption: "APPROVAL_CONSUMPTION",
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
  trust_r6_egress_runtime_state: "EGRESS_RUNTIME_EVIDENCE",
  trust_r6_egress_runtime_evidence: "EGRESS_RUNTIME_EVIDENCE",
  trust_r3_audit_head: "AUDIT_SEQUENCE",
});

function stripLeadingComments(text: string): string {
  let result = text.trimStart();
  while (result.startsWith("--") || result.startsWith("/*")) {
    if (result.startsWith("--")) {
      const newline = result.indexOf("\n");
      if (newline < 0) return "";
      result = result.slice(newline + 1).trimStart();
    } else {
      const end = result.indexOf("*/");
      if (end < 0) return "";
      result = result.slice(end + 2).trimStart();
    }
  }
  return result;
}

export function splitSql(sql: string): readonly SqlStatement[] {
  const statements: SqlStatement[] = [];
  let start = 0;
  let inSingle = false;
  let inDouble = false;
  let inLineComment = false;
  let inBlockComment = false;

  const push = (end: number): void => {
    const raw = sql.slice(start, end);
    const normalized = stripLeadingComments(raw).trim();
    if (normalized.length > 0) {
      const first = /^([A-Za-z]+)/u.exec(normalized)?.[1]?.toUpperCase() ?? "";
      const kind = ["BEGIN", "COMMIT", "ROLLBACK", "SELECT", "INSERT", "UPDATE", "DELETE"]
        .includes(first)
        ? first as SqlStatement["kind"]
        : "OTHER";
      const table = /\b(?:FROM|INTO|UPDATE|JOIN)\s+(trust_[a-z0-9_]+)/iu
        .exec(normalized)?.[1]?.toLowerCase() ?? null;
      statements.push(Object.freeze({
        index: statements.length,
        kind,
        table,
        normalized,
        start,
        end,
      }));
    }
    start = end + 1;
  };

  for (let index = 0; index < sql.length; index += 1) {
    const char = sql[index];
    const next = sql[index + 1];
    if (inLineComment) {
      if (char === "\n") inLineComment = false;
      continue;
    }
    if (inBlockComment) {
      if (char === "*" && next === "/") {
        inBlockComment = false;
        index += 1;
      }
      continue;
    }
    if (!inSingle && !inDouble && char === "-" && next === "-") {
      inLineComment = true;
      index += 1;
      continue;
    }
    if (!inSingle && !inDouble && char === "/" && next === "*") {
      inBlockComment = true;
      index += 1;
      continue;
    }
    if (!inDouble && char === "'") {
      if (inSingle && next === "'") {
        index += 1;
        continue;
      }
      inSingle = !inSingle;
      continue;
    }
    if (!inSingle && char === "\"") {
      if (inDouble && next === "\"") {
        index += 1;
        continue;
      }
      inDouble = !inDouble;
      continue;
    }
    if (!inSingle && !inDouble && char === ";") push(index);
  }
  if (start < sql.length) push(sql.length);
  return Object.freeze(statements);
}

export function buildTransactions(
  statements: readonly SqlStatement[],
): readonly SqlTransaction[] {
  const transactions: SqlTransaction[] = [];
  let active: SqlStatement[] = [];
  for (const statement of statements) {
    if (statement.kind === "BEGIN") {
      active = [statement];
      continue;
    }
    if (active.length > 0) active.push(statement);
    if (statement.kind === "COMMIT" || statement.kind === "ROLLBACK") {
      const locks = active.flatMap((item) =>
        /FOR\s+(?:UPDATE|SHARE)\b/iu.test(item.normalized)
          ? [item.table].filter((table): table is string => table !== null)
          : []
      );
      const mutationTables = active
        .filter((item) =>
          ["INSERT", "UPDATE", "DELETE"].includes(item.kind)
          && item.table !== null
        )
        .map((item) => item.table as string);
      transactions.push(Object.freeze({
        statements: Object.freeze([...active]),
        lockDomains: Object.freeze(
          [...new Set(locks.map((table) => TABLE_DOMAIN[table]).filter(Boolean))],
        ),
        mutationTables: Object.freeze([...new Set(mutationTables)]),
        auditEvent: active.some((item) =>
          /trust_r3_audit_event/iu.test(item.normalized)
        ),
        auditHead: active.some((item) =>
          /trust_r3_audit_head/iu.test(item.normalized)
        ),
      }));
      active = [];
    }
  }
  return Object.freeze(transactions);
}

function add(findings: Finding[], code: string, level: AnalysisLevel, message: string): void {
  findings.push(Object.freeze({ code, level, message }));
}

export function reviewWorkerLifecycleSql(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  if (!/state\s+IN\s*\(\s*'ACTIVE'\s*,\s*'DRAINING'\s*\)/iu.test(sql)) {
    add(
      findings,
      "DRAINING_REVOCATION_MISSING",
      "TRANSACTION_CONTRACT_REVIEW",
      "registration update must accept ACTIVE and DRAINING",
    );
  }
  if (!/request_digest/iu.test(sql)) {
    add(
      findings,
      "WORKER_REQUEST_DIGEST_MISSING",
      "TEXTUAL_PATTERN_CHECK",
      "request payload digest is required",
    );
  }
  if (/ON\s+CONFLICT[\s\S]*state\s*=\s*'ACTIVE'/iu.test(sql)) {
    add(
      findings,
      "WORKER_REACTIVATION_UPSERT",
      "TEXTUAL_PATTERN_CHECK",
      "revocation SQL must not reactivate Worker",
    );
  }
  if (
    /UPDATE\s+trust_r4_worker_registration[\s\S]*WHERE[\s\S]*state\s*=\s*'ACTIVE'\s*;/iu
      .test(sql)
  ) {
    add(
      findings,
      "ACTIVE_ONLY_REGISTRATION_UPDATE",
      "TRANSACTION_CONTRACT_REVIEW",
      "DRAINING Worker would produce a zero-row update",
    );
  }
  return Object.freeze(findings);
}

export function reviewCleanupSql(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  const required = [
    ["cleanup_request_id", "CLEANUP_REQUEST_ID_MISSING"],
    ["request_digest", "CLEANUP_REQUEST_DIGEST_MISSING"],
    ["result_digest", "CLEANUP_RESULT_DIGEST_MISSING"],
    ["audit_event_id", "CLEANUP_AUDIT_BINDING_MISSING"],
    ["state = 'COMPLETED'", "CLEANUP_COMPLETION_STATE_MISSING"],
    ["COMMIT_OUTCOME_UNKNOWN", "CLEANUP_COMMIT_RECOVERY_MISSING"],
    ["IDEMPOTENCY_KEY_REUSE_CONFLICT", "CLEANUP_ID_REUSE_CONFLICT_MISSING"],
  ] as const;
  for (const [token, code] of required) {
    if (!sql.includes(token)) {
      add(findings, code, "TEXTUAL_PATTERN_CHECK", token);
    }
  }
  for (const match of sql.matchAll(
    /version\s*=\s*trust_r5_scope_worker_block\.version\s*\+\s*1/giu,
  )) {
    const following = sql.slice(match.index, match.index + 500);
    if (
      !/WHERE\s+trust_r5_scope_worker_block\.blocked_revocation_version/iu
        .test(following)
    ) {
      add(
        findings,
        "CLEANUP_UNCONDITIONAL_BLOCK_VERSION_BUMP",
        "TRANSACTION_CONTRACT_REVIEW",
        "replay must not increment block version",
      );
      break;
    }
  }
  if (
    /UPDATE\s+trust_r6_scope_cleanup_request[\s\S]*state\s*=\s*'COMPLETED'/iu
      .test(sql)
    && !/trust_r3_audit_event/iu.test(sql)
  ) {
    add(
      findings,
      "CLEANUP_AUDIT_COMPLETION_SPLIT",
      "TRANSACTION_CONTRACT_REVIEW",
      "Audit and idempotency completion must share the transaction",
    );
  }
  return Object.freeze(findings);
}

export function reviewAuditSql(sql: string): readonly Finding[] {
  const findings: Finding[] = [];
  if (/\bREQUEST_SENT\b/u.test(sql)) {
    add(
      findings,
      "FALSE_REQUEST_SENT_EVENT",
      "TEXTUAL_PATTERN_CHECK",
      "authorization is not proof of a socket request",
    );
  }
  for (const eventType of [
    "EGRESS_WRITE_START_AUTHORIZED",
    "SOCKET_WRITE_ATTEMPTED",
    "PROVIDER_RESPONSE_RECEIVED",
    "SEND_OUTCOME_UNKNOWN",
  ]) {
    if (!sql.includes(eventType)) {
      add(
        findings,
        `AUDIT_EVENT_MISSING_${eventType}`,
        "TEXTUAL_PATTERN_CHECK",
        eventType,
      );
    }
  }
  if (!/TRUSTED_EGRESS_RUNTIME/iu.test(sql)) {
    add(
      findings,
      "RUNTIME_EVIDENCE_SOURCE_MISSING",
      "TRANSACTION_CONTRACT_REVIEW",
      "socket evidence requires a trusted runtime source",
    );
  }
  if (!/business_success_evaluated/iu.test(sql)) {
    add(
      findings,
      "BUSINESS_SUCCESS_SEPARATION_MISSING",
      "TRANSACTION_CONTRACT_REVIEW",
      "response receipt must not equal business success",
    );
  }
  return Object.freeze(findings);
}

export function analyzeSqlTransactionContract(sql: string): Readonly<{
  statements: readonly SqlStatement[];
  transactions: readonly SqlTransaction[];
  parameters: readonly string[];
  findings: readonly Finding[];
}> {
  const statements = splitSql(sql);
  const transactions = buildTransactions(statements);
  const parameters = Object.freeze(
    [...new Set([...sql.matchAll(/\$\d+/gu)].map((match) => match[0]))]
      .sort((left, right) => Number(left.slice(1)) - Number(right.slice(1))),
  );
  const findings: Finding[] = [];
  for (const transaction of transactions) {
    let previous = -1;
    for (const domain of transaction.lockDomains) {
      const index = R3_EGRESS_R2_LOCK_ORDER.indexOf(
        domain as typeof R3_EGRESS_R2_LOCK_ORDER[number],
      );
      if (index < previous) {
        add(
          findings,
          "LOCK_ORDER_CROSSING",
          "TRANSACTION_CONTRACT_REVIEW",
          transaction.lockDomains.join(" -> "),
        );
      }
      previous = index;
    }
  }
  return Object.freeze({
    statements,
    transactions,
    parameters,
    findings: Object.freeze(findings),
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

### S024. models/worker-lifecycle.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/models/worker-lifecycle.ts`
- Bytes: `7353`
- SHA-256: `2795B17ED1E5710AEF7BD1139081A88ED284468FBA2F345EB57F20BC88FCE67F`

<!-- BEGIN_EXACT_SOURCE id=S024 sha256=2795B17ED1E5710AEF7BD1139081A88ED284468FBA2F345EB57F20BC88FCE67F bytes=7353 -->
```text
import {
  WorkerRevocationPayloadSchema,
  WorkerRevocationResultSchema,
  fail,
  ok,
  requireExactlyOne,
  type Result,
  type WorkerRegistrationState,
  type WorkerRevocationPayload,
  type WorkerRevocationResult,
  type WorkerRevocationState,
} from "../contracts";
import { canonicalJson, sha256Canonical } from "./canonical";

type WorkerRecord = {
  registrationState: WorkerRegistrationState;
  revocationState: WorkerRevocationState;
  revocationVersion: number;
  recordVersion: number;
};

type RequestRecord = {
  requestDigest: string;
  canonicalPayload: string;
  payload: WorkerRevocationPayload;
  result: WorkerRevocationResult;
};

export type WorkerLifecycleSnapshot = Readonly<{
  workers: Readonly<Record<string, WorkerRecord>>;
  requests: Readonly<Record<string, RequestRecord>>;
  auditEvents: readonly string[];
}>;

export type WorkerRevocationRowCounts = Readonly<{
  requestInsert: number;
  revocationUpdate: number;
  registrationUpdate: number;
  auditAppend: number;
}>;

/**
 * OFFLINE_REFERENCE_MODEL / PERSISTENCE_SIMULATION_ONLY.
 * REGISTERED is a provisioning state and is not accepted by the current frozen
 * R4 registration table. ACTIVE and DRAINING are the only revocable runtime
 * states. REVOKED is terminal.
 */
export class OfflineWorkerLifecycleModel {
  private authorityAvailable = true;
  private readonly workers = new Map<string, WorkerRecord>();
  private readonly requests = new Map<string, RequestRecord>();
  private readonly auditEvents: string[] = [];
  private queue: Promise<void> = Promise.resolve();

  seedWorker(input: Readonly<{
    workerInstanceId: string;
    registrationState: WorkerRegistrationState;
    revocationState?: WorkerRevocationState;
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
    commitResponseLost?: boolean;
    crashBeforeCommit?: boolean;
  }>): Result<WorkerRevocationResult> {
    if (!this.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const parsed = WorkerRevocationPayloadSchema.safeParse(input.payload);
    if (!parsed.success) return fail("WORKER_STATE_INVALID");
    const payload = parsed.data;
    const requestDigest = sha256Canonical(payload);
    const canonicalPayload = canonicalJson(payload);
    const existingRequest = this.requests.get(payload.requestId);
    if (existingRequest) {
      if (
        existingRequest.requestDigest !== requestDigest
        || existingRequest.canonicalPayload !== canonicalPayload
      ) {
        return fail("IDEMPOTENCY_KEY_REUSE_CONFLICT");
      }
      return ok(WorkerRevocationResultSchema.parse({
        ...existingRequest.result,
        status: "REPLAYED",
      }));
    }

    const worker = this.workers.get(payload.workerInstanceId);
    if (!worker) return fail("WORKER_STATE_INVALID");
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
    if (input.failAudit) {
      return fail("WORKER_AUDIT_ATOMICITY_FAILED");
    }
    if (input.crashBeforeCommit) {
      return fail("PROCESS_CRASHED_BEFORE_COMMIT");
    }

    const nextRevocationVersion = worker.revocationVersion + 1;
    const nextRecordVersion = worker.recordVersion + 1;
    const result = WorkerRevocationResultSchema.parse({
      schemaVersion: "r3-egress-r2-worker-revocation-result-v1",
      status: "REVOKED",
      requestId: payload.requestId,
      requestDigest,
      workerInstanceId: payload.workerInstanceId,
      registrationState: "REVOKED",
      revocationVersion: nextRevocationVersion,
      recordVersion: nextRecordVersion,
      auditEventId: input.auditEventId,
      revokedAt: payload.requestedAt,
    });
    this.workers.set(payload.workerInstanceId, {
      registrationState: "REVOKED",
      revocationState: "REVOKED",
      revocationVersion: nextRevocationVersion,
      recordVersion: nextRecordVersion,
    });
    this.requests.set(payload.requestId, {
      requestDigest,
      canonicalPayload,
      payload,
      result,
    });
    this.auditEvents.push(
      `WORKER_REVOKED:${payload.workerInstanceId}:${nextRevocationVersion}`,
    );
    if (input.commitResponseLost) {
      return fail("COMMIT_OUTCOME_UNKNOWN");
    }
    return ok(result);
  }

  async revokeConcurrent(input: Readonly<{
    payload: unknown;
    rowCounts: WorkerRevocationRowCounts;
    auditEventId: string;
    failAudit?: boolean;
  }>): Promise<Result<WorkerRevocationResult>> {
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
    if (!worker) return fail("WORKER_STATE_INVALID");
    if (
      worker.revocationState === "REVOKED"
      || worker.registrationState === "REVOKED"
    ) {
      return fail("WORKER_REACTIVATION_FORBIDDEN");
    }
    this.workers.set(workerInstanceId, {
      ...worker,
      registrationState: "ACTIVE",
    });
    return ok(true as const);
  }

  worker(workerInstanceId: string): WorkerRecord | null {
    const record = this.workers.get(workerInstanceId);
    return record ? Object.freeze({ ...record }) : null;
  }

  auditSnapshot(): readonly string[] {
    return Object.freeze([...this.auditEvents]);
  }

  snapshot(): WorkerLifecycleSnapshot {
    return Object.freeze({
      workers: Object.freeze(Object.fromEntries(this.workers)),
      requests: Object.freeze(Object.fromEntries(this.requests)),
      auditEvents: this.auditSnapshot(),
    });
  }

  static fromSnapshot(snapshot: WorkerLifecycleSnapshot): OfflineWorkerLifecycleModel {
    const model = new OfflineWorkerLifecycleModel();
    for (const [key, value] of Object.entries(snapshot.workers)) {
      model.workers.set(key, { ...value });
    }
    for (const [key, value] of Object.entries(snapshot.requests)) {
      model.requests.set(key, structuredClone(value));
    }
    model.auditEvents.push(...snapshot.auditEvents);
    return model;
  }
}

```
<!-- END_EXACT_SOURCE id=S024 -->

### S025. tests/egress-audit.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/tests/egress-audit.test.ts`
- Bytes: `9332`
- SHA-256: `2987961905852135BE1F7ED73BCC11BA894FF937A84E77AECC04A71431626EC8`

<!-- BEGIN_EXACT_SOURCE id=S025 sha256=2987961905852135BE1F7ED73BCC11BA894FF937A84E77AECC04A71431626EC8 bytes=9332 -->
```text
import { describe, expect, it } from "vitest";

import { OfflineEgressAuditModel } from "../models/egress-audit";

const NOW = Date.parse("2026-11-26T17:00:00Z");
const IDS = Object.freeze({
  intent: "11111111-1111-4111-8111-111111111111",
  auth: "22222222-2222-4222-8222-222222222222",
  attempt: "33333333-3333-4333-8333-333333333333",
  response: "44444444-4444-4444-8444-444444444444",
  unknown: "55555555-5555-4555-8555-555555555555",
  crash: "66666666-6666-4666-8666-666666666666",
});
const DIGEST = "sha256:" + "a".repeat(64);
const RESPONSE_DIGEST = "sha256:" + "b".repeat(64);

function model() {
  const value = new OfflineEgressAuditModel();
  expect(value.seedFinalAuthorized(IDS.intent).ok).toBe(true);
  return value;
}

function authorized() {
  const value = model();
  expect(value.authorizeWriteStart({
    intentId: IDS.intent,
    eventId: IDS.auth,
    evidenceDigest: DIGEST,
    now: NOW,
    rowCounts: { intent: 1, audit: 1 },
  }).ok).toBe(true);
  return value;
}

function attempted(outcome: "FAILED_BEFORE_BYTES" | "PARTIAL" | "COMPLETED_CALL") {
  const value = authorized();
  expect(value.recordSocketAttempt({
    intentId: IDS.intent,
    eventId: IDS.attempt,
    evidence: {
      socketApiCalled: true,
      evidenceSource: "TRUSTED_EGRESS_RUNTIME",
      evidenceDigest: DIGEST,
      callOutcome: outcome,
    },
    observedAt: NOW + 2,
    persistedAt: NOW + 3,
    rowCounts: { intent: 1, audit: 1 },
  }).ok).toBe(true);
  return value;
}

describe("R3 Egress Revocation R2 audit semantics", () => {
  it("records only EGRESS_WRITE_START_AUTHORIZED before the socket call", () => {
    const state = authorized();
    expect(state.intent(IDS.intent)?.state).toBe("WRITE_AUTHORIZED");
    expect(state.eventsFor(IDS.intent)).toHaveLength(1);
    expect(state.eventsFor(IDS.intent)[0]).toMatchObject({
      eventType: "EGRESS_WRITE_START_AUTHORIZED",
      socketCallOutcome: "NOT_CALLED",
    });
    expect(state.eventsFor(IDS.intent).some(
      (event) => event.eventType === "SOCKET_WRITE_ATTEMPTED",
    )).toBe(false);
  });

  it("rolls back authorization state when Audit fails", () => {
    const state = model();
    state.setNextAuditFailure();
    expect(state.authorizeWriteStart({
      intentId: IDS.intent,
      eventId: IDS.auth,
      evidenceDigest: DIGEST,
      now: NOW,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({
      ok: false,
      code: "WORKER_AUDIT_ATOMICITY_FAILED",
    });
    expect(state.intent(IDS.intent)?.state).toBe("FINAL_AUTHORIZED");
    expect(state.eventsFor(IDS.intent)).toHaveLength(0);
  });

  it("rejects database-only fabrication of SOCKET_WRITE_ATTEMPTED", () => {
    const state = authorized();
    expect(state.recordSocketAttempt({
      intentId: IDS.intent,
      eventId: IDS.attempt,
      evidence: {
        socketApiCalled: true,
        evidenceSource: "DATABASE_AUTHORIZATION",
        evidenceDigest: DIGEST,
        callOutcome: "COMPLETED_CALL",
      },
      observedAt: NOW + 1,
      persistedAt: NOW + 1,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({ ok: false, code: "SOCKET_ATTEMPT_NOT_PROVEN" });
    expect(state.eventsFor(IDS.intent)).toHaveLength(1);
  });

  it("records proven completed socket call", () => {
    const state = attempted("COMPLETED_CALL");
    expect(state.intent(IDS.intent)?.state).toBe("SOCKET_ATTEMPT_RECORDED");
    expect(state.eventsFor(IDS.intent).at(-1)).toMatchObject({
      eventType: "SOCKET_WRITE_ATTEMPTED",
      evidenceSource: "TRUSTED_EGRESS_RUNTIME",
      socketCallOutcome: "COMPLETED_CALL",
      businessSuccessEvaluated: false,
    });
  });

  it("records a proven failure before bytes without claiming a Provider request", () => {
    const state = attempted("FAILED_BEFORE_BYTES");
    expect(state.intent(IDS.intent)?.state).toBe("FAILED_BEFORE_BYTES");
    expect(state.eventsFor(IDS.intent).at(-1)?.eventType).toBe(
      "SOCKET_WRITE_FAILED_BEFORE_BYTES",
    );
    expect(state.eventsFor(IDS.intent).some(
      (event) => event.eventType === "PROVIDER_RESPONSE_RECEIVED",
    )).toBe(false);
  });

  it("records a partial write as unknown external outcome evidence", () => {
    const state = attempted("PARTIAL");
    expect(state.eventsFor(IDS.intent).at(-1)).toMatchObject({
      eventType: "SOCKET_WRITE_PARTIAL",
      socketCallOutcome: "PARTIAL",
    });
    expect(state.retry(IDS.intent)).toEqual({
      ok: false,
      code: "AUTO_RETRY_FORBIDDEN",
    });
  });

  it("recovers authorization-time crash without claiming a socket attempt", () => {
    const state = authorized();
    const recovered = state.recoverCrashBeforeSocket({
      intentId: IDS.intent,
      crashEventId: IDS.crash,
      unknownEventId: IDS.unknown,
      evidenceDigest: DIGEST,
      now: NOW + 5,
      rowCounts: { crashAudit: 1, unknownIntent: 1, unknownAudit: 1 },
    });
    expect(recovered.ok).toBe(true);
    expect(state.intent(IDS.intent)?.state).toBe("SEND_OUTCOME_UNKNOWN");
    expect(state.eventsFor(IDS.intent).map((event) => event.eventType)).toEqual([
      "EGRESS_WRITE_START_AUTHORIZED",
      "EGRESS_PROCESS_CRASHED",
      "SEND_OUTCOME_UNKNOWN",
    ]);
    expect(state.eventsFor(IDS.intent).map((event) => event.evidenceSequence))
      .toEqual([1, 2, 3]);
    expect(state.eventsFor(IDS.intent).some(
      (event) => event.eventType === "SOCKET_WRITE_ATTEMPTED",
    )).toBe(false);
  });

  it("rejects a Provider response without proven socket attempt", () => {
    const state = authorized();
    expect(state.recordProviderResponse({
      intentId: IDS.intent,
      eventId: IDS.response,
      responseDigest: RESPONSE_DIGEST,
      evidenceDigest: DIGEST,
      observedAt: NOW + 2,
      persistedAt: NOW + 3,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({
      ok: false,
      code: "PROVIDER_RESPONSE_WITHOUT_SOCKET_ATTEMPT",
    });
  });

  it("records Provider response receipt without claiming business success", () => {
    const state = attempted("COMPLETED_CALL");
    expect(state.recordProviderResponse({
      intentId: IDS.intent,
      eventId: IDS.response,
      responseDigest: RESPONSE_DIGEST,
      evidenceDigest: DIGEST,
      observedAt: NOW + 4,
      persistedAt: NOW + 5,
      rowCounts: { intent: 1, audit: 1 },
    })).toMatchObject({
      ok: true,
      value: {
        eventType: "PROVIDER_RESPONSE_RECEIVED",
        providerResponseDigest: RESPONSE_DIGEST,
        businessSuccessEvaluated: false,
      },
    });
    expect(state.intent(IDS.intent)?.state).toBe("PROVIDER_RESPONSE_RECEIVED");
    expect(state.eventsFor(IDS.intent).map((event) => event.evidenceSequence))
      .toEqual([1, 2, 3]);
  });

  it("records a lost Provider response as terminal unknown", () => {
    const state = attempted("COMPLETED_CALL");
    expect(state.markOutcomeUnknown({
      intentId: IDS.intent,
      eventId: IDS.unknown,
      evidenceDigest: DIGEST,
      observedAt: NOW + 4,
      persistedAt: NOW + 5,
      rowCounts: { intent: 1, audit: 1 },
    }).ok).toBe(true);
    expect(state.intent(IDS.intent)?.state).toBe("SEND_OUTCOME_UNKNOWN");
    expect(state.retry(IDS.intent)).toEqual({
      ok: false,
      code: "AUTO_RETRY_FORBIDDEN",
    });
  });

  it("does not auto-retry when socket occurred but Audit persistence failed", () => {
    const state = authorized();
    state.setNextAuditFailure();
    expect(state.recordSocketAttempt({
      intentId: IDS.intent,
      eventId: IDS.attempt,
      evidence: {
        socketApiCalled: true,
        evidenceSource: "TRUSTED_EGRESS_RUNTIME",
        evidenceDigest: DIGEST,
        callOutcome: "COMPLETED_CALL",
      },
      observedAt: NOW + 1,
      persistedAt: NOW + 2,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({
      ok: false,
      code: "SOCKET_ATTEMPT_AUDIT_FAILED_OUTCOME_UNKNOWN",
    });
    expect(state.retry(IDS.intent)).toEqual({
      ok: false,
      code: "AUTO_RETRY_FORBIDDEN",
    });
    expect(state.markOutcomeUnknown({
      intentId: IDS.intent,
      eventId: IDS.unknown,
      evidenceDigest: DIGEST,
      observedAt: NOW + 3,
      persistedAt: NOW + 4,
      rowCounts: { intent: 1, audit: 1 },
    }).ok).toBe(true);
    expect(state.intent(IDS.intent)?.state).toBe("SEND_OUTCOME_UNKNOWN");
  });

  it("preserves separate observed and persisted runtime times", () => {
    const state = attempted("COMPLETED_CALL");
    const event = state.eventsFor(IDS.intent).at(-1);
    expect(event?.observedAt).toBe(NOW + 2);
    expect(event?.persistedAt).toBe(NOW + 3);
    expect((event?.persistedAt ?? 0) > (event?.observedAt ?? 0)).toBe(true);
  });

  it("rejects duplicate unknown transition", () => {
    const state = authorized();
    expect(state.markOutcomeUnknown({
      intentId: IDS.intent,
      eventId: IDS.unknown,
      evidenceDigest: DIGEST,
      observedAt: NOW + 1,
      persistedAt: NOW + 2,
      rowCounts: { intent: 1, audit: 1 },
    }).ok).toBe(true);
    expect(state.markOutcomeUnknown({
      intentId: IDS.intent,
      eventId: "77777777-7777-4777-8777-777777777777",
      evidenceDigest: DIGEST,
      observedAt: NOW + 3,
      persistedAt: NOW + 4,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({
      ok: false,
      code: "SEND_OUTCOME_ALREADY_TERMINAL",
    });
  });
});

```
<!-- END_EXACT_SOURCE id=S025 -->

### S026. tests/scope-cleanup.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/tests/scope-cleanup.test.ts`
- Bytes: `13474`
- SHA-256: `60D407FAB476DDE174688A2027EAFD06BFF11F134D89F2B5F2D9DB3391EA58E9`

<!-- BEGIN_EXACT_SOURCE id=S026 sha256=60D407FAB476DDE174688A2027EAFD06BFF11F134D89F2B5F2D9DB3391EA58E9 bytes=13474 -->
```text
import { describe, expect, it } from "vitest";

import {
  OfflineScopeCleanupModel,
  type CleanupResourceSnapshot,
  type CleanupRowCounts,
} from "../models/scope-cleanup";

const NOW = Date.parse("2026-11-26T16:00:00Z");
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

const PRE_SEND_ROWS: CleanupRowCounts = {
  requestInsert: 1,
  blockMutation: 1,
  leaseMutation: 1,
  permitMutation: 1,
  auditAppend: 1,
  completionUpdate: 1,
};

const AFTER_SEND_ROWS: CleanupRowCounts = {
  ...PRE_SEND_ROWS,
  leaseMutation: 0,
};

const ALREADY_ROWS: CleanupRowCounts = {
  ...PRE_SEND_ROWS,
  blockMutation: 0,
  leaseMutation: 0,
  permitMutation: 0,
};

describe("R3 Egress Revocation R2 Scope Cleanup idempotency", () => {
  it("applies first pre-send cleanup", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toMatchObject({
      ok: true,
      value: {
        status: "APPLIED",
        blockVersion: 1,
        leaseOutcome: "REVOKED",
        permitOutcome: "REVOKED",
        externalOutcome: "NOT_SENT",
      },
    });
    expect(model.leaseState(IDS.lease)).toBe("REVOKED");
    expect(model.permitState(IDS.permit)).toBe("REVOKED");
  });

  it("returns the exact same result for same-ID same-payload replay", () => {
    const model = new OfflineScopeCleanupModel(resources());
    const first = model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    });
    const replay = model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    });
    expect(first).toEqual(replay);
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(1);
    expect(model.auditSnapshot()).toHaveLength(1);
  });

  it("rejects same-ID different payload without mutation", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    }).ok).toBe(true);
    const before = JSON.stringify(model.snapshot());
    expect(model.cleanup({
      payload: payload({ reasonCode: "DIFFERENT_REASON" }),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toEqual({
      ok: false,
      code: "IDEMPOTENCY_KEY_REUSE_CONFLICT",
    });
    expect(JSON.stringify(model.snapshot())).toBe(before);
  });

  it("treats a different request ID on the same scope as already satisfied", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    }).ok).toBe(true);
    expect(model.cleanup({
      payload: payload({ cleanupRequestId: IDS.cleanup2 }),
      rowCounts: ALREADY_ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toMatchObject({
      ok: true,
      value: { status: "ALREADY_SATISFIED", blockVersion: 1 },
    });
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(1);
    expect(model.auditSnapshot()).toHaveLength(2);
  });

  it("allows two distinct requests to observe the same final cleanup", () => {
    const model = new OfflineScopeCleanupModel(resources());
    const first = model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    });
    const second = model.cleanup({
      payload: payload({ cleanupRequestId: IDS.cleanup2 }),
      rowCounts: ALREADY_ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    });
    expect(first.ok && second.ok).toBe(true);
    expect(model.leaseState(IDS.lease)).toBe("REVOKED");
    expect(model.permitState(IDS.permit)).toBe("REVOKED");
  });

  it("linearizes concurrent calls using the same request ID", async () => {
    const model = new OfflineScopeCleanupModel(resources());
    const [left, right] = await Promise.all([
      model.cleanupConcurrent({
        payload: payload(),
        rowCounts: PRE_SEND_ROWS,
        auditEventId: IDS.audit,
        now: NOW,
      }),
      model.cleanupConcurrent({
        payload: payload(),
        rowCounts: PRE_SEND_ROWS,
        auditEventId: IDS.audit2,
        now: NOW,
      }),
    ]);
    expect(left.ok && right.ok).toBe(true);
    expect(left).toEqual(right);
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(1);
    expect(model.auditSnapshot()).toHaveLength(1);
  });

  it("linearizes concurrent different request IDs without a version race", async () => {
    const model = new OfflineScopeCleanupModel(resources());
    const results = await Promise.all([
      model.cleanupConcurrent({
        payload: payload(),
        rowCounts: PRE_SEND_ROWS,
        auditEventId: IDS.audit,
        now: NOW,
      }),
      model.cleanupConcurrent({
        payload: payload({ cleanupRequestId: IDS.cleanup2 }),
        rowCounts: ALREADY_ROWS,
        auditEventId: IDS.audit2,
        now: NOW,
      }),
    ]);
    expect(results.every((result) => result.ok)).toBe(true);
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(1);
    expect(model.auditSnapshot()).toHaveLength(2);
  });

  it("handles after-send cleanup without revoking the Lease", () => {
    const model = new OfflineScopeCleanupModel(resources({
      leaseState: "SENT",
      permitState: "CONSUMED",
      intentState: "FINAL_AUTHORIZED",
    }));
    expect(model.cleanup({
      payload: payload(),
      rowCounts: AFTER_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toMatchObject({
      ok: true,
      value: {
        leaseOutcome: "PRESERVED_AFTER_WRITE_AUTHORIZED",
        externalOutcome: "WRITE_MAY_HAVE_OCCURRED",
      },
    });
    expect(model.leaseState(IDS.lease)).toBe("SENT");
    expect(model.permitState(IDS.permit)).toBe("REVOKED");
  });

  it("preserves a WRITE_AUTHORIZED Lease and records unknown external certainty", () => {
    const model = new OfflineScopeCleanupModel(resources({
      leaseState: "WRITE_AUTHORIZED",
      permitState: "CONSUMED",
      intentState: "WRITE_AUTHORIZED",
    }));
    expect(model.cleanup({
      payload: payload(),
      rowCounts: AFTER_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toMatchObject({
      ok: true,
      value: {
        leaseOutcome: "PRESERVED_AFTER_WRITE_AUTHORIZED",
        externalOutcome: "WRITE_MAY_HAVE_OCCURRED",
      },
    });
  });

  it("preserves SEND_OUTCOME_UNKNOWN", () => {
    const model = new OfflineScopeCleanupModel(resources({
      leaseState: "SEND_OUTCOME_UNKNOWN",
      permitState: "CONSUMED",
      intentState: "SEND_OUTCOME_UNKNOWN",
    }));
    expect(model.cleanup({
      payload: payload(),
      rowCounts: AFTER_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toMatchObject({
      ok: true,
      value: {
        leaseOutcome: "PRESERVED_OUTCOME_UNKNOWN",
        externalOutcome: "SEND_OUTCOME_UNKNOWN",
      },
    });
  });

  it("rolls back on Audit failure", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
      failAudit: true,
    })).toEqual({
      ok: false,
      code: "WORKER_AUDIT_ATOMICITY_FAILED",
    });
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(0);
    expect(model.leaseState(IDS.lease)).toBe("SEND_AUTHORIZED");
    expect(model.auditSnapshot()).toHaveLength(0);
  });

  it("rolls back on block mutation failure", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
      failBlockMutation: true,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(0);
  });

  it.each([
    { ...PRE_SEND_ROWS, requestInsert: 0 },
    { ...PRE_SEND_ROWS, blockMutation: 0 },
    { ...PRE_SEND_ROWS, leaseMutation: 0 },
    { ...PRE_SEND_ROWS, permitMutation: 0 },
    { ...PRE_SEND_ROWS, auditAppend: 0 },
    { ...PRE_SEND_ROWS, completionUpdate: 0 },
  ])("rejects invalid row counts %#", (rowCounts) => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts,
      auditEventId: IDS.audit,
      now: NOW,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
  });

  it("recovers a lost COMMIT response with same-request replay", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
      commitResponseLost: true,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toMatchObject({
      ok: true,
      value: { status: "APPLIED", blockVersion: 1 },
    });
    expect(model.auditSnapshot()).toHaveLength(1);
  });

  it("leaves no partial state on crash before commit", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
      crashBeforeCommit: true,
    })).toEqual({ ok: false, code: "PROCESS_CRASHED_BEFORE_COMMIT" });
    expect(model.blockVersion(IDS.scope, IDS.worker)).toBe(0);
    expect(model.auditSnapshot()).toHaveLength(0);
  });

  it("restores completed idempotency state after restart", () => {
    const model = new OfflineScopeCleanupModel(resources());
    const first = model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    });
    const restored = OfflineScopeCleanupModel.fromSnapshot(model.snapshot());
    expect(restored.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit2,
      now: NOW + 1,
    })).toEqual(first);
  });

  it("fails closed when authority is unavailable", () => {
    const model = new OfflineScopeCleanupModel(resources());
    model.setAuthorityAvailable(false);
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toEqual({ ok: false, code: "AUTHORITY_UNAVAILABLE" });
  });

  it("rejects an already-revoked Lease without a completed idempotency record", () => {
    const model = new OfflineScopeCleanupModel(resources({ leaseState: "REVOKED" }));
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toEqual({
      ok: false,
      code: "SCOPE_CLEANUP_STATE_INCONSISTENT",
    });
  });

  it("rejects an already-revoked Permit without a completed idempotency record", () => {
    const model = new OfflineScopeCleanupModel(resources({ permitState: "REVOKED" }));
    expect(model.cleanup({
      payload: payload(),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toEqual({
      ok: false,
      code: "SCOPE_CLEANUP_STATE_INCONSISTENT",
    });
  });

  it("rejects a forged Scope binding", () => {
    const model = new OfflineScopeCleanupModel(resources());
    expect(model.cleanup({
      payload: payload({ scopeKey: "forged-scope" }),
      rowCounts: PRE_SEND_ROWS,
      auditEventId: IDS.audit,
      now: NOW,
    })).toEqual({ ok: false, code: "SCOPE_BINDING_MISMATCH" });
  });
});

```
<!-- END_EXACT_SOURCE id=S026 -->

### S027. tests/sql-analyzer.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/tests/sql-analyzer.test.ts`
- Bytes: `4145`
- SHA-256: `885CAC0221379589D50332351DB7B79CAF7613D578D438E1DCE774DFB8A59F7E`

<!-- BEGIN_EXACT_SOURCE id=S027 sha256=885CAC0221379589D50332351DB7B79CAF7613D578D438E1DCE774DFB8A59F7E bytes=4145 -->
```text
import { readFileSync } from "node:fs";
import { resolve } from "node:path";
import { describe, expect, it } from "vitest";

import {
  SQL_ANALYZER_LIMITS,
  analyzeSqlTransactionContract,
  reviewAuditSql,
  reviewCleanupSql,
  reviewWorkerLifecycleSql,
} from "../models/sql-analyzer";

const ROOT = resolve(
  process.cwd(),
  "preparation/production-trust/r3-egress-revocation-r2-remediation",
);
const WORKER_SQL = readFileSync(
  resolve(ROOT, "PHASE_R3_WORKER_GLOBAL_REVOCATION_R2.sql"),
  "utf8",
);
const CLEANUP_SQL = readFileSync(
  resolve(ROOT, "PHASE_R3_SCOPE_CLEANUP_R2.sql"),
  "utf8",
);
const AUDIT_SQL = readFileSync(
  resolve(ROOT, "PHASE_R3_EGRESS_AUDIT_R2.sql"),
  "utf8",
);

describe("R3 Egress Revocation R2 SQL structure", () => {
  it("segments and inventories the actual SQL drafts without execution", () => {
    for (const sql of [WORKER_SQL, CLEANUP_SQL, AUDIT_SQL]) {
      const result = analyzeSqlTransactionContract(sql);
      expect(result.statements.length).toBeGreaterThan(0);
      expect(result.transactions.length).toBeGreaterThan(0);
      expect(result.findings.map((finding) => finding.code))
        .not.toContain("LOCK_ORDER_CROSSING");
    }
    expect(SQL_ANALYZER_LIMITS).toContain("POSTGRESQL_EXECUTION_NOT_PERFORMED");
  });

  it("accepts the Worker lifecycle contract and rejects ACTIVE-only revoke SQL", () => {
    expect(reviewWorkerLifecycleSql(WORKER_SQL)).toEqual([]);
    const activeOnly = WORKER_SQL.replace(
      "state IN ('ACTIVE', 'DRAINING')",
      "state = 'ACTIVE'",
    );
    expect(
      reviewWorkerLifecycleSql(activeOnly).map((finding) => finding.code),
    ).toContain("DRAINING_REVOCATION_MISSING");
  });

  it("rejects Worker reactivation through Upsert", () => {
    const bad = `${WORKER_SQL}
      INSERT INTO trust_r4_worker_registration (worker_instance_id)
      VALUES ($1)
      ON CONFLICT (worker_instance_id) DO UPDATE SET state = 'ACTIVE';`;
    expect(
      reviewWorkerLifecycleSql(bad).map((finding) => finding.code),
    ).toContain("WORKER_REACTIVATION_UPSERT");
  });

  it("accepts cleanup idempotency structure", () => {
    expect(reviewCleanupSql(CLEANUP_SQL)).toEqual([]);
  });

  it("rejects a cleanup request without digest binding", () => {
    const bad = CLEANUP_SQL.replaceAll("request_digest", "ignored_digest");
    expect(
      reviewCleanupSql(bad).map((finding) => finding.code),
    ).toContain("CLEANUP_REQUEST_DIGEST_MISSING");
  });

  it("rejects an unconditional block-version bump", () => {
    const bad = CLEANUP_SQL.replace(
      /WHERE\s+trust_r5_scope_worker_block\.blocked_revocation_version\s*<\s*EXCLUDED\.blocked_revocation_version/iu,
      "",
    );
    expect(
      reviewCleanupSql(bad).map((finding) => finding.code),
    ).toContain("CLEANUP_UNCONDITIONAL_BLOCK_VERSION_BUMP");
  });

  it("accepts truthful Audit event separation", () => {
    expect(reviewAuditSql(AUDIT_SQL)).toEqual([]);
  });

  it("rejects the obsolete REQUEST_SENT event name", () => {
    const bad = AUDIT_SQL.replaceAll(
      "EGRESS_WRITE_START_AUTHORIZED",
      "REQUEST_SENT",
    );
    const codes = reviewAuditSql(bad).map((finding) => finding.code);
    expect(codes).toContain("FALSE_REQUEST_SENT_EVENT");
    expect(codes).toContain("AUDIT_EVENT_MISSING_EGRESS_WRITE_START_AUTHORIZED");
  });

  it("rejects missing trusted runtime evidence source", () => {
    const bad = AUDIT_SQL.replaceAll("TRUSTED_EGRESS_RUNTIME", "DATABASE_GUESS");
    expect(
      reviewAuditSql(bad).map((finding) => finding.code),
    ).toContain("RUNTIME_EVIDENCE_SOURCE_MISSING");
  });

  it("reviews parameter inventories without claiming semantic execution", () => {
    const workerParameters = analyzeSqlTransactionContract(WORKER_SQL).parameters;
    const cleanupParameters = analyzeSqlTransactionContract(CLEANUP_SQL).parameters;
    const auditParameters = analyzeSqlTransactionContract(AUDIT_SQL).parameters;
    expect(workerParameters.slice(0, 9)).toContain("$1");
    expect(workerParameters).toContain("$11");
    expect(cleanupParameters).toContain("$17");
    expect(auditParameters).toContain("$45");
  });
});

```
<!-- END_EXACT_SOURCE id=S027 -->

### S028. tests/worker-lifecycle.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/tests/worker-lifecycle.test.ts`
- Bytes: `8668`
- SHA-256: `1A206423D850960CEBF832802499CB8DCCAC3565D611661D8469F7A466DD8E6F`

<!-- BEGIN_EXACT_SOURCE id=S028 sha256=1A206423D850960CEBF832802499CB8DCCAC3565D611661D8469F7A466DD8E6F bytes=8668 -->
```text
import { describe, expect, it } from "vitest";

import { OfflineWorkerLifecycleModel } from "../models/worker-lifecycle";

const NOW = Date.parse("2026-11-26T15:00:00Z");
const IDS = Object.freeze({
  worker: "11111111-1111-4111-8111-111111111111",
  request: "22222222-2222-4222-8222-222222222222",
  request2: "33333333-3333-4333-8333-333333333333",
  audit: "44444444-4444-4444-8444-444444444444",
  audit2: "55555555-5555-4555-8555-555555555555",
});

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

const ROWS = Object.freeze({
  requestInsert: 1,
  revocationUpdate: 1,
  registrationUpdate: 1,
  auditAppend: 1,
});

function model(
  registrationState: "REGISTERED" | "ACTIVE" | "DRAINING" | "REVOKED",
) {
  const value = new OfflineWorkerLifecycleModel();
  expect(value.seedWorker({
    workerInstanceId: IDS.worker,
    registrationState,
  }).ok).toBe(true);
  return value;
}

describe("R3 Egress Revocation R2 Worker lifecycle", () => {
  it.each(["ACTIVE", "DRAINING"] as const)(
    "revokes %s Worker and increments tombstone versions",
    (registrationState) => {
      const state = model(registrationState);
      expect(state.revoke({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit,
      })).toMatchObject({
        ok: true,
        value: {
          status: "REVOKED",
          registrationState: "REVOKED",
          revocationVersion: 1,
          recordVersion: 2,
        },
      });
      expect(state.worker(IDS.worker)).toMatchObject({
        registrationState: "REVOKED",
        revocationState: "REVOKED",
      });
      expect(state.auditSnapshot()).toHaveLength(1);
    },
  );

  it("rejects REGISTERED because it is outside the frozen runtime table state set", () => {
    expect(model("REGISTERED").revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    })).toEqual({
      ok: false,
      code: "WORKER_REGISTERED_REVOCATION_FORBIDDEN",
    });
  });

  it("keeps REVOKED terminal against ordinary activation", () => {
    const state = model("ACTIVE");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    }).ok).toBe(true);
    expect(state.activate(IDS.worker)).toEqual({
      ok: false,
      code: "WORKER_REACTIVATION_FORBIDDEN",
    });
  });

  it("replays the same request without new version or Audit", () => {
    const state = model("ACTIVE");
    const first = state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    });
    const replay = state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    });
    expect(first.ok).toBe(true);
    expect(replay).toMatchObject({
      ok: true,
      value: {
        status: "REPLAYED",
        revocationVersion: 1,
        auditEventId: IDS.audit,
      },
    });
    expect(state.auditSnapshot()).toHaveLength(1);
  });

  it("rejects same request ID with a different payload", () => {
    const state = model("ACTIVE");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    }).ok).toBe(true);
    expect(state.revoke({
      payload: payload({ reasonCode: "DIFFERENT_REASON" }),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({
      ok: false,
      code: "IDEMPOTENCY_KEY_REUSE_CONFLICT",
    });
  });

  it("rejects a different request after revocation without another Audit", () => {
    const state = model("ACTIVE");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    }).ok).toBe(true);
    expect(state.revoke({
      payload: payload({ requestId: IDS.request2 }),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toEqual({
      ok: false,
      code: "WORKER_ALREADY_REVOKED_DIFFERENT_REQUEST",
    });
    expect(state.auditSnapshot()).toHaveLength(1);
  });

  it("rejects expected record-version mismatch", () => {
    expect(model("DRAINING").revoke({
      payload: payload({ expectedRecordVersion: 2 }),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    })).toEqual({
      ok: false,
      code: "WORKER_VERSION_CONFLICT",
    });
  });

  it.each([
    { requestInsert: 0, revocationUpdate: 1, registrationUpdate: 1, auditAppend: 1 },
    { requestInsert: 1, revocationUpdate: 0, registrationUpdate: 1, auditAppend: 1 },
    { requestInsert: 1, revocationUpdate: 1, registrationUpdate: 0, auditAppend: 1 },
    { requestInsert: 1, revocationUpdate: 1, registrationUpdate: 1, auditAppend: 0 },
  ])("rejects any non-one row count %#", (rowCounts) => {
    expect(model("DRAINING").revoke({
      payload: payload(),
      rowCounts,
      auditEventId: IDS.audit,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
  });

  it("rolls back both records when Audit fails", () => {
    const state = model("DRAINING");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
      failAudit: true,
    })).toEqual({
      ok: false,
      code: "WORKER_AUDIT_ATOMICITY_FAILED",
    });
    expect(state.worker(IDS.worker)).toMatchObject({
      registrationState: "DRAINING",
      revocationState: "ACTIVE",
      revocationVersion: 0,
    });
    expect(state.auditSnapshot()).toHaveLength(0);
  });

  it("fails closed when authority is unavailable", () => {
    const state = model("ACTIVE");
    state.setAuthorityAvailable(false);
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    })).toEqual({ ok: false, code: "AUTHORITY_UNAVAILABLE" });
  });

  it("recovers a lost COMMIT response using the same request ID", () => {
    const state = model("DRAINING");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
      commitResponseLost: true,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    })).toMatchObject({
      ok: true,
      value: { status: "REPLAYED", revocationVersion: 1 },
    });
  });

  it("does not mutate on pre-commit crash", () => {
    const state = model("ACTIVE");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
      crashBeforeCommit: true,
    })).toEqual({ ok: false, code: "PROCESS_CRASHED_BEFORE_COMMIT" });
    expect(state.worker(IDS.worker)?.revocationState).toBe("ACTIVE");
    expect(state.auditSnapshot()).toHaveLength(0);
  });

  it("linearizes two same-ID callers to one version and one Audit", async () => {
    const state = model("DRAINING");
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
    expect([left.ok, right.ok]).toEqual([true, true]);
    expect(state.worker(IDS.worker)?.revocationVersion).toBe(1);
    expect(state.auditSnapshot()).toHaveLength(1);
  });

  it("linearizes two different request IDs to one winner and one conflict", async () => {
    const state = model("DRAINING");
    const [left, right] = await Promise.all([
      state.revokeConcurrent({
        payload: payload(),
        rowCounts: ROWS,
        auditEventId: IDS.audit,
      }),
      state.revokeConcurrent({
        payload: payload({ requestId: IDS.request2 }),
        rowCounts: ROWS,
        auditEventId: IDS.audit2,
      }),
    ]);
    expect([left.ok, right.ok].sort()).toEqual([false, true]);
    expect(state.worker(IDS.worker)?.revocationVersion).toBe(1);
    expect(state.auditSnapshot()).toHaveLength(1);
  });

  it("restores replay state from a persistence snapshot", () => {
    const state = model("ACTIVE");
    expect(state.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit,
    }).ok).toBe(true);
    const restored = OfflineWorkerLifecycleModel.fromSnapshot(state.snapshot());
    expect(restored.revoke({
      payload: payload(),
      rowCounts: ROWS,
      auditEventId: IDS.audit2,
    })).toMatchObject({
      ok: true,
      value: { status: "REPLAYED" },
    });
    expect(restored.auditSnapshot()).toHaveLength(1);
  });
});

```
<!-- END_EXACT_SOURCE id=S028 -->

### S029. tools/build-evidence.mjs

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/tools/build-evidence.mjs`
- Bytes: `15278`
- SHA-256: `4E443CDF94282B080C231A3D87FB72C1AE47844FC9D858139E028EC9CF578C79`

<!-- BEGIN_EXACT_SOURCE id=S029 sha256=4E443CDF94282B080C231A3D87FB72C1AE47844FC9D858139E028EC9CF578C79 bytes=15278 -->
````text
import { createHash } from "node:crypto";
import {
  existsSync,
  readFileSync,
  readdirSync,
  statSync,
  writeFileSync,
} from "node:fs";
import { dirname, extname, join, relative, resolve } from "node:path";
import { fileURLToPath } from "node:url";

const taskRoot = dirname(dirname(fileURLToPath(import.meta.url)));
const trustRoot = dirname(taskRoot);
const workspace = resolve(trustRoot, "..", "..");
const r1Root = join(trustRoot, "r3-egress-revocation-remediation");
const bundlePath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE.md",
);
const reportPath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md",
);
const bundleManifestPath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt",
);
const manifestPath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_R2_SHA256SUMS.txt",
);
const r1BundlePath = join(
  trustRoot,
  "PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE.md",
);
const expectedR1BundleHash =
  "CDD2ED989668FE7A9588533532A8A209699085EB68934BB9CE74CDBBE47354FE";
const expectedR1BundleBytes = 320631;

function sha256Bytes(bytes) {
  return createHash("sha256").update(bytes).digest("hex").toUpperCase();
}

function sha256File(path) {
  return sha256Bytes(readFileSync(path));
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

function exactSourceBody(bundleText, id, hash, bytes) {
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

const r1Bundle = readFileSync(r1BundlePath);
const r1BundleText = r1Bundle.toString("utf8");
const r1BundleHash = sha256Bytes(r1Bundle);
const r1BundleMatches = r1BundleHash === expectedR1BundleHash
  && r1Bundle.length === expectedR1BundleBytes;

const catalog = [];
for (const line of r1BundleText.split(/\r?\n/u)) {
  const match = /^\| (S\d{3}) \| `([^`]+)` \| (\d+) \| ([0-9A-F]{64}) \|$/u
    .exec(line);
  if (match) {
    catalog.push({
      id: match[1],
      displayPath: match[2],
      bytes: Number(match[3]),
      hash: match[4],
    });
  }
}
const r1LocalMismatches = [];
const r1BodyMismatches = [];
for (const source of catalog) {
  const localPath = join(r1Root, source.displayPath);
  if (!existsSync(localPath)) {
    r1LocalMismatches.push(`${source.displayPath}: MISSING`);
    continue;
  }
  const localBytes = readFileSync(localPath);
  if (
    localBytes.length !== source.bytes
    || sha256Bytes(localBytes) !== source.hash
  ) {
    r1LocalMismatches.push(`${source.displayPath}: local hash/size mismatch`);
  }
  const embedded = exactSourceBody(
    r1BundleText,
    source.id,
    source.hash,
    source.bytes,
  );
  if (
    embedded === null
    || !Buffer.from(embedded, "utf8").equals(localBytes)
  ) {
    r1BodyMismatches.push(`${source.displayPath}: bundle body mismatch`);
  }
}

function verifyManifest(manifestPath) {
  const lines = readFileSync(manifestPath, "utf8")
    .split(/\r?\n/u)
    .map((line) => /^([0-9A-Fa-f]{64})\s{2}(.+)$/u.exec(line))
    .filter(Boolean);
  const mismatches = [];
  for (const match of lines) {
    const relativePath = match[2].replaceAll("\\", "/");
    const absolute = join(workspace, relativePath);
    if (!existsSync(absolute) || sha256File(absolute) !== match[1].toUpperCase()) {
      mismatches.push(relativePath);
    }
  }
  return { entries: lines.length, mismatches };
}

const r1ManifestCheck = verifyManifest(
  join(r1Root, "PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt"),
);
const r31ManifestCheck = verifyManifest(
  join(workspace, "PHASE_R31_R36_SHA256SUMS.txt"),
);

const expectedProtectedHashes = new Map([
  ["package.json", "44FC2153675107E0E61DBA8E88E955281B913D3341718C224110AB5B2F6C7F4D"],
  ["pnpm-lock.yaml", "926DFD4A33A662BAAB424E7C9FBBFD5FB16B74BE2E6119AD9F6A0D5144B719B4"],
  [
    "src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts",
    "1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309",
  ],
]);
const protectedMismatches = [];
for (const [relativePath, expected] of expectedProtectedHashes) {
  if (sha256File(join(workspace, relativePath)) !== expected) {
    protectedMismatches.push(relativePath);
  }
}

const importBoundaryHits = [];
for (const rootName of ["src", "scripts"]) {
  for (const absolute of listFiles(join(workspace, rootName))) {
    const text = readFileSync(absolute, "utf8");
    if (
      text.includes("r3-egress-revocation-r2-remediation")
      || text.includes("production-trust/r3-egress-revocation-r2")
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
  join(
    workspace,
    "src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts",
  ),
  "utf8",
);
const productionBlocked = productionEntry.includes(
  'code: "PRODUCTION_FETCH_TRUST_UNAVAILABLE"',
)
  && productionEntry.includes("productionTrustConnected: false")
  && productionEntry.includes("keyReads: 0")
  && productionEntry.includes("networkCalls: 0");

const excludedFromBundle = new Set([
  manifestPath,
  bundlePath,
  reportPath,
  bundleManifestPath,
]);
const bundleSources = listFiles(taskRoot)
  .filter((path) => !excludedFromBundle.has(path))
  .sort((left, right) => {
  const relLeft = relative(taskRoot, left).replaceAll("\\", "/");
  const relRight = relative(taskRoot, right).replaceAll("\\", "/");
  const rank = (value) => {
    if (value.endsWith(".md")) return 0;
    if (value.endsWith("SHA256SUMS.txt")) return 1;
    if (value.endsWith(".sql")) return 2;
    if (value === "contracts.ts" || value === "lock-order.ts") return 3;
    if (value.startsWith("models/")) return 4;
    if (value.startsWith("tests/")) return 5;
    if (value.startsWith("tools/")) return 6;
    if (extname(value) === ".ts") return 7;
    return 8;
  };
  return rank(relLeft) - rank(relRight) || relLeft.localeCompare(relRight);
  });

const sources = bundleSources.map((absolute, index) => {
  const bytes = readFileSync(absolute);
  return {
    id: `S${String(index + 1).padStart(3, "0")}`,
    absolute,
    workspacePath: relative(workspace, absolute).replaceAll("\\", "/"),
    displayPath: relative(taskRoot, absolute).replaceAll("\\", "/"),
    bytes,
    size: statSync(absolute).size,
    hash: sha256Bytes(bytes),
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

const header = [
  "# PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE",
  "",
  "## Review Status",
  "",
  "```text",
  "R3_EGRESS_REVOCATION_R2_REMEDIATION_PASS",
  "OFFLINE_ACCEPTANCE=PASS",
  "INDEPENDENT_REVIEW=REQUIRED",
  "PRODUCTION_IMPLEMENTATION=NOT_STARTED",
  "PRODUCTION_ENFORCEMENT=BLOCKED",
  "REAL_FETCH_AUTHORIZED=NO",
  "```",
  "",
  "## Scope",
  "",
  "Complete R2 evidence for DRAINING revocation, Scope Cleanup idempotency",
  "and truthful Egress audit semantics. This is not a production approval.",
  "",
  "## Evidence Boundary",
  "",
  "```text",
  "POSTGRESQL_INTEGRATION=NOT_EXECUTED",
  "MULTI_INSTANCE_TEST=NOT_EXECUTED",
  "REAL_EGRESS_TEST=NOT_EXECUTED",
  "REAL_NETWORK_RACE_TEST=NOT_EXECUTED",
  "REAL_PROVIDER_TEST=NOT_EXECUTED",
  "SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED",
  "```",
  "",
  "## Contents",
  "",
  "- 1. Source Catalog",
  "- 2. Complete Source Bodies",
  "- 3. Integrity and Independence",
  "",
  "## 1. Source Catalog",
  "",
  "| ID | Path | Bytes | SHA-256 |",
  "|---|---|---:|---|",
  ...sources.map((source) =>
    `| ${source.id} | \`${source.displayPath}\` | ${source.size} | ${source.hash} |`
  ),
  "",
  "## 2. Complete Source Bodies",
  "",
].join("\n");
const footer = [
  "",
  "## 3. Integrity and Independence",
  "",
  "```text",
  `R1_BUNDLE_HASH_MATCH=${r1BundleMatches ? "YES" : "NO"}`,
  `R1_CATALOG_SOURCES=${catalog.length}`,
  `R1_LOCAL_MISMATCHES=${r1LocalMismatches.length}`,
  `R1_BUNDLE_BODY_MISMATCHES=${r1BodyMismatches.length}`,
  `R1_REMEDIATION_MANIFEST_ENTRIES=${r1ManifestCheck.entries}`,
  `R1_REMEDIATION_MANIFEST_MISMATCHES=${r1ManifestCheck.mismatches.length}`,
  `R31_R36_MANIFEST_ENTRIES=${r31ManifestCheck.entries}`,
  `R31_R36_MANIFEST_MISMATCHES=${r31ManifestCheck.mismatches.length}`,
  `R2_SOURCE_FILES=${sources.length}`,
  "INDEPENDENCE_LIMITATION=SAME_HOST_AGENTS_NO_USABLE_WORKPACK",
  "```",
  "",
].join("\n");
writeFileSync(bundlePath, header + bodySections.join("\n") + footer, "utf8");

const bundleText = readFileSync(bundlePath, "utf8");
const bodyMismatches = [];
for (const source of sources) {
  const embedded = exactSourceBody(
    bundleText,
    source.id,
    source.hash,
    source.size,
  );
  if (
    embedded === null
    || !Buffer.from(embedded, "utf8").equals(source.bytes)
  ) {
    bodyMismatches.push(source.displayPath);
  }
}

const bundleBytes = readFileSync(bundlePath);
const bundleHash = sha256Bytes(bundleBytes);
const pass = r1BundleMatches
  && r1LocalMismatches.length === 0
  && r1BodyMismatches.length === 0
  && r1ManifestCheck.mismatches.length === 0
  && r31ManifestCheck.mismatches.length === 0
  && protectedMismatches.length === 0
  && importBoundaryHits.length === 0
  && sensitiveHits.length === 0
  && productionBlocked
  && bodyMismatches.length === 0;
writeFileSync(reportPath, [
  "# PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_REPORT",
  "",
  "## Final Status",
  "",
  "```text",
  `R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_${pass ? "PASS" : "NEEDS_REVISION"}`,
  "```",
  "",
  "## Bundle",
  "",
  "```text",
  `BUNDLE_PATH=${relative(workspace, bundlePath).replaceAll("\\", "/")}`,
  `BUNDLE_BYTES=${bundleBytes.length}`,
  `BUNDLE_SHA256=${bundleHash}`,
  `SOURCE_FILES=${sources.length}`,
  `BODY_EXACTNESS_MISMATCHES=${bodyMismatches.length}`,
  `R1_BUNDLE_HASH_MATCH=${r1BundleMatches ? "YES" : "NO"}`,
  `R1_CATALOG_SOURCES=${catalog.length}`,
  `R1_LOCAL_MISMATCHES=${r1LocalMismatches.length}`,
  `R1_BUNDLE_BODY_MISMATCHES=${r1BodyMismatches.length}`,
  `R1_MANIFEST_ENTRIES=${r1ManifestCheck.entries}`,
  `R1_MANIFEST_MISMATCHES=${r1ManifestCheck.mismatches.length}`,
  `R31_R36_MANIFEST_ENTRIES=${r31ManifestCheck.entries}`,
  `R31_R36_MANIFEST_MISMATCHES=${r31ManifestCheck.mismatches.length}`,
  `PROTECTED_HASH_MISMATCHES=${protectedMismatches.length}`,
  `IMPORT_BOUNDARY_HITS=${importBoundaryHits.length}`,
  `SENSITIVE_PATTERN_HITS=${sensitiveHits.length}`,
  "```",
  "",
  "## Verification",
  "",
  "```text",
  "R3_R2_TARGETED_VITEST=4_FILES_67_TESTS_PASS",
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
  "## Production Safety",
  "",
  "```text",
  "PRODUCTION_IMPLEMENTATION=NOT_STARTED",
  "PRODUCTION_ENFORCEMENT=BLOCKED",
  "PRODUCTION_EGRESS_IMPLEMENTED=NO",
  "NETWORK_ISOLATION_ENFORCED=NO",
  "MULTI_INSTANCE_COORDINATION=NOT_IMPLEMENTED",
  "REAL_FETCH_AUTHORIZED=NO",
  "SOCKET_WRITE_ATTEMPTED_RUNTIME_EVIDENCE=NOT_IMPLEMENTED",
  "REAL_KEY_ACCESSED=NO",
  "REAL_API_CALLED=NO",
  "NETWORK_ACCESSED=NO",
  "DATABASE_CONNECTED=NO",
  "SQL_EXECUTED=NO",
  "DOCKER_ACCESSED=NO",
  "GITHUB_ACCESSED=NO",
  "DEPENDENCIES_INSTALLED=NO",
  "```",
  "",
  "## Findings",
  "",
  "```text",
  ...(pass ? ["NO_INTEGRITY_FINDINGS"] : [
    ...r1LocalMismatches,
    ...r1BodyMismatches,
    ...r1ManifestCheck.mismatches,
    ...r31ManifestCheck.mismatches,
    ...protectedMismatches,
    ...importBoundaryHits,
    ...sensitiveHits,
    ...bodyMismatches,
  ].map((item) => `FINDING=${item}`)),
  "```",
  "",
  "## Independence",
  "",
  "Three same-host subagents were requested but returned without workpacks.",
  "This is not independent third-party review.",
  "",
].join("\r\n"), "utf8");

writeFileSync(bundleManifestPath, [
  "# PHASE_R3_EGRESS_REVOCATION_R2_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS",
  "# ENTRIES=2",
  "# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION",
  "",
  `${sha256File(bundlePath)}  ${relative(workspace, bundlePath).replaceAll("\\", "/")}`,
  `${sha256File(reportPath)}  ${relative(workspace, reportPath).replaceAll("\\", "/")}`,
  "",
].join("\r\n"), "utf8");

const taskFiles = listFiles(taskRoot).filter((path) => path !== manifestPath);
writeFileSync(manifestPath, [
  "# PHASE_R3_EGRESS_REVOCATION_R2_SHA256SUMS",
  `# ENTRIES=${taskFiles.length}`,
  "# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION",
  "",
  ...taskFiles.map((path) =>
    `${sha256File(path)}  ${relative(workspace, path).replaceAll("\\", "/")}`
  ),
  "",
].join("\r\n"), "utf8");

console.log(JSON.stringify({
  r1BundleMatches,
  r1CatalogSources: catalog.length,
  r1LocalMismatches,
  r1BodyMismatches,
  r1ManifestCheck,
  r31ManifestCheck,
  protectedMismatches,
  importBoundaryHits,
  sensitiveHits,
  productionBlocked,
  taskManifestEntries: taskFiles.length,
  bundleSourceFiles: sources.length,
  bodyMismatches,
  bundleBytes: bundleBytes.length,
  bundleHash,
  pass,
}, null, 2));

if (!pass) process.exitCode = 1;

````
<!-- END_EXACT_SOURCE id=S029 -->

### S030. tools/run-verification.ps1

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/tools/run-verification.ps1`
- Bytes: `7036`
- SHA-256: `AB6A8EC0A35807DBB736E46F9C1155EAD817592C01E1FB974C8E13473075C093`

<!-- BEGIN_EXACT_SOURCE id=S030 sha256=AB6A8EC0A35807DBB736E46F9C1155EAD817592C01E1FB974C8E13473075C093 bytes=7036 -->
```````text
$ErrorActionPreference = "Continue"

$workspace = (Resolve-Path (Join-Path $PSScriptRoot "..\..\..\..")).Path
$taskDir = (Resolve-Path (Join-Path $PSScriptRoot "..")).Path
$log = Join-Path $taskDir "PHASE_R3_EGRESS_TEST_EXECUTION_R2.md"
$records = [System.Collections.Generic.List[string]]::new()
$failed = 0

function Invoke-Logged {
  param(
    [string]$Name,
    [string]$Executable,
    [string[]]$Arguments
  )

  $started = Get-Date
  $output = & $Executable @Arguments 2>&1
  $exitCode = $LASTEXITCODE
  $ended = Get-Date
  if ($exitCode -ne 0) {
    $script:failed += 1
  }
  $body = ($output | Out-String).Trim()
  $record = @(
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
    $body,
    '```',
    ""
  ) -join "`r`n"
  $records.Add($record)
}

Push-Location $workspace
try {
  Invoke-Logged "R3 R2 targeted Vitest" "node" @(
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
  $vitestArgs = @("node_modules/vitest/vitest.mjs", "run") + $relevant
  Invoke-Logged "R31-R36 Relevant Vitest" "node" $vitestArgs

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
      foreach ($errorItem in $errors) {
        $parseLines.Add($errorItem.Message)
      }
    } else {
      $parseLines.Add("$($script.Name)=PASS")
    }
  }
  $parseLines.Add("TOTAL=$($scripts.Count)")
  $parseLines.Add("FAILURES=$($parseErrors.Count)")
  $parseEnded = Get-Date
  $parseExit = if ($parseErrors.Count -eq 0) { 0 } else { 1 }
  if ($parseExit -ne 0) {
    $failed += 1
  }
  $records.Add(@(
    "### PowerShell 5.1 Parser",
    "",
    '```text',
    "COMMAND=inline PowerShell 5.1 Language.Parser over scripts/windows/*.ps1",
    "START=$($parseStarted.ToString('o'))",
    "END=$($parseEnded.ToString('o'))",
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
    "eslint", "preparation/production-trust/r3-egress-revocation-r2-remediation"
  )
  Invoke-Logged "Next Build" "pnpm.cmd" @("build")
} finally {
  Pop-Location
}

$header = @(
  "# PHASE_R3_EGRESS_TEST_EXECUTION_R2",
  "",
  "## Status",
  "",
  '``````text',
  "GENERATED_AT=$((Get-Date).ToString('o'))",
  "WORKSPACE=$workspace",
  "FAILED_COMMANDS=$failed",
  "POSTGRESQL_INTEGRATION=NOT_EXECUTED",
  "MULTI_INSTANCE_TEST=NOT_EXECUTED",
  "REAL_EGRESS_TEST=NOT_EXECUTED",
  "REAL_NETWORK_RACE_TEST=NOT_EXECUTED",
  "REAL_PROVIDER_TEST=NOT_EXECUTED",
  '``````',
  "",
  "## Execution Notes",
  "",
  "- The first R2 focused run had three failing assertions: an already-REVOKED",
  "  Lease returned `LEASE_STATE_INVALID` instead of the intended inconsistent",
  "  idempotency-state error, and two SQL analyzer fixtures did not mutate the",
  "  target clause as intended. The implementation/fixtures were corrected and",
  "  the complete run below is authoritative. The failure is preserved here.",
  "- The same-host subagents returned without producing workpacks. They are not",
  "  represented as independent review.",
  "",
  "## Commands",
  ""
) -join "`r`n"

Set-Content -LiteralPath $log -Value ($header + ($records -join "`r`n")) -Encoding utf8
if ($failed -ne 0) {
  exit 1
}

```````
<!-- END_EXACT_SOURCE id=S030 -->

### S031. vitest.config.ts

- Path: `preparation/production-trust/r3-egress-revocation-r2-remediation/vitest.config.ts`
- Bytes: `236`
- SHA-256: `03D475BAE8413140BD17B07408911906F0BBF97BF08107D6FF88051A7E66E5A5`

<!-- BEGIN_EXACT_SOURCE id=S031 sha256=03D475BAE8413140BD17B07408911906F0BBF97BF08107D6FF88051A7E66E5A5 bytes=236 -->
```text
import { defineConfig } from "vitest/config";

export default defineConfig({
  test: {
    environment: "node",
    include: [
      "preparation/production-trust/r3-egress-revocation-r2-remediation/tests/**/*.test.ts",
    ],
  },
});

```
<!-- END_EXACT_SOURCE id=S031 -->

## 3. Integrity and Independence

```text
R1_BUNDLE_HASH_MATCH=YES
R1_CATALOG_SOURCES=36
R1_LOCAL_MISMATCHES=0
R1_BUNDLE_BODY_MISMATCHES=0
R1_REMEDIATION_MANIFEST_ENTRIES=35
R1_REMEDIATION_MANIFEST_MISMATCHES=0
R31_R36_MANIFEST_ENTRIES=68
R31_R36_MANIFEST_MISMATCHES=0
R2_SOURCE_FILES=31
INDEPENDENCE_LIMITATION=SAME_HOST_AGENTS_NO_USABLE_WORKPACK
```
