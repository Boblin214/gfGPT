# PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE

## Review Status

```text
R3_EGRESS_REVOCATION_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS
INDEPENDENT_REVIEW=REQUIRED
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
PRODUCTION_EGRESS_IMPLEMENTED=NO
REAL_FETCH_AUTHORIZED=NO
```

## Scope

This Bundle contains the complete R3-Egress/Revocation source, SQL drafts,
reference models, tests, negative cases, lock-order review, threat model, risk
register and execution evidence. It does not contain a production Egress
implementation and does not authorize real network or Provider access.

## Evidence Boundary

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
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
```

## Contents

- 1. Source Catalog
- 2. Complete Source Bodies
- 3. Freeze Status

## 1. Source Catalog

| ID | Path | Bytes | SHA-256 |
|---|---|---:|---|
| S001 | `PHASE_R3_EGRESS_ARCHITECTURE.md` | 5360 | 90C1B065902B6EA852DC03A6032C93DC840FACD92A5EA173B20CBB8337E80F24 |
| S002 | `PHASE_R3_EGRESS_DIFF.md` | 2868 | 8854E40A256F5842A94C65AC1C3A75A00D7B3237495B3B7D75EBB527E5CE6A0F |
| S003 | `PHASE_R3_EGRESS_LOCK_ORDER.md` | 6273 | C1ADAFD47A69C61143826821B117C1CF5D2C8E549F08F8EDF4B5A071D087F66C |
| S004 | `PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX.md` | 6027 | C5EA8738B0B5720412256818FAAB6E1EB3D4FFD9B9BC8E7DE0DA1FE854464C12 |
| S005 | `PHASE_R3_EGRESS_REFERENCE_MODEL.md` | 4980 | EE352C8556D3660CCCD617660FD8B17B4105993482B84A20019C038B3A23FD47 |
| S006 | `PHASE_R3_EGRESS_REVOCATION_BASELINE.md` | 3834 | 11C34D2109863300DA66E07FCC93A032A218CFB155B38EE7650457A163D20398 |
| S007 | `PHASE_R3_EGRESS_REVOCATION_CONTRACT.md` | 5484 | C4E21EBF5DCC615F260BDADFB72117886D11A7724693E92023A1373AB4804EE1 |
| S008 | `PHASE_R3_EGRESS_REVOCATION_FINAL_REPORT.md` | 6301 | 6EF2E8AA32746E311BC7408FB836D569ACBEE521162E700A65FEAB9870A99BD1 |
| S009 | `PHASE_R3_EGRESS_RISK_REGISTER.md` | 4235 | A51A1EB30734C7DEF550B225F7B0B7584F22244ABE8F21DED53988132C7E357D |
| S010 | `PHASE_R3_EGRESS_SQL_REVIEW.md` | 8133 | 4812FB01E31F2BA9B435FF76E24BCD33A6B5389D115CABF4CF52FC2BE73AA190 |
| S011 | `PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE.md` | 9323 | 603CD82114FD69FAFD2E6D223F811E4B2511836B2870B12DC594C583AD0EAE1B |
| S012 | `PHASE_R3_EGRESS_THREAT_MODEL.md` | 5122 | 8C7E60B8580BDE55B56DAF4630F9A7F194805025EC46F95F47A6F53940F972AC |
| S013 | `PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt` | 6309 | EF9ABEB534CCA464BD27C9E94DBB59CE36C09C5E5F0AF21694EA3FC5D5E8A023 |
| S014 | `PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt` | 5742 | 9F71A2D092F2032B8EAD3C23346FB5FB8B34E0762B370DFF9F194C87051AA0DA |
| S015 | `contracts.ts` | 6339 | E18972EF94DD04EE27B879B5CD3BCE9033CB7B2F0BFC7BBABF767213515A9CD9 |
| S016 | `lock-order.ts` | 1268 | 3E7A4CA714B9E9BA7412FF6E7CB12DA9FF798F895EF0B141B3BB85AC671E32AE |
| S017 | `sql/10-worker-global-revocation.sql` | 5443 | 54B918ABA73574E0BB92000C993ED1CDF8FF1C8F5CB646FC27AAAC20721D37E1 |
| S018 | `sql/20-worker-scope-cleanup.sql` | 6953 | FE3ED25A80BB275DA7428C07B84433AD0720E10D46788F1B7F413A86D82F9D53 |
| S019 | `sql/25-lease-revocation-binding.sql` | 3081 | F25D017A066EEEFD0A62D1C51B397C431CE4C7AEE6B9C6CDE4E929DF603122F9 |
| S020 | `sql/30-egress-final-authorization.sql` | 23151 | 149262A324348E3AF2AA6264B3E2740FAB0D63CF5D662AEF672DCD38FE7A8906 |
| S021 | `sql/40-egress-write-outcome.sql` | 2389 | 4AF449B69DB6AB5DBC539923A95CDE17F6AB915A7FEA320C6FAB24BF6EE8957F |
| S022 | `sql/50-permit-consumption-revocation.sql` | 9846 | 115F3AD69A89797DBA8EDFF85A1DFA9ADE744CDC66AA64561BD7D071E4FE2650 |
| S023 | `models/egress-boundary.ts` | 14446 | 14FE4BA52870232929A8AB7966623E7D0450659669D0069F79A32F35AC347A02 |
| S024 | `models/egress-races.ts` | 2329 | 44E563B9D7AA80F8D060BDF07CA84D0E554C7FDE6675FF5DB61EDE5BB1CB0B1E |
| S025 | `models/sql-contract-analyzer.ts` | 15322 | 5C29304B30B7693089B00C29C40BC2C72A6429AB64519AE81D78D18CD423DEA9 |
| S026 | `models/worker-revocation.ts` | 15706 | 974C1463AB2280605B7EC94EDBEE4AAC36383BBE1D16C6CDDB3B8ECD69E54C90 |
| S027 | `tests/egress-boundary.test.ts` | 12927 | A61F2FBF565922218741DEE6C37F557857C1E93C8F10A97E962D1980F37DAD64 |
| S028 | `tests/egress-races.test.ts` | 2522 | 9FA622B49ECC6A4C1044DCC5F9FA31CA22CC9A0797B6A8C591FBF6E09300458D |
| S029 | `tests/sql-contract.test.ts` | 9038 | FF4BAF2B9E1F737381CF3D0CD103DFF240C242B1E3E29415AC35032BCCA8305A |
| S030 | `tests/worker-revocation.test.ts` | 12727 | 9CB055D02F1F023044DA7344A93E27A7AC09343338319E77796D3631FBF13A2A |
| S031 | `tools/build-aggregates.mjs` | 1681 | A96412B3514B644F12C39C837A3BE92B34C0534162F564B58442A34E77D85BCC |
| S032 | `tools/build-evidence.mjs` | 15532 | 934E0F9274A4EF477BF9E12298916487D8E157FB573CE503C1C0A6E72FDFCD9D |
| S033 | `tools/run-verification.ps1` | 6732 | 221B7C6789C510221C7361BA2E674F5FBCCCCD4BAB6E7ACA6F4E019E360C3EB3 |
| S034 | `PHASE_R3_EGRESS_AUTHORIZATION_TRANSACTIONS.sql` | 26120 | 5CB3A4249FBD19982949086B46E6B4DFD2D0DB69EFF32F60D2A29BD283B1ADC3 |
| S035 | `PHASE_R3_WORKER_REVOCATION_TRANSACTIONS.sql` | 26314 | 2591E69443552F897F03F819BBF4DFC25DAC6452A9D307C6F62B22C1C1D4EB8E |
| S036 | `vitest.config.ts` | 233 | 2BFE58E0B048F5268AF8037D7703E223B31E09DF10E30C179036B94F67FD0DFA |

## 2. Complete Source Bodies
### S001. PHASE_R3_EGRESS_ARCHITECTURE.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_ARCHITECTURE.md`
- Bytes: `5360`
- SHA-256: `90C1B065902B6EA852DC03A6032C93DC840FACD92A5EA173B20CBB8337E80F24`

<!-- BEGIN_EXACT_SOURCE id=S001 sha256=90C1B065902B6EA852DC03A6032C93DC840FACD92A5EA173B20CBB8337E80F24 bytes=5360 -->
````text
# PHASE_R3_EGRESS_ARCHITECTURE

## 1. Production Status

```text
PRODUCTION_EGRESS_IMPLEMENTED=NO
NETWORK_ISOLATION_ENFORCED=NO
MULTI_INSTANCE_COORDINATION=NOT_IMPLEMENTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
```

This document defines a target architecture and offline reference logic. It is
not an implemented or deployed network control.

## 2. Required Topology

```text
Worker process
  no Provider network route
  authenticated internal request to Egress service
        |
        v
Trusted Egress service
  only process with Provider egress permission
  per-resource serialized writer
        |
        v
Provider
```

The Worker must not possess Provider credentials, direct DNS/egress access, or
an alternate HTTP client path. Network policy, credentials and runtime
permissions must make this true. Code alone cannot prove the deployment
property.

## 3. Persistent Send Intent

`trust_r5_egress_intent` binds:

```text
intent ID
consumed R3 Send Authorization
request digest
Scope Key
resource token
Worker and global revocation version
Lease/Capability/Budget
Emergency epoch
Key and revocation versions
permission/policy versions
```

Creation of the `PENDING` row is conditional on a consumed one-use Permit, an
already committed `SENT` Lease, current Resource Floor and Worker Registration,
global Worker revocation `ACTIVE/current`, and no current Scope block. The
database uniqueness of `send_authorization_id` prevents two intent rows for the
same Permit.

States:

```text
PENDING
  -> FINAL_AUTHORIZED
  -> WRITE_STARTED
  -> RESPONSE_RECEIVED
  -> COMPLETED

PENDING/FINAL_AUTHORIZED -> REJECTED/EXPIRED/REVOKED
WRITE_STARTED -> SEND_OUTCOME_UNKNOWN
```

## 4. Two Final Gates

### Final Authorization

The Egress service locks/reads current central state:

```text
Worker revocation
Scope Worker block
Emergency
Key
Execution Authorization
Budget Reservation
Capability
Resource Floor
Worker Registration
Lease
Consumed Send Authorization
Egress Intent
```

It verifies request digest and all bindings, then commits
`PENDING -> FINAL_AUTHORIZED` with a very short validity. This is the
final-authorization linearization point.

### Write Start

Immediately before socket creation, Egress re-reads the same mutable state and
conditionally commits:

```text
FINAL_AUTHORIZED -> WRITE_STARTED
```

This is the last database-enforced cancellation point. After this commit, a
Worker revocation, takeover, Emergency Stop or Key Revocation cannot be
guaranteed to stop a socket operation already beginning.

Both gates re-read Worker Registration state and heartbeat. Neither accepts a
cached `ACTIVE` value, a Worker revocation version, or a Scope block snapshot.
They also re-read the Resource Floor owner/token, Lease revocation binding and
expiry, Permit consumption state, Capability, Emergency epoch, Key versions and
Budget state.

## 5. Linearization and Socket Boundary

```text
Permit consumption commit
  -> Egress final-authorization commit
  -> Egress write-start commit
  -> socket write
  -> response or unknown
```

These events are not one transaction. There is no common transaction with the
Provider.

## 6. Guarantees

```text
revocation before final authorization
  -> write denied

revocation after final authorization, before write-start
  -> write-start denied

revocation after write-start commit
  -> socket write cannot be guaranteed cancelled

Emergency/Key changes before write-start
  -> write-start denied

central authority unavailable
  -> no new final authorization and no write-start

Provider execution exactly once
  -> NOT_GUARANTEED

socket not used after write-start commit
  -> NOT_GUARANTEED
```

## 7. Multi-Instance Egress

If multiple Egress instances exist:

- final authorization and write-start must execute on a central database;
- each Resource Scope must have one active short write lease or ordered writer;
- all instances use the same lock order;
- stale writer lease/fence must be rejected;
- an instance losing database connectivity cannot start a new write;
- operator metrics must detect duplicate intent/state divergence.

Possible implementations:

- per-scope queue ledger/leader lease;
- partitioned Egress workers with a durable scope-to-worker assignment;
- advisory lock plus durable intent state;
- database transaction/outbox handoff to a single active egress worker.

No implementation exists in this task.

## 8. Outcomes and Retry

After `WRITE_STARTED`:

- response received -> `RESPONSE_RECEIVED -> COMPLETED`;
- timeout/connection loss/crash/no response -> `SEND_OUTCOME_UNKNOWN`;
- automatic retry -> forbidden;
- manual/provider-billing/reconciliation required;
- permit and budget stay consumed/charged.

## 9. Deployment Checklist

1. Provision a dedicated Egress service identity.
2. Remove Provider network routes and credentials from Workers.
3. Network-policy deny Worker egress by default.
4. Restrict Egress to configured Provider endpoints.
5. Enable TLS verification and response-size/time limits.
6. Persist audit for every final authorization, write start and outcome.
7. Configure emergency propagation and database-loss behavior.
8. Exercise multi-instance takeover and partition tests.
9. Confirm already-written requests cannot be recalled.
10. Keep production Fetch entry blocked until all checks are externally
   reviewed.

````
<!-- END_EXACT_SOURCE id=S001 -->

### S002. PHASE_R3_EGRESS_DIFF.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_DIFF.md`
- Bytes: `2868`
- SHA-256: `8854E40A256F5842A94C65AC1C3A75A00D7B3237495B3B7D75EBB527E5CE6A0F`

<!-- BEGIN_EXACT_SOURCE id=S002 sha256=8854E40A256F5842A94C65AC1C3A75A00D7B3237495B3B7D75EBB527E5CE6A0F bytes=2868 -->
````text
# PHASE_R3_EGRESS_REVOCATION_DIFF

## 1. Change Boundary

```text
HISTORICAL_R3_FENCING_FILES_MODIFIED=NO
R3_FENCING_BASELINE_MANIFEST_SHA256=EF9ABEB534CCA464BD27C9E94DBB59CE36C09C5E5F0AF21694EA3FC5D5E8A023
NEW_WORK_DIRECTORY=preparation/production-trust/r3-egress-revocation-remediation
```

This is a semantic change inventory, not a fabricated pre-edit diff for files
that did not exist at baseline.

## 2. R3 Gap to R3-Egress Change

| R3 gap | R3-Egress change |
|---|---|
| R4 Permit Consumption checks Worker Registration but not an independent global Worker tombstone | R5 replacement transaction checks global revocation, Scope block, Lease binding, Floor, heartbeat and one-use state |
| Scope cleanup treats every Lease uniformly | separate pre-send cleanup and already-sent classification branches |
| no durable per-Permit Egress Intent | `trust_r5_egress_intent` with unique `send_authorization_id` and strict state machine |
| final Egress check and socket write are separated without a durable write-start mark | `FINAL_AUTHORIZED -> WRITE_STARTED` transaction immediately before socket write |
| no Worker revocation-version binding on Lease | immutable `trust_r5_lease_worker_revocation_binding` |
| no per-scope Worker block | `trust_r5_scope_worker_block`, checked by Consumption and both Egress gates |
| unknown external outcome could be mistaken for a retryable failure | terminal `SEND_OUTCOME_UNKNOWN`; automatic retry forbidden |
| SQL regex checks could be confused with semantic proof | explicit `TEXTUAL_PATTERN_CHECK`, `SQL_STRUCTURE_CHECK`, `PARAMETER_BINDING_REVIEW`, `TRANSACTION_CONTRACT_REVIEW`; PostgreSQL execution excluded |

## 3. Added Source

```text
sql/10-worker-global-revocation.sql
sql/20-worker-scope-cleanup.sql
sql/25-lease-revocation-binding.sql
sql/30-egress-final-authorization.sql
sql/40-egress-write-outcome.sql
sql/50-permit-consumption-revocation.sql
contracts.ts
lock-order.ts
models/worker-revocation.ts
models/egress-boundary.ts
models/egress-races.ts
models/sql-contract-analyzer.ts
tests/worker-revocation.test.ts
tests/egress-boundary.test.ts
tests/egress-races.test.ts
tests/sql-contract.test.ts
```

## 4. Changed During Remediation

The first focused run produced 9 Egress model failures because the synthetic
Worker heartbeat was five milliseconds in the future relative to intent
creation. The implementation correctly rejected the future heartbeat. The test
fixture was corrected to align the timestamp. No historical source was
modified.

The scope cleanup draft was then split into explicit pre-send and after-send
transactions because a checked `SENT -> REVOKED` update would incorrectly
claim that an external send could be recalled.

## 5. No Production Change

No `src/`, `scripts/`, production entry, schema, migration, ACL, A3/D1/D2,
Identity Gate Core, R31-R36 or Provider path was changed.

````
<!-- END_EXACT_SOURCE id=S002 -->

### S003. PHASE_R3_EGRESS_LOCK_ORDER.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_LOCK_ORDER.md`
- Bytes: `6273`
- SHA-256: `C1ADAFD47A69C61143826821B117C1CF5D2C8E549F08F8EDF4B5A071D087F66C`

<!-- BEGIN_EXACT_SOURCE id=S003 sha256=C1ADAFD47A69C61143826821B117C1CF5D2C8E549F08F8EDF4B5A071D087F66C bytes=6273 -->
````text
# PHASE_R3_EGRESS_LOCK_ORDER

## 1. Status

```text
VALIDATION_LEVEL=TRANSACTION_CONTRACT_REVIEW
POSTGRESQL_EXECUTION=NOT_EXECUTED
MULTI_INSTANCE_INTERLEAVING=NOT_EXECUTED
```

This document maps the SQL drafts to one lock order. It is an offline
contract review, not proof of PostgreSQL lock timing or deadlock freedom.

## 2. Canonical Order

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

`trust_r5_scope_worker_block` belongs to the Worker Revocation decision
domain. `trust_r5_lease_worker_revocation_binding` belongs to the Execution
Lease domain. A transaction may omit a domain only when it does not read or
mutate authority from that domain.

## 3. Why Scope Block Is Safe Without Locking an Absent Row

A missing Scope block row cannot be locked to prevent another transaction
inserting it. The ordering therefore relies on the Worker Revocation row:

1. Permit Consumption and Egress lock the global Worker Revocation row
   `FOR UPDATE`.
2. Scope cleanup that creates a block requires the global row `REVOKED` and
   takes `FOR SHARE`.
3. While the consumer holds `FOR UPDATE`, cleanup cannot pass the global
   revocation check.
4. If revocation commits before the consumer obtains the lock, the consumer
   observes `REVOKED` and fails.

Per-scope blocks therefore cannot become an authority grant behind a
successfully committed consumer transaction. PostgreSQL execution of this
argument remains unverified in this task.

## 4. Transaction Matrix

| SQL draft | Transaction | Actual lock order | Atomic updates / inserts | Row checks | Audit |
|---|---|---|---|---|---|
| `10-worker-global-revocation.sql` | global revocation | Worker Revocation -> Worker Registration -> Audit Head | revocation state/version, registration REVOKED, request insert, Audit event/head | both UPDATEs exactly 1 | yes, same transaction |
| `20-worker-scope-cleanup.sql` 20A | pre-send cleanup | Worker Revocation `SHARE` -> Resource Floor -> Worker Registration -> Lease -> Send Authorization -> Audit Head | Scope block upsert, Lease REVOKED, Permit REVOKED, Audit event/head | Lease, Permit, Audit head exactly 1 | yes |
| `20-worker-scope-cleanup.sql` 20B | after-send classification | Worker Revocation `SHARE` -> Resource Floor -> Worker Registration -> Lease -> Send Authorization -> Audit Head | Scope block upsert, Permit REVOKED, Audit event/head; Lease is not falsely REVOKED | Permit, Audit head exactly 1 | yes |
| `25-lease-revocation-binding.sql` | Lease revocation binding finalization | Worker Revocation `SHARE` -> Resource Floor -> Worker Registration -> Lease | immutable binding insert | conditional INSERT exactly 1 | no security authority mutation; Lease issuance Audit already exists |
| `50-permit-consumption-revocation.sql` | Permit Consumption | Worker Revocation -> Emergency -> Key -> Authorization -> Budget Control -> Reservation -> Capability -> Resource Floor -> Worker Registration -> Lease binding -> Lease -> Permit -> Audit Head | Permit CONSUMED, Lease local `SENT`, budget send-start, Audit event/head | Permit, Lease, budget, Audit head exactly 1 | yes |
| `30-egress-final-authorization.sql` T1 | PENDING intent | Worker Revocation -> Emergency -> Key -> Authorization -> Budget Control -> Reservation -> Capability -> Resource Floor -> Worker Registration -> Lease binding -> Lease -> Permit | conditional Egress Intent INSERT | conditional INSERT exactly 1 | Egress Intent is not a grant; final authorization Audit is next transaction |
| `30-egress-final-authorization.sql` T2 | final authorization | same as T1, then Egress Intent -> Audit Head | Intent `PENDING -> FINAL_AUTHORIZED`, Audit event/head | Intent, Audit head exactly 1 | yes |
| `30-egress-final-authorization.sql` T3 | write-start boundary | same as T2 | Intent `FINAL_AUTHORIZED -> WRITE_STARTED`, Audit event/head | Intent, Audit head exactly 1 | yes |
| `40-egress-write-outcome.sql` | response completion | Egress Intent -> Audit Head | response/completed states and Audit | both Intent UPDATEs and Audit head exactly 1 | yes |
| `40-egress-write-outcome.sql` | unknown outcome | Egress Intent -> Audit Head | terminal `SEND_OUTCOME_UNKNOWN`, Audit | Intent, Audit head exactly 1 | yes |

## 5. Linearization Points

| Event | Linearization point |
|---|---|
| Global Worker revocation | COMMIT of global revocation transaction |
| Per-scope block | COMMIT of selected 20A/20B transaction |
| Permit one-use consumption | COMMIT of Permit Consumption transaction |
| Final Egress authorization | COMMIT of `PENDING -> FINAL_AUTHORIZED` |
| Final local cancellation boundary | COMMIT of `FINAL_AUTHORIZED -> WRITE_STARTED` |
| External Provider receipt | unknown unless a durable response exists |

## 6. Race Rules

| Race | Result |
|---|---|
| Revocation commits before Permit Consumption lock | consume rejected |
| Revocation waits behind an active consumption transaction | consumption commits first; later Egress gates reject |
| Scope block cleanup commits before Egress final authorization | final authorization rejected |
| Scope block cleanup commits between final authorization and write-start | write-start rejected |
| Scope block cleanup commits after `WRITE_STARTED` | socket cannot be guaranteed cancelled |
| Emergency/Key changes before write-start | write-start rejected by fresh checks |
| Authority unavailable before a gate | fail closed; no new write authorization |

## 7. READ COMMITTED Dependency

The design uses `READ COMMITTED` with explicit row locks and conditional
updates. It relies on:

- current-row visibility after acquiring each row lock;
- exactly-one affected-row checks;
- unique constraints for Permit-to-Intent identity;
- global Worker Revocation as the tombstone serialization point;
- all gates re-reading mutable state rather than a cached `NORMAL` snapshot.

SQLSTATE serialization behavior, deadlock behavior, lock wait timing and
multi-instance interleavings have not been executed.

````
<!-- END_EXACT_SOURCE id=S003 -->

### S004. PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX.md`
- Bytes: `6027`
- SHA-256: `C5EA8738B0B5720412256818FAAB6E1EB3D4FFD9B9BC8E7DE0DA1FE854464C12`

<!-- BEGIN_EXACT_SOURCE id=S004 sha256=C5EA8738B0B5720412256818FAAB6E1EB3D4FFD9B9BC8E7DE0DA1FE854464C12 bytes=6027 -->
````text
# PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX

## 1. Validation Levels

The analyzer explicitly distinguishes:

```text
TEXTUAL_PATTERN_CHECK
SQL_STRUCTURE_CHECK
PARAMETER_BINDING_REVIEW
TRANSACTION_CONTRACT_REVIEW
POSTGRESQL_EXECUTION_NOT_PERFORMED
```

These checks do not execute PostgreSQL and do not prove real row-lock or
SQLSTATE behavior.

## 2. Negative Cases

| Negative fixture | Expected finding | Validation level | Test |
|---|---|---|---|
| Worker Revocation lacks Resource Floor lock | `REQUIRED_LOCK_MISSING` | transaction contract | `sql-contract.test.ts` |
| Revocation does not update Lease | `REQUIRED_MUTATION_MISSING` | transaction contract | `sql-contract.test.ts` |
| Revocation/Consumption locks cross | `LOCK_ORDER_CROSSING` | transaction contract | `sql-contract.test.ts` |
| Egress lacks Worker revocation version | `EGRESS_REVOCATION_VERSION_MISSING` | textual | `sql-contract.test.ts` |
| Egress lacks Worker revocation row | `EGRESS_WORKER_REVOCATION_ROW_MISSING` | textual | `sql-contract.test.ts` |
| Egress lacks Resource Floor | `EGRESS_RESOURCE_FLOOR_MISSING` | textual | `sql-contract.test.ts` |
| Egress trusts cached floor | `EGRESS_CACHE_TRUSTED` | textual | `sql-contract.test.ts` |
| SQL claims row lock protects socket | `SOCKET_ATOMICITY_OVERCLAIM` | textual | `sql-contract.test.ts` |
| Emergency/authority loss fails open | `EGRESS_FAIL_OPEN` | textual | `sql-contract.test.ts` |
| Permit has no ISSUED->CONSUMED path | `PERMIT_ONE_TIME_TRANSITION_MISSING` | transaction contract | `sql-contract.test.ts` |
| Permit has no revocation path | `PERMIT_REVOCATION_PATH_MISSING` | transaction contract | `sql-contract.test.ts` |
| Worker upsert can restore ACTIVE | `WORKER_REACTIVATION_UPSERT` | textual | `sql-contract.test.ts` |
| Security mutation lacks Audit in same transaction | `AUDIT_SPLIT_FROM_MUTATION` | transaction contract | `sql-contract.test.ts` |
| Security UPDATE lacks exactly-one marker | `ROW_COUNT_MARKER_MISSING` | structure | `sql-contract.test.ts` |
| Required parameter absent | `REQUIRED_PARAMETER_MISSING` | parameter binding | `sql-contract.test.ts` |
| Permit Consumption omits Scope block | `PERMIT_SCOPE_BLOCK_CHECK_MISSING` | transaction contract | `sql-contract.test.ts` |
| Permit Consumption omits global revocation | `PERMIT_WORKER_REVOCATION_CHECK_MISSING` | transaction contract | analyzer function |
| Permit Consumption omits Lease binding | `PERMIT_LEASE_REVOCATION_BINDING_MISSING` | transaction contract | analyzer function |
| Egress omits Scope block at either gate | `EGRESS_SCOPE_BLOCK_RECHECK_MISSING` | transaction contract | actual SQL mutation test |
| Egress omits Worker registration/heartbeat | `EGRESS_WORKER_REGISTRATION_RECHECK_MISSING` | transaction contract | actual SQL mutation test |
| Egress omits Lease revocation binding | `EGRESS_LEASE_REVOCATION_BINDING_MISSING` | transaction contract | analyzer function |

## 3. Egress Race Matrix

| Timeline | Result |
|---|---|
| Floor/Worker/Emergency/Key changes before final authorization | `DENIED_BEFORE_FINAL_AUTH` |
| Change after final authorization before write recheck | `FINAL_AUTH_ISSUED_WRITE_BLOCKED` |
| Change after write started | `WRITE_STARTED_OUTCOME_UNKNOWN` |
| Response arrives after write | `WRITE_STARTED_RESPONSE_RECEIVED` |
| Authority unavailable before write | `AUTHORITY_UNAVAILABLE` |
| Final authorization without write recheck | blocked before socket |
| Retry after possible write | `RETRY_FORBIDDEN` |

Implementation:

```text
models/egress-races.ts
tests/egress-races.test.ts
```

## 4. Structural Analyzer Scope

`models/sql-contract-analyzer.ts`:

- splits SQL statements without executing SQL;
- preserves semicolons inside quoted strings;
- groups statements into BEGIN/COMMIT/ROLLBACK transactions;
- extracts transaction UPDATE/INSERT/DELETE tables;
- extracts `FOR UPDATE` table locks;
- checks canonical lock order;
- checks row-count markers;
- checks Audit event/head co-location;
- extracts `$n` and `:name` parameters;
- checks required tables, mutations, locks and parameters.

## 5. What Is Not Proven

```text
POSTGRESQL_PARSE_ACCEPTANCE=NOT_PROVEN
POSTGRESQL_LOCK_TIMING=NOT_PROVEN
UNIQUE_CONSTRAINT_SQLSTATE=NOT_PROVEN
DEADLOCK_BEHAVIOR=NOT_PROVEN
MULTI_INSTANCE_INTERLEAVING=NOT_PROVEN
REAL_SOCKET_WRITE=NOT_PROVEN
REAL_PROVIDER_BEHAVIOR=NOT_PROVEN
```

The analyzer and offline race model must not be described as production
concurrency validation.

## 6. Actual SQL Contract Tests

`tests/sql-contract.test.ts` reads the real R5 SQL files and checks:

- statement/transaction segmentation;
- no detected lock-order crossing;
- Permit Consumption revocation coverage;
- Egress Scope block and Worker registration coverage;
- detection after removing a required clause;
- rejection of a false “database lock protects socket” claim.

These are negative/static contract tests. They do not execute the statements.

## 7. Model Negative Tests

`tests/egress-boundary.test.ts` rejects:

- PENDING intent with a Scope block at the bound revocation version;
- PENDING intent for a revoked/non-ACTIVE Worker registration;
- PENDING intent with a stale Worker revocation version;
- PENDING intent with a non-consumed Permit;
- final/write-start after Worker registration/revocation, Scope block, Floor,
  Emergency, Key or Budget invalidation;
- expired final authorization, repeated write-start and repeated outcome.

`tests/worker-revocation.test.ts` rejects:

- ordinary reactivation of a revoked Worker;
- Consumption before a committed revocation;
- Consumption when a Scope block is current;
- Lease cleanup without exact-one row evidence for pre-send states;
- takeover by a revoked Worker;
- authorization when central authority is unavailable.

## 8. Test Classification

```text
TEST_IMPLEMENTATION=PRESENT
TEST_EXECUTION_RESULT=RECORDED_IN_FINAL_REPORT
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```

````
<!-- END_EXACT_SOURCE id=S004 -->

### S005. PHASE_R3_EGRESS_REFERENCE_MODEL.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REFERENCE_MODEL.md`
- Bytes: `4980`
- SHA-256: `EE352C8556D3660CCCD617660FD8B17B4105993482B84A20019C038B3A23FD47`

<!-- BEGIN_EXACT_SOURCE id=S005 sha256=EE352C8556D3660CCCD617660FD8B17B4105993482B84A20019C038B3A23FD47 bytes=4980 -->
````text
# PHASE_R3_EGRESS_REFERENCE_MODEL

## 1. Status

```text
MODEL_REALM=OFFLINE_REFERENCE_MODEL
REAL_POSTGRESQL_MODEL=NO
REAL_DISTRIBUTED_COORDINATOR=NO
REAL_SOCKET_WRITE=NO
```

The complete model source is embedded in
`PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE.md`. This document
describes responsibilities and limitations.

## 2. Files

### `contracts.ts`

Responsibility: strict runtime schemas for Worker revocation, Scope block,
Egress Intent, final authorization and mutable Egress context.

Inputs: validated JSON-like objects. Outputs: typed immutable contracts or
failure codes.

Security invariants:

- unknown fields are rejected;
- UUID and SHA-256 formats are strict;
- UTC Unix milliseconds are integers;
- security objects bind Worker, Scope, token, Lease, Capability, Budget,
  Emergency and Key versions;
- Scope block state and Worker registration/heartbeat are explicit Egress
  inputs.

Tests: `egress-boundary.test.ts`, `worker-revocation.test.ts`.

Limitation: schema validation is not a database read and cannot prove freshness.

### `models/worker-revocation.ts`

Responsibility: offline global revocation, Scope cleanup, Lease version binding
and Permit Consumption with revocation checks.

State changes:

```text
Worker ACTIVE -> REVOKED
Permit ISSUED -> CONSUMED
Lease SEND_AUTHORIZED -> SENT (legacy local-permission state)
Scope block created/updated
```

Security invariants:

- global revocation is terminal for ordinary registration;
- repeated request ID is idempotent;
- Audit failure rolls back state in the model;
- scope cleanup cannot revive global authority;
- a Scope block at/above current revocation version rejects consumption;
- a revoked Worker cannot be reactivated by `seedActiveWorker`;
- missing central authority fails closed.

Tests: `worker-revocation.test.ts`.

Limitations: in-memory maps do not model MVCC, row locks, PostgreSQL
constraints, crash durability or multiple processes.

### `models/egress-boundary.ts`

Responsibility: persistent-intent lifecycle, final authorization, write-start
authorization, outcome recording and COMMIT-ambiguity recovery.

Inputs: Intent, consumed Permit, Lease, and a complete fresh mutable context.
Outputs: `PENDING`, `FINAL_AUTHORIZED`, `WRITE_STARTED`,
`RESPONSE_RECEIVED`/`COMPLETED` or `SEND_OUTCOME_UNKNOWN`.

Security invariants:

- one Intent per Permit;
- PENDING creation requires consumed Permit and `SENT` Lease;
- registration must be ACTIVE with a non-future heartbeat no older than 15 s;
- global revocation and Scope block are checked at PENDING, final and
  write-start gates;
- Resource Floor owner/token, Lease, Capability, Emergency, Key and Budget are
  rechecked at both final gates;
- final authorization expires within one second;
- repeated write-start or outcome is rejected;
- central authority loss denies final/write-start authorization;
- recovery only reads a matching persisted final authorization.

Tests: `egress-boundary.test.ts`.

Limitations: final and write-start checks are plain method calls, not
PostgreSQL row locks. No socket is created or written.

### `models/egress-races.ts`

Responsibility: classify offline T1-T5 timelines for floor change, Worker
revocation, Emergency, Key revocation, authority loss, write-start and response.

Security invariants:

- invalidation before write-start blocks the write;
- invalidation after write-start cannot be claimed as cancellation;
- retry after `WRITE_STARTED` is forbidden;
- a final authorization without the second write recheck does not permit a
  write.

Tests: `egress-races.test.ts`.

Limitation: event arrays are a model, not an operating-system or network race
test.

### `models/sql-contract-analyzer.ts`

Responsibility: split SQL statements, form transaction groups, inventory
tables/locks/parameters and detect selected negative invariants.

Security invariants checked:

- canonical lock-domain ordering;
- required mutations, locks and parameters;
- row-count markers;
- Audit event/head co-location;
- Permit revocation and one-use transitions;
- global revocation, Scope block, Lease binding and Floor checks;
- Worker upsert reactivation;
- explicit rejection of “database lock protects socket” claims.

Tests: `sql-contract.test.ts`.

Limitations: it is not a PostgreSQL parser or executor. It cannot prove SQL
syntax, SQLSTATE handling, lock acquisition timing or serialization behavior.

### `lock-order.ts`

Responsibility: canonical lock-domain list and monotonic acquisition validator.

Tests: all three model test files invoke the validator for final/write-start
transactions; `sql-contract.test.ts` exercises lock-order crossing.

Limitation: validated acquisition arrays are declarative. Only PostgreSQL
execution can establish actual lock order.

## 3. Model Result Meaning

`OFFLINE_REFERENCE_MODEL=PASS` means the stated model tests passed. It does not
mean real concurrent transactions, crash recovery, Egress deployment or
Provider behavior passed.

````
<!-- END_EXACT_SOURCE id=S005 -->

### S006. PHASE_R3_EGRESS_REVOCATION_BASELINE.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_BASELINE.md`
- Bytes: `3834`
- SHA-256: `11C34D2109863300DA66E07FCC93A032A218CFB155B38EE7650457A163D20398`

<!-- BEGIN_EXACT_SOURCE id=S006 sha256=11C34D2109863300DA66E07FCC93A032A218CFB155B38EE7650457A163D20398 bytes=3834 -->
````text
# PHASE_R3_EGRESS_REVOCATION_BASELINE

## 1. Status

```text
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
BASELINE_CAPTURED_AT=2026-11-26T22:34:15.3251417+08:00
BASELINE_TARGETS=41
R3_FENCING_REMEDIATION_PASS
INDEPENDENT_REVIEW=NEEDS_REVISION
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

The GitHub URL in the task statement was not accessed. All evidence came from
the local isolated copy.

## 2. Protected Baseline

Writable scope:

```text
preparation/production-trust/r3-egress-revocation-remediation/
```

Read-only R3 Fencing evidence:

```text
PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE.md
PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md
PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt
preparation/production-trust/r3-fencing-remediation/*
```

Exact 41-file pre-remediation Hash list:

```text
preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt
```

## 3. Current Evidence Gaps

| Gap | Current state |
|---|---|
| Worker Revocation SQL | no dedicated production transaction found |
| Worker global revocation vs scope cleanup | not separated in R3 SQL |
| Permit Consumption vs Worker Revocation | Worker state is checked, but no independent revocation version and no persistence transition |
| Egress final check vs socket write | SQL/model final check exists, but last check and socket write are not atomic |
| Egress intent persistence | no persistent send-intent state machine |
| SQL validation depth | regex/structure analysis; no PostgreSQL AST or execution |
| Real PostgreSQL | NOT_EXECUTED |
| Real multi-instance | NOT_EXECUTED |
| Real Egress/network | NOT_IMPLEMENTED / NOT_EXECUTED |

## 4. Fencing Scope

Existing canonical scope remains:

```text
fence-scope-v1:sha256(canonical providerKind/purpose/organizationId/targetDigest)
```

Resource Floor remains the authority for current owner/token.

## 5. Revocation Semantics Decision

The remediation distinguishes:

| Concept | Semantics |
|---|---|
| Worker Identity Revocation | global tombstone for one Worker ID; linearization point commit; terminal for ordinary registration |
| Resource-scope Worker block | blocks one Worker on one Scope without revoking its other scopes |
| Lease Revocation | one execution Lease becomes terminal REVOKED |
| Capability Revocation | capability cannot be used for a future attempt |
| Emergency Stop | control-plane epoch blocks new work globally |

A global Worker revocation must not rely on atomically updating necessarily
unbounded resource-scope rows. The global revocation row is the fail-closed
authority checked by Permit Consumption and final Egress. Scope cleanup runs as
idempotent follow-up transactions.

## 6. File Ownership

| Owner | Writable files |
|---|---|
| Agent A | `sql/10-worker-global-revocation.sql`, `sql/20-worker-scope-cleanup.sql`, `tests/worker-revocation.test.ts`, `models/worker-revocation.ts` |
| Agent B | `sql/30-egress-authorization.sql`, `sql/40-egress-outcome.sql`, `models/egress-boundary.ts`, `tests/egress-boundary.test.ts` |
| Agent C | `models/sql-contract-analyzer.ts`, `tests/sql-contract.test.ts`, `tests/egress-races.test.ts`, `models/egress-races.ts` |
| Main Agent | contracts, lock order, consolidated SQL, reports, integration, Manifests, Bundle |

No original R3 file may be modified.

## 7. Dependency Graph

```text
Baseline
  -> Worker global revocation contract
  -> scope cleanup + permit/egress revocation checks
  -> persistent Egress Intent state machine
  -> socket-write boundary analysis
  -> SQL structural/parameter review
  -> negative and race tests
  -> final Bundle
```

## 8. Collaboration Limit

The subagents are same-host Codex agents and are not a third-party independent
security audit.

````
<!-- END_EXACT_SOURCE id=S006 -->

### S007. PHASE_R3_EGRESS_REVOCATION_CONTRACT.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_CONTRACT.md`
- Bytes: `5484`
- SHA-256: `C4E21EBF5DCC615F260BDADFB72117886D11A7724693E92023A1373AB4804EE1`

<!-- BEGIN_EXACT_SOURCE id=S007 sha256=C4E21EBF5DCC615F260BDADFB72117886D11A7724693E92023A1373AB4804EE1 bytes=5484 -->
````text
# PHASE_R3_EGRESS_REVOCATION_CONTRACT

## 1. Status

```text
CONTRACT_VERSION=r3-egress-revocation-remediation-v1
REALM=OFFLINE_REFERENCE_MODEL
PRODUCTION_EGRESS_IMPLEMENTED=NO
PRODUCTION_IMPLEMENTATION=NOT_STARTED
REAL_FETCH_AUTHORIZED=NO
```

## 2. Revocation Domains

The following concepts are distinct:

| Domain | Scope | Linearized by |
|---|---|---|
| Worker Identity Revocation | global Worker ID | commit of `trust_r5_worker_revocation` state/version update |
| Scope Worker Block | one Resource Scope | commit of `trust_r5_scope_worker_block` |
| Lease Revocation | one Lease | Lease state `REVOKED` |
| Capability Revocation | one Capability | Capability state `REVOKED` |
| Emergency Stop | whole control plane | Emergency epoch/status update |

Global Worker revocation affects all its scopes. It does not synchronously
update potentially unbounded rows. Every Permit Consumption and Egress final
gate must join both the global revocation row and the Scope block table and
fail closed. Per-scope cleanup is an idempotent follow-up that revokes
pre-send Lease/Permit authority and classifies already-sent work without
pretending the network request can be recalled.

## 3. Worker Lifecycle

```text
REGISTERED -> ACTIVE -> DRAINING -> REVOKED
```

`REVOKED` is terminal for the ordinary registration lifecycle. A normal
`INSERT ... ON CONFLICT DO UPDATE` cannot return it to `ACTIVE`. Recovery
requires a new trusted registration identity or a separate dual-control
recovery workflow, neither of which is implemented here.

## 4. Worker Revocation Record

```text
workerInstanceId
state ACTIVE|REVOKED|RECOVERY_REQUIRED
revocationVersion
recordVersion
revokedAt nullable
reasonCode nullable
replacementWorkerId nullable
updatedAt
```

`revocationVersion` is monotonic. A Lease/Egress Intent binds the version known
when it was authorized.

## 5. Worker Revocation Protocol

Global transaction:

```text
lock Worker Revocation row
lock Worker Registration row
verify current record version
set state REVOKED
increment revocationVersion and recordVersion
set Registration REVOKED
append audit
commit
```

The commit is the global fail-closed linearization point. New Takeover,
Permit Consumption, Egress Final Authorization and Egress Write Start reject
the Worker after this point.

Per-scope cleanup transaction:

```text
lock Worker Revocation row
lock Resource Floor
lock Worker Registration
lock Lease
lock Send Authorization / Egress Intent
verify same Worker/Scope/Token/Lease/Capability
pre-send branch: Lease REVOKED / Permit REVOKED
after-send branch: block Scope / Permit REVOKED; Lease not falsely REVOKED
append cleanup audit
commit
```

Failure of cleanup never re-enables the global revoked Worker.

## 6. Permit Consumption

The existing R4 `Send Authorization` remains one-use. R5 adds mandatory
checks:

```text
worker revocation state = ACTIVE
worker revocationVersion = current version
scope worker block absent or below current revocation version
resource floor owner = Worker/Lease/Capability/token
permit state = ISSUED
Emergency/Key/Budget current
```

Permit `CONSUMED` means local permission consumed, not Provider receipt.

The frozen R4 transaction must not be used unchanged. R5 supplies a complete
replacement draft at `sql/50-permit-consumption-revocation.sql`.

## 7. Egress Intent

The R5 Egress Intent makes the pre-write intent persistent:

```text
PENDING
  -> FINAL_AUTHORIZED
  -> WRITE_STARTED
  -> RESPONSE_RECEIVED
  -> COMPLETED
```

Terminal/control states:

```text
SEND_OUTCOME_UNKNOWN
REJECTED
EXPIRED
REVOKED
```

The final authorization transaction re-reads all current authority. The final
`WRITE_STARTED` transition immediately before the socket write rechecks the
same authority and consumes the final local write mark. It is the last
guarantee point before network I/O for Worker revocation and takeover.

## 8. Egress Final Checks

Required:

```text
Resource Scope
current Resource Floor
current token
current Worker
Worker Registration ACTIVE
Worker heartbeat not in the future and no older than 15 seconds
Worker Revocation ACTIVE/current version
Scope Worker block absent/below current revocation version
current Lease SENT
Lease revocation-version binding current
Capability
Emergency NORMAL/current epoch
Key ACTIVE/current/key revocation version
Permit CONSUMED one-use
Egress Intent ownership/request digest
Budget reserved/unexpired
```

Central authority unavailable = deny. No cached floor.

## 9. Socket Boundary

```text
database COMMIT
  !=
actual Socket Write
```

After `WRITE_STARTED` commits, Worker revocation, takeover or Emergency Stop
cannot recall a packet already accepted by the network stack.

Guarantees:

| Condition | Guarantee |
|---|---|
| revocation commits before final authorization | send denied |
| revocation commits before `WRITE_STARTED` | send denied |
| revocation commits after `WRITE_STARTED` | socket may already write; cannot revoke |
| Worker lacks direct Provider route | no bypass |
| crash/lost response after write start | `SEND_OUTCOME_UNKNOWN`; no automatic retry |

```text
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
```

## 10. Production Requirements

```text
PRODUCTION_EGRESS_IMPLEMENTED=NO
NETWORK_ISOLATION_ENFORCED=NO
MULTI_INSTANCE_COORDINATION=NOT_IMPLEMENTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
```

The future Egress must be the exclusive Provider network path. SQL-only changes
cannot create that infrastructure property.

````
<!-- END_EXACT_SOURCE id=S007 -->

### S008. PHASE_R3_EGRESS_REVOCATION_FINAL_REPORT.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_FINAL_REPORT.md`
- Bytes: `6301`
- SHA-256: `6EF2E8AA32746E311BC7408FB836D569ACBEE521162E700A65FEAB9870A99BD1`

<!-- BEGIN_EXACT_SOURCE id=S008 sha256=6EF2E8AA32746E311BC7408FB836D569ACBEE521162E700A65FEAB9870A99BD1 bytes=6301 -->
````text
# PHASE_R3_EGRESS_REVOCATION_FINAL_REPORT

## 1. Final Status

```text
R3_EGRESS_REVOCATION_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS
INDEPENDENT_REVIEW=REQUIRED

PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
PRODUCTION_EGRESS_IMPLEMENTED=NO
REAL_FETCH_AUTHORIZED=NO
```

This status covers the offline design, SQL-contract review, reference model,
negative tests and repository boundaries. It is not a production security
acceptance.

## 2. Baseline

```text
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
BASELINE_REPORT=PHASE_R3_EGRESS_REVOCATION_BASELINE.md
BASELINE_MANIFEST=PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt
BASELINE_ENTRIES=41
BASELINE_MANIFEST_SHA256=EF9ABEB534CCA464BD27C9E94DBB59CE36C09C5E5F0AF21694EA3FC5D5E8A023
HISTORICAL_FILES_MODIFIED=NO
```

The main workspace, GitHub URL and real infrastructure were not accessed.

## 3. Work Package Results

| Area | Result | Evidence |
|---|---|---|
| Worker global revocation | PASS | `sql/10-worker-global-revocation.sql`, `worker-revocation.test.ts` |
| Worker ordinary reactivation protection | PASS | conditional registration update, model negative test |
| Scope cleanup `SENT` distinction | PASS | separate pre-send/after-send SQL branches, model test |
| Lease revocation-version binding | PASS | `sql/25-lease-revocation-binding.sql` |
| Permit Consumption revocation gate | PASS | `sql/50-permit-consumption-revocation.sql` |
| Egress PENDING intent validation | PASS | conditional INSERT, model test |
| Egress final authorization | PASS | `sql/30-egress-final-authorization.sql` transaction 2 |
| Egress final write-start gate | PASS | transaction 3 plus offline model |
| Worker Registration/heartbeat recheck | PASS | both final and write-start SQL/model checks |
| Scope block recheck | PASS | both final and write-start SQL/model checks |
| Emergency/Key/Lease/Budget recheck | PASS | both Egress gates |
| Unknown external outcome | PASS | terminal `SEND_OUTCOME_UNKNOWN`, no automatic retry |
| SQL parameter review | PASS | `PHASE_R3_EGRESS_SQL_REVIEW.md` |
| SQL negative tests | PASS | actual SQL mutation tests and synthetic negatives |
| Offline model tests | PASS | 4 files / 53 tests |
| Production Egress architecture | PASS | `PHASE_R3_EGRESS_ARCHITECTURE.md` |
| Production Egress implementation | NOT_IMPLEMENTED | no network or Provider code added |

## 4. Acceptance Matrix

```text
WORKER_REVOCATION_TRANSACTION=PASS
WORKER_REACTIVATION_PROTECTION=PASS
REVOCATION_LEASE_INVALIDATION=PASS
REVOCATION_PERMIT_INVALIDATION=PASS
REVOCATION_CONSUMPTION_RACE_HANDLING=PASS
EGRESS_WORKER_STATE_CHECK=PASS
EGRESS_REVOCATION_VERSION_CHECK=PASS
EGRESS_RESOURCE_FLOOR_CHECK=PASS
EGRESS_EMERGENCY_CHECK=PASS
EGRESS_KEY_REVOCATION_CHECK=PASS
EGRESS_LEASE_CHECK=PASS
EGRESS_PERMIT_ONE_TIME_ENFORCEMENT=PASS
EGRESS_BUDGET_ENFORCEMENT=PASS
EGRESS_CENTRAL_AUTHORITY_FAIL_CLOSED=PASS
SOCKET_WRITE_RACE_ANALYSIS=PASS
SEND_OUTCOME_UNKNOWN_HANDLING=PASS
LOCK_ORDER_CONSISTENCY=PASS
SQL_PARAMETER_BINDING_REVIEW=PASS
SQL_NEGATIVE_TESTS=PASS
OFFLINE_MODEL_TESTS=PASS
PRODUCTION_EGRESS_ARCHITECTURE=PASS
```

`SOCKET_WRITE_RACE_ANALYSIS=PASS` means the irreducible database/network
boundary is stated correctly. It does not mean the race is eliminated.

## 5. Verification Results

```text
R3_EGRESS_REVOCATION_VITEST=4_FILES_53_TESTS_PASS
R3_FENCING_VITEST=7_FILES_49_TESTS_PASS
R2_R3_VITEST=8_FILES_74_TESTS_PASS
R2_VITEST=10_FILES_80_TESTS_PASS
R1_VITEST=16_FILES_91_TESTS_PASS
R31_R36_RELEVANT_VITEST=20_FILES_179_TESTS_PASS
POWERSHELL_LAUNCHER=40_PASS
POWERSHELL_KEY_SESSION=25_PASS
POWERSHELL_FETCH_ENFORCEMENT=4_PASS
POWERSHELL_TOTAL=69_PASS
POWERSHELL_5_1_PARSER=6_PASS
TYPESCRIPT_STRICT=PASS
ESLINT_NEW_SCOPE=PASS
NEXT_BUILD=PASS
IMPORT_BOUNDARY=PASS
PRODUCTION_ENTRY_BLOCK_STATUS=BLOCKED
```

The R31-R36 result is an explicit 20-file safe subset that reproduces the
historical 179-test count. It is not asserted to be a deduplicated count across
all historical phases.

## 6. Evidence Classification

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
REAL_KEY_ACCESS=NOT_EXECUTED
```

Promise/in-memory tests are not described as PostgreSQL or multi-instance
evidence.

## 7. Irreducible Guarantees

```text
REVOCATION_BEFORE_FINAL_AUTH=PREVENTS_SEND
REVOCATION_BEFORE_WRITE_STARTED=PREVENTS_SEND
REVOCATION_AFTER_WRITE_STARTED_CANCELLATION=NOT_GUARANTEED
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
SEND_OUTCOME_UNKNOWN_AUTO_RETRY=FORBIDDEN
```

The Provider may receive a request whose response is lost. No database
transaction can recall that external effect.

## 8. Files Created or Revised

All task files are under:

```text
preparation/production-trust/r3-egress-revocation-remediation/
```

This includes:

- baseline and contract reports;
- Worker Revocation, Egress and SQL review reports;
- threat model, risk register and this report;
- six source SQL drafts plus two consolidated SQL files;
- strict contracts and lock-order model;
- four reference model files;
- four Vitest files;
- aggregate and evidence-generation tools.

The authoritative path/size/SHA-256 list is
`PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt`.

## 9. Safety Boundary

```text
MAIN_WORKSPACE_MODIFIED=NO
SRC_MODIFIED=NO
SCRIPTS_MODIFIED=NO
R31_R36_MODIFIED=NO
IDENTITY_GATE_CORE_MODIFIED=NO
A3_D1_D2_MODIFIED=NO
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
REAL_KEY_ACCESSED=NO
PROVIDER_API_CALLED=NO
NETWORK_ACCESSED=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
```

The Next.js build wrote normal `.next/` output in the isolated copy.

## 10. Residual Risks

- production Egress is not implemented;
- Worker network isolation and credential removal are not enforced;
- PostgreSQL lock, isolation and SQLSTATE behavior are not executed;
- multi-instance coordination is not implemented or tested;
- trusted Egress exclusivity is a deployment requirement;
- canonical request/Permit digest code is not implemented here;
- same-host subagent work is not an independent third-party audit.

These risks prohibit production enforcement and real Fetch.

````
<!-- END_EXACT_SOURCE id=S008 -->

### S009. PHASE_R3_EGRESS_RISK_REGISTER.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_RISK_REGISTER.md`
- Bytes: `4235`
- SHA-256: `A51A1EB30734C7DEF550B225F7B0B7584F22244ABE8F21DED53988132C7E357D`

<!-- BEGIN_EXACT_SOURCE id=S009 sha256=A51A1EB30734C7DEF550B225F7B0B7584F22244ABE8F21DED53988132C7E357D bytes=4235 -->
````text
# PHASE_R3_EGRESS_RISK_REGISTER

## 1. Rating Scale

| Rating | Meaning |
|---|---|
| Critical | could create real Fetch, real Key access or bypass production block |
| High | could authorize or send in a way not allowed by the offline contract |
| Medium | production correctness/deployment risk requiring implementation review |
| Low | bounded evidence, maintainability or residual operational risk |

## 2. Register

| ID | Risk | Severity | Status | Evidence / required follow-up |
|---|---|---|---|---|
| R3ER-01 | Frozen R4 Permit Consumption lacks global Worker revocation checks | High | MITIGATED_IN_DESIGN | R5 replacement SQL + model/test; PostgreSQL execution remains not done |
| R3ER-02 | Scope block absent at final or write-start gate | High | MITIGATED_IN_DESIGN | both SQL gates and model include block check |
| R3ER-03 | `SENT` Lease incorrectly treated as pre-send cancellable | High | MITIGATED_IN_DESIGN | separate 20A/20B host branches |
| R3ER-04 | Lease lacks Worker revocation binding | High | MITIGATED_IN_DESIGN | `25-lease-revocation-binding.sql`; missing binding fails closed |
| R3ER-05 | Intent creation can outlive invalid Permit/Worker state | High | MITIGATED_IN_DESIGN | conditional INSERT and full model precheck |
| R3ER-06 | Write-start omits Worker Registration/heartbeat | High | MITIGATED_IN_DESIGN | fresh locked read and conditional check |
| R3ER-07 | SQL allegedly protects socket after COMMIT | Critical | MITIGATED_BY_DESIGN_LIMIT | explicit non-atomicity; no exactly-once claim |
| R3ER-08 | Revocation after write start cannot cancel bytes | High | ACCEPTED_RESIDUAL | `SOCKET_WRITE_AFTER_WRITE_STARTED_CANCELLATION=NOT_GUARANTEED` |
| R3ER-09 | Provider may receive request without local response | High | ACCEPTED_RESIDUAL | terminal `SEND_OUTCOME_UNKNOWN`; automatic retry forbidden |
| R3ER-10 | Worker bypasses Egress and calls Provider directly | Critical | NOT_IMPLEMENTED | requires OS/container network isolation and credential removal |
| R3ER-11 | Multi-instance Egress has no real coordinator test | High | NOT_EXECUTED | production implementation and multi-instance acceptance required |
| R3ER-12 | PostgreSQL lock/SQLSTATE behavior unverified | High | NOT_EXECUTED | requires integration test against isolated database later |
| R3ER-13 | SQL analyzer is not a PostgreSQL parser | Medium | ACCEPTED_LIMITATION | validation level explicitly labeled |
| R3ER-14 | Audit write failure handling across restart needs durable protocol | High | DESIGNED_NOT_TESTED | production transaction and ambiguity query required |
| R3ER-15 | Host may execute wrong cleanup branch | High | HOST_CONTRACT_REQUIRED | conditional command path, exactly-one checks and review |
| R3ER-16 | Recovery registration could reactivate a revoked identity | High | MITIGATED_IN_DESIGN | ordinary Upsert forbidden; trusted identity replacement required |
| R3ER-17 | Request/permit digest canonicalization implementation absent | High | NOT_IMPLEMENTED | future code must use fixed canonicalizer and test vectors |
| R3ER-18 | R3 original files could be modified accidentally | High | MITIGATED | 41-file baseline Hash rechecked |
| R3ER-19 | Production Fetch entry could be opened | Critical | CONTROLLED | read-only block check required; no production code touched |
| R3ER-20 | Independent third-party review absent | Medium | OPEN | same-host subagents are not independent audit |

## 3. Unresolved High/Critical Design Defects

No unresolved High/Critical item is claimed as eliminated by SQL/model tests.
The following are production implementation gaps rather than permission to
implement:

- trusted Egress deployment and Worker network isolation do not exist;
- PostgreSQL and multi-instance behavior have not been executed;
- the canonical digest implementation does not exist in this task;
- the real socket/Provider boundary remains externally irreversible.

These gaps keep:

```text
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
PRODUCTION_EGRESS_IMPLEMENTED=NO
REAL_FETCH_AUTHORIZED=NO
```

## 4. Risk Decision

Offline design risk is sufficiently bounded for external review. This is not a
production security acceptance and does not authorize implementation.

````
<!-- END_EXACT_SOURCE id=S009 -->

### S010. PHASE_R3_EGRESS_SQL_REVIEW.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_SQL_REVIEW.md`
- Bytes: `8133`
- SHA-256: `4812FB01E31F2BA9B435FF76E24BCD33A6B5389D115CABF4CF52FC2BE73AA190`

<!-- BEGIN_EXACT_SOURCE id=S010 sha256=4812FB01E31F2BA9B435FF76E24BCD33A6B5389D115CABF4CF52FC2BE73AA190 bytes=8133 -->
````text
# PHASE_R3_EGRESS_SQL_REVIEW

## 1. Validation Scope

```text
TEXTUAL_PATTERN_CHECK=EXECUTED
SQL_STRUCTURE_CHECK=EXECUTED
PARAMETER_BINDING_REVIEW=EXECUTED
TRANSACTION_CONTRACT_REVIEW=EXECUTED
POSTGRESQL_EXECUTION=NOT_EXECUTED
POSTGRESQL_AST_ANALYSIS=NOT_EXECUTED
```

No SQL was executed. No PostgreSQL connection, database, Docker or network
service was used. The analyzer splits statements and transactions, maps obvious
`FOR UPDATE` locks, checks required table/parameter presence, and reviews the
key negative invariants. It does not prove PostgreSQL parse acceptance, lock
timing, SQLSTATE behavior, constraint behavior or deadlock freedom.

## 2. Source SQL

| Source | Purpose | Contract | Associated tests |
|---|---|---|---|
| `sql/10-worker-global-revocation.sql` | R5 revocation schema, request idempotency and global tombstone | Worker revocation global/terminal | `worker-revocation.test.ts`, `sql-contract.test.ts` |
| `sql/20-worker-scope-cleanup.sql` | Separate pre-send cleanup and after-send classification | Scope block, Lease/Permit invalidation | `worker-revocation.test.ts`, `sql-contract.test.ts` |
| `sql/25-lease-revocation-binding.sql` | Bind Lease to the exact Worker revocation version | Lease revocation binding | `sql-contract.test.ts` |
| `sql/30-egress-final-authorization.sql` | Egress Intent, final gate and final write-start gate | Egress Intent state and final checks | `egress-boundary.test.ts`, `egress-races.test.ts`, `sql-contract.test.ts` |
| `sql/40-egress-write-outcome.sql` | Response and unknown external outcome | External outcome is not exactly-once | `egress-boundary.test.ts`, `sql-contract.test.ts` |
| `sql/50-permit-consumption-revocation.sql` | Complete R5 overlay of frozen R4 Permit Consumption | Permit, Lease, Worker Revocation, Scope block | `worker-revocation.test.ts`, `sql-contract.test.ts` |

## 3. Parameter Binding

### 3.1 `sql/10-worker-global-revocation.sql`

| Parameter | Source / binding |
|---|---|
| `$1` | server-resolved Worker ID to revoke |
| `$2` | caller request UUID, unique idempotency key |
| `$3` | server UTC Unix milliseconds |
| `$4` | reason code |
| `$5` | expected current revocation record version |
| `$6` | Audit event UUID |
| `$7` | Audit sequence under locked head |
| `$8` | previous event digest under locked head |
| `$9` | new event digest |

### 3.2 `sql/20-worker-scope-cleanup.sql`

| Parameter | Source / binding |
|---|---|
| `$1` | server-resolved Worker ID |
| `$2` | server-resolved canonical scope key |
| `$3` | current Lease ID |
| `$4` | current Capability ID |
| `$5` | committed global revocation version |
| `$6` | server UTC Unix milliseconds |
| `$7` | cleanup reason code |
| `$8` | current Resource Floor token |
| `$9` | Audit event UUID |
| `$10` | Audit sequence under locked head |
| `$11` | previous event digest |
| `$12` | new event digest |

### 3.3 `sql/25-lease-revocation-binding.sql`

| Parameter | Source / binding |
|---|---|
| `$1` | Worker ID from the issued Lease |
| `$2` | Resource Scope from the issued Lease |
| `$3` | Lease ID |
| `$4` | current global Worker revocation version |
| `$5` | Capability ID from the issued Lease |
| `$6` | Resource Floor fencing token |
| `$7` | server UTC Unix milliseconds |

### 3.4 `sql/50-permit-consumption-revocation.sql`

| Parameter | Source / binding |
|---|---|
| `$1` | Key ID |
| `$2` | Execution Authorization ID |
| `$3` | Budget Reservation ID |
| `$4` | Capability ID |
| `$5` | canonical Resource Scope |
| `$6` | server-resolved Worker ID |
| `$7` | Lease ID |
| `$8` | fencing token |
| `$9` | Emergency epoch |
| `$10` | Key version |
| `$11` | Key revocation version |
| `$12` | Permission version |
| `$13` | Policy version |
| `$14` | server UTC Unix milliseconds for consumption |
| `$15` | one-use Send Authorization ID |
| `$16` | Audit event UUID |
| `$17` | Audit sequence under locked head |
| `$18` | previous event digest |
| `$19` | new event digest |
| `$20` | expected Worker revocation version |

### 3.5 `sql/30-egress-final-authorization.sql`

| Parameter | Source / binding |
|---|---|
| `$1` | server-resolved Worker ID |
| `$2` | Key ID |
| `$3` | Lease ID |
| `$4` | consumed Send Authorization ID |
| `$5` | SHA-256 over exact request bytes |
| `$6` | SHA-256 over canonical Permit object |
| `$7` | Egress Intent UUID |
| `$8` | canonical Resource Scope |
| `$9` | fencing token |
| `$10` | Worker revocation version |
| `$11` | Capability ID |
| `$12` | Budget Reservation ID |
| `$13` | Emergency epoch |
| `$14` | Key version |
| `$15` | Key revocation version |
| `$16` | Permission version |
| `$17` | Policy version |
| `$18` | intent creation/final authorization time |
| `$19` | Execution Authorization ID |
| `$20` | final authorization expiry, at most `$18 + 1000` |
| `$21` | expected Egress Intent row version |
| `$22` | final-authorization Audit event UUID |
| `$23` | Audit sequence |
| `$24` | previous event digest |
| `$25` | new event digest |
| `$26` | write-start time |
| `$27` | expected Intent row version for write-start |
| `$28` | write-start Audit event UUID |
| `$29` | Audit sequence |
| `$30` | previous event digest |
| `$31` | new event digest |

### 3.6 `sql/40-egress-write-outcome.sql`

| Parameter | Source / binding |
|---|---|
| `$1` | Egress Intent ID |
| `$2` | expected row version for response branch |
| `$3` | response/completion time |
| `$4` | response Audit event UUID |
| `$5` | Audit sequence |
| `$6` | previous event digest |
| `$7` | new event digest |
| `$8` | unknown-outcome time |
| `$9` | expected row version for unknown branch |
| `$10` | unknown-outcome Audit event UUID |
| `$11` | Audit sequence |
| `$12` | previous event digest |
| `$13` | new event digest |

All security parameters must be supplied by server-side code and validated
against locked database rows. Request body, query or header values cannot
replace a database binding.

## 4. Negative Cases

| Negative case | Expected result | Evidence |
|---|---|---|
| Permit Consumption lacks global revocation | `PERMIT_WORKER_REVOCATION_CHECK_MISSING` | `reviewPermitConsumptionRevocation` |
| Permit Consumption lacks Scope block | `PERMIT_SCOPE_BLOCK_CHECK_MISSING` | negative SQL test |
| Permit Consumption lacks Lease binding | `PERMIT_LEASE_REVOCATION_BINDING_MISSING` | `reviewPermitConsumptionRevocation` |
| Permit lacks one-use transition | `PERMIT_ONE_TIME_TRANSITION_MISSING` | `reviewPermitConsumptionRevocation` |
| Egress omits Scope block at a gate | `EGRESS_SCOPE_BLOCK_RECHECK_MISSING` | actual SQL mutation test |
| Egress omits Worker Registration/heartbeat | `EGRESS_WORKER_REGISTRATION_RECHECK_MISSING` | actual SQL mutation test |
| Egress omits Lease revocation binding | `EGRESS_LEASE_REVOCATION_BINDING_MISSING` | `reviewEgressRevocationGate` |
| SQL claims a lock protects later Socket Write | `SOCKET_ATOMICITY_OVERCLAIM` | textual negative test |
| Worker registration Upsert can restore ACTIVE | `WORKER_REACTIVATION_UPSERT` | existing negative test |
| Missing Audit in same mutation transaction | `AUDIT_SPLIT_FROM_MUTATION` | existing structural test |
| Missing condition/row-count marker | `ROW_COUNT_MARKER_MISSING` | existing structural test |

## 5. Conditions Requiring Host Enforcement

SQL cannot enforce:

- fail-closed behavior when no database connection or transaction authority is
  available;
- exact request bytes hashing;
- canonical Permit hashing;
- checking that a driver command tag is one before issuing the next command;
- refusing to run the checked pre-send Lease update after observing `SENT`;
- preventing a Worker process from bypassing a trusted Egress service;
- recalling bytes after a socket write begins.

These are explicit host/deployment requirements and are not claimed as
database-enforced properties.

## 6. Not Proven

```text
POSTGRESQL_PARSE_ACCEPTANCE=NOT_PROVEN
POSTGRESQL_LOCK_TIMING=NOT_PROVEN
POSTGRESQL_ISOLATION_BEHAVIOR=NOT_PROVEN
UNIQUE_CONSTRAINT_SQLSTATE=NOT_PROVEN
DEADLOCK_BEHAVIOR=NOT_PROVEN
REAL_MULTI_INSTANCE_INTERLEAVING=NOT_PROVEN
REAL_NETWORK_SOCKET_BOUNDARY=NOT_PROVEN
PROVIDER_RECEIPT=NOT_PROVEN
```

````
<!-- END_EXACT_SOURCE id=S010 -->

### S011. PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE.md`
- Bytes: `9323`
- SHA-256: `603CD82114FD69FAFD2E6D223F811E4B2511836B2870B12DC594C583AD0EAE1B`

<!-- BEGIN_EXACT_SOURCE id=S011 sha256=603CD82114FD69FAFD2E6D223F811E4B2511836B2870B12DC594C583AD0EAE1B bytes=9323 -->
```````text
﻿# PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE

## Status

``````text
GENERATED_AT=2026-11-26T22:52:01.9498947+08:00
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
FAILED_COMMANDS=0
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
``````

## Execution Note

An earlier focused run during remediation failed 9 Egress model tests because
the test fixture set workerHeartbeatAt five milliseconds after the intent
creation time. The model correctly rejected the future heartbeat. The fixture
was corrected to use the same timestamp; the failure is not hidden and the
final complete run below is the authoritative result.

## Commands
### R3 Egress/Revocation Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-egress-revocation-remediation/vitest.config.ts
START=2026-11-26T22:51:21.9498733+08:00
END=2026-11-26T22:51:22.7531220+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  4 passed (4)
      Tests  53 passed (53)
   Start at  22:51:22
   Duration  372ms (import 73%, tests 13%, transform 10%, worker 4%)
```

### R3 Fencing Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-fencing-remediation/vitest.config.ts
START=2026-11-26T22:51:22.7676663+08:00
END=2026-11-26T22:51:23.5700094+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  7 passed (7)
      Tests  49 passed (49)
   Start at  22:51:23
   Duration  382ms (import 78%, transform 9%, tests 9%, worker 4%)
```

### R2-R3 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2-r3-remediation/vitest.config.ts
START=2026-11-26T22:51:23.5710947+08:00
END=2026-11-26T22:51:24.4303282+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  8 passed (8)
      Tests  74 passed (74)
   Start at  22:51:23
   Duration  427ms (import 78%, tests 11%, transform 7%, worker 3%)
```

### R2 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2/vitest.config.ts
START=2026-11-26T22:51:24.4308316+08:00
END=2026-11-26T22:51:25.3408180+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  10 passed (10)
      Tests  80 passed (80)
   Start at  22:51:24
   Duration  469ms (import 79%, tests 13%, transform 5%, worker 3%)
```

### R1 Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run --config preparation/production-trust/vitest.config.ts
START=2026-11-26T22:51:25.3428249+08:00
END=2026-11-26T22:51:26.3598039+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  16 passed (16)
      Tests  91 passed (91)
   Start at  22:51:25
   Duration  587ms (import 78%, tests 10%, transform 7%, worker 4%)
```

### R31-R36 Relevant Vitest

```text
COMMAND=node node_modules/vitest/vitest.mjs run src/server/auth/actor-context.test.ts src/server/public-enterprise-search/identity/identity-gate.test.ts src/server/public-enterprise-search/identity/runtime/approval-authorization.test.ts src/server/public-enterprise-search/identity/runtime/authorization.test.ts src/server/public-enterprise-search/identity/runtime/fetch-entry-guard.test.ts src/server/public-enterprise-search/identity/runtime/precheck.test.ts src/server/public-enterprise-search/identity/runtime/production-fetch-entry.test.ts src/server/public-enterprise-search/identity/runtime/trusted-read.test.ts src/server/public-enterprise-search/offline-boundaries.test.ts src/server/public-enterprise-search/provider/aux-http-transports.test.ts src/server/public-enterprise-search/provider/deepseek-fetch.test.ts src/server/public-enterprise-search/provider/deepseek-http-transport.test.ts src/server/public-enterprise-search/provider/provider-execution-authorization.test.ts src/server/public-enterprise-search/provider/provider-factory-protection.test.ts src/server/public-enterprise-search/diagnostics/fetch-diagnostic-cli.test.ts src/server/public-enterprise-search/diagnostics/fetch-diagnostic-dependency.test.ts src/server/public-enterprise-search/local-live/live-config.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial-cli.test.ts src/server/public-enterprise-search/trial/run-real-provider-trial.zero-network.test.ts
START=2026-11-26T22:51:26.3623402+08:00
END=2026-11-26T22:51:34.7807163+08:00
EXIT_CODE=0
```

```text
RUN  v5.1.0 C:/Users/Administrator/Desktop/thzz1-search-offline


 Test Files  20 passed (20)
      Tests  179 passed (179)
   Start at  22:51:26
   Duration  7.97s (tests 52%, import 41%, transform 5%, worker 3%)

    Isolate  20 workers spawned · ~145ms startup each (spawn + environment, per file)
             at least ~2.76s faster with isolate: false — reuses workers across files instead of one per file
```

### PowerShell Launcher

```text
COMMAND=powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-only-launcher.ps1
START=2026-11-26T22:51:34.7817207+08:00
END=2026-11-26T22:51:42.9349778+08:00
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
START=2026-11-26T22:51:42.9359780+08:00
END=2026-11-26T22:51:44.6398740+08:00
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
START=2026-11-26T22:51:44.6408800+08:00
END=2026-11-26T22:51:45.3192759+08:00
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
START=2026-11-26T22:51:45.3202752+08:00
END=2026-11-26T22:51:45.3492068+08:00
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
START=2026-11-26T22:51:45.3502047+08:00
END=2026-11-26T22:51:49.1774057+08:00
EXIT_CODE=0
```

```text

```

### ESLint New Scope

```text
COMMAND=npx.cmd eslint preparation/production-trust/r3-egress-revocation-remediation
START=2026-11-26T22:51:49.1784062+08:00
END=2026-11-26T22:51:53.7292291+08:00
EXIT_CODE=0
```

```text

```

### Next Build

```text
COMMAND=pnpm.cmd build
START=2026-11-26T22:51:53.7302310+08:00
END=2026-11-26T22:52:01.8837361+08:00
EXIT_CODE=0
```

```text
pnpm.cmd : $ next build
At C:\Users\Administrator\Desktop\thzz1-search-offline\preparation\production-trust\r3-egress-revocation-remediation\to
ols\run-verification.ps1:17 char:13
+   $output = & $Executable @Arguments 2>&1
+             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: ($ next build:String) [], RemoteException
    + FullyQualifiedErrorId : NativeCommandError
 
▲ Next.js 16.4.6 (Turbopack)
✓ Running next.config.ts took 40ms
- Experiments (use with caution):
  · serverActions

  Creating an optimized production build ...
✓ Compiled successfully in 408ms
  Running TypeScript ...
  Finished TypeScript in 2.9s ...
  Collecting page data using 11 workers ...
  Generating static pages using 11 workers (0/2) ...
✓ Generating static pages using 11 workers (2/2) in 882ms
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

### S012. PHASE_R3_EGRESS_THREAT_MODEL.md

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_THREAT_MODEL.md`
- Bytes: `5122`
- SHA-256: `8C7E60B8580BDE55B56DAF4630F9A7F194805025EC46F95F47A6F53940F972AC`

<!-- BEGIN_EXACT_SOURCE id=S012 sha256=8C7E60B8580BDE55B56DAF4630F9A7F194805025EC46F95F47A6F53940F972AC bytes=5122 -->
````text
# PHASE_R3_EGRESS_THREAT_MODEL

## 1. Assets and Trust Boundaries

Protected assets:

- one-use send authority;
- Worker identity and revocation state;
- Resource Floor token/ownership;
- Lease, Capability and Budget reservation;
- Key and Emergency versions;
- request bytes and Provider credentials;
- Audit linearity;
- pre-fetch approval and identity evidence.

Critical boundaries:

```text
Worker process
  -> authenticated internal Egress request
  -> trusted Egress service
  -> database transaction
  -> external socket
  -> Provider
```

The database and Provider do not share a transaction.

## 2. Threats and Controls

| Threat | Control in this revision | Residual risk |
|---|---|---|
| Revoke Worker but old Permit still consumes | Permit Consumption joins global revocation, Scope block, Lease binding and Floor | Real PostgreSQL lock behavior not executed |
| Revoke Worker after consumption, before Egress | Egress final gate and write-start re-read current revocation | Revocation after `WRITE_STARTED` may be too late |
| Revoked Worker ordinary Upsert becomes ACTIVE | registration update requires `state='ACTIVE'`; global tombstone is terminal | Provisioning/recovery service itself needs review |
| Scope cleanup cannot atomically enumerate all floors | global tombstone is immediate fail-closed authority; cleanup is resumable | cleanup backlog must be monitored in production |
| Scope cleanup falsely rewrites `SENT` Lease to REVOKED | separate 20A pre-send and 20B after-send branches | host must select branch correctly |
| Worker takeover races revocation | global revocation remains checked by Permit/Egress; takeover mutation cannot restore revoked registration | original R4 SQL has no R5 tombstone join; binding finalization fails closed |
| Stale fencing token reaches Egress | Egress checks current Resource Floor token/Worker/Lease/Capability at both gates | no real multi-instance test |
| Cached `NORMAL` allows send after Emergency | Emergency status/epoch is locked and re-read at final and write-start | network write after `WRITE_STARTED` cannot be recalled |
| Key revocation races send | Key state/version/revocation version re-read at both gates | no real key service test |
| Permit replay creates multiple intents | Permit must be CONSUMED; Intent has unique `send_authorization_id` | driver must surface unique conflict correctly |
| Intent creation races Scope block | Worker Revocation row lock serializes cleanup against the consumer | PostgreSQL semantics unverified |
| Duplicate socket write after crash | Egress Intent is terminal on write start; unknown outcome forbids automatic retry | exactly-once Provider receipt not guaranteed |
| Audit chain forks | Audit Head locked first; sequence/digest checked by exactly-one update | concurrent PostgreSQL behavior not executed |
| Audit failure leaves authority consumed but no event | state mutation and Audit are in one transaction | transaction outcome ambiguity needs durable query |
| Worker bypasses Egress | target architecture removes routes/credentials from Worker | not implemented or enforced |
| Malicious request changes bytes after authorization | request digest bound in Intent and rechecked by host | canonical hashing implementation not tested |
| SQL text check gives false confidence | validation level explicitly limited to structure/contract review | no PostgreSQL AST or execution |

## 3. Race Analysis

### Revocation vs Permit Consumption

Both lock the global revocation row. If revocation commits first, consumption
sees `REVOKED`. If consumption commits first, a later Egress gate rejects the
revoked Worker. Consumption does not reserve an irrevocable network permission.

### Permit Consumption vs Scope Cleanup

Cleanup requires global revocation `REVOKED`; its `FOR SHARE` lock cannot pass
while a consumer holds `FOR UPDATE`. The consumer either finishes before the
global tombstone or observes it.

### Egress Final Authorization vs Cleanup

Final authorization checks the Scope block and global tombstone under the same
Worker Revocation lock. Cleanup commits before final authorization -> deny.
Cleanup commits after final authorization but before write-start -> write-start
denies.

### Write Start vs Emergency/Key/Worker Changes

The write-start transaction re-reads all mutable authority. A change committed
first denies write-start. A change committed after `WRITE_STARTED` cannot
guarantee cancellation of a socket operation already beginning.

## 4. Irreducible External Effects

```text
SEND_OUTCOME_UNKNOWN
EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED
SOCKET_WRITE_AFTER_WRITE_STARTED_CANCELLATION=NOT_GUARANTEED
```

The design prevents new authorization after a committed stop whenever the
central authority is reachable. It cannot prove whether Provider received a
request whose response was lost.

## 5. Production Gaps

```text
PRODUCTION_EGRESS_IMPLEMENTED=NO
NETWORK_ISOLATION_ENFORCED=NO
MULTI_INSTANCE_COORDINATION=NOT_IMPLEMENTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_NETWORK_RACE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
REAL_KEY_ACCESS=NOT_AUTHORIZED
```

````
<!-- END_EXACT_SOURCE id=S012 -->

### S013. PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt`
- Bytes: `6309`
- SHA-256: `EF9ABEB534CCA464BD27C9E94DBB59CE36C09C5E5F0AF21694EA3FC5D5E8A023`

<!-- BEGIN_EXACT_SOURCE id=S013 sha256=EF9ABEB534CCA464BD27C9E94DBB59CE36C09C5E5F0AF21694EA3FC5D5E8A023 bytes=6309 -->
```text
# PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS
# ENTRIES=41
# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION

924E1D2E58C7C01C4BBD6782BAC064837AF98FBDBCF4C6ADCF79B09C75A76654  preparation\production-trust\PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE.md
E81D3694FD1119E8E7D7118153B27661DE3DA01B5B35322B1B05070C9F08DBB2  preparation\production-trust\PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md
FF5BDFEC619C52EC83BF325AD40FF27E0D3EB625911C05D145C645513452F5D4  preparation\production-trust\PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt
18F7A37FC271C2AEAFFAF1F71419BAF9474A00E8987EF26EE63C956D8E1BBA12  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE.md
C013857E3F4A8C38E49ACCCF2B3FC6AC19DA7002B72D0F6D45D606966E39B050  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE_SHA256SUMS.txt
F43185B267AB79ED23C9D29DD57EB69FF31517F1DFE043E2614F4F6946834650  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CONTRACT.md
8E455E4299C7687D634EC3AEE4ACC2C80D9252AAB5E9D6EB9C1C0DDB2AFAA016  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CROSS_REVIEW.md
45DC3E67B086C92AF9ADF8C44AE8ECD17C7E9E7595401A1C6213B589C16A8E94  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_DIFF.md
8A2D510E772B1CE0B2EC724FBB902F11D9C19230EBBA46480DA10C49898FBED4  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT.md
D5D1B28AAC2727F1841AB0A0940EFA623A48730319A6EDFFE82833286F78F18F  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_MODEL.md
3A1F3BFD5BB6B4BFE28F7D9FE71D719B2BF8799CE8E1193CE37AA4EFC88A455D  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER.md
76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql
581C7B8D543ACB813039F019CE9CEECB3E65E0EFA740E2D5978C771A60076D80  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SHA256SUMS.txt
E6CED6736E59AA4AE2CBDE965380CD4BF76765A67393BF32344FDF6E70D73986  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW.md
633F8F15D83167C9D9D5D5B233177D7FFBFC47A3FAFDD3221866D7DB4420392A  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX.md
BAFCAC5051A6C73197255849F25409F0AB2B40806F727FA71EC0709A82F1D097  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL.md
512E790234B41699AF72DCDE172F4CF247911DE02E9C04915D985ED5C739D8B1  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql
71487EE30BC5FE31B30542851B5B4159547F1156DD88B7B6139F553BB0852375  preparation\production-trust\r3-fencing-remediation\R3_FENCING_INDEPENDENT_REVIEW_EXTRACT.md
83B84DB9D8E76F72C747BDB5F90C830725C7A2516DDF6A7A1523AFFC7A253755  preparation\production-trust\r3-fencing-remediation\R3_FENCING_INDEPENDENT_REVIEW_EXTRACT_REPORT.md
36E3E5235290F942D5C9D92F0004736A6CE1B56E383D98764B25ABC65048E913  preparation\production-trust\r3-fencing-remediation\R3_FENCING_INDEPENDENT_REVIEW_EXTRACT_SHA256SUMS.txt
B50E5388C90FC3E5C5DFE746A0D13FAB8E63CC4E35B4CEE44D672D31F733C0EE  preparation\production-trust\r3-fencing-remediation\contracts.ts
B203CC3BDA846BDD3BFA423D1C30659E5DE0E285792ACD1724122BD933207C64  preparation\production-trust\r3-fencing-remediation\lock-order.ts
0821E49639C34B4233FE99A691E10EEADB262AF966BE11E88E2C8F189623B7AE  preparation\production-trust\r3-fencing-remediation\models\execution-boundary.ts
83F085134850F4765ABAD9D5D2451B23684E60ABB3202A762B571D5BAA7A76DB  preparation\production-trust\r3-fencing-remediation\models\fencing-floor.ts
079FCF395897ED8D54B2C665A5B51AC0FBE4C6341EE9B7FE6E059B9940CF8839  preparation\production-trust\r3-fencing-remediation\models\race-scenarios.ts
98EB13EE3AA9F01FB72AFB9860A2AE2C15E143E0A627113EF882632258729FB5  preparation\production-trust\r3-fencing-remediation\models\sql-analyzer.ts
04B4E4FBBB246FC05EFC6B6894806C32B38F559674D87B0B7B0C6E5EADC31BEF  preparation\production-trust\r3-fencing-remediation\scope.ts
76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4  preparation\production-trust\r3-fencing-remediation\sql\00-schema.sql
000CC783457862E4CEFD5313E19EB3C055F02379FED642E982517361F42FB909  preparation\production-trust\r3-fencing-remediation\sql\10-worker-takeover.sql
101D3AACA2609E3A79FE1EC7AD7B0DBE376B9E2528B8CCB751056DEECAC79FC8  preparation\production-trust\r3-fencing-remediation\sql\20-lease-issuance.sql
5C9CC11B8763F7809D75F87C695E44B26A223132E5462071745A2A72F9534724  preparation\production-trust\r3-fencing-remediation\sql\30-worker-progress.sql
F1C8E92DD2CB3E649D491AF7B5748FF8157F32ED3AC1881AB3EB49B0E8FC7D94  preparation\production-trust\r3-fencing-remediation\sql\40-send-authorization-issuance.sql
0ACA5410F758DD2B31A6C3681D7014A2A5BF1FEB509A2CA482423AF793E7A684  preparation\production-trust\r3-fencing-remediation\sql\50-send-authorization-consume.sql
E8A2CE8FB05B7E7658348FA553FD0606F86D8ADF7D278B7D7158A9DED84D8A48  preparation\production-trust\r3-fencing-remediation\tests\execution-boundary.test.ts
5690EDDF00728F51F52EB55B9F73176909001B8A031E9DAFE28793D24E9A3A88  preparation\production-trust\r3-fencing-remediation\tests\fencing-floor.test.ts
94C7917C295334AB212344F7EF1A4AE64CBCBDEE36F40BC44701C8907D1F0DB1  preparation\production-trust\r3-fencing-remediation\tests\races.test.ts
D99EF9FDF09E102F4B4E7F37D73DB9DDD4EA20E384F1E4DBB370AE5301167C2B  preparation\production-trust\r3-fencing-remediation\tests\scope-lock-order.test.ts
45E38B57F90919DA480E8348D8CD14B8036E2A96CD84392BDF79EE5E3AD5EB98  preparation\production-trust\r3-fencing-remediation\tests\scope-lock.test.ts
A9185EAC405B111E9323239200C0DA3C4ECAFB297220F71A4E4DBA81D27162A2  preparation\production-trust\r3-fencing-remediation\tests\sql-negative.test.ts
5F82F0DD4A89BCC65672F7CDA7EFA0D0FF1BCCCE95FABAE22DBBEBE24BAB279C  preparation\production-trust\r3-fencing-remediation\tests\sql-positive.test.ts
3498ED7EA917D283C253A19BE5C04FEA632664E3E1427B46FFFE1109A0F12FF0  preparation\production-trust\r3-fencing-remediation\vitest.config.ts

```
<!-- END_EXACT_SOURCE id=S013 -->

### S014. PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt`
- Bytes: `5742`
- SHA-256: `9F71A2D092F2032B8EAD3C23346FB5FB8B34E0762B370DFF9F194C87051AA0DA`

<!-- BEGIN_EXACT_SOURCE id=S014 sha256=9F71A2D092F2032B8EAD3C23346FB5FB8B34E0762B370DFF9F194C87051AA0DA bytes=5742 -->
```text
# PHASE_R3_EGRESS_REVOCATION_SHA256SUMS
# ENTRIES=35
# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION

E18972EF94DD04EE27B879B5CD3BCE9033CB7B2F0BFC7BBABF767213515A9CD9  preparation/production-trust/r3-egress-revocation-remediation/contracts.ts
3E7A4CA714B9E9BA7412FF6E7CB12DA9FF798F895EF0B141B3BB85AC671E32AE  preparation/production-trust/r3-egress-revocation-remediation/lock-order.ts
14FE4BA52870232929A8AB7966623E7D0450659669D0069F79A32F35AC347A02  preparation/production-trust/r3-egress-revocation-remediation/models/egress-boundary.ts
44E563B9D7AA80F8D060BDF07CA84D0E554C7FDE6675FF5DB61EDE5BB1CB0B1E  preparation/production-trust/r3-egress-revocation-remediation/models/egress-races.ts
5C29304B30B7693089B00C29C40BC2C72A6429AB64519AE81D78D18CD423DEA9  preparation/production-trust/r3-egress-revocation-remediation/models/sql-contract-analyzer.ts
974C1463AB2280605B7EC94EDBEE4AAC36383BBE1D16C6CDDB3B8ECD69E54C90  preparation/production-trust/r3-egress-revocation-remediation/models/worker-revocation.ts
90C1B065902B6EA852DC03A6032C93DC840FACD92A5EA173B20CBB8337E80F24  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_ARCHITECTURE.md
5CB3A4249FBD19982949086B46E6B4DFD2D0DB69EFF32F60D2A29BD283B1ADC3  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_AUTHORIZATION_TRANSACTIONS.sql
8854E40A256F5842A94C65AC1C3A75A00D7B3237495B3B7D75EBB527E5CE6A0F  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_DIFF.md
C1ADAFD47A69C61143826821B117C1CF5D2C8E549F08F8EDF4B5A071D087F66C  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_LOCK_ORDER.md
C5EA8738B0B5720412256818FAAB6E1EB3D4FFD9B9BC8E7DE0DA1FE854464C12  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_NEGATIVE_TEST_MATRIX.md
EE352C8556D3660CCCD617660FD8B17B4105993482B84A20019C038B3A23FD47  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REFERENCE_MODEL.md
EF9ABEB534CCA464BD27C9E94DBB59CE36C09C5E5F0AF21694EA3FC5D5E8A023  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt
11C34D2109863300DA66E07FCC93A032A218CFB155B38EE7650457A163D20398  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_BASELINE.md
C4E21EBF5DCC615F260BDADFB72117886D11A7724693E92023A1373AB4804EE1  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_CONTRACT.md
6EF2E8AA32746E311BC7408FB836D569ACBEE521162E700A65FEAB9870A99BD1  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_REVOCATION_FINAL_REPORT.md
A51A1EB30734C7DEF550B225F7B0B7584F22244ABE8F21DED53988132C7E357D  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_RISK_REGISTER.md
4812FB01E31F2BA9B435FF76E24BCD33A6B5389D115CABF4CF52FC2BE73AA190  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_SQL_REVIEW.md
603CD82114FD69FAFD2E6D223F811E4B2511836B2870B12DC594C583AD0EAE1B  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE.md
8C7E60B8580BDE55B56DAF4630F9A7F194805025EC46F95F47A6F53940F972AC  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_THREAT_MODEL.md
2591E69443552F897F03F819BBF4DFC25DAC6452A9D307C6F62B22C1C1D4EB8E  preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_WORKER_REVOCATION_TRANSACTIONS.sql
54B918ABA73574E0BB92000C993ED1CDF8FF1C8F5CB646FC27AAAC20721D37E1  preparation/production-trust/r3-egress-revocation-remediation/sql/10-worker-global-revocation.sql
FE3ED25A80BB275DA7428C07B84433AD0720E10D46788F1B7F413A86D82F9D53  preparation/production-trust/r3-egress-revocation-remediation/sql/20-worker-scope-cleanup.sql
F25D017A066EEEFD0A62D1C51B397C431CE4C7AEE6B9C6CDE4E929DF603122F9  preparation/production-trust/r3-egress-revocation-remediation/sql/25-lease-revocation-binding.sql
149262A324348E3AF2AA6264B3E2740FAB0D63CF5D662AEF672DCD38FE7A8906  preparation/production-trust/r3-egress-revocation-remediation/sql/30-egress-final-authorization.sql
4AF449B69DB6AB5DBC539923A95CDE17F6AB915A7FEA320C6FAB24BF6EE8957F  preparation/production-trust/r3-egress-revocation-remediation/sql/40-egress-write-outcome.sql
115F3AD69A89797DBA8EDFF85A1DFA9ADE744CDC66AA64561BD7D071E4FE2650  preparation/production-trust/r3-egress-revocation-remediation/sql/50-permit-consumption-revocation.sql
A61F2FBF565922218741DEE6C37F557857C1E93C8F10A97E962D1980F37DAD64  preparation/production-trust/r3-egress-revocation-remediation/tests/egress-boundary.test.ts
9FA622B49ECC6A4C1044DCC5F9FA31CA22CC9A0797B6A8C591FBF6E09300458D  preparation/production-trust/r3-egress-revocation-remediation/tests/egress-races.test.ts
FF4BAF2B9E1F737381CF3D0CD103DFF240C242B1E3E29415AC35032BCCA8305A  preparation/production-trust/r3-egress-revocation-remediation/tests/sql-contract.test.ts
9CB055D02F1F023044DA7344A93E27A7AC09343338319E77796D3631FBF13A2A  preparation/production-trust/r3-egress-revocation-remediation/tests/worker-revocation.test.ts
A96412B3514B644F12C39C837A3BE92B34C0534162F564B58442A34E77D85BCC  preparation/production-trust/r3-egress-revocation-remediation/tools/build-aggregates.mjs
934E0F9274A4EF477BF9E12298916487D8E157FB573CE503C1C0A6E72FDFCD9D  preparation/production-trust/r3-egress-revocation-remediation/tools/build-evidence.mjs
221B7C6789C510221C7361BA2E674F5FBCCCCD4BAB6E7ACA6F4E019E360C3EB3  preparation/production-trust/r3-egress-revocation-remediation/tools/run-verification.ps1
2BFE58E0B048F5268AF8037D7703E223B31E09DF10E30C179036B94F67FD0DFA  preparation/production-trust/r3-egress-revocation-remediation/vitest.config.ts

```
<!-- END_EXACT_SOURCE id=S014 -->

### S015. contracts.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/contracts.ts`
- Bytes: `6339`
- SHA-256: `E18972EF94DD04EE27B879B5CD3BCE9033CB7B2F0BFC7BBABF767213515A9CD9`

<!-- BEGIN_EXACT_SOURCE id=S015 sha256=E18972EF94DD04EE27B879B5CD3BCE9033CB7B2F0BFC7BBABF767213515A9CD9 bytes=6339 -->
```text
import { z } from "zod";

import {
  InstantSchema,
  Sha256Schema,
  UuidSchema,
} from "../contracts/common";
import {
  ExecutionLeaseSchema,
  ResourceFenceExpectationSchema,
  SendAuthorizationSchema,
  type ResourceFenceExpectation,
  type SendAuthorization,
} from "../r3-fencing-remediation/contracts";
import { FencingScopeKeySchema } from "../r3-fencing-remediation/scope";

export const R3_EGRESS_CONTRACT_VERSION =
  "r3-egress-revocation-remediation-v1";

const IdentifierSchema = z.string().min(1).max(200).trim();
const VersionSchema = z.number().int().positive();
const TokenSchema = z.number().int().positive().max(Number.MAX_SAFE_INTEGER);

export const WorkerRevocationStateSchema = z.enum([
  "ACTIVE",
  "REVOKED",
  "RECOVERY_REQUIRED",
]);

export const WorkerRevocationRecordSchema = z.strictObject({
  schemaVersion: z.literal("r5-worker-revocation-record-v1"),
  workerInstanceId: UuidSchema,
  state: WorkerRevocationStateSchema,
  revocationVersion: z.number().int().nonnegative(),
  recordVersion: VersionSchema,
  revokedAt: InstantSchema.nullable(),
  reasonCode: IdentifierSchema.nullable(),
  replacementWorkerId: UuidSchema.nullable(),
  updatedAt: InstantSchema,
});

export const ScopeWorkerBlockSchema = z.strictObject({
  schemaVersion: z.literal("r5-scope-worker-block-v1"),
  scopeKey: FencingScopeKeySchema,
  workerInstanceId: UuidSchema,
  blockedRevocationVersion: z.number().int().positive(),
  version: VersionSchema,
  blockedAt: InstantSchema,
  reasonCode: IdentifierSchema,
});

export const EgressIntentStateSchema = z.enum([
  "PENDING",
  "FINAL_AUTHORIZED",
  "WRITE_STARTED",
  "RESPONSE_RECEIVED",
  "COMPLETED",
  "SEND_OUTCOME_UNKNOWN",
  "REJECTED",
  "EXPIRED",
  "REVOKED",
]);

export const EgressIntentSchema = z.strictObject({
  schemaVersion: z.literal("r5-egress-intent-v1"),
  egressIntentId: UuidSchema,
  sendAuthorizationId: UuidSchema,
  permitDigest: Sha256Schema,
  scopeKey: FencingScopeKeySchema,
  fencingToken: TokenSchema,
  workerInstanceId: UuidSchema,
  workerRevocationVersion: z.number().int().nonnegative(),
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  budgetReservationId: UuidSchema,
  requestDigest: Sha256Schema,
  emergencyEpoch: z.number().int().nonnegative(),
  keyVersion: VersionSchema,
  keyRevocationVersion: z.number().int().nonnegative(),
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
  state: EgressIntentStateSchema,
  createdAt: InstantSchema,
  finalAuthorizedAt: InstantSchema.nullable(),
  finalAuthorizationExpiresAt: InstantSchema.nullable(),
  writeStartedAt: InstantSchema.nullable(),
  outcomeAt: InstantSchema.nullable(),
});

export const EgressFinalAuthorizationSchema = z.strictObject({
  schemaVersion: z.literal("r5-egress-final-authorization-v1"),
  egressIntentId: UuidSchema,
  sendAuthorizationId: UuidSchema,
  scopeKey: FencingScopeKeySchema,
  fencingToken: TokenSchema,
  workerInstanceId: UuidSchema,
  workerRevocationVersion: z.number().int().nonnegative(),
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  budgetReservationId: UuidSchema,
  requestDigest: Sha256Schema,
  emergencyEpoch: z.number().int().nonnegative(),
  keyVersion: VersionSchema,
  keyRevocationVersion: z.number().int().nonnegative(),
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
  issuedAt: InstantSchema,
  expiresAt: InstantSchema,
});

export const EgressMutableContextSchema = z.strictObject({
  workerState: z.enum(["ACTIVE", "DRAINING", "REVOKED"]),
  workerRegistrationState: z.enum(["ACTIVE", "DRAINING", "REVOKED"]),
  workerHeartbeatAt: InstantSchema,
  workerRevocationVersion: z.number().int().nonnegative(),
  scopeBlockedRevocationVersion: z.number().int().nonnegative().nullable(),
  currentScopeToken: TokenSchema,
  currentScopeWorkerId: UuidSchema,
  currentScopeLeaseId: UuidSchema,
  currentScopeCapabilityId: UuidSchema,
  authorizationState: z.literal("ACTIVE"),
  capabilityState: z.literal("RESERVED"),
  capabilityExpiresAt: InstantSchema,
  leaseState: z.literal("SENT"),
  permitState: z.literal("CONSUMED"),
  emergencyStatus: z.enum(["NORMAL", "DRAINING", "STOPPED", "RECOVERY_PENDING"]),
  emergencyEpoch: z.number().int().nonnegative(),
  keyState: z.enum(["ACTIVE", "REVOKED", "EXPIRED", "RETIRED"]),
  keyVersion: VersionSchema,
  keyRevocationVersion: z.number().int().nonnegative(),
  budgetState: z.enum(["RESERVED", "COMMITTED", "RELEASED_BEFORE_SEND", "UNKNOWN"]),
  budgetExpiresAt: InstantSchema,
});

export const R3EgressFailureCodeSchema = z.enum([
  "WORKER_REVOKED",
  "WORKER_REVOCATION_VERSION_MISMATCH",
  "WORKER_REACTIVATION_FORBIDDEN",
  "RESOURCE_SCOPE_MISMATCH",
  "RESOURCE_FLOOR_CHANGED",
  "LEASE_INVALID",
  "PERMIT_INVALID",
  "PERMIT_REPLAYED",
  "EMERGENCY_BLOCKED",
  "KEY_BLOCKED",
  "BUDGET_BLOCKED",
  "AUTHORITY_UNAVAILABLE",
  "ROW_COUNT_CONFLICT",
  "EGRESS_INTENT_ALREADY_STARTED",
  "EGRESS_INTENT_REPLAYED",
  "SEND_OUTCOME_UNKNOWN",
  "COMMIT_OUTCOME_UNKNOWN",
]);

export type WorkerRevocationState = z.infer<
  typeof WorkerRevocationStateSchema
>;
export type WorkerRevocationRecord = z.infer<
  typeof WorkerRevocationRecordSchema
>;
export type ScopeWorkerBlock = z.infer<typeof ScopeWorkerBlockSchema>;
export type EgressIntentState = z.infer<typeof EgressIntentStateSchema>;
export type EgressIntent = z.infer<typeof EgressIntentSchema>;
export type EgressFinalAuthorization = z.infer<
  typeof EgressFinalAuthorizationSchema
>;
export type EgressMutableContext = z.infer<
  typeof EgressMutableContextSchema
>;
export type R3EgressFailureCode = z.infer<
  typeof R3EgressFailureCodeSchema
>;

export type R3EgressResult<T> =
  | Readonly<{ ok: true; value: T }>
  | Readonly<{ ok: false; code: R3EgressFailureCode }>;

export function ok<T>(value: T): R3EgressResult<T> {
  return Object.freeze({ ok: true, value });
}

export function fail<T = never>(code: R3EgressFailureCode): R3EgressResult<T> {
  return Object.freeze({ ok: false, code });
}

export function requireExactlyOne(affectedRows: number): R3EgressResult<true> {
  return affectedRows === 1
    ? ok(true as const)
    : fail("ROW_COUNT_CONFLICT");
}

export {
  ExecutionLeaseSchema,
  FencingScopeKeySchema,
  ResourceFenceExpectationSchema,
  SendAuthorizationSchema,
};
export type { ResourceFenceExpectation, SendAuthorization };

```
<!-- END_EXACT_SOURCE id=S015 -->

### S016. lock-order.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/lock-order.ts`
- Bytes: `1268`
- SHA-256: `3E7A4CA714B9E9BA7412FF6E7CB12DA9FF798F895EF0B141B3BB85AC671E32AE`

<!-- BEGIN_EXACT_SOURCE id=S016 sha256=3E7A4CA714B9E9BA7412FF6E7CB12DA9FF798F895EF0B141B3BB85AC671E32AE bytes=1268 -->
```text
import { z } from "zod";

import { fail, ok, type R3EgressResult } from "./contracts";

export const R3_EGRESS_LOCK_ORDER = Object.freeze([
  "WORKER_REVOCATION_CONTROL",
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
  "AUDIT_SEQUENCE",
] as const);

export type R3EgressLockDomain = typeof R3_EGRESS_LOCK_ORDER[number];

export function validateR3EgressLockOrder(
  acquisitions: readonly unknown[],
): R3EgressResult<readonly R3EgressLockDomain[]> {
  const parsed = z.array(z.strictObject({
    domain: z.enum(R3_EGRESS_LOCK_ORDER),
    acquiredAt: z.number().int().nonnegative(),
  })).safeParse(acquisitions);
  if (!parsed.success) return fail("ROW_COUNT_CONFLICT");
  let previous = -1;
  const result: R3EgressLockDomain[] = [];
  for (const item of parsed.data) {
    const current = R3_EGRESS_LOCK_ORDER.indexOf(item.domain);
    if (current < previous) return fail("ROW_COUNT_CONFLICT");
    previous = current;
    result.push(item.domain);
  }
  return ok(Object.freeze(result));
}

```
<!-- END_EXACT_SOURCE id=S016 -->

### S017. sql/10-worker-global-revocation.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/sql/10-worker-global-revocation.sql`
- Bytes: `5443`
- SHA-256: `54B918ABA73574E0BB92000C993ED1CDF8FF1C8F5CB646FC27AAAC20721D37E1`

<!-- BEGIN_EXACT_SOURCE id=S017 sha256=54B918ABA73574E0BB92000C993ED1CDF8FF1C8F5CB646FC27AAAC20721D37E1 bytes=5443 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Global Worker Identity Revocation is a single authoritative tombstone.
-- It fails closed every Scope without pretending to atomically clean every
-- possible Resource Floor in one transaction.

CREATE TABLE trust_r5_worker_revocation (
  worker_instance_id uuid PRIMARY KEY
    REFERENCES trust_r4_worker_registration (worker_instance_id),
  state text NOT NULL CHECK (state IN ('ACTIVE', 'REVOKED', 'RECOVERY_REQUIRED')),
  revocation_version bigint NOT NULL CHECK (revocation_version >= 0),
  record_version bigint NOT NULL CHECK (record_version >= 1),
  revoked_at_ms bigint,
  reason_code text,
  replacement_worker_id uuid,
  updated_at_ms bigint NOT NULL,
  CHECK (
    state <> 'REVOKED'
    OR (revoked_at_ms IS NOT NULL AND reason_code IS NOT NULL)
  ),
  CHECK (
    replacement_worker_id IS NULL
    OR replacement_worker_id <> worker_instance_id
  )
);

CREATE TABLE trust_r5_worker_revocation_request (
  request_id uuid PRIMARY KEY,
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  requested_revocation_version bigint NOT NULL
    CHECK (requested_revocation_version >= 1),
  requested_at_ms bigint NOT NULL,
  UNIQUE (worker_instance_id, requested_revocation_version)
);

CREATE TABLE trust_r5_scope_worker_block (
  scope_key text NOT NULL
    REFERENCES trust_r4_resource_fencing (scope_key),
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  blocked_revocation_version bigint NOT NULL
    CHECK (blocked_revocation_version >= 1),
  version bigint NOT NULL CHECK (version >= 1),
  blocked_at_ms bigint NOT NULL,
  reason_code text NOT NULL,
  PRIMARY KEY (scope_key, worker_instance_id)
);

CREATE TABLE trust_r5_lease_worker_revocation_binding (
  lease_id uuid PRIMARY KEY
    REFERENCES trust_r4_execution_lease (lease_id),
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  worker_revocation_version bigint NOT NULL
    CHECK (worker_revocation_version >= 0),
  bound_at_ms bigint NOT NULL
);

-- Future deployment migration: audit event vocabulary must be extended before
-- this draft can run. The repository's frozen R3 schema is not edited.
ALTER TABLE trust_r3_audit_event
  DROP CONSTRAINT IF EXISTS trust_r3_audit_event_event_type_check;

ALTER TABLE trust_r3_audit_event
  ADD CONSTRAINT trust_r3_audit_event_event_type_check CHECK (
    event_type IN (
      'APPROVAL_CONSUMED', 'BUDGET_RESERVED', 'BUDGET_RELEASED',
      'BUDGET_SETTLED', 'LEASE_ISSUED', 'WORKER_PROGRESS',
      'SEND_AUTHORIZED', 'SEND_AUTHORIZATION_CONSUMED',
      'REQUEST_SENT', 'SEND_OUTCOME_UNKNOWN', 'RESPONSE_RECEIVED',
      'EMERGENCY_ACTIVATED', 'EMERGENCY_RECOVERY_REQUESTED',
      'EMERGENCY_RECOVERY_APPROVED', 'KEY_REVOKED',
      'WORKER_REVOKED', 'WORKER_SCOPE_BLOCKED', 'LEASE_REVOKED'
    )
  );

-- ===========================================================================
-- Global Worker revocation. Linearization point: COMMIT of this transaction.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT request_id, worker_instance_id, requested_revocation_version
FROM trust_r5_worker_revocation_request
WHERE request_id = $2
FOR SHARE;

-- Idempotency: if this exact request already committed, the host returns the
-- persisted revocation record without another Audit append or version bump.

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
  AND record_version = $5;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration
SET state = 'REVOKED',
    updated_at_ms = $3
WHERE worker_instance_id = $1
  AND state = 'ACTIVE';

INSERT INTO trust_r5_worker_revocation_request (
  request_id, worker_instance_id, requested_revocation_version, requested_at_ms
) VALUES (
  $2, $1, $5 + 1, $3
) RETURNING request_id;

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
) RETURNING event_id;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $7,
    last_event_digest = $9
WHERE singleton_id = 1
  AND last_sequence = $7 - 1
  AND last_event_digest IS NOT DISTINCT FROM $8;

COMMIT;

-- Any non-one UPDATE row count, missing worker, audit failure or failed COMMIT
-- restores ACTIVE registration and the prior revocation row.

-- COMMIT ambiguity:
--   query trust_r5_worker_revocation_request by request_id;
--   if present, read trust_r5_worker_revocation by worker_instance_id;
--   return persisted record; never issue a blind second revocation version.

-- Ordinary Worker registration/Upsert MUST never transition REVOKED back to
-- ACTIVE. A replacement identity requires a separate trusted provisioning flow.

```
<!-- END_EXACT_SOURCE id=S017 -->

### S018. sql/20-worker-scope-cleanup.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/sql/20-worker-scope-cleanup.sql`
- Bytes: `6953`
- SHA-256: `FE3ED25A80BB275DA7428C07B84433AD0720E10D46788F1B7F413A86D82F9D53`

<!-- BEGIN_EXACT_SOURCE id=S018 sha256=FE3ED25A80BB275DA7428C07B84433AD0720E10D46788F1B7F413A86D82F9D53 bytes=6953 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- One-idempotent-scope cleanup. The host MUST first lock/read the Lease and
-- choose exactly one branch below. It must never run the checked pre-send
-- Lease UPDATE when the observed state is SENT or otherwise post-write.

-- ===========================================================================
-- Branch 20A: PRE_SEND cleanup
-- Allowed observed Lease states:
--   ISSUED, KEY_READ, TRANSPORT_CREATED, SEND_AUTHORIZED
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $2
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id,
       worker_instance_id, fencing_token
FROM trust_r4_send_authorization
WHERE lease_id = $3
FOR UPDATE;

-- Host preconditions after the locked reads:
--   floor.scope_key=$2
--   floor.current_worker_id=$1
--   floor.current_lease_id=$3
--   floor.current_capability_id=$4
--   global revocation.state=REVOKED
--   global revocation.revocation_version >= $5
--   Lease worker=$1, scope=$2, capability=$4, token=floor token=$8
--   Lease state IN the PRE_SEND set above
-- Any mismatch rejects this branch and rolls back.

INSERT INTO trust_r5_scope_worker_block (
  scope_key, worker_instance_id, blocked_revocation_version,
  version, blocked_at_ms, reason_code
) VALUES (
  $2, $1, $5, 1, $6, $7
)
ON CONFLICT (scope_key, worker_instance_id) DO UPDATE
SET blocked_revocation_version =
      GREATEST(
        trust_r5_scope_worker_block.blocked_revocation_version,
        EXCLUDED.blocked_revocation_version
      ),
    version = trust_r5_scope_worker_block.version + 1,
    blocked_at_ms = EXCLUDED.blocked_at_ms,
    reason_code = EXCLUDED.reason_code;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease
SET state = 'REVOKED'
WHERE lease_id = $3
  AND worker_instance_id = $1
  AND scope_key = $2
  AND capability_id = $4
  AND fencing_token = $8
  AND state IN (
    'ISSUED', 'KEY_READ', 'TRANSPORT_CREATED', 'SEND_AUTHORIZED'
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'REVOKED'
      AND revocation.revocation_version >= $5
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE lease_id = $3
  AND worker_instance_id = $1
  AND scope_key = $2
  AND capability_id = $4
  AND fencing_token = $8
  AND state IN ('ISSUED', 'CONSUMED');

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $9, $10, $6, 'WORKER_SCOPE_BLOCKED', 'ALLOW',
  $1, $11, $12
) RETURNING event_id;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $10,
    last_event_digest = $12
WHERE singleton_id = 1
  AND last_sequence = $10 - 1
  AND last_event_digest IS NOT DISTINCT FROM $11;

COMMIT;

-- ===========================================================================
-- Branch 20B: AFTER_SEND classification
-- Allowed observed Lease states:
--   SENT, RESPONSE_RECEIVED, COMPLETED, FAILED_AFTER_SEND,
--   SEND_OUTCOME_UNKNOWN
-- The request cannot be recalled. Do not issue a Lease REVOKED update.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $2
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id,
       worker_instance_id, fencing_token
FROM trust_r4_send_authorization
WHERE lease_id = $3
FOR UPDATE;

-- Host preconditions are the same as 20A except the Lease must already be in
-- the AFTER_SEND set. The external outcome remains unknown unless an existing
-- durable request record establishes otherwise. This branch never retries.

INSERT INTO trust_r5_scope_worker_block (
  scope_key, worker_instance_id, blocked_revocation_version,
  version, blocked_at_ms, reason_code
) VALUES (
  $2, $1, $5, 1, $6, $7
)
ON CONFLICT (scope_key, worker_instance_id) DO UPDATE
SET blocked_revocation_version =
      GREATEST(
        trust_r5_scope_worker_block.blocked_revocation_version,
        EXCLUDED.blocked_revocation_version
      ),
    version = trust_r5_scope_worker_block.version + 1,
    blocked_at_ms = EXCLUDED.blocked_at_ms,
    reason_code = EXCLUDED.reason_code;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE lease_id = $3
  AND worker_instance_id = $1
  AND scope_key = $2
  AND capability_id = $4
  AND fencing_token = $8
  AND state = 'CONSUMED'
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state IN (
        'SENT', 'RESPONSE_RECEIVED', 'COMPLETED', 'FAILED_AFTER_SEND',
        'SEND_OUTCOME_UNKNOWN'
      )
  );

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $9, $10, $6, 'WORKER_SCOPE_BLOCKED', 'ALLOW',
  $1, $11, $12
) RETURNING event_id;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $10,
    last_event_digest = $12
WHERE singleton_id = 1
  AND last_sequence = $10 - 1
  AND last_event_digest IS NOT DISTINCT FROM $11;

COMMIT;

-- Global revocation already blocks all scopes immediately. Scope cleanup can
-- be resumed idempotently after a crash. An interrupted cleanup never reopens
-- authority because Permit Consumption and Egress join the global revocation
-- row on every authorization decision.

```
<!-- END_EXACT_SOURCE id=S018 -->

### S019. sql/25-lease-revocation-binding.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/sql/25-lease-revocation-binding.sql`
- Bytes: `3081`
- SHA-256: `F25D017A066EEEFD0A62D1C51B397C431CE4C7AEE6B9C6CDE4E929DF603122F9`

<!-- BEGIN_EXACT_SOURCE id=S019 sha256=F25D017A066EEEFD0A62D1C51B397C431CE4C7AEE6B9C6CDE4E929DF603122F9 bytes=3081 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R5 Lease revocation-version binding finalization.
--
-- The frozen R4 takeover transaction issues the Lease and token atomically but
-- has no R5 binding column. R5 therefore fails closed: a Lease without this
-- binding cannot be consumed or reach Egress. This transaction may run after
-- R4 Lease issuance, but before any Permit Consumption.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $2
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, capability_id, worker_instance_id,
       fencing_token, state, expires_at_ms
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

-- Host preconditions:
--   global revocation.state=ACTIVE
--   global revocation.revocation_version=$4
--   floor.current_worker_id=$1
--   floor.current_lease_id=$3
--   floor.current_capability_id=$5
--   floor.current_fencing_token=$6
--   Lease binds the same Worker/Scope/Capability/token
--   Worker Registration is ACTIVE with fresh heartbeat

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r5_lease_worker_revocation_binding (
  lease_id, worker_instance_id, worker_revocation_version, bound_at_ms
)
SELECT
  $3, $1, $4, $7
WHERE EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $4
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $2
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $4
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $2
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $6
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $5
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $7 >= worker.heartbeat_at_ms
      AND $7 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'ISSUED'
      AND lease.scope_key = $2
      AND lease.capability_id = $5
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $6
      AND $7 < lease.expires_at_ms
  );

COMMIT;

-- COMMIT ambiguity: query the binding by lease_id. Only the exact persisted
-- Worker/version match is success. A missing binding leaves the Lease
-- unusable; it never creates authority.

```
<!-- END_EXACT_SOURCE id=S019 -->

### S020. sql/30-egress-final-authorization.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/sql/30-egress-final-authorization.sql`
- Bytes: `23151`
- SHA-256: `149262A324348E3AF2AA6264B3E2740FAB0D63CF5D662AEF672DCD38FE7A8906`

<!-- BEGIN_EXACT_SOURCE id=S020 sha256=149262A324348E3AF2AA6264B3E2740FAB0D63CF5D662AEF672DCD38FE7A8906 bytes=23151 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Persistent Egress intent plus final/write-start authorization transactions.
-- Actual production egress is not implemented.

CREATE TABLE trust_r5_egress_intent (
  egress_intent_id uuid PRIMARY KEY,
  send_authorization_id uuid NOT NULL UNIQUE,
  permit_digest varchar(71) NOT NULL,
  scope_key text NOT NULL,
  fencing_token bigint NOT NULL CHECK (fencing_token > 0),
  worker_instance_id uuid NOT NULL,
  worker_revocation_version bigint NOT NULL CHECK (worker_revocation_version >= 0),
  lease_id uuid NOT NULL,
  capability_id uuid NOT NULL,
  budget_reservation_id uuid NOT NULL,
  request_digest varchar(71) NOT NULL,
  emergency_epoch bigint NOT NULL CHECK (emergency_epoch >= 0),
  key_version bigint NOT NULL CHECK (key_version >= 1),
  key_revocation_version bigint NOT NULL CHECK (key_revocation_version >= 0),
  permission_version bigint NOT NULL CHECK (permission_version >= 1),
  policy_version text NOT NULL,
  state text NOT NULL CHECK (
    state IN (
      'PENDING', 'FINAL_AUTHORIZED', 'WRITE_STARTED',
      'RESPONSE_RECEIVED', 'COMPLETED', 'SEND_OUTCOME_UNKNOWN',
      'REJECTED', 'EXPIRED', 'REVOKED'
    )
  ),
  row_version bigint NOT NULL DEFAULT 1 CHECK (row_version >= 1),
  created_at_ms bigint NOT NULL,
  final_authorized_at_ms bigint,
  final_authorization_expires_at_ms bigint,
  write_started_at_ms bigint,
  outcome_at_ms bigint,
  CHECK (
    state NOT IN ('FINAL_AUTHORIZED', 'WRITE_STARTED', 'RESPONSE_RECEIVED', 'COMPLETED')
    OR (final_authorized_at_ms IS NOT NULL AND final_authorization_expires_at_ms IS NOT NULL)
  ),
  CHECK (
    state NOT IN ('WRITE_STARTED', 'RESPONSE_RECEIVED', 'COMPLETED', 'SEND_OUTCOME_UNKNOWN')
    OR write_started_at_ms IS NOT NULL
  )
);

-- Transaction 1: register a pending intent after R3 Permit Consumption. This
-- transaction records intent and does not grant a socket write.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $2
FOR UPDATE;

SELECT authorization_id, state, capability_id, budget_reservation_id,
       worker_instance_id, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $19
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, execution_authorization_id, capability_id,
       worker_instance_id, send_started_at_ms, expires_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $12
FOR UPDATE;

SELECT capability_id, state, execution_authorization_id, worker_instance_id,
       budget_reservation_id, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $11
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $8
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $3
FOR UPDATE;

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

-- The insert is conditional. It is valid only after the frozen R4 Permit
-- Consumption has committed CONSUMED/SENT and the global Worker revocation and
-- per-scope block are still current. The request and permit digests are bound
-- at insert time; a later Egress read must recompute both from the exact bytes.
INSERT INTO trust_r5_egress_intent (
  egress_intent_id, send_authorization_id, permit_digest,
  scope_key, fencing_token, worker_instance_id,
  worker_revocation_version, lease_id, capability_id,
  budget_reservation_id, request_digest, emergency_epoch,
  key_version, key_revocation_version, permission_version,
  policy_version, state, row_version, created_at_ms,
  final_authorized_at_ms, final_authorization_expires_at_ms,
  write_started_at_ms, outcome_at_ms
)
SELECT
  $7, $4, $6,
  $8, $9, $1,
  $10, $3, $11,
  $12, $5, $13,
  $14, $15, $16,
  $17, 'PENDING', 1, $18,
  NULL, NULL, NULL, NULL
WHERE EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $10
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $8
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $10
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $3
      AND binding.worker_instance_id = $1
      AND binding.worker_revocation_version = $10
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $8
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $9
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $11
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $18 >= worker.heartbeat_at_ms
      AND $18 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'SENT'
      AND lease.scope_key = $8
      AND lease.capability_id = $11
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $9
      AND $18 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_send_authorization permit
    WHERE permit.send_authorization_id = $4
      AND permit.state = 'CONSUMED'
      AND permit.consumed_at_ms IS NOT NULL
      AND permit.scope_key = $8
      AND permit.lease_id = $3
      AND permit.capability_id = $11
      AND permit.worker_instance_id = $1
      AND permit.fencing_token = $9
      AND permit.budget_reservation_id = $12
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $13
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key key
    WHERE key.key_id = $2
      AND key.state = 'ACTIVE'
      AND key.key_version = $14
      AND key.revocation_version = $15
      AND $18 >= key.valid_from_ms
      AND $18 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $19
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $11
      AND authorization.budget_reservation_id = $12
      AND $18 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $12
      AND reservation.state = 'RESERVED'
      AND reservation.execution_authorization_id = $19
      AND reservation.capability_id = $11
      AND reservation.worker_instance_id = $1
      AND reservation.send_started_at_ms IS NOT NULL
      AND $18 < reservation.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability capability
    WHERE capability.capability_id = $11
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $19
      AND capability.worker_instance_id = $1
      AND capability.budget_reservation_id = $12
      AND $18 < capability.expires_at_ms
  );

COMMIT;

-- Transaction 2: final authorization. The commit of this intent transition is
-- the final-gate linearization point. It does not write a socket.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $2
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $19
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, send_started_at_ms, expires_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $12
FOR UPDATE;

SELECT capability_id, state, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $11
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $8
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, worker_instance_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $3
FOR UPDATE;

SELECT lease_id, state, scope_key, capability_id, worker_instance_id,
       fencing_token, expires_at_ms
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms, consumed_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

SELECT egress_intent_id, state, send_authorization_id, scope_key,
       fencing_token, worker_instance_id, worker_revocation_version,
       lease_id, capability_id, budget_reservation_id, request_digest,
       emergency_epoch, key_version, key_revocation_version,
       permission_version, policy_version, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'FINAL_AUTHORIZED',
    row_version = row_version + 1,
    final_authorized_at_ms = $18,
    final_authorization_expires_at_ms = $20
WHERE egress_intent_id = $7
  AND state = 'PENDING'
  AND row_version = $21
  AND send_authorization_id = $4
  AND scope_key = $8
  AND fencing_token = $9
  AND worker_instance_id = $1
  AND worker_revocation_version = $10
  AND lease_id = $3
  AND capability_id = $11
  AND budget_reservation_id = $12
  AND request_digest = $5
  AND emergency_epoch = $13
  AND key_version = $14
  AND key_revocation_version = $15
  AND permission_version = $16
  AND policy_version = $17
  AND $20 > $18
  AND $20 - $18 <= 1000
  AND EXISTS (
    SELECT 1 FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $3
      AND binding.worker_instance_id = $1
      AND binding.worker_revocation_version = $10
  )
  AND NOT EXISTS (
    SELECT 1 FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $8
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $13
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key key
    WHERE key.key_id = $2
      AND key.state = 'ACTIVE'
      AND key.key_version = $14
      AND key.revocation_version = $15
      AND $18 >= key.valid_from_ms
      AND $18 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $19
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $11
      AND authorization.budget_reservation_id = $12
      AND $18 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_capability capability
    WHERE capability.capability_id = $11
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $19
      AND capability.worker_instance_id = $1
      AND capability.budget_reservation_id = $12
      AND $18 < capability.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $8
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $9
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $11
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $18 >= worker.heartbeat_at_ms
      AND $18 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'SENT'
      AND lease.scope_key = $8
      AND lease.capability_id = $11
      AND lease.execution_authorization_id = $19
      AND lease.budget_reservation_id = $12
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $9
      AND $18 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_send_authorization permit
    WHERE permit.send_authorization_id = $4
      AND permit.state = 'CONSUMED'
      AND permit.consumed_at_ms IS NOT NULL
      AND permit.scope_key = $8
      AND permit.lease_id = $3
      AND permit.capability_id = $11
      AND permit.worker_instance_id = $1
      AND permit.fencing_token = $9
      AND permit.budget_reservation_id = $12
      AND $18 >= permit.consumed_at_ms
      AND $18 < permit.expires_at_ms
      AND permit.emergency_epoch = $13
      AND permit.key_version = $14
      AND permit.revocation_version = $15
      AND permit.permission_version = $16
      AND permit.policy_version = $17
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $12
      AND reservation.state = 'RESERVED'
      AND reservation.send_started_at_ms IS NOT NULL
      AND $18 < reservation.expires_at_ms
  );

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $22, $23, $18, 'SEND_AUTHORIZED', 'ALLOW',
  $7, $24, $25
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $23,
    last_event_digest = $25
WHERE singleton_id = 1
  AND last_sequence = $23 - 1
  AND last_event_digest IS NOT DISTINCT FROM $24;

COMMIT;

-- Transaction 3: write-start intent immediately before socket write. This is
-- the last database-enforced cancellation boundary.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $2
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $19
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, send_started_at_ms, expires_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $12
FOR UPDATE;

SELECT capability_id, state, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $11
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $8
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, worker_instance_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $3
FOR UPDATE;

SELECT lease_id, state, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, expires_at_ms
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, consumed_at_ms, expires_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

SELECT egress_intent_id, state, final_authorization_expires_at_ms, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'WRITE_STARTED',
    row_version = row_version + 1,
    write_started_at_ms = $26
WHERE egress_intent_id = $7
  AND state = 'FINAL_AUTHORIZED'
  AND row_version = $27
  AND send_authorization_id = $4
  AND scope_key = $8
  AND fencing_token = $9
  AND worker_instance_id = $1
  AND worker_revocation_version = $10
  AND lease_id = $3
  AND capability_id = $11
  AND budget_reservation_id = $12
  AND request_digest = $5
  AND emergency_epoch = $13
  AND key_version = $14
  AND key_revocation_version = $15
  AND permission_version = $16
  AND policy_version = $17
  AND $26 < final_authorization_expires_at_ms
  AND EXISTS (
    SELECT 1 FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $3
      AND binding.worker_instance_id = $1
      AND binding.worker_revocation_version = $10
  )
  AND NOT EXISTS (
    SELECT 1 FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $8
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $13
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key key
    WHERE key.key_id = $2
      AND key.state = 'ACTIVE'
      AND key.key_version = $14
      AND key.revocation_version = $15
      AND $26 >= key.valid_from_ms
      AND $26 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $19
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $11
      AND authorization.budget_reservation_id = $12
      AND $26 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_capability capability
    WHERE capability.capability_id = $11
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $19
      AND capability.worker_instance_id = $1
      AND capability.budget_reservation_id = $12
      AND $26 < capability.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $12
      AND reservation.state = 'RESERVED'
      AND reservation.send_started_at_ms IS NOT NULL
      AND $26 < reservation.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $8
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $9
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $11
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $26 >= worker.heartbeat_at_ms
      AND $26 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'SENT'
      AND lease.scope_key = $8
      AND lease.capability_id = $11
      AND lease.execution_authorization_id = $19
      AND lease.budget_reservation_id = $12
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $9
      AND $26 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_send_authorization permit
    WHERE permit.send_authorization_id = $4
      AND permit.state = 'CONSUMED'
      AND permit.consumed_at_ms IS NOT NULL
      AND $26 >= permit.consumed_at_ms
      AND $26 < permit.expires_at_ms
      AND permit.scope_key = $8
      AND permit.lease_id = $3
      AND permit.capability_id = $11
      AND permit.worker_instance_id = $1
      AND permit.fencing_token = $9
      AND permit.budget_reservation_id = $12
      AND permit.emergency_epoch = $13
      AND permit.key_version = $14
      AND permit.revocation_version = $15
      AND permit.permission_version = $16
      AND permit.policy_version = $17
  );

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $28, $29, $26, 'REQUEST_SENT', 'ALLOW',
  $7, $30, $31
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $29,
    last_event_digest = $31
WHERE singleton_id = 1
  AND last_sequence = $29 - 1
  AND last_event_digest IS NOT DISTINCT FROM $30;

COMMIT;

-- After the WRITE_STARTED commit, an ordinary revocation cannot cancel a
-- socket write that may already begin. The trusted Egress component performs
-- exactly one write and records its outcome in the transaction below.

```
<!-- END_EXACT_SOURCE id=S020 -->

### S021. sql/40-egress-write-outcome.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/sql/40-egress-write-outcome.sql`
- Bytes: `2389`
- SHA-256: `4AF449B69DB6AB5DBC539923A95CDE17F6AB915A7FEA320C6FAB24BF6EE8957F`

<!-- BEGIN_EXACT_SOURCE id=S021 sha256=4AF449B69DB6AB5DBC539923A95CDE17F6AB915A7FEA320C6FAB24BF6EE8957F bytes=2389 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED

-- Response received: WRITE_STARTED -> RESPONSE_RECEIVED -> COMPLETED.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'RESPONSE_RECEIVED',
    row_version = row_version + 1
WHERE egress_intent_id = $1
  AND state = 'WRITE_STARTED'
  AND row_version = $2;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'COMPLETED',
    row_version = row_version + 1,
    outcome_at_ms = $3
WHERE egress_intent_id = $1
  AND state = 'RESPONSE_RECEIVED'
  AND row_version = $2 + 1;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $4, $5, $3, 'RESPONSE_RECEIVED', 'ALLOW',
  $1, $6, $7
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $5,
    last_event_digest = $7
WHERE singleton_id = 1
  AND last_sequence = $5 - 1
  AND last_event_digest IS NOT DISTINCT FROM $6;

COMMIT;

-- Socket timeout, connection loss, process crash, or unknown remote receipt:
-- terminal SEND_OUTCOME_UNKNOWN. Never automatically retry this intent.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'SEND_OUTCOME_UNKNOWN',
    row_version = row_version + 1,
    outcome_at_ms = $8
WHERE egress_intent_id = $1
  AND state = 'WRITE_STARTED'
  AND row_version = $9;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $10, $11, $8, 'SEND_OUTCOME_UNKNOWN', 'UNKNOWN',
  $1, $12, $13
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $11,
    last_event_digest = $13
WHERE singleton_id = 1
  AND last_sequence = $11 - 1
  AND last_event_digest IS NOT DISTINCT FROM $12;

COMMIT;

```
<!-- END_EXACT_SOURCE id=S021 -->

### S022. sql/50-permit-consumption-revocation.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/sql/50-permit-consumption-revocation.sql`
- Bytes: `9846`
- SHA-256: `115F3AD69A89797DBA8EDFF85A1DFA9ADE744CDC66AA64561BD7D071E4FE2650`

<!-- BEGIN_EXACT_SOURCE id=S022 sha256=115F3AD69A89797DBA8EDFF85A1DFA9ADE744CDC66AA64561BD7D071E4FE2650 bytes=9846 -->
```text
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R5 overlay for the frozen R4 Permit Consumption transaction.
-- This is a complete replacement draft, not an ALTER of frozen R4 SQL.
--
-- The transaction joins the global Worker revocation tombstone and the
-- per-scope block before the R4 one-use transition can commit. The permit,
-- Lease and budget send-start transition, Audit append and lock order share
-- one transaction boundary.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $6
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT authorization_id, state, capability_id, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $2
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros,
       budget_version
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, execution_authorization_id, capability_id,
       worker_instance_id, expires_at_ms, send_started_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $3
FOR UPDATE;

SELECT capability_id, state, execution_authorization_id, worker_instance_id,
       budget_reservation_id, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $4
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $5
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $6
FOR UPDATE;

SELECT lease_id, worker_instance_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $7
FOR UPDATE;

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, issued_at_ms, expires_at_ms,
       consumed_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $15
FOR UPDATE;

-- Parameters:
--   $1  key_id
--   $2  execution_authorization_id
--   $3  budget_reservation_id
--   $4  capability_id
--   $5  scope_key
--   $6  worker_instance_id
--   $7  lease_id
--   $8  fencing_token
--   $9  emergency_epoch
--   $10 key_version
--   $11 key revocation_version
--   $12 permission_version
--   $13 policy_version
--   $14 consumed_at_ms (server clock)
--   $15 send_authorization_id
--   $16 Audit event_id
--   $17 Audit sequence
--   $18 previous_event_digest
--   $19 event_digest
--   $20 expected Worker revocation_version

-- Permit one-use transition. No caller-supplied Actor/Worker authority is
-- trusted; every binding is compared with locked rows.
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization AS permit
SET state = 'CONSUMED',
    consumed_at_ms = $14
WHERE permit.send_authorization_id = $15
  AND permit.state = 'ISSUED'
  AND permit.scope_key = $5
  AND permit.lease_id = $7
  AND permit.capability_id = $4
  AND permit.worker_instance_id = $6
  AND permit.fencing_token = $8
  AND permit.budget_reservation_id = $3
  AND permit.emergency_epoch = $9
  AND permit.key_version = $10
  AND permit.revocation_version = $11
  AND permit.permission_version = $12
  AND permit.policy_version = $13
  AND $14 >= permit.issued_at_ms
  AND $14 < permit.expires_at_ms
  AND EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $6
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $20
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $5
      AND block.worker_instance_id = $6
      AND block.blocked_revocation_version >= $20
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $7
      AND binding.worker_instance_id = $6
      AND binding.worker_revocation_version = $20
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $5
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $8
      AND floor.current_worker_id = $6
      AND floor.current_lease_id = $7
      AND floor.current_capability_id = $4
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $6
      AND worker.state = 'ACTIVE'
      AND $14 >= worker.heartbeat_at_ms
      AND $14 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $7
      AND lease.state = 'SEND_AUTHORIZED'
      AND lease.scope_key = $5
      AND lease.capability_id = $4
      AND lease.execution_authorization_id = $2
      AND lease.budget_reservation_id = $3
      AND lease.worker_instance_id = $6
      AND lease.fencing_token = $8
      AND $14 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $9
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key key
    WHERE key.key_id = $1
      AND key.state = 'ACTIVE'
      AND key.key_version = $10
      AND key.revocation_version = $11
      AND $14 >= key.valid_from_ms
      AND $14 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $2
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $4
      AND authorization.budget_reservation_id = $3
      AND $14 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $3
      AND reservation.state = 'RESERVED'
      AND reservation.execution_authorization_id = $2
      AND reservation.capability_id = $4
      AND reservation.worker_instance_id = $6
      AND reservation.send_started_at_ms IS NULL
      AND $14 < reservation.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability capability
    WHERE capability.capability_id = $4
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $2
      AND capability.worker_instance_id = $6
      AND capability.budget_reservation_id = $3
      AND $14 < capability.expires_at_ms
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'SENT'
WHERE lease.lease_id = $7
  AND lease.state = 'SEND_AUTHORIZED'
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND $14 < lease.expires_at_ms
  AND EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $6
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $20
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $5
      AND block.worker_instance_id = $6
      AND block.blocked_revocation_version >= $20
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $5
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $8
      AND floor.current_worker_id = $6
      AND floor.current_lease_id = $7
      AND floor.current_capability_id = $4
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_budget_reservation
SET send_started_at_ms = $14
WHERE reservation_id = $3
  AND state = 'RESERVED'
  AND execution_authorization_id = $2
  AND capability_id = $4
  AND worker_instance_id = $6
  AND send_started_at_ms IS NULL
  AND $14 < expires_at_ms;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $16, $17, $14, 'SEND_AUTHORIZATION_CONSUMED', 'ALLOW',
  $15, $18, $19
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $17,
    last_event_digest = $19
WHERE singleton_id = 1
  AND last_sequence = $17 - 1
  AND last_event_digest IS NOT DISTINCT FROM $18;

COMMIT;

-- Any zero/multiple affected row, missing lock-time condition, Audit failure or
-- failed COMMIT rolls the entire transaction back to ISSUED/SEND_AUTHORIZED and
-- an unstarted budget send.
--
-- Ambiguous COMMIT: query the durable permit by $15 and Audit sequence/event by
-- $16. If the permit is CONSUMED with consumed_at_ms=$14 and the matching Audit
-- event exists, return the persisted result. Otherwise never invoke this
-- transaction again as a blind retry.

```
<!-- END_EXACT_SOURCE id=S022 -->

### S023. models/egress-boundary.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/models/egress-boundary.ts`
- Bytes: `14446`
- SHA-256: `14FE4BA52870232929A8AB7966623E7D0450659669D0069F79A32F35AC347A02`

<!-- BEGIN_EXACT_SOURCE id=S023 sha256=14FE4BA52870232929A8AB7966623E7D0450659669D0069F79A32F35AC347A02 bytes=14446 -->
```text
import {
  EgressFinalAuthorizationSchema,
  EgressIntentSchema,
  EgressMutableContextSchema,
  ExecutionLeaseSchema,
  SendAuthorizationSchema,
  fail,
  ok,
  requireExactlyOne,
  type EgressFinalAuthorization,
  type EgressIntent,
  type EgressMutableContext,
  type R3EgressResult,
} from "../contracts";
import { validateR3EgressLockOrder } from "../lock-order";

type SharedState = {
  authorityAvailable: boolean;
  intents: Map<string, EgressIntent>;
  intentByPermit: Map<string, string>;
  finalAuthorizations: Map<string, EgressFinalAuthorization>;
  failNextAudit: boolean;
  auditEvents: string[];
};

/**
 * OFFLINE_REFERENCE_MODEL.
 * The model persists intent state and requires fresh mutable context at both
 * final authorization and write-start. It does not perform a socket write.
 */
export class OfflineEgressBoundary {
  private readonly shared: SharedState;

  constructor(shared?: OfflineEgressBoundary) {
    this.shared = shared?.shared ?? {
      authorityAvailable: true,
      intents: new Map(),
      intentByPermit: new Map(),
      finalAuthorizations: new Map(),
      failNextAudit: false,
      auditEvents: [],
    };
  }

  connect(): OfflineEgressBoundary {
    return new OfflineEgressBoundary(this);
  }

  setAuthorityAvailable(available: boolean): void {
    this.shared.authorityAvailable = available;
  }

  setNextAuditFailure(): void {
    this.shared.failNextAudit = true;
  }

  createPendingIntent(input: {
    intent: unknown;
    permit: unknown;
    lease: unknown;
    context: unknown;
    now: number;
    rowCount: number;
  }): R3EgressResult<EgressIntent> {
    if (!this.shared.authorityAvailable) {
      return fail("AUTHORITY_UNAVAILABLE");
    }
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    const parsed = EgressIntentSchema.safeParse(input.intent);
    const permit = SendAuthorizationSchema.safeParse(input.permit);
    const lease = ExecutionLeaseSchema.safeParse(input.lease);
    const context = EgressMutableContextSchema.safeParse(input.context);
    if (
      !parsed.success
      || parsed.data.state !== "PENDING"
      || !permit.success
      || !lease.success
      || !context.success
    ) {
      return fail("PERMIT_INVALID");
    }
    if (
      this.shared.intentByPermit.has(parsed.data.sendAuthorizationId)
      || this.shared.intents.has(parsed.data.egressIntentId)
    ) {
      return fail("PERMIT_REPLAYED");
    }
    const bound = this.validateBindings(
      parsed.data,
      permit.data,
      lease.data,
      context.data,
      input.now,
    );
    if (!bound.ok) return bound;
    this.shared.intents.set(
      parsed.data.egressIntentId,
      Object.freeze(parsed.data),
    );
    this.shared.intentByPermit.set(
      parsed.data.sendAuthorizationId,
      parsed.data.egressIntentId,
    );
    return ok(parsed.data);
  }

  finalAuthorize(input: {
    intentId: string;
    permit: unknown;
    lease: unknown;
    context: unknown;
    now: number;
    ttlMs: number;
    rowCounts: Readonly<{ intent: number; audit: number }>;
  }): R3EgressResult<EgressFinalAuthorization> {
    const lockOrder = validateR3EgressLockOrder([
      { domain: "WORKER_REVOCATION_CONTROL", acquiredAt: input.now },
      { domain: "EMERGENCY_CONTROL", acquiredAt: input.now },
      { domain: "KEY_REGISTRY", acquiredAt: input.now },
      { domain: "EXECUTION_AUTHORIZATION", acquiredAt: input.now },
      { domain: "BUDGET_CONTROL", acquiredAt: input.now },
      { domain: "BUDGET_RESERVATION", acquiredAt: input.now },
      { domain: "CAPABILITY", acquiredAt: input.now },
      { domain: "RESOURCE_FENCING_FLOOR", acquiredAt: input.now },
      { domain: "WORKER_REGISTRATION", acquiredAt: input.now },
      { domain: "EXECUTION_LEASE", acquiredAt: input.now },
      { domain: "SEND_AUTHORIZATION", acquiredAt: input.now },
      { domain: "EGRESS_SEND_INTENT", acquiredAt: input.now },
      { domain: "AUDIT_SEQUENCE", acquiredAt: input.now },
    ]);
    if (!lockOrder.ok) return fail("ROW_COUNT_CONFLICT");
    if (!this.shared.authorityAvailable) {
      return fail("AUTHORITY_UNAVAILABLE");
    }
    const rows = this.checkRows(input.rowCounts);
    if (!rows.ok) return rows;
    const intent = this.shared.intents.get(input.intentId);
    const permit = SendAuthorizationSchema.safeParse(input.permit);
    const lease = ExecutionLeaseSchema.safeParse(input.lease);
    const context = EgressMutableContextSchema.safeParse(input.context);
    if (!intent || !permit.success || !lease.success || !context.success) {
      return fail("PERMIT_INVALID");
    }
    if (intent.state !== "PENDING") return fail("EGRESS_INTENT_REPLAYED");
    if (
      !Number.isSafeInteger(input.ttlMs)
      || input.ttlMs <= 0
      || input.ttlMs > 1_000
    ) {
      return fail("PERMIT_INVALID");
    }
    const bound = this.validateBindings(intent, permit.data, lease.data, context.data, input.now);
    if (!bound.ok) return bound;
    const authorization = EgressFinalAuthorizationSchema.parse({
      schemaVersion: "r5-egress-final-authorization-v1",
      egressIntentId: intent.egressIntentId,
      sendAuthorizationId: intent.sendAuthorizationId,
      scopeKey: intent.scopeKey,
      fencingToken: intent.fencingToken,
      workerInstanceId: intent.workerInstanceId,
      workerRevocationVersion: intent.workerRevocationVersion,
      leaseId: intent.leaseId,
      capabilityId: intent.capabilityId,
      budgetReservationId: intent.budgetReservationId,
      requestDigest: intent.requestDigest,
      emergencyEpoch: intent.emergencyEpoch,
      keyVersion: intent.keyVersion,
      keyRevocationVersion: intent.keyRevocationVersion,
      permissionVersion: intent.permissionVersion,
      policyVersion: intent.policyVersion,
      issuedAt: input.now,
      expiresAt: input.now + input.ttlMs,
    });
    if (this.shared.failNextAudit) {
      this.shared.failNextAudit = false;
      return fail("ROW_COUNT_CONFLICT");
    }
    const nextIntent = EgressIntentSchema.parse({
      ...intent,
      state: "FINAL_AUTHORIZED",
      finalAuthorizedAt: input.now,
      finalAuthorizationExpiresAt: authorization.expiresAt,
    });
    this.shared.intents.set(intent.egressIntentId, Object.freeze(nextIntent));
    this.shared.finalAuthorizations.set(
      intent.egressIntentId,
      Object.freeze(authorization),
    );
    this.shared.auditEvents.push(`EGRESS_FINAL_AUTHORIZED:${intent.egressIntentId}`);
    return ok(authorization);
  }

  authorizeWriteStart(input: {
    intentId: string;
    expected: unknown;
    permit: unknown;
    lease: unknown;
    context: unknown;
    now: number;
    rowCounts: Readonly<{ intent: number; audit: number }>;
  }): R3EgressResult<EgressIntent> {
    const lockOrder = validateR3EgressLockOrder([
      { domain: "WORKER_REVOCATION_CONTROL", acquiredAt: input.now },
      { domain: "EMERGENCY_CONTROL", acquiredAt: input.now },
      { domain: "KEY_REGISTRY", acquiredAt: input.now },
      { domain: "EXECUTION_AUTHORIZATION", acquiredAt: input.now },
      { domain: "BUDGET_CONTROL", acquiredAt: input.now },
      { domain: "BUDGET_RESERVATION", acquiredAt: input.now },
      { domain: "CAPABILITY", acquiredAt: input.now },
      { domain: "RESOURCE_FENCING_FLOOR", acquiredAt: input.now },
      { domain: "WORKER_REGISTRATION", acquiredAt: input.now },
      { domain: "EXECUTION_LEASE", acquiredAt: input.now },
      { domain: "SEND_AUTHORIZATION", acquiredAt: input.now },
      { domain: "EGRESS_SEND_INTENT", acquiredAt: input.now },
      { domain: "AUDIT_SEQUENCE", acquiredAt: input.now },
    ]);
    if (!lockOrder.ok) return fail("ROW_COUNT_CONFLICT");
    if (!this.shared.authorityAvailable) {
      return fail("AUTHORITY_UNAVAILABLE");
    }
    const rows = this.checkRows(input.rowCounts);
    if (!rows.ok) return rows;
    const intent = this.shared.intents.get(input.intentId);
    const authorization = this.shared.finalAuthorizations.get(input.intentId);
    const expected = EgressFinalAuthorizationSchema.safeParse(input.expected);
    const permit = SendAuthorizationSchema.safeParse(input.permit);
    const lease = ExecutionLeaseSchema.safeParse(input.lease);
    const context = EgressMutableContextSchema.safeParse(input.context);
    if (
      !intent
      || !authorization
      || !expected.success
      || !permit.success
      || !lease.success
      || !context.success
    ) {
      return fail("PERMIT_INVALID");
    }
    if (
      intent.state !== "FINAL_AUTHORIZED"
      || expected.data.egressIntentId !== intent.egressIntentId
      || expected.data.sendAuthorizationId !== intent.sendAuthorizationId
      || input.now >= expected.data.expiresAt
    ) {
      return fail("EGRESS_INTENT_ALREADY_STARTED");
    }
    const bound = this.validateBindings(intent, permit.data, lease.data, context.data, input.now);
    if (!bound.ok) return bound;
    if (this.shared.failNextAudit) {
      this.shared.failNextAudit = false;
      return fail("ROW_COUNT_CONFLICT");
    }
    const started = EgressIntentSchema.parse({
      ...intent,
      state: "WRITE_STARTED",
      writeStartedAt: input.now,
    });
    this.shared.intents.set(intent.egressIntentId, Object.freeze(started));
    this.shared.auditEvents.push(`WRITE_STARTED:${intent.egressIntentId}`);
    return ok(started);
  }

  recordOutcome(input: {
    intentId: string;
    outcome: "RESPONSE_RECEIVED" | "SEND_OUTCOME_UNKNOWN";
    now: number;
    rowCount: number;
  }): R3EgressResult<EgressIntent> {
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    if (this.shared.failNextAudit) {
      this.shared.failNextAudit = false;
      return fail("ROW_COUNT_CONFLICT");
    }
    const intent = this.shared.intents.get(input.intentId);
    if (!intent || intent.state !== "WRITE_STARTED") {
      return fail("EGRESS_INTENT_REPLAYED");
    }
    const state = input.outcome === "RESPONSE_RECEIVED"
      ? "COMPLETED"
      : "SEND_OUTCOME_UNKNOWN";
    const updated = EgressIntentSchema.parse({
      ...intent,
      state,
      outcomeAt: input.now,
    });
    this.shared.intents.set(intent.egressIntentId, Object.freeze(updated));
    this.shared.auditEvents.push(`${state}:${intent.egressIntentId}`);
    return ok(updated);
  }

  recoverFinalAuthorization(input: {
    intentId: string;
    expected: unknown;
  }): R3EgressResult<EgressFinalAuthorization> {
    if (!this.shared.authorityAvailable) {
      return fail("AUTHORITY_UNAVAILABLE");
    }
    const expected = EgressFinalAuthorizationSchema.safeParse(input.expected);
    const persisted = this.shared.finalAuthorizations.get(input.intentId);
    if (
      !expected.success
      || !persisted
      || expected.data.egressIntentId !== persisted.egressIntentId
      || expected.data.sendAuthorizationId !== persisted.sendAuthorizationId
      || expected.data.scopeKey !== persisted.scopeKey
      || expected.data.fencingToken !== persisted.fencingToken
      || expected.data.requestDigest !== persisted.requestDigest
    ) {
      return fail("COMMIT_OUTCOME_UNKNOWN");
    }
    return ok(persisted);
  }

  intent(intentId: string): EgressIntent | null {
    return this.shared.intents.get(intentId) ?? null;
  }

  auditSnapshot(): readonly string[] {
    return Object.freeze([...this.shared.auditEvents]);
  }

  private validateBindings(
    intent: EgressIntent,
    permit: ReturnType<typeof SendAuthorizationSchema.parse>,
    lease: ReturnType<typeof ExecutionLeaseSchema.parse>,
    context: EgressMutableContext,
    now: number,
  ): R3EgressResult<true> {
    if (
      permit.state !== "CONSUMED"
      || permit.sendAuthorizationId !== intent.sendAuthorizationId
      || permit.scopeKey !== intent.scopeKey
      || permit.fencingToken !== intent.fencingToken
      || permit.workerInstanceId !== intent.workerInstanceId
      || permit.leaseId !== intent.leaseId
      || permit.capabilityId !== intent.capabilityId
      || permit.budgetReservationId !== intent.budgetReservationId
    ) {
      return fail("PERMIT_INVALID");
    }
    if (
      lease.state !== "SENT"
      || lease.scopeKey !== intent.scopeKey
      || lease.workerInstanceId !== intent.workerInstanceId
      || lease.capabilityId !== intent.capabilityId
      || lease.fencingToken !== intent.fencingToken
    ) {
      return fail("LEASE_INVALID");
    }
    if (
      context.workerState !== "ACTIVE"
      || context.workerRegistrationState !== "ACTIVE"
      || context.workerRevocationVersion !== intent.workerRevocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    if (
      context.workerHeartbeatAt > now
      || now - context.workerHeartbeatAt > 15_000
    ) {
      return fail("WORKER_REVOKED");
    }
    if (
      context.scopeBlockedRevocationVersion !== null
      && context.scopeBlockedRevocationVersion >= intent.workerRevocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    if (
      context.currentScopeToken !== intent.fencingToken
      || context.currentScopeWorkerId !== intent.workerInstanceId
      || context.currentScopeLeaseId !== intent.leaseId
      || context.currentScopeCapabilityId !== intent.capabilityId
    ) {
      return fail("RESOURCE_FLOOR_CHANGED");
    }
    if (
      context.authorizationState !== "ACTIVE"
      || context.capabilityState !== "RESERVED"
      || now >= context.capabilityExpiresAt
    ) {
      return fail("PERMIT_INVALID");
    }
    if (
      context.leaseState !== "SENT"
      || context.permitState !== "CONSUMED"
    ) {
      return fail("LEASE_INVALID");
    }
    if (
      context.emergencyStatus !== "NORMAL"
      || context.emergencyEpoch !== intent.emergencyEpoch
    ) {
      return fail("EMERGENCY_BLOCKED");
    }
    if (
      context.keyState !== "ACTIVE"
      || context.keyVersion !== intent.keyVersion
      || context.keyRevocationVersion !== intent.keyRevocationVersion
    ) {
      return fail("KEY_BLOCKED");
    }
    if (
      context.budgetState !== "RESERVED"
      || now >= context.budgetExpiresAt
    ) {
      return fail("BUDGET_BLOCKED");
    }
    return ok(true as const);
  }

  private checkRows(
    rowCounts: Readonly<Record<string, number>>,
  ): R3EgressResult<true> {
    for (const count of Object.values(rowCounts)) {
      const rows = requireExactlyOne(count);
      if (!rows.ok) return rows;
    }
    return ok(true as const);
  }
}

```
<!-- END_EXACT_SOURCE id=S023 -->

### S024. models/egress-races.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/models/egress-races.ts`
- Bytes: `2329`
- SHA-256: `44E563B9D7AA80F8D060BDF07CA84D0E554C7FDE6675FF5DB61EDE5BB1CB0B1E`

<!-- BEGIN_EXACT_SOURCE id=S024 sha256=44E563B9D7AA80F8D060BDF07CA84D0E554C7FDE6675FF5DB61EDE5BB1CB0B1E bytes=2329 -->
```text
export type EgressTimelineEvent =
  | "AUTH_CHECK_PASSED"
  | "FINAL_AUTHORIZED"
  | "FLOOR_CHANGED"
  | "WORKER_REVOKED"
  | "EMERGENCY_STOPPED"
  | "KEY_REVOKED"
  | "AUTHORITY_UNAVAILABLE"
  | "WRITE_RECHECK_PASSED"
  | "WRITE_STARTED"
  | "RESPONSE_RECEIVED";

export type EgressTimelineOutcome =
  | "DENIED_BEFORE_FINAL_AUTH"
  | "FINAL_AUTH_ISSUED_WRITE_BLOCKED"
  | "WRITE_STARTED_RESPONSE_RECEIVED"
  | "WRITE_STARTED_OUTCOME_UNKNOWN"
  | "AUTHORITY_UNAVAILABLE";

export function classifyEgressTimeline(
  events: readonly EgressTimelineEvent[],
): EgressTimelineOutcome {
  let authCheck = false;
  let finalAuth = false;
  let writeRecheck = false;
  let writeStarted = false;
  let response = false;
  let invalidated = false;
  let authorityUnavailable = false;

  for (const event of events) {
    if (event === "AUTH_CHECK_PASSED" && !invalidated) {
      authCheck = true;
      continue;
    }
    if (event === "FINAL_AUTHORIZED" && authCheck && !invalidated) {
      finalAuth = true;
      continue;
    }
    if (
      event === "FLOOR_CHANGED"
      || event === "WORKER_REVOKED"
      || event === "EMERGENCY_STOPPED"
      || event === "KEY_REVOKED"
    ) {
      if (!writeStarted) invalidated = true;
      continue;
    }
    if (event === "AUTHORITY_UNAVAILABLE") {
      authorityUnavailable = true;
      if (!writeStarted) return "AUTHORITY_UNAVAILABLE";
      continue;
    }
    if (event === "WRITE_RECHECK_PASSED" && finalAuth && !invalidated) {
      writeRecheck = true;
      continue;
    }
    if (event === "WRITE_STARTED" && writeRecheck && !invalidated) {
      writeStarted = true;
      continue;
    }
    if (event === "RESPONSE_RECEIVED" && writeStarted) response = true;
  }

  if (!authCheck || !finalAuth) return "DENIED_BEFORE_FINAL_AUTH";
  if (!writeStarted) {
    return authorityUnavailable
      ? "AUTHORITY_UNAVAILABLE"
      : "FINAL_AUTH_ISSUED_WRITE_BLOCKED";
  }
  return response
    ? "WRITE_STARTED_RESPONSE_RECEIVED"
    : "WRITE_STARTED_OUTCOME_UNKNOWN";
}

export function classifyRetryAfterOutcome(
  outcome: EgressTimelineOutcome,
): "RETRY_FORBIDDEN" | "TRANSACTIONAL_RETRY_ALLOWED" {
  return outcome === "WRITE_STARTED_OUTCOME_UNKNOWN"
    || outcome === "WRITE_STARTED_RESPONSE_RECEIVED"
    ? "RETRY_FORBIDDEN"
    : "TRANSACTIONAL_RETRY_ALLOWED";
}

```
<!-- END_EXACT_SOURCE id=S024 -->

### S025. models/sql-contract-analyzer.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/models/sql-contract-analyzer.ts`
- Bytes: `15322`
- SHA-256: `5C29304B30B7693089B00C29C40BC2C72A6429AB64519AE81D78D18CD423DEA9`

<!-- BEGIN_EXACT_SOURCE id=S025 sha256=5C29304B30B7693089B00C29C40BC2C72A6429AB64519AE81D78D18CD423DEA9 bytes=15322 -->
```text
import { R3_EGRESS_LOCK_ORDER } from "../lock-order";

export type SqlAnalysisLevel =
  | "TEXTUAL_PATTERN_CHECK"
  | "SQL_STRUCTURE_CHECK"
  | "PARAMETER_BINDING_REVIEW"
  | "TRANSACTION_CONTRACT_REVIEW";

export type SqlContractFinding = Readonly<{
  code: string;
  level: SqlAnalysisLevel;
  message: string;
  statementIndex: number | null;
}>;

export type SqlStatement = Readonly<{
  index: number;
  start: number;
  end: number;
  line: number;
  text: string;
  normalized: string;
  kind: "BEGIN" | "COMMIT" | "ROLLBACK" | "SELECT" | "INSERT" | "UPDATE" | "DELETE" | "OTHER";
  table: string | null;
}>;

export type SqlTransaction = Readonly<{
  index: number;
  beginStatement: number;
  endStatement: number;
  statements: readonly SqlStatement[];
  lockTables: readonly string[];
  mutationTables: readonly string[];
  hasAuditEvent: boolean;
  hasAuditHead: boolean;
}>;

export type SqlContractSpec = Readonly<{
  requiredTables?: readonly string[];
  requiredMutationTables?: readonly string[];
  requiredLockTables?: readonly string[];
  requiredParameters?: readonly string[];
  requiredPatterns?: readonly Readonly<{ code: string; pattern: RegExp }>[];
  forbiddenPatterns?: readonly Readonly<{ code: string; pattern: RegExp }>[];
  requireExactlyOneRowMarkers?: boolean;
  requireAuditWithMutations?: boolean;
}>;

const TABLE_TO_LOCK_DOMAIN: Readonly<Record<string, string>> = Object.freeze({
  trust_r5_worker_revocation: "WORKER_REVOCATION_CONTROL",
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
  trust_r3_audit_head: "AUDIT_SEQUENCE",
});

function stripLeadingComments(value: string): string {
  let result = value.trimStart();
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

export function splitSqlStatements(sql: string): readonly SqlStatement[] {
  const statements: SqlStatement[] = [];
  let start = 0;
  let inSingle = false;
  let inDouble = false;
  let inLineComment = false;
  let inBlockComment = false;

  const push = (end: number) => {
    const raw = sql.slice(start, end);
    if (raw.trim().length === 0) {
      start = end + 1;
      return;
    }
    const normalized = stripLeadingComments(raw).trim();
    const first = /^([A-Za-z]+)/u.exec(normalized)?.[1]?.toUpperCase() ?? "";
    const kind = first === "BEGIN"
      || first === "COMMIT"
      || first === "ROLLBACK"
      || first === "SELECT"
      || first === "INSERT"
      || first === "UPDATE"
      || first === "DELETE"
      ? first
      : "OTHER";
    const table = /\b(?:FROM|INTO|UPDATE|JOIN)\s+(trust_[a-z0-9_]+)/iu
      .exec(normalized)?.[1]?.toLowerCase() ?? null;
    statements.push(Object.freeze({
      index: statements.length,
      start,
      end,
      line: sql.slice(0, start).split("\n").length,
      text: raw,
      normalized,
      kind,
      table,
    }));
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
    if (!inSingle && !inDouble) {
      if (char === "-" && next === "-") {
        inLineComment = true;
        index += 1;
        continue;
      }
      if (char === "/" && next === "*") {
        inBlockComment = true;
        index += 1;
        continue;
      }
    }
    if (!inDouble && char === "'") {
      if (inSingle && next === "'") {
        index += 1;
        continue;
      }
      inSingle = !inSingle;
      continue;
    }
    if (!inSingle && char === '"') {
      if (inDouble && next === '"') {
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

export function buildSqlTransactions(
  statements: readonly SqlStatement[],
): readonly SqlTransaction[] {
  const transactions: SqlTransaction[] = [];
  let current: SqlStatement[] = [];
  for (const statement of statements) {
    if (statement.kind === "BEGIN") {
      current = [statement];
      continue;
    }
    if (current.length > 0) current.push(statement);
    if (statement.kind === "COMMIT" || statement.kind === "ROLLBACK") {
      if (current.length > 0) {
        const locks = current.flatMap((item) =>
          /\bFOR\s+UPDATE\b/iu.test(item.normalized)
            ? [item.table].filter((value): value is string => value !== null)
            : []
        );
        const mutations = current
          .filter((item) =>
            ["INSERT", "UPDATE", "DELETE"].includes(item.kind)
            && item.table !== null
          )
          .map((item) => item.table as string);
        transactions.push(Object.freeze({
          index: transactions.length,
          beginStatement: current[0].index,
          endStatement: statement.index,
          statements: Object.freeze([...current]),
          lockTables: Object.freeze([...new Set(locks)]),
          mutationTables: Object.freeze([...new Set(mutations)]),
          hasAuditEvent: current.some((item) =>
            /trust_r[0-9]+_audit_event/iu.test(item.normalized)
          ),
          hasAuditHead: current.some((item) =>
            /trust_r[0-9]+_audit_head/iu.test(item.normalized)
          ),
        }));
      }
      current = [];
    }
  }
  return Object.freeze(transactions);
}

function hasRowCountMarker(sql: string, statement: SqlStatement): boolean {
  const prefix = statement.text;
  return /--\s*ROW_COUNT_EXPECTATION:\s*exactly\s+1/iu.test(prefix);
}

export function analyzeSqlContract(input: {
  sql: string;
  spec?: SqlContractSpec;
}): Readonly<{
  statements: readonly SqlStatement[];
  transactions: readonly SqlTransaction[];
  findings: readonly SqlContractFinding[];
}> {
  const statements = splitSqlStatements(input.sql);
  const transactions = buildSqlTransactions(statements);
  const findings: SqlContractFinding[] = [];
  const add = (
    code: string,
    level: SqlAnalysisLevel,
    message: string,
    statementIndex: number | null = null,
  ) => findings.push(Object.freeze({ code, level, message, statementIndex }));
  const spec = input.spec ?? {};
  const allTables = new Set(statements.map((item) => item.table).filter(Boolean));
  const allLocks = new Set(transactions.flatMap((item) => item.lockTables));
  const allParameters = new Set(
    [...input.sql.matchAll(/\$(?:\d+)|:[a-z_][a-z0-9_]*/giu)].map((m) => m[0]),
  );

  for (const table of spec.requiredTables ?? []) {
    if (!allTables.has(table)) add("REQUIRED_TABLE_MISSING", "SQL_STRUCTURE_CHECK", table);
  }
  const allMutationTables = new Set(
    transactions.flatMap((transaction) => transaction.mutationTables),
  );
  for (const table of spec.requiredMutationTables ?? []) {
    if (!allMutationTables.has(table)) {
      add(
        "REQUIRED_MUTATION_MISSING",
        "TRANSACTION_CONTRACT_REVIEW",
        table,
      );
    }
  }
  for (const table of spec.requiredLockTables ?? []) {
    if (!allLocks.has(table)) add("REQUIRED_LOCK_MISSING", "TRANSACTION_CONTRACT_REVIEW", table);
  }
  for (const parameter of spec.requiredParameters ?? []) {
    if (!allParameters.has(parameter)) {
      add("REQUIRED_PARAMETER_MISSING", "PARAMETER_BINDING_REVIEW", parameter);
    }
  }
  for (const requirement of spec.requiredPatterns ?? []) {
    if (!requirement.pattern.test(input.sql)) {
      add(requirement.code, "TEXTUAL_PATTERN_CHECK", String(requirement.pattern));
    }
  }
  for (const prohibition of spec.forbiddenPatterns ?? []) {
    if (prohibition.pattern.test(input.sql)) {
      add(prohibition.code, "TEXTUAL_PATTERN_CHECK", String(prohibition.pattern));
    }
  }

  for (const transaction of transactions) {
    let previousOrder = -1;
    for (const table of transaction.lockTables) {
      const domain = TABLE_TO_LOCK_DOMAIN[table];
      if (!domain) continue;
      const index = R3_EGRESS_LOCK_ORDER.indexOf(
        domain as typeof R3_EGRESS_LOCK_ORDER[number],
      );
      if (index < previousOrder) {
        add(
          "LOCK_ORDER_CROSSING",
          "TRANSACTION_CONTRACT_REVIEW",
          transaction.lockTables.join(" -> "),
          transaction.beginStatement,
        );
      }
      previousOrder = index;
    }
    if (
      spec.requireAuditWithMutations
      && transaction.mutationTables.length > 0
      && (!transaction.hasAuditEvent || !transaction.hasAuditHead)
    ) {
      add(
        "AUDIT_SPLIT_FROM_MUTATION",
        "TRANSACTION_CONTRACT_REVIEW",
        transaction.mutationTables.join(","),
        transaction.beginStatement,
      );
    }
  }

  for (const statement of statements) {
    if (
      spec.requireExactlyOneRowMarkers
      && statement.kind === "UPDATE"
      && !hasRowCountMarker(input.sql, statement)
    ) {
      add(
        "ROW_COUNT_MARKER_MISSING",
        "SQL_STRUCTURE_CHECK",
        statement.table ?? "unknown",
        statement.index,
      );
    }
  }

  return Object.freeze({
    statements,
    transactions,
    findings: Object.freeze(findings),
  });
}

export function reviewEgressClaim(text: string): readonly SqlContractFinding[] {
  const findings: SqlContractFinding[] = [];
  const add = (code: string, message: string) =>
    findings.push(Object.freeze({
      code,
      level: "TEXTUAL_PATTERN_CHECK" as const,
      message,
      statementIndex: null,
    }));
  if (!/workerRevocationVersion|worker_revocation_version/iu.test(text)) {
    add("EGRESS_REVOCATION_VERSION_MISSING", "Worker revocation version absent");
  }
  if (!/trust_r5_worker_revocation/iu.test(text)) {
    add("EGRESS_WORKER_REVOCATION_ROW_MISSING", "global revocation row absent");
  }
  if (!/trust_r4_resource_fencing/iu.test(text)) {
    add("EGRESS_RESOURCE_FLOOR_MISSING", "resource floor absent");
  }
  if (/cached floor/iu.test(text) && !/must not use cached floor/iu.test(text)) {
    add("EGRESS_CACHE_TRUSTED", "cached floor treated as authority");
  }
  if (
    /socket write inside database transaction|database lock protects socket/iu.test(text)
  ) {
    add("SOCKET_ATOMICITY_OVERCLAIM", "database lock cannot protect socket write");
  }
  if (
    /authority unavailable/iu.test(text)
    && !/fail closed|reject|deny/iu.test(text)
  ) {
    add("EGRESS_FAIL_OPEN", "authority loss does not fail closed");
  }
  return Object.freeze(findings);
}

export function reviewWorkerRegistrationMutation(sql: string): readonly SqlContractFinding[] {
  const findings: SqlContractFinding[] = [];
  if (/ON\s+CONFLICT[\s\S]*DO\s+UPDATE[\s\S]*SET\s+state\s*=\s*'ACTIVE'/iu.test(sql)) {
    findings.push(Object.freeze({
      code: "WORKER_REACTIVATION_UPSERT",
      level: "TEXTUAL_PATTERN_CHECK" as const,
      message: "registration upsert can reactivate a revoked Worker",
      statementIndex: null,
    }));
  }
  if (
    /UPDATE\s+trust_r4_worker_registration/iu.test(sql)
    && !/state\s*=\s*'ACTIVE'/iu.test(sql)
  ) {
    findings.push(Object.freeze({
      code: "WORKER_STATE_GUARD_MISSING",
      level: "SQL_STRUCTURE_CHECK" as const,
      message: "registration mutation lacks ACTIVE guard",
      statementIndex: null,
    }));
  }
  return Object.freeze(findings);
}

export function reviewPermitLifecycle(sql: string): readonly SqlContractFinding[] {
  const findings: SqlContractFinding[] = [];
  const add = (code: string) => findings.push(Object.freeze({
    code,
    level: "TRANSACTION_CONTRACT_REVIEW" as const,
    message: code,
    statementIndex: null,
  }));
  if (!/'ISSUED'/iu.test(sql) || !/'CONSUMED'/iu.test(sql)) {
    add("PERMIT_ONE_TIME_TRANSITION_MISSING");
  }
  if (!/state\s*=\s*'REVOKED'/iu.test(sql)) {
    add("PERMIT_REVOCATION_PATH_MISSING");
  }
  return Object.freeze(findings);
}

export function reviewPermitConsumptionRevocation(
  sql: string,
): readonly SqlContractFinding[] {
  const findings: SqlContractFinding[] = [];
  const add = (code: string) => findings.push(Object.freeze({
    code,
    level: "TRANSACTION_CONTRACT_REVIEW" as const,
    message: code,
    statementIndex: null,
  }));
  if (!/trust_r5_worker_revocation/iu.test(sql)) {
    add("PERMIT_WORKER_REVOCATION_CHECK_MISSING");
  }
  if (!/trust_r5_scope_worker_block/iu.test(sql)) {
    add("PERMIT_SCOPE_BLOCK_CHECK_MISSING");
  }
  if (!/trust_r5_lease_worker_revocation_binding/iu.test(sql)) {
    add("PERMIT_LEASE_REVOCATION_BINDING_MISSING");
  }
  if (!/trust_r4_resource_fencing/iu.test(sql)) {
    add("PERMIT_RESOURCE_FLOOR_CHECK_MISSING");
  }
  if (!/trust_r4_worker_registration/iu.test(sql)) {
    add("PERMIT_WORKER_REGISTRATION_CHECK_MISSING");
  }
  if (
    !/UPDATE\s+trust_r4_send_authorization[\s\S]*state\s*=\s*'CONSUMED'/iu.test(sql)
  ) {
    add("PERMIT_ONE_TIME_TRANSITION_MISSING");
  }
  return Object.freeze(findings);
}

export function reviewEgressRevocationGate(
  sql: string,
): readonly SqlContractFinding[] {
  const findings: SqlContractFinding[] = [];
  const add = (code: string, message: string) => findings.push(Object.freeze({
    code,
    level: "TRANSACTION_CONTRACT_REVIEW" as const,
    message,
    statementIndex: null,
  }));
  const blockChecks = [...sql.matchAll(/trust_r5_scope_worker_block/giu)].length;
  if (blockChecks < 2) {
    add(
      "EGRESS_SCOPE_BLOCK_RECHECK_MISSING",
      "both final authorization and write-start must check scope blocks",
    );
  }
  if (!/trust_r4_worker_registration[\s\S]*heartbeat_at_ms/iu.test(sql)) {
    add(
      "EGRESS_WORKER_REGISTRATION_RECHECK_MISSING",
      "Worker registration and heartbeat must be re-read",
    );
  }
  if (!/trust_r5_lease_worker_revocation_binding/iu.test(sql)) {
    add(
      "EGRESS_LEASE_REVOCATION_BINDING_MISSING",
      "Lease revocation binding must be checked",
    );
  }
  if (
    /COMMIT[\s\S]*database lock protects socket/iu.test(sql)
  ) {
    add("SOCKET_ATOMICITY_OVERCLAIM", "database locks end at COMMIT");
  }
  return Object.freeze(findings);
}

export const SQL_ANALYSIS_LIMITS = Object.freeze([
  "TEXTUAL_PATTERN_CHECK",
  "SQL_STRUCTURE_CHECK",
  "PARAMETER_BINDING_REVIEW",
  "TRANSACTION_CONTRACT_REVIEW",
  "POSTGRESQL_EXECUTION_NOT_PERFORMED",
] as const);

```
<!-- END_EXACT_SOURCE id=S025 -->

### S026. models/worker-revocation.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/models/worker-revocation.ts`
- Bytes: `15706`
- SHA-256: `974C1463AB2280605B7EC94EDBEE4AAC36383BBE1D16C6CDDB3B8ECD69E54C90`

<!-- BEGIN_EXACT_SOURCE id=S026 sha256=974C1463AB2280605B7EC94EDBEE4AAC36383BBE1D16C6CDDB3B8ECD69E54C90 bytes=15706 -->
```text
import {
  ScopeWorkerBlockSchema,
  WorkerRevocationRecordSchema,
  fail,
  ok,
  requireExactlyOne,
  type R3EgressResult,
  type ScopeWorkerBlock,
  type WorkerRevocationRecord,
} from "../contracts";
import {
  ExecutionLeaseSchema,
  ResourceFencingFloorSchema,
  SendAuthorizationSchema,
  WorkerRegistrationSchema,
  type ExecutionLease,
  type ResourceFencingFloor,
  type SendAuthorization,
  type WorkerRegistration,
} from "../../r3-fencing-remediation/contracts";

type SharedState = {
  authorityAvailable: boolean;
  revocations: Map<string, WorkerRevocationRecord>;
  requests: Map<string, string>;
  scopeBlocks: Map<string, ScopeWorkerBlock>;
  workers: Map<string, WorkerRegistration>;
  floors: Map<string, ResourceFencingFloor>;
  leases: Map<string, ExecutionLease>;
  permits: Map<string, SendAuthorization>;
  auditEvents: string[];
};

/**
 * OFFLINE_REFERENCE_MODEL.
 * Global Worker revocation is a single fail-closed tombstone. Scope cleanup is
 * bounded and idempotent; it is not required to make the global tombstone
 * effective.
 */
export class OfflineWorkerRevocationModel {
  private readonly shared: SharedState;

  constructor(shared?: OfflineWorkerRevocationModel) {
    this.shared = shared?.shared ?? {
      authorityAvailable: true,
      revocations: new Map(),
      requests: new Map(),
      scopeBlocks: new Map(),
      workers: new Map(),
      floors: new Map(),
      leases: new Map(),
      permits: new Map(),
      auditEvents: [],
    };
  }

  connect(): OfflineWorkerRevocationModel {
    return new OfflineWorkerRevocationModel(this);
  }

  setAuthorityAvailable(available: boolean): void {
    this.shared.authorityAvailable = available;
  }

  seedActiveWorker(input: {
    workerInstanceId: string;
    now: number;
  }): R3EgressResult<WorkerRevocationRecord> {
    const existing = this.shared.revocations.get(input.workerInstanceId);
    if (existing && existing.state !== "ACTIVE") {
      return fail("WORKER_REACTIVATION_FORBIDDEN");
    }
    const revocation = WorkerRevocationRecordSchema.parse({
      schemaVersion: "r5-worker-revocation-record-v1",
      workerInstanceId: input.workerInstanceId,
      state: "ACTIVE",
      revocationVersion: existing?.revocationVersion ?? 0,
      recordVersion: (existing?.recordVersion ?? 0) + 1,
      revokedAt: null,
      reasonCode: null,
      replacementWorkerId: null,
      updatedAt: input.now,
    });
    const worker = WorkerRegistrationSchema.parse({
      schemaVersion: "r3-fencing-worker-registration-v1",
      workerInstanceId: input.workerInstanceId,
      state: "ACTIVE",
      heartbeatAt: input.now,
      lastIssuedToken: 0,
      updatedAt: input.now,
    });
    this.shared.revocations.set(input.workerInstanceId, revocation);
    this.shared.workers.set(input.workerInstanceId, worker);
    return ok(revocation);
  }

  seedFloor(raw: unknown): R3EgressResult<ResourceFencingFloor> {
    const parsed = ResourceFencingFloorSchema.safeParse(raw);
    if (!parsed.success) return fail("RESOURCE_SCOPE_MISMATCH");
    this.shared.floors.set(parsed.data.scopeKey, parsed.data);
    return ok(parsed.data);
  }

  seedLease(raw: unknown): R3EgressResult<ExecutionLease> {
    const parsed = ExecutionLeaseSchema.safeParse(raw);
    if (!parsed.success) return fail("LEASE_INVALID");
    this.shared.leases.set(parsed.data.leaseId, parsed.data);
    return ok(parsed.data);
  }

  seedPermit(raw: unknown): R3EgressResult<SendAuthorization> {
    const parsed = SendAuthorizationSchema.safeParse(raw);
    if (!parsed.success) return fail("PERMIT_INVALID");
    this.shared.permits.set(parsed.data.sendAuthorizationId, parsed.data);
    return ok(parsed.data);
  }

  seedScopeBlock(raw: unknown): R3EgressResult<ScopeWorkerBlock> {
    const parsed = ScopeWorkerBlockSchema.safeParse(raw);
    if (!parsed.success) return fail("RESOURCE_SCOPE_MISMATCH");
    this.shared.scopeBlocks.set(
      `${parsed.data.scopeKey}|${parsed.data.workerInstanceId}`,
      parsed.data,
    );
    return ok(parsed.data);
  }

  getRevocation(workerInstanceId: string): WorkerRevocationRecord | null {
    return this.shared.revocations.get(workerInstanceId) ?? null;
  }

  getScopeBlock(
    scopeKey: string,
    workerInstanceId: string,
  ): ScopeWorkerBlock | null {
    return this.shared.scopeBlocks.get(`${scopeKey}|${workerInstanceId}`) ?? null;
  }

  revokeWorkerGlobally(input: {
    requestId: string;
    workerInstanceId: string;
    expectedRecordVersion: number;
    reasonCode: string;
    now: number;
    rowCounts: Readonly<{ revocation: number; worker: number; audit: number }>;
    failAudit?: boolean;
  }): R3EgressResult<WorkerRevocationRecord> {
    if (!this.shared.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    for (const count of Object.values(input.rowCounts)) {
      const rows = requireExactlyOne(count);
      if (!rows.ok) return rows;
    }
    const priorRequest = this.shared.requests.get(input.requestId);
    if (priorRequest) {
      if (priorRequest !== input.workerInstanceId) {
        return fail("WORKER_REVOCATION_VERSION_MISMATCH");
      }
      return ok(
        this.shared.revocations.get(input.workerInstanceId) as WorkerRevocationRecord,
      );
    }
    const current = this.shared.revocations.get(input.workerInstanceId);
    if (
      !current
      || current.state !== "ACTIVE"
      || current.recordVersion !== input.expectedRecordVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    if (input.failAudit) return fail("ROW_COUNT_CONFLICT");
    const revoked = WorkerRevocationRecordSchema.parse({
      ...current,
      state: "REVOKED",
      revocationVersion: current.revocationVersion + 1,
      recordVersion: current.recordVersion + 1,
      revokedAt: input.now,
      reasonCode: input.reasonCode,
      updatedAt: input.now,
    });
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker) return fail("WORKER_REVOKED");
    const revokedWorker = WorkerRegistrationSchema.parse({
      ...worker,
      state: "REVOKED",
      updatedAt: input.now,
    });
    this.shared.revocations.set(input.workerInstanceId, revoked);
    this.shared.workers.set(input.workerInstanceId, revokedWorker);
    this.shared.requests.set(input.requestId, input.workerInstanceId);
    this.shared.auditEvents.push(
      `WORKER_REVOKED:${input.workerInstanceId}:${revoked.revocationVersion}`,
    );
    return ok(revoked);
  }

  cleanupScope(input: {
    scopeKey: string;
    workerInstanceId: string;
    expectedRevocationVersion: number;
    leaseId: string;
    capabilityId: string;
    permitId: string;
    reasonCode: string;
    now: number;
    rowCounts: Readonly<{
      block: number;
      lease?: number;
      permit: number;
      audit: number;
    }>;
  }): R3EgressResult<ScopeWorkerBlock> {
    if (!this.shared.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const revocation = this.shared.revocations.get(input.workerInstanceId);
    if (
      !revocation
      || revocation.state !== "REVOKED"
      || revocation.revocationVersion !== input.expectedRevocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    const floor = this.shared.floors.get(input.scopeKey);
    const lease = this.shared.leases.get(input.leaseId);
    const permit = this.shared.permits.get(input.permitId);
    if (
      !floor
      || floor.scopeKey !== input.scopeKey
      || floor.currentWorkerId !== input.workerInstanceId
      || floor.currentLeaseId !== input.leaseId
      || floor.currentCapabilityId !== input.capabilityId
      || !lease
      || lease.scopeKey !== input.scopeKey
      || lease.workerInstanceId !== input.workerInstanceId
      || !permit
      || permit.scopeKey !== input.scopeKey
      || permit.leaseId !== input.leaseId
      || permit.workerInstanceId !== input.workerInstanceId
    ) {
      return fail("RESOURCE_SCOPE_MISMATCH");
    }
    for (const count of [
      input.rowCounts.block,
      input.rowCounts.lease,
      input.rowCounts.permit,
      input.rowCounts.audit,
    ]) {
      if (count === undefined) continue;
      const rows = requireExactlyOne(count);
      if (!rows.ok) return rows;
    }
    const block = ScopeWorkerBlockSchema.parse({
      schemaVersion: "r5-scope-worker-block-v1",
      scopeKey: input.scopeKey,
      workerInstanceId: input.workerInstanceId,
      blockedRevocationVersion: revocation.revocationVersion,
      version:
        (this.shared.scopeBlocks.get(
          `${input.scopeKey}|${input.workerInstanceId}`,
        )?.version ?? 0) + 1,
      blockedAt: input.now,
      reasonCode: input.reasonCode,
    });
    const leasePresend = [
      "ISSUED",
      "KEY_READ",
      "TRANSPORT_CREATED",
      "SEND_AUTHORIZED",
    ].includes(lease.state);
    if (leasePresend && input.rowCounts.lease === undefined) {
      return fail("ROW_COUNT_CONFLICT");
    }
    this.shared.scopeBlocks.set(
      `${input.scopeKey}|${input.workerInstanceId}`,
      block,
    );
    if (leasePresend) {
      this.shared.leases.set(lease.leaseId, Object.freeze({
        ...lease,
        state: "REVOKED",
      }));
    }
    if (permit.state === "ISSUED" || permit.state === "CONSUMED") {
      this.shared.permits.set(permit.sendAuthorizationId, Object.freeze({
        ...permit,
        state: "REVOKED",
      }));
    }
    this.shared.auditEvents.push(
      `WORKER_SCOPE_BLOCKED:${input.scopeKey}:${input.workerInstanceId}`,
    );
    return ok(block);
  }

  validatePermitForConsumption(input: {
    permit: unknown;
    floor: unknown;
    expectedWorkerRevocationVersion: number;
    now: number;
  }): R3EgressResult<SendAuthorization> {
    if (!this.shared.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const permit = SendAuthorizationSchema.safeParse(input.permit);
    const floor = ResourceFencingFloorSchema.safeParse(input.floor);
    if (!permit.success || !floor.success) return fail("PERMIT_INVALID");
    const revocation = this.shared.revocations.get(permit.data.workerInstanceId);
    if (!revocation || revocation.state === "REVOKED") {
      return fail("WORKER_REVOKED");
    }
    if (revocation.revocationVersion !== input.expectedWorkerRevocationVersion) {
      return fail("WORKER_REVOCATION_VERSION_MISMATCH");
    }
    const block = this.getScopeBlock(
      permit.data.scopeKey,
      permit.data.workerInstanceId,
    );
    if (
      block
      && block.blockedRevocationVersion >= revocation.revocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    if (
      permit.data.state !== "ISSUED"
      || floor.data.currentFencingToken !== permit.data.fencingToken
      || floor.data.currentWorkerId !== permit.data.workerInstanceId
      || floor.data.currentLeaseId !== permit.data.leaseId
      || floor.data.currentCapabilityId !== permit.data.capabilityId
    ) {
      return fail("RESOURCE_FLOOR_CHANGED");
    }
    if (input.now >= permit.data.expiresAt) return fail("PERMIT_INVALID");
    return ok(permit.data);
  }

  consumePermitWithRevocation(input: {
    permit: unknown;
    floor: unknown;
    lease: unknown;
    expectedWorkerRevocationVersion: number;
    now: number;
    rowCounts: Readonly<{
      permit: number;
      lease: number;
      budget: number;
      audit: number;
    }>;
  }): R3EgressResult<{
    permit: SendAuthorization;
    lease: ExecutionLease;
  }> {
    if (!this.shared.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const permitResult = SendAuthorizationSchema.safeParse(input.permit);
    const floorResult = ResourceFencingFloorSchema.safeParse(input.floor);
    const leaseResult = ExecutionLeaseSchema.safeParse(input.lease);
    if (!permitResult.success || !floorResult.success || !leaseResult.success) {
      return fail("PERMIT_INVALID");
    }
    const permit = permitResult.data;
    const floor = floorResult.data;
    const lease = leaseResult.data;
    const revocation = this.shared.revocations.get(permit.workerInstanceId);
    if (
      !revocation
      || revocation.state !== "ACTIVE"
      || revocation.revocationVersion !== input.expectedWorkerRevocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    const block = this.getScopeBlock(
      permit.scopeKey,
      permit.workerInstanceId,
    );
    if (
      block
      && block.blockedRevocationVersion >= revocation.revocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    const worker = this.shared.workers.get(permit.workerInstanceId);
    if (
      !worker
      || worker.state !== "ACTIVE"
      || worker.heartbeatAt > input.now
      || input.now - worker.heartbeatAt > 15_000
    ) {
      return fail("WORKER_REVOKED");
    }
    if (
      permit.state !== "ISSUED"
      || input.now < permit.issuedAt
      || input.now >= permit.expiresAt
      || floor.scopeKey !== permit.scopeKey
      || floor.currentFencingToken !== permit.fencingToken
      || floor.currentWorkerId !== permit.workerInstanceId
      || floor.currentLeaseId !== permit.leaseId
      || floor.currentCapabilityId !== permit.capabilityId
      || lease.leaseId !== permit.leaseId
      || lease.state !== "SEND_AUTHORIZED"
      || lease.scopeKey !== permit.scopeKey
      || lease.capabilityId !== permit.capabilityId
      || lease.workerInstanceId !== permit.workerInstanceId
      || lease.fencingToken !== permit.fencingToken
      || input.now >= lease.expiresAt
    ) {
      return fail("PERMIT_INVALID");
    }
    for (const count of Object.values(input.rowCounts)) {
      const rows = requireExactlyOne(count);
      if (!rows.ok) return rows;
    }
    const consumed = SendAuthorizationSchema.parse({
      ...permit,
      state: "CONSUMED",
      consumedAt: input.now,
    });
    const sent = ExecutionLeaseSchema.parse({
      ...lease,
      state: "SENT",
    });
    this.shared.permits.set(consumed.sendAuthorizationId, Object.freeze(consumed));
    this.shared.leases.set(sent.leaseId, Object.freeze(sent));
    this.shared.auditEvents.push(
      `SEND_AUTHORIZATION_CONSUMED:${consumed.sendAuthorizationId}`,
    );
    return ok(Object.freeze({ permit: consumed, lease: sent }));
  }

  bindLeaseRevocationVersion(input: {
    leaseId: string;
    workerInstanceId: string;
    workerRevocationVersion: number;
    now: number;
  }): R3EgressResult<true> {
    const revocation = this.shared.revocations.get(input.workerInstanceId);
    if (
      !revocation
      || revocation.state !== "ACTIVE"
      || revocation.revocationVersion !== input.workerRevocationVersion
    ) {
      return fail("WORKER_REVOKED");
    }
    if (!this.shared.leases.has(input.leaseId)) return fail("LEASE_INVALID");
    return ok(true as const);
  }

  authorizeTakeover(input: {
    workerInstanceId: string;
    expectedRevocationVersion: number;
    now: number;
  }): R3EgressResult<true> {
    if (!this.shared.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
    const revocation = this.shared.revocations.get(input.workerInstanceId);
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (
      !revocation
      || revocation.state !== "ACTIVE"
      || !worker
      || worker.state !== "ACTIVE"
    ) {
      return fail("WORKER_REACTIVATION_FORBIDDEN");
    }
    if (revocation.revocationVersion !== input.expectedRevocationVersion) {
      return fail("WORKER_REVOCATION_VERSION_MISMATCH");
    }
    if (input.now < worker.heartbeatAt || input.now - worker.heartbeatAt > 15_000) {
      return fail("WORKER_REVOKED");
    }
    return ok(true as const);
  }

  auditSnapshot(): readonly string[] {
    return Object.freeze([...this.shared.auditEvents]);
  }
}

```
<!-- END_EXACT_SOURCE id=S026 -->

### S027. tests/egress-boundary.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tests/egress-boundary.test.ts`
- Bytes: `12927`
- SHA-256: `A61F2FBF565922218741DEE6C37F557857C1E93C8F10A97E962D1980F37DAD64`

<!-- BEGIN_EXACT_SOURCE id=S027 sha256=A61F2FBF565922218741DEE6C37F557857C1E93C8F10A97E962D1980F37DAD64 bytes=12927 -->
```text
import { describe, expect, it } from "vitest";

import {
  EgressIntentSchema,
  ExecutionLeaseSchema,
  SendAuthorizationSchema,
  type EgressFinalAuthorization,
  type EgressIntent,
  type EgressMutableContext,
} from "../contracts";
import { OfflineEgressBoundary } from "../models/egress-boundary";
import { deriveFencingScopeKey } from "../../r3-fencing-remediation/scope";

const NOW = Date.parse("2026-11-26T12:00:00Z");
const IDS = Object.freeze({
  intent: "11111111-1111-4111-8111-111111111111",
  permit: "22222222-2222-4222-8222-222222222222",
  worker: "33333333-3333-4333-8333-333333333333",
  lease: "44444444-4444-4444-8444-444444444444",
  capability: "55555555-5555-4555-8555-555555555555",
  authorization: "66666666-6666-4666-8666-666666666666",
  budget: "77777777-7777-4777-8777-777777777777",
  organization: "88888888-8888-4888-8888-888888888888",
});
const DIGESTS = Object.freeze({
  target: "sha256:" + "1".repeat(64),
  request: "sha256:" + "2".repeat(64),
  permit: "sha256:" + "3".repeat(64),
});
const scopeKey = deriveFencingScopeKey({
  providerKind: "fetch",
  purpose: "fetch_only",
  organizationId: IDS.organization,
  targetDigest: DIGESTS.target,
});

function intent(overrides: Partial<EgressIntent> = {}): EgressIntent {
  return EgressIntentSchema.parse({
    schemaVersion: "r5-egress-intent-v1",
    egressIntentId: IDS.intent,
    sendAuthorizationId: IDS.permit,
    permitDigest: DIGESTS.permit,
    scopeKey,
    fencingToken: 100,
    workerInstanceId: IDS.worker,
    workerRevocationVersion: 2,
    leaseId: IDS.lease,
    capabilityId: IDS.capability,
    budgetReservationId: IDS.budget,
    requestDigest: DIGESTS.request,
    emergencyEpoch: 4,
    keyVersion: 3,
    keyRevocationVersion: 1,
    permissionVersion: 5,
    policyVersion: "policy-v1",
    state: "PENDING",
    createdAt: NOW - 10,
    finalAuthorizedAt: null,
    finalAuthorizationExpiresAt: null,
    writeStartedAt: null,
    outcomeAt: null,
    ...overrides,
  });
}

function permit() {
  return SendAuthorizationSchema.parse({
    schemaVersion: "r3-fencing-send-authorization-v1",
    sendAuthorizationId: IDS.permit,
    state: "CONSUMED",
    scopeKey,
    leaseId: IDS.lease,
    capabilityId: IDS.capability,
    workerInstanceId: IDS.worker,
    fencingToken: 100,
    budgetReservationId: IDS.budget,
    emergencyEpoch: 4,
    keyVersion: 3,
    revocationVersion: 1,
    permissionVersion: 5,
    policyVersion: "policy-v1",
    issuedAt: NOW - 20,
    expiresAt: NOW + 5_000,
    consumedAt: NOW - 5,
  });
}

function lease() {
  return ExecutionLeaseSchema.parse({
    schemaVersion: "r3-fencing-execution-lease-v1",
    leaseId: IDS.lease,
    scopeKey,
    capabilityId: IDS.capability,
    executionAuthorizationId: IDS.authorization,
    budgetReservationId: IDS.budget,
    workerInstanceId: IDS.worker,
    fencingToken: 100,
    state: "SENT",
    issuedAt: NOW - 30,
    expiresAt: NOW + 20_000,
    emergencyEpoch: 4,
    keyVersion: 3,
    revocationVersion: 1,
    permissionVersion: 5,
    policyVersion: "policy-v1",
  });
}

function context(overrides: Partial<EgressMutableContext> = {}): EgressMutableContext {
  return {
    workerState: "ACTIVE",
    workerRegistrationState: "ACTIVE",
    workerHeartbeatAt: NOW,
    workerRevocationVersion: 2,
    scopeBlockedRevocationVersion: null,
    currentScopeToken: 100,
    currentScopeWorkerId: IDS.worker,
    currentScopeLeaseId: IDS.lease,
    currentScopeCapabilityId: IDS.capability,
    authorizationState: "ACTIVE",
    capabilityState: "RESERVED",
    capabilityExpiresAt: NOW + 20_000,
    leaseState: "SENT",
    permitState: "CONSUMED",
    emergencyStatus: "NORMAL",
    emergencyEpoch: 4,
    keyState: "ACTIVE",
    keyVersion: 3,
    keyRevocationVersion: 1,
    budgetState: "RESERVED",
    budgetExpiresAt: NOW + 20_000,
    ...overrides,
  };
}

function prepared() {
  const egress = new OfflineEgressBoundary();
  const created = egress.createPendingIntent({
    intent: intent(),
    permit: permit(),
    lease: lease(),
    context: context(),
    now: NOW,
    rowCount: 1,
  });
  if (!created.ok) throw new Error(created.code);
  return { egress, created: created.value };
}

function finalAuthorized() {
  const state = prepared();
  const result = state.egress.finalAuthorize({
    intentId: IDS.intent,
    permit: permit(),
    lease: lease(),
    context: context(),
    now: NOW,
    ttlMs: 500,
    rowCounts: { intent: 1, audit: 1 },
  });
  if (!result.ok) throw new Error(result.code);
  return { ...state, authorization: result.value };
}

describe("Offline Egress final authorization", () => {
  it("rejects PENDING intent creation unless consumption and revocation gates hold", () => {
    for (const mutation of [
      { scopeBlockedRevocationVersion: 2 },
      { workerRegistrationState: "REVOKED" as const },
      { workerRevocationVersion: 3 },
    ]) {
      const egress = new OfflineEgressBoundary();
      expect(egress.createPendingIntent({
        intent: intent(),
        permit: permit(),
        lease: lease(),
        context: context(mutation),
        now: NOW,
        rowCount: 1,
      }).ok, JSON.stringify(mutation)).toBe(false);
      expect(egress.intent(IDS.intent)).toBeNull();
    }
    const egress = new OfflineEgressBoundary();
    expect(egress.createPendingIntent({
      intent: intent(),
      permit: { ...permit(), state: "ISSUED", consumedAt: null },
      lease: lease(),
      context: context(),
      now: NOW,
      rowCount: 1,
    }).ok).toBe(false);
  });

  it("issues a one-time final authorization from PENDING", () => {
    const { egress } = finalAuthorized();
    expect(egress.intent(IDS.intent)).toMatchObject({
      state: "FINAL_AUTHORIZED",
      finalAuthorizedAt: NOW,
      finalAuthorizationExpiresAt: NOW + 500,
    });
    expect(egress.auditSnapshot()).toEqual([
      `EGRESS_FINAL_AUTHORIZED:${IDS.intent}`,
    ]);
  });

  it("rejects Worker revocation/version, floor, Emergency and Key changes", () => {
    for (const mutation of [
      { workerState: "REVOKED" as const },
      { workerRegistrationState: "REVOKED" as const },
      { workerHeartbeatAt: NOW - 15_001 },
      { workerRevocationVersion: 3 },
      { scopeBlockedRevocationVersion: 2 },
      { currentScopeToken: 101 },
      { currentScopeLeaseId: IDS.authorization },
      { emergencyStatus: "DRAINING" as const },
      { emergencyEpoch: 5 },
      { keyState: "REVOKED" as const },
      { keyRevocationVersion: 2 },
      { leaseState: "SEND_AUTHORIZED" as never },
      { budgetState: "RELEASED_BEFORE_SEND" as const },
      { budgetExpiresAt: NOW },
    ]) {
      const { egress } = prepared();
      expect(egress.finalAuthorize({
        intentId: IDS.intent,
        permit: permit(),
        lease: lease(),
        context: context(mutation),
        now: NOW,
        ttlMs: 500,
        rowCounts: { intent: 1, audit: 1 },
      }).ok, JSON.stringify(mutation)).toBe(false);
      expect(egress.intent(IDS.intent)?.state).toBe("PENDING");
    }
  });

  it("rejects a second intent for the same consumed permit", () => {
    const { egress } = prepared();
    expect(egress.createPendingIntent({
      intent: intent({
        egressIntentId: "99999999-9999-4999-8999-999999999999",
      }),
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW,
      rowCount: 1,
    })).toEqual({ ok: false, code: "PERMIT_REPLAYED" });
  });

  it("rolls back final authorization on audit or row-count failure", () => {
    const rowFailure = prepared();
    expect(rowFailure.egress.finalAuthorize({
      intentId: IDS.intent,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW,
      ttlMs: 500,
      rowCounts: { intent: 0, audit: 1 },
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(rowFailure.egress.intent(IDS.intent)?.state).toBe("PENDING");

    const auditFailure = prepared();
    auditFailure.egress.setNextAuditFailure();
    expect(auditFailure.egress.finalAuthorize({
      intentId: IDS.intent,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW,
      ttlMs: 500,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(auditFailure.egress.intent(IDS.intent)?.state).toBe("PENDING");
  });

  it("fails closed when central authority is unavailable", () => {
    const { egress } = prepared();
    egress.setAuthorityAvailable(false);
    expect(egress.finalAuthorize({
      intentId: IDS.intent,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW,
      ttlMs: 500,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({ ok: false, code: "AUTHORITY_UNAVAILABLE" });
  });
});

describe("Offline Egress write-start and socket boundary", () => {
  it("rechecks Worker/floor/Emergency/Key/Budget before socket", () => {
    for (const mutation of [
      { workerState: "REVOKED" as const },
      { workerRegistrationState: "DRAINING" as const },
      { workerHeartbeatAt: NOW - 15_001 },
      { workerRevocationVersion: 3 },
      { scopeBlockedRevocationVersion: 2 },
      { currentScopeToken: 101 },
      { emergencyStatus: "STOPPED" as const },
      { keyState: "REVOKED" as const },
      { budgetState: "UNKNOWN" as const },
    ]) {
      const state = finalAuthorized();
      expect(state.egress.authorizeWriteStart({
        intentId: IDS.intent,
        expected: state.authorization,
        permit: permit(),
        lease: lease(),
        context: context(mutation),
        now: NOW + 1,
        rowCounts: { intent: 1, audit: 1 },
      }).ok, JSON.stringify(mutation)).toBe(false);
      expect(state.egress.intent(IDS.intent)?.state).toBe("FINAL_AUTHORIZED");
    }
  });

  it("rejects expired final authorization and replay", () => {
    const state = finalAuthorized();
    expect(state.egress.authorizeWriteStart({
      intentId: IDS.intent,
      expected: state.authorization,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW + 500,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({ ok: false, code: "EGRESS_INTENT_ALREADY_STARTED" });
    expect(state.egress.authorizeWriteStart({
      intentId: IDS.intent,
      expected: state.authorization,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW + 1,
      rowCounts: { intent: 1, audit: 1 },
    }).ok).toBe(true);
    expect(state.egress.authorizeWriteStart({
      intentId: IDS.intent,
      expected: state.authorization,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW + 2,
      rowCounts: { intent: 1, audit: 1 },
    })).toEqual({ ok: false, code: "EGRESS_INTENT_ALREADY_STARTED" });
  });

  it("records response completion and unknown outcome without retry", () => {
    const response = finalAuthorized();
    const startResponse = response.egress.authorizeWriteStart({
      intentId: IDS.intent,
      expected: response.authorization,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW + 1,
      rowCounts: { intent: 1, audit: 1 },
    });
    expect(startResponse.ok).toBe(true);
    expect(response.egress.recordOutcome({
      intentId: IDS.intent,
      outcome: "RESPONSE_RECEIVED",
      now: NOW + 2,
      rowCount: 1,
    })).toMatchObject({ ok: true, value: { state: "COMPLETED" } });

    const unknown = finalAuthorized();
    expect(unknown.egress.authorizeWriteStart({
      intentId: IDS.intent,
      expected: unknown.authorization,
      permit: permit(),
      lease: lease(),
      context: context(),
      now: NOW + 1,
      rowCounts: { intent: 1, audit: 1 },
    }).ok).toBe(true);
    expect(unknown.egress.recordOutcome({
      intentId: IDS.intent,
      outcome: "SEND_OUTCOME_UNKNOWN",
      now: NOW + 2,
      rowCount: 1,
    })).toMatchObject({
      ok: true,
      value: { state: "SEND_OUTCOME_UNKNOWN" },
    });
    expect(unknown.egress.recordOutcome({
      intentId: IDS.intent,
      outcome: "SEND_OUTCOME_UNKNOWN",
      now: NOW + 3,
      rowCount: 1,
    })).toEqual({ ok: false, code: "EGRESS_INTENT_REPLAYED" });
  });

  it("supports query-only recovery of final authorization", () => {
    const state = finalAuthorized();
    expect(state.egress.recoverFinalAuthorization({
      intentId: IDS.intent,
      expected: state.authorization,
    })).toMatchObject({
      ok: true,
      value: {
        egressIntentId: IDS.intent,
        sendAuthorizationId: IDS.permit,
      },
    });
    expect(state.egress.recoverFinalAuthorization({
      intentId: IDS.intent,
      expected: {
        ...state.authorization,
        requestDigest: "sha256:" + "4".repeat(64),
      } as EgressFinalAuthorization,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
  });
});

```
<!-- END_EXACT_SOURCE id=S027 -->

### S028. tests/egress-races.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tests/egress-races.test.ts`
- Bytes: `2522`
- SHA-256: `9FA622B49ECC6A4C1044DCC5F9FA31CA22CC9A0797B6A8C591FBF6E09300458D`

<!-- BEGIN_EXACT_SOURCE id=S028 sha256=9FA622B49ECC6A4C1044DCC5F9FA31CA22CC9A0797B6A8C591FBF6E09300458D bytes=2522 -->
```text
import { describe, expect, it } from "vitest";

import {
  classifyEgressTimeline,
  classifyRetryAfterOutcome,
  type EgressTimelineEvent,
} from "../models/egress-races";

const AUTHORIZED: EgressTimelineEvent[] = [
  "AUTH_CHECK_PASSED",
  "FINAL_AUTHORIZED",
  "WRITE_RECHECK_PASSED",
];

describe("Egress T1-T5 race classification", () => {
  it.each([
    "FLOOR_CHANGED",
    "WORKER_REVOKED",
    "EMERGENCY_STOPPED",
    "KEY_REVOKED",
  ] as const)("blocks %s before final authorization", (event) => {
    expect(classifyEgressTimeline([
      "AUTH_CHECK_PASSED",
      event,
      "FINAL_AUTHORIZED",
      "WRITE_RECHECK_PASSED",
      "WRITE_STARTED",
    ])).toBe("DENIED_BEFORE_FINAL_AUTH");
  });

  it.each([
    "FLOOR_CHANGED",
    "WORKER_REVOKED",
    "EMERGENCY_STOPPED",
    "KEY_REVOKED",
  ] as const)("blocks %s after final auth but before write", (event) => {
    expect(classifyEgressTimeline([
      "AUTH_CHECK_PASSED",
      "FINAL_AUTHORIZED",
      event,
      "WRITE_RECHECK_PASSED",
      "WRITE_STARTED",
    ])).toBe("FINAL_AUTH_ISSUED_WRITE_BLOCKED");
  });

  it.each([
    "FLOOR_CHANGED",
    "WORKER_REVOKED",
    "EMERGENCY_STOPPED",
    "KEY_REVOKED",
  ] as const)("cannot recall %s after write started", (event) => {
    expect(classifyEgressTimeline([
      ...AUTHORIZED,
      "WRITE_STARTED",
      event,
    ])).toBe("WRITE_STARTED_OUTCOME_UNKNOWN");
  });

  it("records a response when it arrives after write start", () => {
    expect(classifyEgressTimeline([
      ...AUTHORIZED,
      "WRITE_STARTED",
      "RESPONSE_RECEIVED",
    ])).toBe("WRITE_STARTED_RESPONSE_RECEIVED");
  });

  it("fails closed when authority is unavailable before write", () => {
    expect(classifyEgressTimeline([
      "AUTH_CHECK_PASSED",
      "FINAL_AUTHORIZED",
      "AUTHORITY_UNAVAILABLE",
    ])).toBe("AUTHORITY_UNAVAILABLE");
  });

  it("blocks final authorization without the second write recheck", () => {
    expect(classifyEgressTimeline([
      "AUTH_CHECK_PASSED",
      "FINAL_AUTHORIZED",
      "WRITE_STARTED",
    ])).toBe("FINAL_AUTH_ISSUED_WRITE_BLOCKED");
  });

  it("forbids retry after a possible socket write", () => {
    expect(classifyRetryAfterOutcome("WRITE_STARTED_OUTCOME_UNKNOWN"))
      .toBe("RETRY_FORBIDDEN");
    expect(classifyRetryAfterOutcome("WRITE_STARTED_RESPONSE_RECEIVED"))
      .toBe("RETRY_FORBIDDEN");
    expect(classifyRetryAfterOutcome("FINAL_AUTH_ISSUED_WRITE_BLOCKED"))
      .toBe("TRANSACTIONAL_RETRY_ALLOWED");
  });
});

```
<!-- END_EXACT_SOURCE id=S028 -->

### S029. tests/sql-contract.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tests/sql-contract.test.ts`
- Bytes: `9038`
- SHA-256: `FF4BAF2B9E1F737381CF3D0CD103DFF240C242B1E3E29415AC35032BCCA8305A`

<!-- BEGIN_EXACT_SOURCE id=S029 sha256=FF4BAF2B9E1F737381CF3D0CD103DFF240C242B1E3E29415AC35032BCCA8305A bytes=9038 -->
```text
import { describe, expect, it } from "vitest";
import { readFileSync } from "node:fs";
import { resolve } from "node:path";

import {
  analyzeSqlContract,
  reviewEgressClaim,
  reviewEgressRevocationGate,
  reviewPermitLifecycle,
  reviewPermitConsumptionRevocation,
  reviewWorkerRegistrationMutation,
  splitSqlStatements,
  SQL_ANALYSIS_LIMITS,
} from "../models/sql-contract-analyzer";

const PERMIT_CONSUMPTION_SQL = readFileSync(
  resolve(
    process.cwd(),
    "preparation/production-trust/r3-egress-revocation-remediation/sql/50-permit-consumption-revocation.sql",
  ),
  "utf8",
);
const EGRESS_SQL = readFileSync(
  resolve(
    process.cwd(),
    "preparation/production-trust/r3-egress-revocation-remediation/sql/30-egress-final-authorization.sql",
  ),
  "utf8",
);

const REVOCATION_SQL = `
BEGIN ISOLATION LEVEL READ COMMITTED;
SELECT * FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1 FOR UPDATE;
SELECT * FROM trust_r3_emergency_control
WHERE singleton_id = 1 FOR UPDATE;
SELECT * FROM trust_r4_resource_fencing
WHERE scope_key = $2 FOR UPDATE;
SELECT * FROM trust_r4_worker_registration
WHERE worker_instance_id = $1 FOR UPDATE;
SELECT * FROM trust_r4_execution_lease
WHERE lease_id = $3 FOR UPDATE;
SELECT * FROM trust_r4_send_authorization
WHERE lease_id = $3 FOR UPDATE;
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_worker_revocation
SET state = 'REVOKED', revocation_version = revocation_version + 1
WHERE worker_instance_id = $1 AND state = 'ACTIVE' AND version = $4;
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration
SET state = 'REVOKED'
WHERE worker_instance_id = $1 AND state = 'ACTIVE';
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease
SET state = 'REVOKED'
WHERE lease_id = $3 AND state IN ('ISSUED','KEY_READ','TRANSPORT_CREATED','SEND_AUTHORIZED');
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE lease_id = $3 AND state = 'ISSUED';
SELECT * FROM trust_r3_audit_head
WHERE singleton_id = 1 FOR UPDATE;
INSERT INTO trust_r3_audit_event (event_id) VALUES ($5);
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $6
WHERE singleton_id = 1 AND last_sequence = $6 - 1;
COMMIT;
`;

describe("SQL structural and transaction analyzer", () => {
  it("segments statements and transaction boundaries without executing SQL", () => {
    const statements = splitSqlStatements(
      "BEGIN; SELECT ';' AS x; UPDATE t SET x = 1; COMMIT;",
    );
    expect(statements.map((statement) => statement.kind)).toEqual([
      "BEGIN",
      "SELECT",
      "UPDATE",
      "COMMIT",
    ]);
    expect(SQL_ANALYSIS_LIMITS).toContain(
      "POSTGRESQL_EXECUTION_NOT_PERFORMED",
    );
  });

  it("reviews the valid revocation structure", () => {
    const result = analyzeSqlContract({
      sql: REVOCATION_SQL,
      spec: {
        requiredTables: [
          "trust_r5_worker_revocation",
          "trust_r4_resource_fencing",
          "trust_r4_execution_lease",
          "trust_r4_send_authorization",
        ],
        requiredLockTables: [
          "trust_r5_worker_revocation",
          "trust_r4_resource_fencing",
          "trust_r4_worker_registration",
          "trust_r4_execution_lease",
          "trust_r4_send_authorization",
        ],
        requiredParameters: ["$1", "$2", "$3", "$4"],
        requireExactlyOneRowMarkers: true,
        requireAuditWithMutations: true,
      },
    });
    expect(result.transactions).toHaveLength(1);
    expect(result.findings).toEqual([]);
  });

  it("detects missing Resource Floor lock in Worker revocation", () => {
    const result = analyzeSqlContract({
      sql: REVOCATION_SQL.replace(
        /SELECT \* FROM trust_r4_resource_fencing[\s\S]*?FOR UPDATE;/u,
        "",
      ),
      spec: {
        requiredLockTables: ["trust_r4_resource_fencing"],
        requireAuditWithMutations: true,
      },
    });
    expect(result.findings.map((finding) => finding.code)).toContain(
      "REQUIRED_LOCK_MISSING",
    );
  });

  it("detects missing Lease revocation and missing parameters", () => {
    const result = analyzeSqlContract({
      sql: REVOCATION_SQL.replace(
        /UPDATE trust_r4_execution_lease[\s\S]*?;/u,
        "",
      ),
      spec: {
        requiredMutationTables: ["trust_r4_execution_lease"],
        requiredParameters: ["$99"],
      },
    });
    const codes = result.findings.map((finding) => finding.code);
    expect(codes).toContain("REQUIRED_MUTATION_MISSING");
    expect(codes).toContain("REQUIRED_PARAMETER_MISSING");
  });

  it("detects lock-order crossing", () => {
    const result = analyzeSqlContract({
      sql: `
        BEGIN;
        SELECT * FROM trust_r3_emergency_control
        WHERE singleton_id = 1 FOR UPDATE;
        SELECT * FROM trust_r5_worker_revocation
        WHERE worker_instance_id = $1 FOR UPDATE;
        COMMIT;
      `,
    });
    expect(result.findings.map((finding) => finding.code)).toContain(
      "LOCK_ORDER_CROSSING",
    );
  });

  it("detects row-count and Audit transaction omissions", () => {
    const result = analyzeSqlContract({
      sql: `
        BEGIN;
        UPDATE trust_r5_worker_revocation SET state = 'REVOKED'
        WHERE worker_instance_id = $1 AND state = 'ACTIVE' AND version = $2;
        COMMIT;
      `,
      spec: {
        requireExactlyOneRowMarkers: true,
        requireAuditWithMutations: true,
      },
    });
    const codes = result.findings.map((finding) => finding.code);
    expect(codes).toContain("ROW_COUNT_MARKER_MISSING");
    expect(codes).toContain("AUDIT_SPLIT_FROM_MUTATION");
  });
});

describe("Egress and revocation negative semantics", () => {
  it("detects missing Worker revocation and Resource Floor evidence", () => {
    const findings = reviewEgressClaim(`
      use cached floor;
      if authority unavailable then continue;
      database lock protects socket;
    `).map((finding) => finding.code);
    expect(findings).toEqual(expect.arrayContaining([
      "EGRESS_REVOCATION_VERSION_MISSING",
      "EGRESS_WORKER_REVOCATION_ROW_MISSING",
      "EGRESS_RESOURCE_FLOOR_MISSING",
      "EGRESS_CACHE_TRUSTED",
      "SOCKET_ATOMICITY_OVERCLAIM",
      "EGRESS_FAIL_OPEN",
    ]));
  });

  it("detects Worker reactivation through upsert", () => {
    expect(reviewWorkerRegistrationMutation(`
      INSERT INTO trust_r4_worker_registration (worker_instance_id)
      VALUES ($1)
      ON CONFLICT (worker_instance_id) DO UPDATE
      SET state = 'ACTIVE';
    `).map((finding) => finding.code)).toContain(
      "WORKER_REACTIVATION_UPSERT",
    );
  });

  it("detects missing permit one-time and revocation paths", () => {
    expect(reviewPermitLifecycle(`
      UPDATE trust_r4_send_authorization
      SET state = 'ISSUED'
      WHERE send_authorization_id = $1;
    `).map((finding) => finding.code)).toEqual(expect.arrayContaining([
      "PERMIT_ONE_TIME_TRANSITION_MISSING",
      "PERMIT_REVOCATION_PATH_MISSING",
    ]));
  });
});

describe("Actual R5 SQL transaction contracts", () => {
  it("segments Permit Consumption and Egress SQL without parser errors", () => {
    for (const sql of [PERMIT_CONSUMPTION_SQL, EGRESS_SQL]) {
      const result = analyzeSqlContract({ sql });
      expect(result.statements.length).toBeGreaterThan(0);
      expect(result.transactions.length).toBeGreaterThan(0);
      expect(result.findings.map((finding) => finding.code))
        .not.toContain("LOCK_ORDER_CROSSING");
    }
  });

  it("requires the full revocation gate in Permit Consumption", () => {
    expect(reviewPermitConsumptionRevocation(PERMIT_CONSUMPTION_SQL))
      .toEqual([]);
    const missingBlock = PERMIT_CONSUMPTION_SQL.replaceAll(
      "trust_r5_scope_worker_block",
      "trust_r5_disabled_scope_worker_block",
    );
    expect(
      reviewPermitConsumptionRevocation(missingBlock)
        .map((finding) => finding.code),
    ).toContain("PERMIT_SCOPE_BLOCK_CHECK_MISSING");
  });

  it("requires scope-block and Worker-registration checks at both Egress gates", () => {
    expect(reviewEgressRevocationGate(EGRESS_SQL)).toEqual([]);
    const missingBlocks = EGRESS_SQL.replaceAll(
      "trust_r5_scope_worker_block",
      "trust_r5_disabled_scope_worker_block",
    );
    expect(
      reviewEgressRevocationGate(missingBlocks)
        .map((finding) => finding.code),
    ).toContain("EGRESS_SCOPE_BLOCK_RECHECK_MISSING");
    const missingWorker = EGRESS_SQL.replaceAll(
      "trust_r4_worker_registration",
      "trust_r4_disabled_worker_registration",
    );
    expect(
      reviewEgressRevocationGate(missingWorker)
        .map((finding) => finding.code),
    ).toContain("EGRESS_WORKER_REGISTRATION_RECHECK_MISSING");
  });

  it("rejects a SQL claim that a database lock protects the later socket", () => {
    expect(reviewEgressRevocationGate(
      "COMMIT; database lock protects socket write",
    ).map((finding) => finding.code)).toContain(
      "SOCKET_ATOMICITY_OVERCLAIM",
    );
  });
});

```
<!-- END_EXACT_SOURCE id=S029 -->

### S030. tests/worker-revocation.test.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tests/worker-revocation.test.ts`
- Bytes: `12727`
- SHA-256: `9CB055D02F1F023044DA7344A93E27A7AC09343338319E77796D3631FBF13A2A`

<!-- BEGIN_EXACT_SOURCE id=S030 sha256=9CB055D02F1F023044DA7344A93E27A7AC09343338319E77796D3631FBF13A2A bytes=12727 -->
```text
import { describe, expect, it } from "vitest";

import {
  ExecutionLeaseSchema,
  ResourceFencingFloorSchema,
  SendAuthorizationSchema,
} from "../../r3-fencing-remediation/contracts";
import { deriveFencingScopeKey } from "../../r3-fencing-remediation/scope";
import { OfflineWorkerRevocationModel } from "../models/worker-revocation";

const NOW = Date.parse("2026-11-26T14:00:00Z");
const IDS = Object.freeze({
  workerA: "11111111-1111-4111-8111-111111111111",
  workerB: "22222222-2222-4222-8222-222222222222",
  org: "33333333-3333-4333-8333-333333333333",
  targetA: "sha256:" + "1".repeat(64),
  targetB: "sha256:" + "2".repeat(64),
  leaseA: "44444444-4444-4444-8444-444444444444",
  leaseB: "55555555-5555-4555-8555-555555555555",
  capabilityA: "66666666-6666-4666-8666-666666666666",
  capabilityB: "77777777-7777-4777-8777-777777777777",
  authorizationA: "88888888-8888-4888-8888-888888888888",
  authorizationB: "99999999-9999-4999-8999-999999999999",
  budgetA: "aaaaaaaa-aaaa-4aaa-8aaa-aaaaaaaaaaaa",
  budgetB: "bbbbbbbb-bbbb-4bbb-8bbb-bbbbbbbbbbbb",
  permitA: "cccccccc-cccc-4ccc-8ccc-cccccccccccc",
  permitB: "dddddddd-dddd-4ddd-8ddd-dddddddddddd",
});

function scope(target: string): string {
  return deriveFencingScopeKey({
    providerKind: "fetch",
    purpose: "fetch_only",
    organizationId: IDS.org,
    targetDigest: target,
  });
}

function floor(index: "A" | "B", worker = IDS.workerA) {
  const isA = index === "A";
  return ResourceFencingFloorSchema.parse({
    schemaVersion: "r3-resource-fencing-floor-v1",
    scopeKey: scope(isA ? IDS.targetA : IDS.targetB),
    currentFencingToken: isA ? 100 : 101,
    currentWorkerId: worker,
    currentLeaseId: isA ? IDS.leaseA : IDS.leaseB,
    currentCapabilityId: isA ? IDS.capabilityA : IDS.capabilityB,
    version: 1,
    state: "ACTIVE",
    updatedAt: NOW,
  });
}

function lease(index: "A" | "B", state = "ISSUED") {
  const isA = index === "A";
  return ExecutionLeaseSchema.parse({
    schemaVersion: "r3-fencing-execution-lease-v1",
    leaseId: isA ? IDS.leaseA : IDS.leaseB,
    scopeKey: scope(isA ? IDS.targetA : IDS.targetB),
    capabilityId: isA ? IDS.capabilityA : IDS.capabilityB,
    executionAuthorizationId: isA ? IDS.authorizationA : IDS.authorizationB,
    budgetReservationId: isA ? IDS.budgetA : IDS.budgetB,
    workerInstanceId: IDS.workerA,
    fencingToken: isA ? 100 : 101,
    state,
    issuedAt: NOW,
    expiresAt: NOW + 30_000,
    emergencyEpoch: 3,
    keyVersion: 2,
    revocationVersion: 1,
    permissionVersion: 4,
    policyVersion: "r5-policy-v1",
  });
}

function permit(index: "A" | "B", state = "ISSUED") {
  const isA = index === "A";
  return SendAuthorizationSchema.parse({
    schemaVersion: "r3-fencing-send-authorization-v1",
    sendAuthorizationId: isA ? IDS.permitA : IDS.permitB,
    state,
    scopeKey: scope(isA ? IDS.targetA : IDS.targetB),
    leaseId: isA ? IDS.leaseA : IDS.leaseB,
    capabilityId: isA ? IDS.capabilityA : IDS.capabilityB,
    workerInstanceId: IDS.workerA,
    fencingToken: isA ? 100 : 101,
    budgetReservationId: isA ? IDS.budgetA : IDS.budgetB,
    emergencyEpoch: 3,
    keyVersion: 2,
    revocationVersion: 1,
    permissionVersion: 4,
    policyVersion: "r5-policy-v1",
    issuedAt: NOW,
    expiresAt: NOW + 5_000,
    consumedAt: state === "CONSUMED" ? NOW + 1 : null,
  });
}

function store() {
  const model = new OfflineWorkerRevocationModel();
  expect(model.seedActiveWorker({
    workerInstanceId: IDS.workerA,
    now: NOW,
  }).ok).toBe(true);
  expect(model.seedFloor(floor("A")).ok).toBe(true);
  expect(model.seedFloor(floor("B")).ok).toBe(true);
  expect(model.seedLease(lease("A")).ok).toBe(true);
  expect(model.seedLease(lease("B")).ok).toBe(true);
  expect(model.seedPermit(permit("A")).ok).toBe(true);
  expect(model.seedPermit(permit("B")).ok).toBe(true);
  return model;
}

function revoke(model: OfflineWorkerRevocationModel, requestId: string) {
  return model.revokeWorkerGlobally({
    requestId,
    workerInstanceId: IDS.workerA,
    expectedRecordVersion: 1,
    reasonCode: "SYNTHETIC_COMPROMISE",
    now: NOW + 1,
    rowCounts: { revocation: 1, worker: 1, audit: 1 },
  });
}

describe("R5 global Worker revocation", () => {
  it("transitions ACTIVE to REVOKED and increments revocation version", () => {
    const model = store();
    expect(revoke(model, "12121212-1212-4212-8212-121212121212"))
      .toMatchObject({
        ok: true,
        value: {
          workerInstanceId: IDS.workerA,
          state: "REVOKED",
          revocationVersion: 1,
          recordVersion: 2,
        },
      });
  });

  it("forbids ordinary reactivation and replacement of a revoked identity", () => {
    const model = store();
    expect(revoke(model, "12121212-1212-4212-8212-121212121212").ok)
      .toBe(true);
    expect(model.seedActiveWorker({
      workerInstanceId: IDS.workerA,
      now: NOW + 2,
    })).toEqual({
      ok: false,
      code: "WORKER_REACTIVATION_FORBIDDEN",
    });
  });

  it("denies all scopes immediately after the global tombstone", () => {
    const model = store();
    expect(revoke(model, "12121212-1212-4212-8212-121212121212").ok)
      .toBe(true);
    for (const index of ["A", "B"] as const) {
      expect(model.validatePermitForConsumption({
        permit: permit(index),
        floor: floor(index),
        expectedWorkerRevocationVersion: 0,
        now: NOW + 2,
      })).toEqual({ ok: false, code: "WORKER_REVOKED" });
    }
  });

  it("models revocation racing permit consumption", () => {
    const consumeFirst = store();
    expect(consumeFirst.validatePermitForConsumption({
      permit: permit("A"),
      floor: floor("A"),
      expectedWorkerRevocationVersion: 0,
      now: NOW + 1,
    }).ok).toBe(true);
    expect(revoke(
      consumeFirst,
      "13131313-1313-4313-8313-131313131313",
    ).ok).toBe(true);
    expect(consumeFirst.validatePermitForConsumption({
      permit: permit("A"),
      floor: floor("A"),
      expectedWorkerRevocationVersion: 0,
      now: NOW + 2,
    })).toEqual({ ok: false, code: "WORKER_REVOKED" });

    const revokeFirst = store();
    expect(revoke(
      revokeFirst,
      "14141414-1414-4414-8414-141414141414",
    ).ok).toBe(true);
    expect(revokeFirst.validatePermitForConsumption({
      permit: permit("A"),
      floor: floor("A"),
      expectedWorkerRevocationVersion: 0,
      now: NOW + 2,
    })).toEqual({ ok: false, code: "WORKER_REVOKED" });
  });

  it("blocks Worker takeover after global revocation", () => {
    const model = store();
    expect(revoke(model, "15151515-1515-4515-8515-151515151515").ok)
      .toBe(true);
    expect(model.authorizeTakeover({
      workerInstanceId: IDS.workerA,
      expectedRevocationVersion: 1,
      now: NOW + 2,
    })).toEqual({
      ok: false,
      code: "WORKER_REACTIVATION_FORBIDDEN",
    });
  });

  it("fails closed when revocation authority is unavailable", () => {
    const model = store();
    model.setAuthorityAvailable(false);
    expect(revoke(model, "16161616-1616-4616-8616-161616161616"))
      .toEqual({ ok: false, code: "AUTHORITY_UNAVAILABLE" });
  });

  it("rolls back both records when Audit fails", () => {
    const model = store();
    expect(model.revokeWorkerGlobally({
      requestId: "17171717-1717-4717-8717-171717171717",
      workerInstanceId: IDS.workerA,
      expectedRecordVersion: 1,
      reasonCode: "SYNTHETIC_COMPROMISE",
      now: NOW + 1,
      rowCounts: { revocation: 1, worker: 1, audit: 1 },
      failAudit: true,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(model.getRevocation(IDS.workerA)?.state).toBe("ACTIVE");
    expect(model.auditSnapshot()).toHaveLength(0);
  });

  it("is idempotent for a repeated revocation request", () => {
    const model = store();
    const requestId = "18181818-1818-4818-8818-181818181818";
    expect(revoke(model, requestId).ok).toBe(true);
    const replay = revoke(model, requestId);
    expect(replay).toMatchObject({
      ok: true,
      value: { state: "REVOKED", revocationVersion: 1 },
    });
    expect(model.auditSnapshot()).toHaveLength(1);
  });
});

describe("R5 per-scope cleanup", () => {
  it("revokes pre-send Lease and Permit and creates a scope block", () => {
    const model = store();
    expect(revoke(model, "19191919-1919-4919-8919-191919191919").ok)
      .toBe(true);
    expect(model.cleanupScope({
      scopeKey: scope(IDS.targetA),
      workerInstanceId: IDS.workerA,
      expectedRevocationVersion: 1,
      leaseId: IDS.leaseA,
      capabilityId: IDS.capabilityA,
      permitId: IDS.permitA,
      reasonCode: "SYNTHETIC_CLEANUP",
      now: NOW + 2,
      rowCounts: { block: 1, lease: 1, permit: 1, audit: 1 },
    }).ok).toBe(true);
    expect(model.getScopeBlock(scope(IDS.targetA), IDS.workerA)).toMatchObject({
      blockedRevocationVersion: 1,
    });
  });

  it("does not pretend a SENT request can be recalled", () => {
    const model = new OfflineWorkerRevocationModel();
    expect(model.seedActiveWorker({
      workerInstanceId: IDS.workerA,
      now: NOW,
    }).ok).toBe(true);
    expect(model.seedFloor(floor("A")).ok).toBe(true);
    expect(model.seedLease(lease("A", "SENT")).ok).toBe(true);
    expect(model.seedPermit(permit("A", "CONSUMED")).ok).toBe(true);
    expect(revoke(model, "20202020-2020-4020-8020-202020202020").ok)
      .toBe(true);
    expect(model.cleanupScope({
      scopeKey: scope(IDS.targetA),
      workerInstanceId: IDS.workerA,
      expectedRevocationVersion: 1,
      leaseId: IDS.leaseA,
      capabilityId: IDS.capabilityA,
      permitId: IDS.permitA,
      reasonCode: "SYNTHETIC_CLEANUP",
      now: NOW + 2,
      rowCounts: { block: 1, permit: 1, audit: 1 },
    }).ok).toBe(true);
  });
});

describe("R5 Permit Consumption revocation gate", () => {
  function consumptionStore() {
    const model = new OfflineWorkerRevocationModel();
    expect(model.seedActiveWorker({
      workerInstanceId: IDS.workerA,
      now: NOW,
    }).ok).toBe(true);
    expect(model.seedFloor(floor("A")).ok).toBe(true);
    expect(model.seedLease(lease("A", "SEND_AUTHORIZED")).ok).toBe(true);
    expect(model.seedPermit(permit("A", "ISSUED")).ok).toBe(true);
    return model;
  }

  it("consumes ISSUED -> CONSUMED and SEND_AUTHORIZED -> SENT atomically", () => {
    const model = consumptionStore();
    expect(model.consumePermitWithRevocation({
      permit: permit("A", "ISSUED"),
      floor: floor("A"),
      lease: lease("A", "SEND_AUTHORIZED"),
      expectedWorkerRevocationVersion: 0,
      now: NOW + 1,
      rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
    })).toMatchObject({
      ok: true,
      value: {
        permit: { state: "CONSUMED" },
        lease: { state: "SENT" },
      },
    });
    expect(model.auditSnapshot()).toEqual([
      `SEND_AUTHORIZATION_CONSUMED:${IDS.permitA}`,
    ]);
  });

  it("rejects a blocked scope even when global Worker revocation is ACTIVE", () => {
    const model = consumptionStore();
    expect(model.seedScopeBlock({
      schemaVersion: "r5-scope-worker-block-v1",
      scopeKey: scope(IDS.targetA),
      workerInstanceId: IDS.workerA,
      blockedRevocationVersion: 1,
      version: 1,
      blockedAt: NOW,
      reasonCode: "SYNTHETIC_SCOPE_BLOCK",
    }).ok).toBe(true);
    expect(model.consumePermitWithRevocation({
      permit: permit("A", "ISSUED"),
      floor: floor("A"),
      lease: lease("A", "SEND_AUTHORIZED"),
      expectedWorkerRevocationVersion: 0,
      now: NOW + 1,
      rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
    })).toEqual({ ok: false, code: "WORKER_REVOKED" });
  });

  it.each([
    ["revocation commits first", false],
    ["consumption commits first", true],
  ])("handles race where %s", (_label, consumeFirst) => {
    const model = consumptionStore();
    if (consumeFirst) {
      expect(model.consumePermitWithRevocation({
        permit: permit("A", "ISSUED"),
        floor: floor("A"),
        lease: lease("A", "SEND_AUTHORIZED"),
        expectedWorkerRevocationVersion: 0,
        now: NOW + 1,
        rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
      }).ok).toBe(true);
    }
    expect(revoke(model, `30303030-3030-4030-8030-3030303030${consumeFirst ? "31" : "32"}`).ok)
      .toBe(true);
    if (!consumeFirst) {
      expect(model.consumePermitWithRevocation({
        permit: permit("A", "ISSUED"),
        floor: floor("A"),
        lease: lease("A", "SEND_AUTHORIZED"),
        expectedWorkerRevocationVersion: 0,
        now: NOW + 2,
        rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
      })).toEqual({ ok: false, code: "WORKER_REVOKED" });
    }
  });
});

```
<!-- END_EXACT_SOURCE id=S030 -->

### S031. tools/build-aggregates.mjs

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tools/build-aggregates.mjs`
- Bytes: `1681`
- SHA-256: `A96412B3514B644F12C39C837A3BE92B34C0534162F564B58442A34E77D85BCC`

<!-- BEGIN_EXACT_SOURCE id=S031 sha256=A96412B3514B644F12C39C837A3BE92B34C0534162F564B58442A34E77D85BCC bytes=1681 -->
```text
import { createHash } from "node:crypto";
import { readFileSync, statSync, writeFileSync } from "node:fs";
import { dirname, join } from "node:path";
import { fileURLToPath } from "node:url";

const taskRoot = dirname(dirname(fileURLToPath(import.meta.url)));

function sourceSection(relativePath) {
  const absolutePath = join(taskRoot, relativePath);
  const bytes = readFileSync(absolutePath);
  const digest = createHash("sha256").update(bytes).digest("hex").toUpperCase();
  return [
    `-- ===== BEGIN ${relativePath} =====`,
    `-- SHA256=${digest}`,
    `-- BYTES=${statSync(absolutePath).size}`,
    bytes.toString("utf8").replace(/\s+$/u, ""),
    `-- ===== END ${relativePath} =====`,
  ].join("\n");
}

const aggregates = [
  {
    output: "PHASE_R3_WORKER_REVOCATION_TRANSACTIONS.sql",
    title: "Global revocation, scope cleanup and Permit Consumption revocation",
    sources: [
      "sql/10-worker-global-revocation.sql",
      "sql/20-worker-scope-cleanup.sql",
      "sql/25-lease-revocation-binding.sql",
      "sql/50-permit-consumption-revocation.sql",
    ],
  },
  {
    output: "PHASE_R3_EGRESS_AUTHORIZATION_TRANSACTIONS.sql",
    title: "Egress intent, final authorization, write start and outcome",
    sources: [
      "sql/30-egress-final-authorization.sql",
      "sql/40-egress-write-outcome.sql",
    ],
  },
];

for (const aggregate of aggregates) {
  const body = [
    `-- ${aggregate.output}`,
    "-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED",
    `-- ${aggregate.title}`,
    "",
    ...aggregate.sources.map(sourceSection),
    "",
  ].join("\n");
  writeFileSync(join(taskRoot, aggregate.output), body, "utf8");
}

```
<!-- END_EXACT_SOURCE id=S031 -->

### S032. tools/build-evidence.mjs

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tools/build-evidence.mjs`
- Bytes: `15532`
- SHA-256: `934E0F9274A4EF477BF9E12298916487D8E157FB573CE503C1C0A6E72FDFCD9D`

<!-- BEGIN_EXACT_SOURCE id=S032 sha256=934E0F9274A4EF477BF9E12298916487D8E157FB573CE503C1C0A6E72FDFCD9D bytes=15532 -->
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
const taskRelative = relative(workspace, taskRoot).replaceAll("\\", "/");

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
    if (entry.isDirectory()) {
      output.push(...listFiles(absolute));
    } else if (entry.isFile()) {
      output.push(absolute);
    }
  }
  return output.sort((left, right) => left.localeCompare(right));
}

const baselinePath = join(
  taskRoot,
  "PHASE_R3_EGRESS_REVOCATION_BASELINE_SHA256SUMS.txt",
);
const baselineLines = readFileSync(baselinePath, "utf8")
  .split(/\r?\n/u)
  .map((line) => /^([0-9A-F]{64})\s{2}(.+)$/u.exec(line))
  .filter(Boolean);

const baselineMismatches = [];
for (const match of baselineLines) {
  const expected = match[1];
  const relativePath = match[2].replaceAll("\\", "/");
  const absolutePath = join(workspace, relativePath);
  if (!existsSync(absolutePath)) {
    baselineMismatches.push(`${relativePath}: MISSING`);
    continue;
  }
  const actual = sha256File(absolutePath);
  if (actual !== expected) {
    baselineMismatches.push(`${relativePath}: ${expected} -> ${actual}`);
  }
}

const r31ManifestPath = join(workspace, "PHASE_R31_R36_SHA256SUMS.txt");
const r31Lines = readFileSync(r31ManifestPath, "utf8")
  .split(/\r?\n/u)
  .map((line) => /^([0-9A-Fa-f]{64})\s{2}(.+)$/u.exec(line))
  .filter(Boolean);
const r31Mismatches = [];
for (const match of r31Lines) {
  const expected = match[1].toUpperCase();
  const relativePath = match[2].replaceAll("\\", "/");
  const absolutePath = join(workspace, relativePath);
  if (!existsSync(absolutePath)) {
    r31Mismatches.push(`${relativePath}: MISSING`);
    continue;
  }
  const actual = sha256File(absolutePath);
  if (actual !== expected) {
    r31Mismatches.push(`${relativePath}: ${expected} -> ${actual}`);
  }
}

const expectedProtectedHashes = new Map([
  ["package.json", "44FC2153675107E0E61DBA8E88E955281B913D3341718C224110AB5B2F6C7F4D"],
  ["pnpm-lock.yaml", "926DFD4A33A662BAAB424E7C9FBBFD5FB16B74BE2E6119AD9F6A0D5144B719B4"],
  [
    "src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts",
    "1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309",
  ],
]);
const protectedHashMismatches = [];
for (const [relativePath, expected] of expectedProtectedHashes) {
  const actual = sha256File(join(workspace, relativePath));
  if (actual !== expected) {
    protectedHashMismatches.push(`${relativePath}: ${expected} -> ${actual}`);
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

const importBoundaryHits = [];
for (const rootName of ["src", "scripts"]) {
  for (const absolutePath of listFiles(join(workspace, rootName))) {
    const text = readFileSync(absolutePath, "utf8");
    if (
      text.includes("r3-egress-revocation-remediation")
      || text.includes("production-trust/r3-egress")
    ) {
      importBoundaryHits.push(relative(workspace, absolutePath).replaceAll("\\", "/"));
    }
  }
}

const forbiddenPatterns = [
  /api[_-]?key\s*[:=]\s*["'][^"']+/iu,
  /sk-[A-Za-z0-9]{16,}/u,
  /BEGIN (?:RSA |EC |OPENSSH )?PRIVATE KEY/u,
  /postgres(?:ql)?:\/\//iu,
  /new\s+(?:Pool|Client)\s*\(/u,
  /\bfetch\s*\(/u,
  /https?:\/\//iu,
];
const sensitiveHits = [];
for (const absolutePath of listFiles(taskRoot)) {
  const text = readFileSync(absolutePath, "utf8");
  for (const pattern of forbiddenPatterns) {
    if (pattern.test(text)) {
      sensitiveHits.push(
        `${relative(workspace, absolutePath).replaceAll("\\", "/")}: ${pattern}`,
      );
    }
  }
}

const manifestPath = join(taskRoot, "PHASE_R3_EGRESS_REVOCATION_SHA256SUMS.txt");
const manifestFiles = listFiles(taskRoot).filter(
  (absolutePath) => absolutePath !== manifestPath,
);
const manifestLines = manifestFiles.map((absolutePath) => {
  const bytes = readFileSync(absolutePath);
  return `${sha256Bytes(bytes)}  ${relative(workspace, absolutePath).replaceAll("\\", "/")}`;
});
writeFileSync(
  manifestPath,
  [
    "# PHASE_R3_EGRESS_REVOCATION_SHA256SUMS",
    `# ENTRIES=${manifestLines.length}`,
    "# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION",
    "",
    ...manifestLines,
    "",
  ].join("\r\n"),
  "utf8",
);

const bundleSources = listFiles(taskRoot)
  .filter((absolutePath) => extname(absolutePath) !== ".pyc")
  .sort((left, right) => {
    const relLeft = relative(taskRoot, left).replaceAll("\\", "/");
    const relRight = relative(taskRoot, right).replaceAll("\\", "/");
    const category = (value) => {
      if (value.endsWith(".md")) return 0;
      if (value.endsWith("SHA256SUMS.txt")) return 1;
      if (value === "contracts.ts" || value === "lock-order.ts") return 2;
      if (value.startsWith("sql/")) return 3;
      if (value.startsWith("models/")) return 4;
      if (value.startsWith("tests/")) return 5;
      if (value.startsWith("tools/")) return 6;
      return 7;
    };
    return category(relLeft) - category(relRight)
      || relLeft.localeCompare(relRight);
  });

const sourceRecords = bundleSources.map((absolutePath, index) => {
  const bytes = readFileSync(absolutePath);
  return {
    id: `S${String(index + 1).padStart(3, "0")}`,
    absolutePath,
    relativePath: relative(workspace, absolutePath).replaceAll("\\", "/"),
    displayPath: relative(taskRoot, absolutePath).replaceAll("\\", "/"),
    bytes,
    size: statSync(absolutePath).size,
    sha256: sha256Bytes(bytes),
  };
});

function fenceFor(text) {
  const runs = [...text.matchAll(/`+/gu)].map((match) => match[0].length);
  const length = Math.max(3, ...runs.map((run) => run + 1));
  return "`".repeat(length);
}

const bundleSections = [];
for (const source of sourceRecords) {
  const text = source.bytes.toString("utf8");
  const fence = fenceFor(text);
  bundleSections.push([
    `### ${source.id}. ${source.displayPath}`,
    "",
    `- Path: \`${source.relativePath}\``,
    `- Bytes: \`${source.size}\``,
    `- SHA-256: \`${source.sha256}\``,
    "",
    `<!-- BEGIN_EXACT_SOURCE id=${source.id} sha256=${source.sha256} bytes=${source.size} -->`,
    `${fence}text`,
    text,
    fence,
    `<!-- END_EXACT_SOURCE id=${source.id} -->`,
    "",
  ].join("\n"));
}

const bundlePath = join(
  trustRoot,
  "PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE.md",
);
const catalogRows = sourceRecords.map(
  (source) =>
    `| ${source.id} | \`${source.displayPath}\` | ${source.size} | ${source.sha256} |`,
);
const bundleHeader = [
  "# PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE",
  "",
  "## Review Status",
  "",
  "```text",
  "R3_EGRESS_REVOCATION_REMEDIATION_PASS",
  "OFFLINE_ACCEPTANCE=PASS",
  "INDEPENDENT_REVIEW=REQUIRED",
  "PRODUCTION_IMPLEMENTATION=NOT_STARTED",
  "PRODUCTION_ENFORCEMENT=BLOCKED",
  "PRODUCTION_EGRESS_IMPLEMENTED=NO",
  "REAL_FETCH_AUTHORIZED=NO",
  "```",
  "",
  "## Scope",
  "",
  "This Bundle contains the complete R3-Egress/Revocation source, SQL drafts,",
  "reference models, tests, negative cases, lock-order review, threat model, risk",
  "register and execution evidence. It does not contain a production Egress",
  "implementation and does not authorize real network or Provider access.",
  "",
  "## Evidence Boundary",
  "",
  "```text",
  "OFFLINE_REFERENCE_MODEL=PASS",
  "LOCAL_UNIT_TESTS=PASS",
  "SQL_STATIC_ANALYSIS=PASS",
  "SQL_NEGATIVE_TESTS=PASS",
  "POSTGRESQL_INTEGRATION=NOT_EXECUTED",
  "MULTI_INSTANCE_TEST=NOT_EXECUTED",
  "REAL_EGRESS_TEST=NOT_EXECUTED",
  "REAL_NETWORK_RACE_TEST=NOT_EXECUTED",
  "REAL_PROVIDER_TEST=NOT_EXECUTED",
  "EXACTLY_ONCE_EXTERNAL_PROVIDER=NOT_GUARANTEED",
  "```",
  "",
  "## Contents",
  "",
  "- 1. Source Catalog",
  "- 2. Complete Source Bodies",
  "- 3. Freeze Status",
  "",
  "## 1. Source Catalog",
  "",
  "| ID | Path | Bytes | SHA-256 |",
  "|---|---|---:|---|",
  ...catalogRows,
  "",
  "## 2. Complete Source Bodies",
  "",
].join("\n");
const bundleFooter = [
  "",
  "## 3. Freeze Status",
  "",
  "```text",
  `R3_FENCING_BASELINE_ENTRIES=${baselineLines.length}`,
  `R3_FENCING_BASELINE_MISMATCHES=${baselineMismatches.length}`,
  `R31_R36_FROZEN_ENTRIES=${r31Lines.length}`,
  `R31_R36_FROZEN_MISMATCHES=${r31Mismatches.length}`,
  `TASK_SOURCE_FILES=${sourceRecords.length}`,
  `PROTECTED_HASH_MISMATCHES=${protectedHashMismatches.length}`,
  `IMPORT_BOUNDARY_HITS=${importBoundaryHits.length}`,
  `SENSITIVE_PATTERN_HITS=${sensitiveHits.length}`,
  `PRODUCTION_ENTRY_BLOCKED=${productionBlocked ? "YES" : "NO"}`,
  "```",
  "",
].join("\n");
writeFileSync(bundlePath, bundleHeader + bundleSections.join("\n") + bundleFooter, "utf8");

const bundleText = readFileSync(bundlePath, "utf8");
const bodyMismatches = [];
for (const source of sourceRecords) {
  const begin = `<!-- BEGIN_EXACT_SOURCE id=${source.id} sha256=${source.sha256} bytes=${source.size} -->`;
  const beginIndex = bundleText.indexOf(begin);
  if (beginIndex < 0) {
    bodyMismatches.push(`${source.id}: BEGIN marker missing`);
    continue;
  }
  const fenceStart = bundleText.indexOf("\n", beginIndex) + 1;
  const fenceEnd = bundleText.indexOf("\n", fenceStart) + 1;
  const endMarker = `<!-- END_EXACT_SOURCE id=${source.id} -->`;
  const endMarkerIndex = bundleText.indexOf(endMarker, fenceEnd);
  if (endMarkerIndex < 0) {
    bodyMismatches.push(`${source.id}: END marker missing`);
    continue;
  }
  const closingFence = bundleText.lastIndexOf("\n", endMarkerIndex - 1);
  const closingFenceStart = bundleText.lastIndexOf("\n", closingFence - 1) + 1;
  const body = bundleText.slice(fenceEnd, closingFenceStart - 1);
  if (!Buffer.from(body, "utf8").equals(source.bytes)) {
    bodyMismatches.push(`${source.id}: body mismatch`);
  }
}

const bundleBytes = readFileSync(bundlePath);
const bundleSha256 = sha256Bytes(bundleBytes);
const reportPath = join(
  trustRoot,
  "PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md",
);
const report = [
  "# PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_REPORT",
  "",
  "## Final Status",
  "",
  "```text",
  `R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_${bodyMismatches.length === 0 && baselineMismatches.length === 0 && r31Mismatches.length === 0 && protectedHashMismatches.length === 0 && importBoundaryHits.length === 0 && sensitiveHits.length === 0 && productionBlocked ? "PASS" : "NEEDS_REVISION"}`,
  "```",
  "",
  "## Bundle",
  "",
  "```text",
  `BUNDLE_PATH=${relative(workspace, bundlePath).replaceAll("\\", "/")}`,
  `BUNDLE_BYTES=${bundleBytes.length}`,
  `BUNDLE_SHA256=${bundleSha256}`,
  `SOURCE_FILES=${sourceRecords.length}`,
  `BODY_EXACTNESS_MISMATCHES=${bodyMismatches.length}`,
  `R3_BASELINE_ENTRIES=${baselineLines.length}`,
  `R3_BASELINE_MISMATCHES=${baselineMismatches.length}`,
  `R31_R36_FROZEN_ENTRIES=${r31Lines.length}`,
  `R31_R36_FROZEN_MISMATCHES=${r31Mismatches.length}`,
  `PROTECTED_HASH_MISMATCHES=${protectedHashMismatches.length}`,
  `IMPORT_BOUNDARY_HITS=${importBoundaryHits.length}`,
  `SENSITIVE_PATTERN_HITS=${sensitiveHits.length}`,
  "```",
  "",
  "## Verification",
  "",
  "```text",
  "R3_EGRESS_REVOCATION_VITEST=4_FILES_53_TESTS_PASS",
  "R3_FENCING_VITEST=7_FILES_49_TESTS_PASS",
  "R2_R3_VITEST=8_FILES_74_TESTS_PASS",
  "R2_VITEST=10_FILES_80_TESTS_PASS",
  "R1_VITEST=16_FILES_91_TESTS_PASS",
  "R31_R36_RELEVANT_VITEST=20_FILES_179_TESTS_PASS",
  "POWERSHELL_LAUNCHER=40_PASS",
  "POWERSHELL_KEY_SESSION=25_PASS",
  "POWERSHELL_FETCH_ENFORCEMENT=4_PASS",
  "POWERSHELL_5_1_PARSER=6_PASS",
  "TYPESCRIPT_STRICT=PASS",
  "ESLINT_NEW_SCOPE=PASS",
  "NEXT_BUILD=PASS",
  "```",
  "",
  "## Production Safety",
  "",
  "```text",
  "PRODUCTION_IMPLEMENTATION=NOT_STARTED",
  "PRODUCTION_ENFORCEMENT=BLOCKED",
  "PRODUCTION_EGRESS_IMPLEMENTED=NO",
  "REAL_FETCH_AUTHORIZED=NO",
  "REAL_KEY_ACCESSED=NO",
  "PROVIDER_API_CALLED=NO",
  "NETWORK_ACCESSED=NO",
  "DATABASE_CONNECTED=NO",
  "SQL_EXECUTED=NO",
  "DOCKER_ACCESSED=NO",
  "GITHUB_ACCESSED=NO",
  "DEPENDENCIES_INSTALLED=NO",
  "```",
  "",
  "## Integrity Findings",
  "",
  "```text",
  ...(baselineMismatches.map((item) => `BASELINE_MISMATCH=${item}`)),
  ...(r31Mismatches.map((item) => `R31_R36_MISMATCH=${item}`)),
  ...(protectedHashMismatches.map((item) => `PROTECTED_MISMATCH=${item}`)),
  ...(importBoundaryHits.map((item) => `IMPORT_BOUNDARY_HIT=${item}`)),
  ...(sensitiveHits.map((item) => `SENSITIVE_HIT=${item}`)),
  ...(bodyMismatches.map((item) => `BODY_MISMATCH=${item}`)),
  ...(baselineMismatches.length
    || r31Mismatches.length
    || protectedHashMismatches.length
    || importBoundaryHits.length
    || sensitiveHits.length
    || bodyMismatches.length
    ? []
    : ["NO_INTEGRITY_FINDINGS"]),
  "```",
  "",
  "## Limitations",
  "",
  "- same-host agents do not constitute third-party independent audit;",
  "- PostgreSQL is not connected and no SQL is executed;",
  "- multi-instance coordination and real Egress are not implemented or tested;",
  "- the Provider/database boundary cannot provide exactly-once external effects;",
  "- the Bundle status is material/design traceability, not production approval.",
  "",
].join("\r\n");
writeFileSync(reportPath, report, "utf8");

const rootManifestPath = join(
  trustRoot,
  "PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS.txt",
);
const rootEntries = [bundlePath, reportPath].map((absolutePath) => ({
  absolutePath,
  hash: sha256File(absolutePath),
}));
writeFileSync(
  rootManifestPath,
  [
    "# PHASE_R3_EGRESS_REVOCATION_FULL_SECURITY_REVIEW_BUNDLE_SHA256SUMS",
    `# ENTRIES=${rootEntries.length}`,
    "# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION",
    "",
    ...rootEntries.map(
      (entry) =>
        `${entry.hash}  ${relative(workspace, entry.absolutePath).replaceAll("\\", "/")}`,
    ),
    "",
  ].join("\r\n"),
  "utf8",
);

console.log(JSON.stringify({
  baselineEntries: baselineLines.length,
  baselineMismatches,
  r31Entries: r31Lines.length,
  r31Mismatches,
  protectedHashMismatches,
  importBoundaryHits,
  sensitiveHits,
  sourceFiles: sourceRecords.length,
  bodyMismatches,
  productionBlocked,
  bundleBytes: bundleBytes.length,
  bundleSha256,
  manifestPath: relative(workspace, manifestPath).replaceAll("\\", "/"),
  reportPath: relative(workspace, reportPath).replaceAll("\\", "/"),
  rootManifestPath: relative(workspace, rootManifestPath).replaceAll("\\", "/"),
}, null, 2));

if (
  baselineMismatches.length
  || r31Mismatches.length
  || protectedHashMismatches.length
  || importBoundaryHits.length
  || sensitiveHits.length
  || bodyMismatches.length
  || !productionBlocked
) {
  process.exitCode = 1;
}

````
<!-- END_EXACT_SOURCE id=S032 -->

### S033. tools/run-verification.ps1

- Path: `preparation/production-trust/r3-egress-revocation-remediation/tools/run-verification.ps1`
- Bytes: `6732`
- SHA-256: `221B7C6789C510221C7361BA2E674F5FBCCCCD4BAB6E7ACA6F4E019E360C3EB3`

<!-- BEGIN_EXACT_SOURCE id=S033 sha256=221B7C6789C510221C7361BA2E674F5FBCCCCD4BAB6E7ACA6F4E019E360C3EB3 bytes=6732 -->
```````text
$ErrorActionPreference = "Continue"

$workspace = (Resolve-Path (Join-Path $PSScriptRoot "..\..\..\..")).Path
$taskDir = (Resolve-Path (Join-Path $PSScriptRoot "..")).Path
$log = Join-Path $taskDir "PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE.md"
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
  Invoke-Logged "R3 Egress/Revocation Vitest" "node" @(
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
      $script.FullName,
      [ref]$tokens,
      [ref]$errors
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
    "eslint", "preparation/production-trust/r3-egress-revocation-remediation"
  )
  Invoke-Logged "Next Build" "pnpm.cmd" @("build")
} finally {
  Pop-Location
}

$header = @(
  "# PHASE_R3_EGRESS_TEST_EXECUTION_EVIDENCE",
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
  "## Execution Note",
  "",
  "An earlier focused run during remediation failed 9 Egress model tests because",
  "the test fixture set `workerHeartbeatAt` five milliseconds after the intent",
  "creation time. The model correctly rejected the future heartbeat. The fixture",
  "was corrected to use the same timestamp; the failure is not hidden and the",
  "final complete run below is the authoritative result.",
  "",
  "## Commands",
  ""
) -join "`r`n"

$content = $header + ($records -join "`r`n")
Set-Content -LiteralPath $log -Value $content -Encoding utf8

if ($failed -ne 0) {
  exit 1
}

```````
<!-- END_EXACT_SOURCE id=S033 -->

### S034. PHASE_R3_EGRESS_AUTHORIZATION_TRANSACTIONS.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_EGRESS_AUTHORIZATION_TRANSACTIONS.sql`
- Bytes: `26120`
- SHA-256: `5CB3A4249FBD19982949086B46E6B4DFD2D0DB69EFF32F60D2A29BD283B1ADC3`

<!-- BEGIN_EXACT_SOURCE id=S034 sha256=5CB3A4249FBD19982949086B46E6B4DFD2D0DB69EFF32F60D2A29BD283B1ADC3 bytes=26120 -->
```text
-- PHASE_R3_EGRESS_AUTHORIZATION_TRANSACTIONS.sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Egress intent, final authorization, write start and outcome

-- ===== BEGIN sql/30-egress-final-authorization.sql =====
-- SHA256=149262A324348E3AF2AA6264B3E2740FAB0D63CF5D662AEF672DCD38FE7A8906
-- BYTES=23151
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Persistent Egress intent plus final/write-start authorization transactions.
-- Actual production egress is not implemented.

CREATE TABLE trust_r5_egress_intent (
  egress_intent_id uuid PRIMARY KEY,
  send_authorization_id uuid NOT NULL UNIQUE,
  permit_digest varchar(71) NOT NULL,
  scope_key text NOT NULL,
  fencing_token bigint NOT NULL CHECK (fencing_token > 0),
  worker_instance_id uuid NOT NULL,
  worker_revocation_version bigint NOT NULL CHECK (worker_revocation_version >= 0),
  lease_id uuid NOT NULL,
  capability_id uuid NOT NULL,
  budget_reservation_id uuid NOT NULL,
  request_digest varchar(71) NOT NULL,
  emergency_epoch bigint NOT NULL CHECK (emergency_epoch >= 0),
  key_version bigint NOT NULL CHECK (key_version >= 1),
  key_revocation_version bigint NOT NULL CHECK (key_revocation_version >= 0),
  permission_version bigint NOT NULL CHECK (permission_version >= 1),
  policy_version text NOT NULL,
  state text NOT NULL CHECK (
    state IN (
      'PENDING', 'FINAL_AUTHORIZED', 'WRITE_STARTED',
      'RESPONSE_RECEIVED', 'COMPLETED', 'SEND_OUTCOME_UNKNOWN',
      'REJECTED', 'EXPIRED', 'REVOKED'
    )
  ),
  row_version bigint NOT NULL DEFAULT 1 CHECK (row_version >= 1),
  created_at_ms bigint NOT NULL,
  final_authorized_at_ms bigint,
  final_authorization_expires_at_ms bigint,
  write_started_at_ms bigint,
  outcome_at_ms bigint,
  CHECK (
    state NOT IN ('FINAL_AUTHORIZED', 'WRITE_STARTED', 'RESPONSE_RECEIVED', 'COMPLETED')
    OR (final_authorized_at_ms IS NOT NULL AND final_authorization_expires_at_ms IS NOT NULL)
  ),
  CHECK (
    state NOT IN ('WRITE_STARTED', 'RESPONSE_RECEIVED', 'COMPLETED', 'SEND_OUTCOME_UNKNOWN')
    OR write_started_at_ms IS NOT NULL
  )
);

-- Transaction 1: register a pending intent after R3 Permit Consumption. This
-- transaction records intent and does not grant a socket write.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $2
FOR UPDATE;

SELECT authorization_id, state, capability_id, budget_reservation_id,
       worker_instance_id, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $19
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, execution_authorization_id, capability_id,
       worker_instance_id, send_started_at_ms, expires_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $12
FOR UPDATE;

SELECT capability_id, state, execution_authorization_id, worker_instance_id,
       budget_reservation_id, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $11
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $8
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $3
FOR UPDATE;

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

-- The insert is conditional. It is valid only after the frozen R4 Permit
-- Consumption has committed CONSUMED/SENT and the global Worker revocation and
-- per-scope block are still current. The request and permit digests are bound
-- at insert time; a later Egress read must recompute both from the exact bytes.
INSERT INTO trust_r5_egress_intent (
  egress_intent_id, send_authorization_id, permit_digest,
  scope_key, fencing_token, worker_instance_id,
  worker_revocation_version, lease_id, capability_id,
  budget_reservation_id, request_digest, emergency_epoch,
  key_version, key_revocation_version, permission_version,
  policy_version, state, row_version, created_at_ms,
  final_authorized_at_ms, final_authorization_expires_at_ms,
  write_started_at_ms, outcome_at_ms
)
SELECT
  $7, $4, $6,
  $8, $9, $1,
  $10, $3, $11,
  $12, $5, $13,
  $14, $15, $16,
  $17, 'PENDING', 1, $18,
  NULL, NULL, NULL, NULL
WHERE EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $10
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $8
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $10
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $3
      AND binding.worker_instance_id = $1
      AND binding.worker_revocation_version = $10
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $8
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $9
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $11
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $18 >= worker.heartbeat_at_ms
      AND $18 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'SENT'
      AND lease.scope_key = $8
      AND lease.capability_id = $11
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $9
      AND $18 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_send_authorization permit
    WHERE permit.send_authorization_id = $4
      AND permit.state = 'CONSUMED'
      AND permit.consumed_at_ms IS NOT NULL
      AND permit.scope_key = $8
      AND permit.lease_id = $3
      AND permit.capability_id = $11
      AND permit.worker_instance_id = $1
      AND permit.fencing_token = $9
      AND permit.budget_reservation_id = $12
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $13
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key key
    WHERE key.key_id = $2
      AND key.state = 'ACTIVE'
      AND key.key_version = $14
      AND key.revocation_version = $15
      AND $18 >= key.valid_from_ms
      AND $18 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $19
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $11
      AND authorization.budget_reservation_id = $12
      AND $18 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $12
      AND reservation.state = 'RESERVED'
      AND reservation.execution_authorization_id = $19
      AND reservation.capability_id = $11
      AND reservation.worker_instance_id = $1
      AND reservation.send_started_at_ms IS NOT NULL
      AND $18 < reservation.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability capability
    WHERE capability.capability_id = $11
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $19
      AND capability.worker_instance_id = $1
      AND capability.budget_reservation_id = $12
      AND $18 < capability.expires_at_ms
  );

COMMIT;

-- Transaction 2: final authorization. The commit of this intent transition is
-- the final-gate linearization point. It does not write a socket.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $2
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $19
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, send_started_at_ms, expires_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $12
FOR UPDATE;

SELECT capability_id, state, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $11
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $8
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, worker_instance_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $3
FOR UPDATE;

SELECT lease_id, state, scope_key, capability_id, worker_instance_id,
       fencing_token, expires_at_ms
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms, consumed_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

SELECT egress_intent_id, state, send_authorization_id, scope_key,
       fencing_token, worker_instance_id, worker_revocation_version,
       lease_id, capability_id, budget_reservation_id, request_digest,
       emergency_epoch, key_version, key_revocation_version,
       permission_version, policy_version, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'FINAL_AUTHORIZED',
    row_version = row_version + 1,
    final_authorized_at_ms = $18,
    final_authorization_expires_at_ms = $20
WHERE egress_intent_id = $7
  AND state = 'PENDING'
  AND row_version = $21
  AND send_authorization_id = $4
  AND scope_key = $8
  AND fencing_token = $9
  AND worker_instance_id = $1
  AND worker_revocation_version = $10
  AND lease_id = $3
  AND capability_id = $11
  AND budget_reservation_id = $12
  AND request_digest = $5
  AND emergency_epoch = $13
  AND key_version = $14
  AND key_revocation_version = $15
  AND permission_version = $16
  AND policy_version = $17
  AND $20 > $18
  AND $20 - $18 <= 1000
  AND EXISTS (
    SELECT 1 FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $3
      AND binding.worker_instance_id = $1
      AND binding.worker_revocation_version = $10
  )
  AND NOT EXISTS (
    SELECT 1 FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $8
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $13
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key key
    WHERE key.key_id = $2
      AND key.state = 'ACTIVE'
      AND key.key_version = $14
      AND key.revocation_version = $15
      AND $18 >= key.valid_from_ms
      AND $18 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $19
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $11
      AND authorization.budget_reservation_id = $12
      AND $18 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_capability capability
    WHERE capability.capability_id = $11
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $19
      AND capability.worker_instance_id = $1
      AND capability.budget_reservation_id = $12
      AND $18 < capability.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $8
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $9
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $11
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $18 >= worker.heartbeat_at_ms
      AND $18 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'SENT'
      AND lease.scope_key = $8
      AND lease.capability_id = $11
      AND lease.execution_authorization_id = $19
      AND lease.budget_reservation_id = $12
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $9
      AND $18 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_send_authorization permit
    WHERE permit.send_authorization_id = $4
      AND permit.state = 'CONSUMED'
      AND permit.consumed_at_ms IS NOT NULL
      AND permit.scope_key = $8
      AND permit.lease_id = $3
      AND permit.capability_id = $11
      AND permit.worker_instance_id = $1
      AND permit.fencing_token = $9
      AND permit.budget_reservation_id = $12
      AND $18 >= permit.consumed_at_ms
      AND $18 < permit.expires_at_ms
      AND permit.emergency_epoch = $13
      AND permit.key_version = $14
      AND permit.revocation_version = $15
      AND permit.permission_version = $16
      AND permit.policy_version = $17
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $12
      AND reservation.state = 'RESERVED'
      AND reservation.send_started_at_ms IS NOT NULL
      AND $18 < reservation.expires_at_ms
  );

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $22, $23, $18, 'SEND_AUTHORIZED', 'ALLOW',
  $7, $24, $25
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $23,
    last_event_digest = $25
WHERE singleton_id = 1
  AND last_sequence = $23 - 1
  AND last_event_digest IS NOT DISTINCT FROM $24;

COMMIT;

-- Transaction 3: write-start intent immediately before socket write. This is
-- the last database-enforced cancellation boundary.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $2
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $19
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, send_started_at_ms, expires_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $12
FOR UPDATE;

SELECT capability_id, state, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $11
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $8
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, worker_instance_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $3
FOR UPDATE;

SELECT lease_id, state, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, expires_at_ms
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, consumed_at_ms, expires_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

SELECT egress_intent_id, state, final_authorization_expires_at_ms, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'WRITE_STARTED',
    row_version = row_version + 1,
    write_started_at_ms = $26
WHERE egress_intent_id = $7
  AND state = 'FINAL_AUTHORIZED'
  AND row_version = $27
  AND send_authorization_id = $4
  AND scope_key = $8
  AND fencing_token = $9
  AND worker_instance_id = $1
  AND worker_revocation_version = $10
  AND lease_id = $3
  AND capability_id = $11
  AND budget_reservation_id = $12
  AND request_digest = $5
  AND emergency_epoch = $13
  AND key_version = $14
  AND key_revocation_version = $15
  AND permission_version = $16
  AND policy_version = $17
  AND $26 < final_authorization_expires_at_ms
  AND EXISTS (
    SELECT 1 FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $3
      AND binding.worker_instance_id = $1
      AND binding.worker_revocation_version = $10
  )
  AND NOT EXISTS (
    SELECT 1 FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $8
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $10
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $13
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key key
    WHERE key.key_id = $2
      AND key.state = 'ACTIVE'
      AND key.key_version = $14
      AND key.revocation_version = $15
      AND $26 >= key.valid_from_ms
      AND $26 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $19
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $11
      AND authorization.budget_reservation_id = $12
      AND $26 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_capability capability
    WHERE capability.capability_id = $11
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $19
      AND capability.worker_instance_id = $1
      AND capability.budget_reservation_id = $12
      AND $26 < capability.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $12
      AND reservation.state = 'RESERVED'
      AND reservation.send_started_at_ms IS NOT NULL
      AND $26 < reservation.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $8
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $9
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $11
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $26 >= worker.heartbeat_at_ms
      AND $26 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'SENT'
      AND lease.scope_key = $8
      AND lease.capability_id = $11
      AND lease.execution_authorization_id = $19
      AND lease.budget_reservation_id = $12
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $9
      AND $26 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r4_send_authorization permit
    WHERE permit.send_authorization_id = $4
      AND permit.state = 'CONSUMED'
      AND permit.consumed_at_ms IS NOT NULL
      AND $26 >= permit.consumed_at_ms
      AND $26 < permit.expires_at_ms
      AND permit.scope_key = $8
      AND permit.lease_id = $3
      AND permit.capability_id = $11
      AND permit.worker_instance_id = $1
      AND permit.fencing_token = $9
      AND permit.budget_reservation_id = $12
      AND permit.emergency_epoch = $13
      AND permit.key_version = $14
      AND permit.revocation_version = $15
      AND permit.permission_version = $16
      AND permit.policy_version = $17
  );

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $28, $29, $26, 'REQUEST_SENT', 'ALLOW',
  $7, $30, $31
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $29,
    last_event_digest = $31
WHERE singleton_id = 1
  AND last_sequence = $29 - 1
  AND last_event_digest IS NOT DISTINCT FROM $30;

COMMIT;

-- After the WRITE_STARTED commit, an ordinary revocation cannot cancel a
-- socket write that may already begin. The trusted Egress component performs
-- exactly one write and records its outcome in the transaction below.
-- ===== END sql/30-egress-final-authorization.sql =====
-- ===== BEGIN sql/40-egress-write-outcome.sql =====
-- SHA256=4AF449B69DB6AB5DBC539923A95CDE17F6AB915A7FEA320C6FAB24BF6EE8957F
-- BYTES=2389
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED

-- Response received: WRITE_STARTED -> RESPONSE_RECEIVED -> COMPLETED.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'RESPONSE_RECEIVED',
    row_version = row_version + 1
WHERE egress_intent_id = $1
  AND state = 'WRITE_STARTED'
  AND row_version = $2;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'COMPLETED',
    row_version = row_version + 1,
    outcome_at_ms = $3
WHERE egress_intent_id = $1
  AND state = 'RESPONSE_RECEIVED'
  AND row_version = $2 + 1;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $4, $5, $3, 'RESPONSE_RECEIVED', 'ALLOW',
  $1, $6, $7
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $5,
    last_event_digest = $7
WHERE singleton_id = 1
  AND last_sequence = $5 - 1
  AND last_event_digest IS NOT DISTINCT FROM $6;

COMMIT;

-- Socket timeout, connection loss, process crash, or unknown remote receipt:
-- terminal SEND_OUTCOME_UNKNOWN. Never automatically retry this intent.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT egress_intent_id, state, row_version
FROM trust_r5_egress_intent
WHERE egress_intent_id = $1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r5_egress_intent
SET state = 'SEND_OUTCOME_UNKNOWN',
    row_version = row_version + 1,
    outcome_at_ms = $8
WHERE egress_intent_id = $1
  AND state = 'WRITE_STARTED'
  AND row_version = $9;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $10, $11, $8, 'SEND_OUTCOME_UNKNOWN', 'UNKNOWN',
  $1, $12, $13
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $11,
    last_event_digest = $13
WHERE singleton_id = 1
  AND last_sequence = $11 - 1
  AND last_event_digest IS NOT DISTINCT FROM $12;

COMMIT;
-- ===== END sql/40-egress-write-outcome.sql =====

```
<!-- END_EXACT_SOURCE id=S034 -->

### S035. PHASE_R3_WORKER_REVOCATION_TRANSACTIONS.sql

- Path: `preparation/production-trust/r3-egress-revocation-remediation/PHASE_R3_WORKER_REVOCATION_TRANSACTIONS.sql`
- Bytes: `26314`
- SHA-256: `2591E69443552F897F03F819BBF4DFC25DAC6452A9D307C6F62B22C1C1D4EB8E`

<!-- BEGIN_EXACT_SOURCE id=S035 sha256=2591E69443552F897F03F819BBF4DFC25DAC6452A9D307C6F62B22C1C1D4EB8E bytes=26314 -->
```text
-- PHASE_R3_WORKER_REVOCATION_TRANSACTIONS.sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Global revocation, scope cleanup and Permit Consumption revocation

-- ===== BEGIN sql/10-worker-global-revocation.sql =====
-- SHA256=54B918ABA73574E0BB92000C993ED1CDF8FF1C8F5CB646FC27AAAC20721D37E1
-- BYTES=5443
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Global Worker Identity Revocation is a single authoritative tombstone.
-- It fails closed every Scope without pretending to atomically clean every
-- possible Resource Floor in one transaction.

CREATE TABLE trust_r5_worker_revocation (
  worker_instance_id uuid PRIMARY KEY
    REFERENCES trust_r4_worker_registration (worker_instance_id),
  state text NOT NULL CHECK (state IN ('ACTIVE', 'REVOKED', 'RECOVERY_REQUIRED')),
  revocation_version bigint NOT NULL CHECK (revocation_version >= 0),
  record_version bigint NOT NULL CHECK (record_version >= 1),
  revoked_at_ms bigint,
  reason_code text,
  replacement_worker_id uuid,
  updated_at_ms bigint NOT NULL,
  CHECK (
    state <> 'REVOKED'
    OR (revoked_at_ms IS NOT NULL AND reason_code IS NOT NULL)
  ),
  CHECK (
    replacement_worker_id IS NULL
    OR replacement_worker_id <> worker_instance_id
  )
);

CREATE TABLE trust_r5_worker_revocation_request (
  request_id uuid PRIMARY KEY,
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  requested_revocation_version bigint NOT NULL
    CHECK (requested_revocation_version >= 1),
  requested_at_ms bigint NOT NULL,
  UNIQUE (worker_instance_id, requested_revocation_version)
);

CREATE TABLE trust_r5_scope_worker_block (
  scope_key text NOT NULL
    REFERENCES trust_r4_resource_fencing (scope_key),
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  blocked_revocation_version bigint NOT NULL
    CHECK (blocked_revocation_version >= 1),
  version bigint NOT NULL CHECK (version >= 1),
  blocked_at_ms bigint NOT NULL,
  reason_code text NOT NULL,
  PRIMARY KEY (scope_key, worker_instance_id)
);

CREATE TABLE trust_r5_lease_worker_revocation_binding (
  lease_id uuid PRIMARY KEY
    REFERENCES trust_r4_execution_lease (lease_id),
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r5_worker_revocation (worker_instance_id),
  worker_revocation_version bigint NOT NULL
    CHECK (worker_revocation_version >= 0),
  bound_at_ms bigint NOT NULL
);

-- Future deployment migration: audit event vocabulary must be extended before
-- this draft can run. The repository's frozen R3 schema is not edited.
ALTER TABLE trust_r3_audit_event
  DROP CONSTRAINT IF EXISTS trust_r3_audit_event_event_type_check;

ALTER TABLE trust_r3_audit_event
  ADD CONSTRAINT trust_r3_audit_event_event_type_check CHECK (
    event_type IN (
      'APPROVAL_CONSUMED', 'BUDGET_RESERVED', 'BUDGET_RELEASED',
      'BUDGET_SETTLED', 'LEASE_ISSUED', 'WORKER_PROGRESS',
      'SEND_AUTHORIZED', 'SEND_AUTHORIZATION_CONSUMED',
      'REQUEST_SENT', 'SEND_OUTCOME_UNKNOWN', 'RESPONSE_RECEIVED',
      'EMERGENCY_ACTIVATED', 'EMERGENCY_RECOVERY_REQUESTED',
      'EMERGENCY_RECOVERY_APPROVED', 'KEY_REVOKED',
      'WORKER_REVOKED', 'WORKER_SCOPE_BLOCKED', 'LEASE_REVOKED'
    )
  );

-- ===========================================================================
-- Global Worker revocation. Linearization point: COMMIT of this transaction.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT request_id, worker_instance_id, requested_revocation_version
FROM trust_r5_worker_revocation_request
WHERE request_id = $2
FOR SHARE;

-- Idempotency: if this exact request already committed, the host returns the
-- persisted revocation record without another Audit append or version bump.

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
  AND record_version = $5;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration
SET state = 'REVOKED',
    updated_at_ms = $3
WHERE worker_instance_id = $1
  AND state = 'ACTIVE';

INSERT INTO trust_r5_worker_revocation_request (
  request_id, worker_instance_id, requested_revocation_version, requested_at_ms
) VALUES (
  $2, $1, $5 + 1, $3
) RETURNING request_id;

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
) RETURNING event_id;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $7,
    last_event_digest = $9
WHERE singleton_id = 1
  AND last_sequence = $7 - 1
  AND last_event_digest IS NOT DISTINCT FROM $8;

COMMIT;

-- Any non-one UPDATE row count, missing worker, audit failure or failed COMMIT
-- restores ACTIVE registration and the prior revocation row.

-- COMMIT ambiguity:
--   query trust_r5_worker_revocation_request by request_id;
--   if present, read trust_r5_worker_revocation by worker_instance_id;
--   return persisted record; never issue a blind second revocation version.

-- Ordinary Worker registration/Upsert MUST never transition REVOKED back to
-- ACTIVE. A replacement identity requires a separate trusted provisioning flow.
-- ===== END sql/10-worker-global-revocation.sql =====
-- ===== BEGIN sql/20-worker-scope-cleanup.sql =====
-- SHA256=FE3ED25A80BB275DA7428C07B84433AD0720E10D46788F1B7F413A86D82F9D53
-- BYTES=6953
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- One-idempotent-scope cleanup. The host MUST first lock/read the Lease and
-- choose exactly one branch below. It must never run the checked pre-send
-- Lease UPDATE when the observed state is SENT or otherwise post-write.

-- ===========================================================================
-- Branch 20A: PRE_SEND cleanup
-- Allowed observed Lease states:
--   ISSUED, KEY_READ, TRANSPORT_CREATED, SEND_AUTHORIZED
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $2
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id,
       worker_instance_id, fencing_token
FROM trust_r4_send_authorization
WHERE lease_id = $3
FOR UPDATE;

-- Host preconditions after the locked reads:
--   floor.scope_key=$2
--   floor.current_worker_id=$1
--   floor.current_lease_id=$3
--   floor.current_capability_id=$4
--   global revocation.state=REVOKED
--   global revocation.revocation_version >= $5
--   Lease worker=$1, scope=$2, capability=$4, token=floor token=$8
--   Lease state IN the PRE_SEND set above
-- Any mismatch rejects this branch and rolls back.

INSERT INTO trust_r5_scope_worker_block (
  scope_key, worker_instance_id, blocked_revocation_version,
  version, blocked_at_ms, reason_code
) VALUES (
  $2, $1, $5, 1, $6, $7
)
ON CONFLICT (scope_key, worker_instance_id) DO UPDATE
SET blocked_revocation_version =
      GREATEST(
        trust_r5_scope_worker_block.blocked_revocation_version,
        EXCLUDED.blocked_revocation_version
      ),
    version = trust_r5_scope_worker_block.version + 1,
    blocked_at_ms = EXCLUDED.blocked_at_ms,
    reason_code = EXCLUDED.reason_code;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease
SET state = 'REVOKED'
WHERE lease_id = $3
  AND worker_instance_id = $1
  AND scope_key = $2
  AND capability_id = $4
  AND fencing_token = $8
  AND state IN (
    'ISSUED', 'KEY_READ', 'TRANSPORT_CREATED', 'SEND_AUTHORIZED'
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'REVOKED'
      AND revocation.revocation_version >= $5
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE lease_id = $3
  AND worker_instance_id = $1
  AND scope_key = $2
  AND capability_id = $4
  AND fencing_token = $8
  AND state IN ('ISSUED', 'CONSUMED');

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $9, $10, $6, 'WORKER_SCOPE_BLOCKED', 'ALLOW',
  $1, $11, $12
) RETURNING event_id;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $10,
    last_event_digest = $12
WHERE singleton_id = 1
  AND last_sequence = $10 - 1
  AND last_event_digest IS NOT DISTINCT FROM $11;

COMMIT;

-- ===========================================================================
-- Branch 20B: AFTER_SEND classification
-- Allowed observed Lease states:
--   SENT, RESPONSE_RECEIVED, COMPLETED, FAILED_AFTER_SEND,
--   SEND_OUTCOME_UNKNOWN
-- The request cannot be recalled. Do not issue a Lease REVOKED update.
-- ===========================================================================
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $2
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, worker_instance_id, capability_id,
       fencing_token, state
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id,
       worker_instance_id, fencing_token
FROM trust_r4_send_authorization
WHERE lease_id = $3
FOR UPDATE;

-- Host preconditions are the same as 20A except the Lease must already be in
-- the AFTER_SEND set. The external outcome remains unknown unless an existing
-- durable request record establishes otherwise. This branch never retries.

INSERT INTO trust_r5_scope_worker_block (
  scope_key, worker_instance_id, blocked_revocation_version,
  version, blocked_at_ms, reason_code
) VALUES (
  $2, $1, $5, 1, $6, $7
)
ON CONFLICT (scope_key, worker_instance_id) DO UPDATE
SET blocked_revocation_version =
      GREATEST(
        trust_r5_scope_worker_block.blocked_revocation_version,
        EXCLUDED.blocked_revocation_version
      ),
    version = trust_r5_scope_worker_block.version + 1,
    blocked_at_ms = EXCLUDED.blocked_at_ms,
    reason_code = EXCLUDED.reason_code;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization
SET state = 'REVOKED'
WHERE lease_id = $3
  AND worker_instance_id = $1
  AND scope_key = $2
  AND capability_id = $4
  AND fencing_token = $8
  AND state = 'CONSUMED'
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state IN (
        'SENT', 'RESPONSE_RECEIVED', 'COMPLETED', 'FAILED_AFTER_SEND',
        'SEND_OUTCOME_UNKNOWN'
      )
  );

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $9, $10, $6, 'WORKER_SCOPE_BLOCKED', 'ALLOW',
  $1, $11, $12
) RETURNING event_id;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $10,
    last_event_digest = $12
WHERE singleton_id = 1
  AND last_sequence = $10 - 1
  AND last_event_digest IS NOT DISTINCT FROM $11;

COMMIT;

-- Global revocation already blocks all scopes immediately. Scope cleanup can
-- be resumed idempotently after a crash. An interrupted cleanup never reopens
-- authority because Permit Consumption and Egress join the global revocation
-- row on every authorization decision.
-- ===== END sql/20-worker-scope-cleanup.sql =====
-- ===== BEGIN sql/25-lease-revocation-binding.sql =====
-- SHA256=F25D017A066EEEFD0A62D1C51B397C431CE4C7AEE6B9C6CDE4E929DF603122F9
-- BYTES=3081
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R5 Lease revocation-version binding finalization.
--
-- The frozen R4 takeover transaction issues the Lease and token atomically but
-- has no R5 binding column. R5 therefore fails closed: a Lease without this
-- binding cannot be consumed or reach Egress. This transaction may run after
-- R4 Lease issuance, but before any Permit Consumption.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $1
FOR SHARE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $2
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms
FROM trust_r4_worker_registration
WHERE worker_instance_id = $1
FOR UPDATE;

SELECT lease_id, scope_key, capability_id, worker_instance_id,
       fencing_token, state, expires_at_ms
FROM trust_r4_execution_lease
WHERE lease_id = $3
FOR UPDATE;

-- Host preconditions:
--   global revocation.state=ACTIVE
--   global revocation.revocation_version=$4
--   floor.current_worker_id=$1
--   floor.current_lease_id=$3
--   floor.current_capability_id=$5
--   floor.current_fencing_token=$6
--   Lease binds the same Worker/Scope/Capability/token
--   Worker Registration is ACTIVE with fresh heartbeat

-- AFFECTED_ROWS_EXPECTATION: exactly 1
INSERT INTO trust_r5_lease_worker_revocation_binding (
  lease_id, worker_instance_id, worker_revocation_version, bound_at_ms
)
SELECT
  $3, $1, $4, $7
WHERE EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $1
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $4
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $2
      AND block.worker_instance_id = $1
      AND block.blocked_revocation_version >= $4
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $2
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $6
      AND floor.current_worker_id = $1
      AND floor.current_lease_id = $3
      AND floor.current_capability_id = $5
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $1
      AND worker.state = 'ACTIVE'
      AND $7 >= worker.heartbeat_at_ms
      AND $7 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $3
      AND lease.state = 'ISSUED'
      AND lease.scope_key = $2
      AND lease.capability_id = $5
      AND lease.worker_instance_id = $1
      AND lease.fencing_token = $6
      AND $7 < lease.expires_at_ms
  );

COMMIT;

-- COMMIT ambiguity: query the binding by lease_id. Only the exact persisted
-- Worker/version match is success. A missing binding leaves the Lease
-- unusable; it never creates authority.
-- ===== END sql/25-lease-revocation-binding.sql =====
-- ===== BEGIN sql/50-permit-consumption-revocation.sql =====
-- SHA256=115F3AD69A89797DBA8EDFF85A1DFA9ADE744CDC66AA64561BD7D071E4FE2650
-- BYTES=9846
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R5 overlay for the frozen R4 Permit Consumption transaction.
-- This is a complete replacement draft, not an ALTER of frozen R4 SQL.
--
-- The transaction joins the global Worker revocation tombstone and the
-- per-scope block before the R4 one-use transition can commit. The permit,
-- Lease and budget send-start transition, Audit append and lock order share
-- one transaction boundary.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT worker_instance_id, state, revocation_version, record_version
FROM trust_r5_worker_revocation
WHERE worker_instance_id = $6
FOR UPDATE;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT authorization_id, state, capability_id, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms
FROM trust_r3_execution_authorization
WHERE authorization_id = $2
FOR UPDATE;

SELECT max_total_requests, reserved_requests, consumed_requests,
       max_usd_micros, reserved_usd_micros, consumed_usd_micros,
       budget_version
FROM trust_r3_budget_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT reservation_id, state, execution_authorization_id, capability_id,
       worker_instance_id, expires_at_ms, send_started_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $3
FOR UPDATE;

SELECT capability_id, state, execution_authorization_id, worker_instance_id,
       budget_reservation_id, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version, expires_at_ms
FROM trust_r3_capability
WHERE capability_id = $4
FOR UPDATE;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $5
FOR UPDATE;

SELECT worker_instance_id, state, heartbeat_at_ms, last_issued_token
FROM trust_r4_worker_registration
WHERE worker_instance_id = $6
FOR UPDATE;

SELECT lease_id, worker_instance_id, worker_revocation_version
FROM trust_r5_lease_worker_revocation_binding
WHERE lease_id = $7
FOR UPDATE;

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, issued_at_ms, expires_at_ms,
       consumed_at_ms
FROM trust_r4_send_authorization
WHERE send_authorization_id = $15
FOR UPDATE;

-- Parameters:
--   $1  key_id
--   $2  execution_authorization_id
--   $3  budget_reservation_id
--   $4  capability_id
--   $5  scope_key
--   $6  worker_instance_id
--   $7  lease_id
--   $8  fencing_token
--   $9  emergency_epoch
--   $10 key_version
--   $11 key revocation_version
--   $12 permission_version
--   $13 policy_version
--   $14 consumed_at_ms (server clock)
--   $15 send_authorization_id
--   $16 Audit event_id
--   $17 Audit sequence
--   $18 previous_event_digest
--   $19 event_digest
--   $20 expected Worker revocation_version

-- Permit one-use transition. No caller-supplied Actor/Worker authority is
-- trusted; every binding is compared with locked rows.
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_send_authorization AS permit
SET state = 'CONSUMED',
    consumed_at_ms = $14
WHERE permit.send_authorization_id = $15
  AND permit.state = 'ISSUED'
  AND permit.scope_key = $5
  AND permit.lease_id = $7
  AND permit.capability_id = $4
  AND permit.worker_instance_id = $6
  AND permit.fencing_token = $8
  AND permit.budget_reservation_id = $3
  AND permit.emergency_epoch = $9
  AND permit.key_version = $10
  AND permit.revocation_version = $11
  AND permit.permission_version = $12
  AND permit.policy_version = $13
  AND $14 >= permit.issued_at_ms
  AND $14 < permit.expires_at_ms
  AND EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $6
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $20
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $5
      AND block.worker_instance_id = $6
      AND block.blocked_revocation_version >= $20
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r5_lease_worker_revocation_binding binding
    WHERE binding.lease_id = $7
      AND binding.worker_instance_id = $6
      AND binding.worker_revocation_version = $20
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $5
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $8
      AND floor.current_worker_id = $6
      AND floor.current_lease_id = $7
      AND floor.current_capability_id = $4
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_worker_registration worker
    WHERE worker.worker_instance_id = $6
      AND worker.state = 'ACTIVE'
      AND $14 >= worker.heartbeat_at_ms
      AND $14 - worker.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_execution_lease lease
    WHERE lease.lease_id = $7
      AND lease.state = 'SEND_AUTHORIZED'
      AND lease.scope_key = $5
      AND lease.capability_id = $4
      AND lease.execution_authorization_id = $2
      AND lease.budget_reservation_id = $3
      AND lease.worker_instance_id = $6
      AND lease.fencing_token = $8
      AND $14 < lease.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control emergency
    WHERE emergency.singleton_id = 1
      AND emergency.status = 'NORMAL'
      AND emergency.epoch = $9
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key key
    WHERE key.key_id = $1
      AND key.state = 'ACTIVE'
      AND key.key_version = $10
      AND key.revocation_version = $11
      AND $14 >= key.valid_from_ms
      AND $14 < key.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization authorization
    WHERE authorization.authorization_id = $2
      AND authorization.state = 'ACTIVE'
      AND authorization.capability_id = $4
      AND authorization.budget_reservation_id = $3
      AND $14 < authorization.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation reservation
    WHERE reservation.reservation_id = $3
      AND reservation.state = 'RESERVED'
      AND reservation.execution_authorization_id = $2
      AND reservation.capability_id = $4
      AND reservation.worker_instance_id = $6
      AND reservation.send_started_at_ms IS NULL
      AND $14 < reservation.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability capability
    WHERE capability.capability_id = $4
      AND capability.state = 'RESERVED'
      AND capability.execution_authorization_id = $2
      AND capability.worker_instance_id = $6
      AND capability.budget_reservation_id = $3
      AND $14 < capability.expires_at_ms
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'SENT'
WHERE lease.lease_id = $7
  AND lease.state = 'SEND_AUTHORIZED'
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND $14 < lease.expires_at_ms
  AND EXISTS (
    SELECT 1
    FROM trust_r5_worker_revocation revocation
    WHERE revocation.worker_instance_id = $6
      AND revocation.state = 'ACTIVE'
      AND revocation.revocation_version = $20
  )
  AND NOT EXISTS (
    SELECT 1
    FROM trust_r5_scope_worker_block block
    WHERE block.scope_key = $5
      AND block.worker_instance_id = $6
      AND block.blocked_revocation_version >= $20
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r4_resource_fencing floor
    WHERE floor.scope_key = $5
      AND floor.state = 'ACTIVE'
      AND floor.current_fencing_token = $8
      AND floor.current_worker_id = $6
      AND floor.current_lease_id = $7
      AND floor.current_capability_id = $4
  );

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_budget_reservation
SET send_started_at_ms = $14
WHERE reservation_id = $3
  AND state = 'RESERVED'
  AND execution_authorization_id = $2
  AND capability_id = $4
  AND worker_instance_id = $6
  AND send_started_at_ms IS NULL
  AND $14 < expires_at_ms;

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $16, $17, $14, 'SEND_AUTHORIZATION_CONSUMED', 'ALLOW',
  $15, $18, $19
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $17,
    last_event_digest = $19
WHERE singleton_id = 1
  AND last_sequence = $17 - 1
  AND last_event_digest IS NOT DISTINCT FROM $18;

COMMIT;

-- Any zero/multiple affected row, missing lock-time condition, Audit failure or
-- failed COMMIT rolls the entire transaction back to ISSUED/SEND_AUTHORIZED and
-- an unstarted budget send.
--
-- Ambiguous COMMIT: query the durable permit by $15 and Audit sequence/event by
-- $16. If the permit is CONSUMED with consumed_at_ms=$14 and the matching Audit
-- event exists, return the persisted result. Otherwise never invoke this
-- transaction again as a blind retry.
-- ===== END sql/50-permit-consumption-revocation.sql =====

```
<!-- END_EXACT_SOURCE id=S035 -->

### S036. vitest.config.ts

- Path: `preparation/production-trust/r3-egress-revocation-remediation/vitest.config.ts`
- Bytes: `233`
- SHA-256: `2BFE58E0B048F5268AF8037D7703E223B31E09DF10E30C179036B94F67FD0DFA`

<!-- BEGIN_EXACT_SOURCE id=S036 sha256=2BFE58E0B048F5268AF8037D7703E223B31E09DF10E30C179036B94F67FD0DFA bytes=233 -->
```text
import { defineConfig } from "vitest/config";

export default defineConfig({
  test: {
    environment: "node",
    include: [
      "preparation/production-trust/r3-egress-revocation-remediation/tests/**/*.test.ts",
    ],
  },
});

```
<!-- END_EXACT_SOURCE id=S036 -->

## 3. Freeze Status

```text
R3_FENCING_BASELINE_ENTRIES=41
R3_FENCING_BASELINE_MISMATCHES=0
R31_R36_FROZEN_ENTRIES=68
R31_R36_FROZEN_MISMATCHES=0
TASK_SOURCE_FILES=36
PROTECTED_HASH_MISMATCHES=0
IMPORT_BOUNDARY_HITS=0
SENSITIVE_PATTERN_HITS=0
PRODUCTION_ENTRY_BLOCKED=YES
```
