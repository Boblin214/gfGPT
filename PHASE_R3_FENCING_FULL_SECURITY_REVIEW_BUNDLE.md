# PHASE_R3_FENCING_FULL_SECURITY_REVIEW_BUNDLE

## Bundle Control

```text
BUNDLE_STATUS=R3_FENCING_REMEDIATION_PASS
GENERATED_AT=2026-11-26T12:54:39.182Z
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
SOURCE_FILES=53
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
SQL_EXECUTED=NO
DATABASE_CONNECTED=NO
```

## Table of Contents

- A. R3 Fencing Reports
- B. Complete SQL Drafts
- C. Reference Models
- D. Tests
- E. Required Consolidated Artifacts
- F. Original R2-R3 Comparative Material
- G. Freeze Evidence
- H. Test Results
- I. Source Catalog
- J. Included Source Bodies

## H. Test Results

| Command | Result | Class |
|---|---|---|
| `node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-fencing-remediation/vitest.config.ts` | 7 files / 49 tests PASS | OFFLINE_REFERENCE_MODEL + SQL_STATIC |
| R2-R3 regression | 8 files / 74 tests PASS | offline model |
| R2 regression | 10 files / 80 tests PASS | offline model |
| R1 regression | 16 files / 91 tests PASS | offline model |
| R31-R36 relevant | 24 files / 179 tests PASS | synthetic/mock |
| PowerShell frozen tests | 69/69 PASS | synthetic |
| PowerShell 5.1 Parser | PASS / 6 scripts | static |
| TypeScript strict | PASS | static |
| ESLint | PASS | static |
| Next.js production build | PASS | offline build |

## H.2 Defects Closed

- SQL moved from Worker `fence_floor` to persistent resource floor.
- Every Lease/progress/permit/egress boundary checks current scope floor.
- Takeover allocates token, updates floor, inserts Lease and audits in one transaction.
- Old ACTIVE Worker registration no longer supplies authorization.
- Revoked Worker cannot be silently reactivated.
- Permit replay, Emergency, Key revocation and authority loss fail closed.
- Final Egress design performs a fresh current-floor check and cannot guarantee recall after socket write.

## H.3 Residual Risks

- `REQUIRES_POSTGRESQL_INTEGRATION`
- `REQUIRES_REAL_MULTI_INSTANCE_TEST`
- `REQUIRES_REAL_EGRESS_TEST`
- `REQUIRES_EXTERNAL_PROVIDER_TEST`
- final floor read and socket write remain non-atomic
- production egress must be the only Provider network route

## I. Source Catalog

| ID | Category | Path | Bytes | SHA-256 |
|---|---|---|---:|---|
| S001 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE.md` | 4585 | 18F7A37FC271C2AEAFFAF1F71419BAF9474A00E8987EF26EE63C956D8E1BBA12 |
| S002 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CONTRACT.md` | 3495 | F43185B267AB79ED23C9D29DD57EB69FF31517F1DFE043E2614F4F6946834650 |
| S003 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CROSS_REVIEW.md` | 1629 | 8E455E4299C7687D634EC3AEE4ACC2C80D9252AAB5E9D6EB9C1C0DDB2AFAA016 |
| S004 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_DIFF.md` | 1635 | 45DC3E67B086C92AF9ADF8C44AE8ECD17C7E9E7595401A1C6213B589C16A8E94 |
| S005 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT.md` | 5730 | 8A2D510E772B1CE0B2EC724FBB902F11D9C19230EBBA46480DA10C49898FBED4 |
| S006 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_MODEL.md` | 3639 | D5D1B28AAC2727F1841AB0A0940EFA623A48730319A6EDFFE82833286F78F18F |
| S007 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER.md` | 2591 | 3A1F3BFD5BB6B4BFE28F7D9FE71D719B2BF8799CE8E1193CE37AA4EFC88A455D |
| S008 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW.md` | 3680 | E6CED6736E59AA4AE2CBDE965380CD4BF76765A67393BF32344FDF6E70D73986 |
| S009 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX.md` | 3647 | 633F8F15D83167C9D9D5D5B233177D7FFBFC47A3FAFDD3221866D7DB4420392A |
| S010 | A_R3F_REPORT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL.md` | 4302 | BAFCAC5051A6C73197255849F25409F0AB2B40806F727FA71EC0709A82F1D097 |
| S011 | B_R3F_SQL | `preparation\production-trust\r3-fencing-remediation\sql\00-schema.sql` | 4974 | 76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4 |
| S012 | B_R3F_SQL | `preparation\production-trust\r3-fencing-remediation\sql\10-worker-takeover.sql` | 6889 | 000CC783457862E4CEFD5313E19EB3C055F02379FED642E982517361F42FB909 |
| S013 | B_R3F_SQL | `preparation\production-trust\r3-fencing-remediation\sql\20-lease-issuance.sql` | 2645 | 101D3AACA2609E3A79FE1EC7AD7B0DBE376B9E2528B8CCB751056DEECAC79FC8 |
| S014 | B_R3F_SQL | `preparation\production-trust\r3-fencing-remediation\sql\30-worker-progress.sql` | 9891 | 5C9CC11B8763F7809D75F87C695E44B26A223132E5462071745A2A72F9534724 |
| S015 | B_R3F_SQL | `preparation\production-trust\r3-fencing-remediation\sql\40-send-authorization-issuance.sql` | 5964 | F1C8E92DD2CB3E649D491AF7B5748FF8157F32ED3AC1881AB3EB49B0E8FC7D94 |
| S016 | B_R3F_SQL | `preparation\production-trust\r3-fencing-remediation\sql\50-send-authorization-consume.sql` | 8641 | 0ACA5410F758DD2B31A6C3681D7014A2A5BF1FEB509A2CA482423AF793E7A684 |
| S017 | C_R3F_MODEL_SUPPORT | `preparation\production-trust\r3-fencing-remediation\contracts.ts` | 5758 | B50E5388C90FC3E5C5DFE746A0D13FAB8E63CC4E35B4CEE44D672D31F733C0EE |
| S018 | C_R3F_MODEL_SUPPORT | `preparation\production-trust\r3-fencing-remediation\lock-order.ts` | 2228 | B203CC3BDA846BDD3BFA423D1C30659E5DE0E285792ACD1724122BD933207C64 |
| S019 | C_R3F_MODEL_SUPPORT | `preparation\production-trust\r3-fencing-remediation\scope.ts` | 1743 | 04B4E4FBBB246FC05EFC6B6894806C32B38F559674D87B0B7B0C6E5EADC31BEF |
| S020 | C_R3F_MODEL_SUPPORT | `preparation\production-trust\r3-fencing-remediation\vitest.config.ts` | 223 | 3498ED7EA917D283C253A19BE5C04FEA632664E3E1427B46FFFE1109A0F12FF0 |
| S021 | C_R3F_MODEL | `preparation\production-trust\r3-fencing-remediation\models\execution-boundary.ts` | 10815 | 0821E49639C34B4233FE99A691E10EEADB262AF966BE11E88E2C8F189623B7AE |
| S022 | C_R3F_MODEL | `preparation\production-trust\r3-fencing-remediation\models\fencing-floor.ts` | 13954 | 83F085134850F4765ABAD9D5D2451B23684E60ABB3202A762B571D5BAA7A76DB |
| S023 | C_R3F_MODEL | `preparation\production-trust\r3-fencing-remediation\models\race-scenarios.ts` | 6481 | 079FCF395897ED8D54B2C665A5B51AC0FBE4C6341EE9B7FE6E059B9940CF8839 |
| S024 | C_R3F_MODEL | `preparation\production-trust\r3-fencing-remediation\models\sql-analyzer.ts` | 7155 | 98EB13EE3AA9F01FB72AFB9860A2AE2C15E143E0A627113EF882632258729FB5 |
| S025 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\execution-boundary.test.ts` | 8680 | E8A2CE8FB05B7E7658348FA553FD0606F86D8ADF7D278B7D7158A9DED84D8A48 |
| S026 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\fencing-floor.test.ts` | 7331 | 5690EDDF00728F51F52EB55B9F73176909001B8A031E9DAFE28793D24E9A3A88 |
| S027 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\races.test.ts` | 9955 | 94C7917C295334AB212344F7EF1A4AE64CBCBDEE36F40BC44701C8907D1F0DB1 |
| S028 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\scope-lock-order.test.ts` | 3687 | D99EF9FDF09E102F4B4E7F37D73DB9DDD4EA20E384F1E4DBB370AE5301167C2B |
| S029 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\scope-lock.test.ts` | 4417 | 45E38B57F90919DA480E8348D8CD14B8036E2A96CD84392BDF79EE5E3AD5EB98 |
| S030 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\sql-negative.test.ts` | 4328 | A9185EAC405B111E9323239200C0DA3C4ECAFB297220F71A4E4DBA81D27162A2 |
| S031 | D_R3F_TEST | `preparation\production-trust\r3-fencing-remediation\tests\sql-positive.test.ts` | 2404 | 5F82F0DD4A89BCC65672F7CDA7EFA0D0FF1BCCCE95FABAE22DBBEBE24BAB279C |
| S032 | E_R3F_ARTIFACT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql` | 4974 | 76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4 |
| S033 | E_R3F_ARTIFACT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql` | 35018 | 512E790234B41699AF72DCDE172F4CF247911DE02E9C04915D985ED5C739D8B1 |
| S034 | E_R3F_ARTIFACT | `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SHA256SUMS.txt` | 5233 | 581C7B8D543ACB813039F019CE9CEECB3E65E0EFA740E2D5978C771A60076D80 |
| S035 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/contracts.ts` | 12209 | 905F300FFDBD9C31545F775F126ADB2AC6186EC997D4E4A3A0642F53735D8B5D |
| S036 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/lock-order.ts` | 2260 | BFBE3374B1BCB5521D52FC9191CD42CBAD77AC43A67FD9AF84202001CD5344EA |
| S037 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/models/fencing-registry.ts` | 5510 | 58CF8B73866D8107FD01835617E3D554016060DD92FF8E20B12FF21685178D55 |
| S038 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/models/execution-lease.ts` | 28892 | BA86F24E1FDC9E2862A83E6ECEAA02B54F237AFEE34542EB6BA23FCBC5802AB1 |
| S039 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/sql/00-schema.sql` | 12896 | 7EFB81B768F0B037D3DFA7218F4C1D2F3EB476F3E847A19FFA8CDFD0C22BBD69 |
| S040 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/sql/10-lease-issuance.sql` | 5124 | 2DB415FE7D2CD867AA48648941CA2869CB48AD1F04386250E8786A3A11DF0116 |
| S041 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/sql/20-worker-progress.sql` | 5958 | C56E0437EE45860A26D1FA25981187C441C922FB830C8288BDBB952594C3E1CD |
| S042 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/sql/30-send-authorization-issuance.sql` | 3518 | 8178ABC188D29E8D766AF5DF4A7E537F015A444877CF88483C3777EDD76102BD |
| S043 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/sql/40-send-authorization-consume.sql` | 4389 | 93EB68288F6B2E319C37BFEE8E6CE754D7DB8690D167B43B471C128E7235240B |
| S044 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/sql/70-fencing-registry.sql` | 1060 | C089AADA9F5D583EA78CFC218F935B8E268CA66F81C74AE60F207C58B99F00EB |
| S045 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/tests/execution-lease.test.ts` | 21893 | 80FE63A0E5FB5CC764C418696AD4161E402558F495C2D28F4DDCFF4C9375F6FB |
| S046 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/tests/fencing-audit-emergency.test.ts` | 8185 | 02ED83707FDA735091910825FA0AABA5BA6B69DD6EDFE7472CFDBE181C1059BD |
| S047 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FENCING_MODEL.md` | 2589 | 48D0E33681FEEBCD11BD674B4BF744461DED4DB8DB43F15D638FEC968827121A |
| S048 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_THREAT_MODEL.md` | 3925 | 6945F66EC216A932698DB0707745A73DE8D29034C0A781ECB7A5910D32B213A5 |
| S049 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_RISK_REGISTER.md` | 1907 | 04357AA0F8D0F7262954900E9350A03E0C916CD3FFD66D9F88A16C9BB69EEA5D |
| S050 | F_R2_R3_COMPARATIVE | `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FINAL_REPORT.md` | 7736 | 9917648CA16E3A88DCC7E2ACA0D5877DC370A530D2484BA24849D59265739DA9 |
| S051 | F_R2_R3_COMPARATIVE | `preparation/production-trust/PHASE_R2_R3_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md` | 4240 | 7F9D6B4908850BA2597BB7939F3A4B8D45A5B8BB8EFA9CFF5ACBA0CFC4AAAC8C |
| S052 | G_FREEZE_EVIDENCE | `PHASE_R31_R36_SHA256SUMS.txt` | 9031 | D0191FBB856E284AE40614A16F9B92B69B45D1D59DB4E2FAD4D52DDB1DC4778C |
| S053 | G_FREEZE_EVIDENCE | `src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts` | 933 | 1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309 |

## J. Included Source Bodies

### S001. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE.md`
- Bytes: `4585`
- SHA-256: `18F7A37FC271C2AEAFFAF1F71419BAF9474A00E8987EF26EE63C956D8E1BBA12`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S001 sha256=18F7A37FC271C2AEAFFAF1F71419BAF9474A00E8987EF26EE63C956D8E1BBA12 bytes=4585 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_BASELINE

## 1. Status

```text
WORKSPACE=C:\Users\Administrator\Desktop\thzz1-search-offline
BASELINE_CAPTURED_AT=2026-11-26T20:28:03.4300231+08:00
R2_R3_REMEDIATION_PASS
INDEPENDENT_REVIEW=NEEDS_REVISION
FENCING_SQL_MODEL_CONSISTENCY=NEEDS_REVISION
BASELINE_HASH_TARGETS=53
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

## 2. Protected Baseline

All existing R1, R2, R2–R3 and R31–R36 files are immutable for this task.
Revision output is confined to:

```text
preparation/production-trust/r3-fencing-remediation/
```

The exact 53-file pre-remediation list with size and SHA-256 is:

```text
preparation/production-trust/r3-fencing-remediation/PHASE_R3_FENCING_REMEDIATION_BASELINE_SHA256SUMS.txt
```

## 3. Fencing Files Reviewed

| File | Current semantics | Treatment |
|---|---|---|
| `r2-r3-remediation/contracts.ts` | defines Worker and FencingAllocation, no resource floor | read-only source; R4 contract redefines normalized Scope Key |
| `r2-r3-remediation/lock-order.ts` | global fence control, no resource floor domain | read-only source; R4 adds resource-floor lock order |
| `r2-r3-remediation/sql/00-schema.sql` | Worker `fence_floor` and global next-token control | read-only source; new R4 schema adds resource floor |
| `r2-r3-remediation/sql/10-lease-issuance.sql` | global token allocation and Worker floor update | read-only source; new R4 transaction |
| `r2-r3-remediation/sql/20-worker-progress.sql` | checks Worker `.fence_floor` only | read-only source; new R4 resource-floor check |
| `r2-r3-remediation/sql/30-send-authorization-issuance.sql` | checks Worker `.fence_floor` only | read-only source; new R4 resource-floor check |
| `r2-r3-remediation/sql/40-send-authorization-consume.sql` | checks Worker `.fence_floor` only | read-only source; new R4 resource-floor check |
| `r2-r3-remediation/sql/70-fencing-registry.sql` | updates global counter and Worker floor | read-only source; new R4 resource takeover transaction |
| `r2-r3-remediation/models/fencing-registry.ts` | per-resource in-memory floor | read-only source; R4 model must mirror persistent resource floor |
| `r2-r3-remediation/models/execution-lease.ts` | Lease/send checks use Worker floor | read-only source; R4 model must check resource floor |
| `r2-r3-remediation/tests/fencing-audit-emergency.test.ts` | resource floor model tests | read-only source; R4 adds takeover and stale boundary tests |
| `r2-r3-remediation/tests/execution-lease.test.ts` | Worker-centric fencing checks | read-only source; R4 adds scope-bound boundary tests |
| `r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FENCING_MODEL.md` | says scope is resource/Capability | read-only source; R4 makes explicit |
| `r2-r3-remediation/PHASE_R2_R3_REMEDIATION_THREAT_MODEL.md` | identifies egress/fence risks | read-only source; R4 threat review |
| `r2-r3-remediation/PHASE_R2_R3_REMEDIATION_RISK_REGISTER.md` | contains residual fence/egress risks | read-only source; R4 risk update |

## 4. Confirmed Defect

The R2–R3 SQL checks use the resource effectively as the unique Capability and
authorizes Worker progress by:

```text
trust_r3_worker_registration.fence_floor = lease.fencing_token
```

The offline model separately maintains per-resource floors. Therefore:

```text
MODEL_SCOPE=resource-scoped
SQL_SCOPE=Worker-floor
CONSISTENCY=FAIL
```

## 5. File Ownership

| Owner | Writable files |
|---|---|
| Agent A | `sql/00-schema.sql`, `sql/10-worker-takeover.sql`, `sql/20-lease-issuance.sql`, `sql/30-worker-progress.sql`, `sql/40-send-authorization-issuance.sql`, `sql/50-send-authorization-consume.sql` |
| Agent B | `models/fencing-floor.ts`, `tests/fencing-floor.test.ts`, `models/execution-boundary.ts`, `tests/execution-boundary.test.ts` |
| Agent C | `tests/races.test.ts`, `models/race-scenarios.ts`, threat/risk review material |
| Main Agent | R4 contracts, lock order, SQL analyzer, reports, integration tests, Manifest and Bundle |

No file has concurrent writers. Original R2–R3 files are read-only.

## 6. Dependency Graph

```text
Baseline
  -> normalized resource Scope Key
  -> persistent resource floor + monotonic token
  -> atomic takeover
  -> Lease / progress / permit checks
  -> final egress check
  -> race/threat tests
  -> cross-review
  -> Bundle
```

## 7. Collaboration Record

Three same-host Codex subagents are used for independent implementation work.
They share the same model and host and are not an external third-party audit.
The main Agent performs integration and cross-review.
<!-- END_EXACT_SOURCE id=S001 -->

### S002. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CONTRACT.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CONTRACT.md`
- Bytes: `3495`
- SHA-256: `F43185B267AB79ED23C9D29DD57EB69FF31517F1DFE043E2614F4F6946834650`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S002 sha256=F43185B267AB79ED23C9D29DD57EB69FF31517F1DFE043E2614F4F6946834650 bytes=3495 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_CONTRACT

## 1. Status

```text
CONTRACT_VERSION=r2-r3-fencing-remediation-v1
REALM=OFFLINE_REFERENCE_MODEL
PRODUCTION_IMPLEMENTATION=NOT_STARTED
REAL_FETCH_AUTHORIZED=NO
```

Machine-readable contracts:

```text
preparation/production-trust/r3-fencing-remediation/contracts.ts
preparation/production-trust/r3-fencing-remediation/scope.ts
preparation/production-trust/r3-fencing-remediation/lock-order.ts
```

## 2. Resource Scope

The canonical Fencing Scope Key is:

```text
fence-scope-v1:sha256:<64 lowercase hex>
```

Derived deterministically from:

```text
domain = r3-fencing-resource-scope-v1
providerKind = fetch
purpose = fetch_only
organizationId
targetDigest
```

Canonical fields are sorted and hashed with SHA-256. Capability ID, Lease ID,
Worker ID and Approval ID are excluded because takeover must update the same
resource across old and new Lease/Capability identities.

Organization ID is included so one tenant's target cannot advance another
tenant's floor.

## 3. Authority Rule

```text
WORKER_REGISTRATION_FLOOR IS NOT AUTHORITY
RESOURCE_FLOOR IS AUTHORITY
```

The persistent authoritative record is:

```text
trust_r4_resource_fencing(
  scope_key,
  current_fencing_token,
  current_worker_id,
  current_lease_id,
  current_capability_id,
  version,
  state,
  updated_at_ms
)
```

Worker `last_issued_token` is diagnostic only. A stale Worker remains
`ACTIVE` in registration but cannot authorize any operation because it is no
longer the current resource-floor owner.

## 4. Scope Objects

Every Execution Lease and Send Authorization contains `scopeKey`. Lease
validation checks:

```text
lease.scopeKey == floor.scopeKey
lease.fencingToken == floor.currentFencingToken
lease.workerInstanceId == floor.currentWorkerId
lease.leaseId == floor.currentLeaseId
lease.capabilityId == floor.currentCapabilityId
```

## 5. Token Allocation

```text
trust_r4_fencing_token_control.next_token
```

is a persistent global monotonic allocator. It may produce token values shared
across scopes, but authorization compares only the current floor of the
requested scope. A higher token in another scope cannot invalidate this scope.

## 6. Takeover

The takeover linearization point is the commit of one transaction containing:

```text
resource floor initialize/select FOR UPDATE
token allocation
current floor owner update
Worker registration liveness update
Lease insertion
audit append
```

The old Worker's resource ownership ends when this transaction commits, not
when its process exits or when its Registration is changed.

## 7. Failure Codes

```text
RESOURCE_SCOPE_MISMATCH
RESOURCE_FLOOR_NOT_FOUND
RESOURCE_FLOOR_CONFLICT
FENCING_TOKEN_STALE
FENCING_TOKEN_NOT_MONOTONIC
WORKER_NOT_CURRENT
LEASE_NOT_CURRENT
WORKER_NOT_ACTIVE
LEASE_STATE_INVALID
LEASE_EXPIRED
SEND_AUTHORIZATION_INVALID
SEND_AUTHORIZATION_EXPIRED
SEND_AUTHORIZATION_REPLAYED
EMERGENCY_STOP_ACTIVE
EMERGENCY_EPOCH_MISMATCH
KEY_REVOKED
KEY_VERSION_MISMATCH
BUDGET_RESERVATION_CONFLICT
BUDGET_RESERVATION_EXPIRED
ROW_COUNT_CONFLICT
AUTHORITY_UNAVAILABLE
COMMIT_OUTCOME_UNKNOWN
SEND_OUTCOME_UNKNOWN
```

## 8. Compatibility Impact

| Previous R3 | R4 |
|---|---|
| Worker floor used in SQL | persistent resource floor |
| model-only `resourceFloors` | persistent resource record mirrored in model |
| no scope field in Lease/Permit | scope key required |
| takeover implicit | explicit atomic takeover |

This is a new schema version. Existing R2-R3 files remain unchanged.
<!-- END_EXACT_SOURCE id=S002 -->

### S003. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CROSS_REVIEW.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CROSS_REVIEW.md`
- Bytes: `1629`
- SHA-256: `8E455E4299C7687D634EC3AEE4ACC2C80D9252AAB5E9D6EB9C1C0DDB2AFAA016`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S003 sha256=8E455E4299C7687D634EC3AEE4ACC2C80D9252AAB5E9D6EB9C1C0DDB2AFAA016 bytes=1629 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_CROSS_REVIEW

## 1. Review Result

```text
SQL_MODEL_SCOPE=MATCH
RESOURCE_FLOOR_AUTHORITY=MATCH
LOCK_ORDER=MATCH
ROW_COUNT_PATHS=MATCH
STALE_WORKER_BOUNDARIES=MATCH
EMERGENCY_KEY_CHECKS=MATCH
EGRESS_FRESH_READ=DESIGN_ONLY
```

No unresolved P0 defect remains in the authorized offline scope.

## 2. Findings Closed

| Finding | Resolution |
|---|---|
| SQL used Worker floor | all boundaries use resource floor |
| model and SQL scope differed | canonical shared Scope Key |
| old ACTIVE registration could authorize | registration is liveness/diagnostic only |
| revoked Worker could be reactivated by upsert | conflict-safe insert + active-only conditional update |
| model exposed unguarded Lease state write | transition requires resource floor, mutable context and row count |
| permit replay path skipped context | replay now checks current floor and mutable context |
| Takeover floor state not checked | non-ACTIVE floor rejects takeover |
| final egress depended on design text only | SQL/model fresh-floor check plus fail-closed tests |

## 3. Collaboration Limitations

```text
INDEPENDENCE_LIMITATION=SAME_HOST_MODEL_SUBAGENTS_NOT_EXTERNAL_AUDIT
OWNERSHIP_PROCESS_NOTE=Agent B reported early creation of some parent-owned files; main agent reviewed and retained final versions
AGENT_A_FINAL_NOTE=Agent A's follow-up correction was interrupted; main agent completed the Worker state correction and reran all tests
```

## 4. Validation Limits

```text
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```
<!-- END_EXACT_SOURCE id=S003 -->

### S004. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_DIFF.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_DIFF.md`
- Bytes: `1635`
- SHA-256: `45DC3E67B086C92AF9ADF8C44AE8ECD17C7E9E7595401A1C6213B589C16A8E94`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S004 sha256=45DC3E67B086C92AF9ADF8C44AE8ECD17C7E9E7595401A1C6213B589C16A8E94 bytes=1635 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_DIFF

## 1. Resource Scope

Before:

```text
SQL: Worker registration fence_floor
Model: resourceFloors Map
README: resource-scoped statement
```

After:

```text
Scope Key = fence-scope-v1:sha256(canonical provider/target/organization)
SQL authority = trust_r4_resource_fencing
Model authority = OfflinePersistentFencingFloor.floors by same key
Worker floor = diagnostic only
```

## 2. Takeover

Before:

```text
global token incremented
Worker floor updated
no persistent resource owner record
```

After:

```text
initialize/lock resource floor
lock token control
allocate token
update current token/Worker/Lease/Capability/version
conditional Worker registration update (REVOKED cannot reactivate)
insert Lease
append audit
```

## 3. Authorization Boundaries

Before:

```text
Worker Progress: Worker fence_floor
Permit Issuance: Worker fence_floor
Permit Consumption: Worker fence_floor
```

After:

```text
every boundary checks current resource floor:
  scope
  token
  Worker
  Lease
  Capability
```

## 4. Egress

Before:

```text
final egress requirement described, but SQL proof still used Worker floor
```

After:

```text
final fresh central resource-floor read
fail closed if authority unavailable
reject old/current-owner mismatch
one-use permit
```

The final read and socket write remain non-atomic.

## 5. Tests

Before:

```text
resource floor model tests, but SQL tests did not prove resource floor
```

After:

```text
positive SQL structural analysis
ten negative SQL/egress cases
takeover races
old Worker progress/permit/consume/egress denial
central authority fail-closed
```
<!-- END_EXACT_SOURCE id=S004 -->

### S005. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT.md`
- Bytes: `5730`
- SHA-256: `8A2D510E772B1CE0B2EC724FBB902F11D9C19230EBBA46480DA10C49898FBED4`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S005 sha256=8A2D510E772B1CE0B2EC724FBB902F11D9C19230EBBA46480DA10C49898FBED4 bytes=5730 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT

## 1. Final Status

```text
R3_FENCING_REMEDIATION_PASS
OFFLINE_ACCEPTANCE=PASS

PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

This is an offline design/reference-model acceptance only.

## 2. Required Acceptance

```text
RESOURCE_SCOPE_UNIFICATION=PASS
PERSISTENT_RESOURCE_FLOOR=PASS
MONOTONIC_TOKEN_ALLOCATION=PASS
ATOMIC_WORKER_TAKEOVER=PASS
STALE_WORKER_REJECTION=PASS
LEASE_FENCING_ENFORCEMENT=PASS
PROGRESS_FENCING_ENFORCEMENT=PASS
SEND_AUTH_FENCING_ENFORCEMENT=PASS
PERMIT_CONSUMPTION_FENCING_ENFORCEMENT=PASS
LOCK_ORDER_CONSISTENCY=PASS
SQL_ROW_COUNT_ENFORCEMENT=PASS
SQL_MODEL_CONSISTENCY=PASS
EMERGENCY_AND_KEY_COMPATIBILITY=PASS
EGRESS_BOUNDARY_DESIGN=PASS
SQL_NEGATIVE_TESTS=PASS
OFFLINE_MODEL_TESTS=PASS
```

## 3. Defect Resolution

Before:

```text
SQL authorization: Worker registration fence_floor
offline model: per-resource floor
old Worker could remain ACTIVE with a historical token
```

After:

```text
authority: trust_r4_resource_fencing by canonical scope_key
Worker registration: liveness/diagnostic only
current token/Worker/Lease/Capability: one persisted owner
old Worker: rejected at progress, permit, consume and egress
```

## 4. Scope Key

```text
fence-scope-v1:sha256:<64 lowercase hex>
```

Derived from:

```text
domain=r3-fencing-resource-scope-v1
providerKind=fetch
purpose=fetch_only
organizationId
targetDigest
```

Capability and Lease are excluded so a replacement Lease for the same
protected resource advances the same floor.

## 5. Transaction and Locking Result

Canonical order:

```text
EMERGENCY_CONTROL
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
-> AUDIT_SEQUENCE
```

Takeover commits resource floor update, Lease insertion and audit in one
transaction. All security updates declare exactly one affected row.

## 6. Additional Findings Closed

- A revoked Worker can no longer be silently reactivated by registration
  conflict handling.
- Lease state transition in the model now requires a current resource-floor
  expectation, mutable security context and explicit row count.
- Send Authorization replay revalidates mutable Emergency/Key/Budget context.
- Resource floor state must be ACTIVE before takeover.
- Audit failure, row-count failure, unknown commit and central authority loss
  fail closed.

## 7. Tests

```text
R3 fencing Vitest:             7 files / 49 tests PASS
R2-R3 regression:             8 files / 74 tests PASS
R2 regression:                10 files / 80 tests PASS
R1 regression:                16 files / 91 tests PASS
R31-R36 relevant regression:  24 files / 179 tests PASS
PowerShell total:             69/69 PASS
PowerShell 5.1 Parser:        PASS / 6 scripts
TypeScript strict:            PASS
ESLint:                       PASS
Next.js production build:     PASS
```

Evidence boundaries:

```text
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```

## 8. Files Created

Required remediation reports and SQL:

```text
PHASE_R3_FENCING_REMEDIATION_BASELINE.md
PHASE_R3_FENCING_REMEDIATION_BASELINE_SHA256SUMS.txt
PHASE_R3_FENCING_REMEDIATION_CONTRACT.md
PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql
PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql
PHASE_R3_FENCING_REMEDIATION_MODEL.md
PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW.md
PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX.md
PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL.md
PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER.md
PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT.md
PHASE_R3_FENCING_REMEDIATION_SHA256SUMS.txt
```

Reference implementation:

```text
scope.ts
contracts.ts
lock-order.ts
vitest.config.ts
models/fencing-floor.ts
models/execution-boundary.ts
models/race-scenarios.ts
models/sql-analyzer.ts
tests/fencing-floor.test.ts
tests/execution-boundary.test.ts
tests/races.test.ts
tests/scope-lock.test.ts
tests/scope-lock-order.test.ts
tests/sql-positive.test.ts
tests/sql-negative.test.ts
```

## 9. Cross-Review

The main Agent reviewed the merged SQL and model:

```text
SQL_MODEL_SCOPE=MATCH
RESOURCE_FLOOR_AUTHORITY=MATCH
OLD_WORKER_REJECTION=MATCH
LOCK_ORDER=MATCH
ROW_COUNT_PATHS=MATCH
EGRESS_FRESH_READ=DESIGN_ONLY
```

Collaboration limitations:

- Agents are same-host Codex subagents, not external independent auditors;
- Agent B reported accidentally creating some parent-owned files during early
  role interpretation; final parent-owned files were reviewed by the main
  Agent and current tests pass;
- Agent A's later Worker-state correction was interrupted and completed by the
  main Agent within the allowed directory.

## 10. Residual Risks

- real PostgreSQL locking/unique/SQLSTATE behavior is not executed;
- real multi-instance takeover is not executed;
- the trusted Egress network choke point is not deployed;
- a takeover after the final floor read can race with the actual socket write;
- Provider does not interpret application fencing;
- scope derivation changes may require migration compatibility review;
- no external independent audit.

## 11. Safety Boundaries

```text
MAIN_WORKSPACE_MODIFIED=NO
SRC_SCRIPTS_MODIFIED=NO
R31_R36_MODIFIED=NO
IDENTITY_CORE_MODIFIED=NO
A3_D1_D2_MODIFIED=NO
REAL_KEY_ACCESSED=NO
REAL_API_CALLED=NO
NETWORK_ACCESSED=NO
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
```

## 12. Stop State

```text
STOP_AFTER_R3_FENCING_OFFLINE_ACCEPTANCE
NEXT_PHASE=NOT_STARTED
PRODUCTION_AUTHORIZATION=NOT_GRANTED
```
<!-- END_EXACT_SOURCE id=S005 -->

### S006. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_MODEL.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_MODEL.md`
- Bytes: `3639`
- SHA-256: `D5D1B28AAC2727F1841AB0A0940EFA623A48730319A6EDFFE82833286F78F18F`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S006 sha256=D5D1B28AAC2727F1841AB0A0940EFA623A48730319A6EDFFE82833286F78F18F bytes=3639 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_MODEL

## 1. Model Files

```text
models/fencing-floor.ts
models/execution-boundary.ts
models/race-scenarios.ts
models/sql-analyzer.ts
```

All are `OFFLINE_REFERENCE_MODEL`; none is production wiring.

## 2. Persistent Floor Model

`OfflinePersistentFencingFloor` models:

```text
authoritative floor per scopeKey
global monotonic token allocator
Worker registration liveness metadata
current token/Worker/Lease/Capability
Lease and audit records
```

The synchronous takeover method is one linearization point:

```text
validate authority
validate Scope Key
validate row counts
idempotent Lease check
verify token monotonicity for this scope
verify Worker state
update floor owner/token/version
update Worker diagnostic token
insert Lease
append audit
```

An old Worker remains `ACTIVE` in Registration but fails because the resource
floor points to another Worker/Lease/token.

## 3. Lease and Permit Boundary

`OfflineExecutionBoundary` revalidates the current resource floor for:

```text
KEY_READ
TRANSPORT_CREATED
Send Authorization Issuance
Send Authorization Consumption
Egress write
```

Every transition requires explicit row counts. The authoritative transition
helper validates current floor token/Worker/Lease/Capability and the legal
Lease state transition before mutating state.

## 4. Permit Lifecycle

```text
ISSUED -> CONSUMED
```

Only one consumption succeeds. Replay returns
`SEND_AUTHORIZATION_REPLAYED`. A permit's scope/Worker/Lease/Capability/token
must equal the current floor.

`SENT` means the local one-use write permission was consumed. It does not prove
Provider receipt.

## 5. Egress Model

Before returning `networkWriteAllowed=true`, the model:

```text
validates row count
validates consumed permit/attempt marker
re-reads current resource floor
checks Worker, Lease, Capability, token
checks Lease state SENT
checks Emergency epoch and Key/revocation versions
checks budget state/expiry
```

Central authority loss returns an error. No cached floor is used.

## 6. Race Model

`models/race-scenarios.ts` classifies:

```text
takeover before permit consumption -> stale denial
takeover after permit consumption before write -> write blocked
takeover after write start -> cannot recall; unknown without response
Emergency/Key revoke -> block pre-write stages
authority unavailable -> fail closed
```

## 7. SQL/Model Mapping

| State/operation | SQL draft | Model |
|---|---|---|
| floor initialization/takeover | `10-worker-takeover.sql` | `takeover()` |
| idempotent lookup after unknown COMMIT | `20-lease-issuance.sql` | `recoverTakeover()` |
| `ISSUED -> KEY_READ` | `30-worker-progress.sql` | `progressLease()` |
| `KEY_READ -> TRANSPORT_CREATED` | `30-worker-progress.sql` | `progressLease()` |
| permit issuance | `40-send-authorization-issuance.sql` | `issuePermit()` |
| permit consumption | `50-send-authorization-consume.sql` | `consumePermit()` |
| final egress check | `50-send-authorization-consume.sql` second transaction | `authorizeEgress()` |

## 8. Invariants

```text
one current floor per normalized Scope Key
one current owner token/Worker/Lease/Capability binding
token strictly increases for the same scope
different scopes have independent floor comparisons
old token cannot authorize progress/issuance/consumption/egress
permit cannot be replayed
Emergency and Key checks cannot be bypassed by fencing
authority unavailable fails closed
```

## 9. Limitations

The model is synchronous and single-process. It does not prove PostgreSQL row
locks, unique-conflict behavior, deadlocks, multi-instance timing or a real
network egress choke point.
<!-- END_EXACT_SOURCE id=S006 -->

### S007. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER.md`
- Bytes: `2591`
- SHA-256: `3A1F3BFD5BB6B4BFE28F7D9FE71D719B2BF8799CE8E1193CE37AA4EFC88A455D`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S007 sha256=3A1F3BFD5BB6B4BFE28F7D9FE71D719B2BF8799CE8E1193CE37AA4EFC88A455D bytes=2591 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER

## 1. Closed Design Risks

| Risk | Resolution | Status |
|---|---|---|
| model resource floor vs SQL Worker floor | all R4 SQL and model checks use the normalized resource scope floor | CLOSED_OFFLINE |
| old Worker registration remains ACTIVE and gets authority | registration no longer grants fencing authority | CLOSED_OFFLINE |
| higher token globally invalidates unrelated resource | floor comparison is scoped to canonical scope key | CLOSED_OFFLINE |
| token allocation outside floor transaction | takeover transaction must allocate, update floor, Lease and audit together | CLOSED_STATIC |
| Worker takeover leaves old floor owner | floor current token/Worker/Lease/Capability updated atomically | CLOSED_STATIC |
| consume permit with stale token | permit consumption lock/check includes current scope floor | CLOSED_OFFLINE |
| final egress trusts cache | design requires fresh central floor check | CLOSED_DESIGN |
| unknown commit causes blind reallocation | recovery reads persisted Lease by scope/token and never reallocates blindly | CLOSED_OFFLINE |

## 2. Open Risks

| ID | Severity | Risk | Status |
|---|---|---|---|
| R3F-R1 | HIGH | No real PostgreSQL transaction/lock execution | POSTGRESQL_INTEGRATION=NOT_EXECUTED |
| R3F-R2 | CRITICAL if deployed | No real multi-instance takeover test | MULTI_INSTANCE_TEST=NOT_EXECUTED |
| R3F-R3 | CRITICAL if egress bypassed | Worker still able to reach Provider directly | production architecture blocker |
| R3F-R4 | HIGH | Final floor read and socket write are not atomic | residual window |
| R3F-R5 | HIGH | Central authority outage can halt work | intentional fail-closed availability cost |
| R3F-R6 | HIGH | Provider does not understand application fencing | trusted egress component mandatory |
| R3F-R7 | MEDIUM | Scope derivation changes reduce takeover compatibility with pre-R4 design | migration/compatibility review required |
| R3F-R8 | HIGH | No external independent audit | internal subagents are same host/model |

## 3. Failure Semantics

- If floor authority unavailable: no new allocation/progress/permit/egress.
- If old token: reject.
- If Worker/Lease not current owner: reject.
- If permit already consumed: reject with replay.
- If write already started: cannot recall; record unknown if no response.
- If COMMIT response lost: query scope and expected Lease; only return exact
  persisted takeover, otherwise investigate.

## 4. Production State

```text
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```
<!-- END_EXACT_SOURCE id=S007 -->

### S008. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW.md`
- Bytes: `3680`
- SHA-256: `E6CED6736E59AA4AE2CBDE965380CD4BF76765A67393BF32344FDF6E70D73986`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S008 sha256=E6CED6736E59AA4AE2CBDE965380CD4BF76765A67393BF32344FDF6E70D73986 bytes=3680 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW

## 1. Scope

```text
SQL_MODE=STATIC_REVIEW_ONLY
SQL_EXECUTED=NO
DATABASE_CONNECTED=NO
POSTGRESQL_INTEGRATION=NOT_EXECUTED
```

Files:

```text
sql/00-schema.sql
sql/10-worker-takeover.sql
sql/20-lease-issuance.sql
sql/30-worker-progress.sql
sql/40-send-authorization-issuance.sql
sql/50-send-authorization-consume.sql
PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql
```

## 2. Baseline Defect

```text
R2-R3 SQL:
  checks trust_r3_worker_registration.fence_floor

R2-R3 model:
  checks resourceFloors[scopeKey]
```

This allowed SQL to accept an old Worker whose Registration still contained a
historic token even after another Worker became current for the same resource.

## 3. Remediation

New authority:

```text
trust_r4_resource_fencing(
  scope_key PRIMARY KEY,
  current_fencing_token,
  current_worker_id,
  current_lease_id,
  current_capability_id,
  version,
  state
)
```

Worker registration `last_issued_token` is diagnostic, never authorization.

First use:

```text
INSERT floor token=0 ON CONFLICT DO NOTHING
SELECT floor FOR UPDATE
```

Takeover transaction:

```text
lock resource floor
lock persistent token control
allocate higher token
update floor current token/Worker/Lease/Capability/version
require active Worker registration without reactivating REVOKED
insert Lease
append audit
COMMIT
```

## 4. Boundary Checks

| Boundary | Resource floor | Worker | Lease | Capability | Emergency | Key | Budget | Audit |
|---|---|---|---|---|---|---|---|---|
| Lease takeover | lock/update | active | insert/bind | bind | check | check | check | yes |
| Lease recovery | lock | current | exact existing | bind | check | check | check | read-only |
| Worker progress | lock/exact | exact | exact | exact | check | check | check | yes |
| Send issuance | lock/exact | exact | exact | exact | check | check | check | yes |
| Permit consumption | lock/exact | exact | exact | exact | check | check | check | yes |
| Final egress read | current read | exact | exact | exact | check | check | reserved | permission is one-use |

## 5. Lock Order

```text
EMERGENCY_CONTROL
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
-> AUDIT_SEQUENCE
```

## 6. Row Count

Every security-sensitive UPDATE has:

```text
-- ROW_COUNT_EXPECTATION: exactly 1
```

The driver must check command tags and roll back the entire transaction for any
value other than one.

## 7. Negative Static Tests

`tests/sql-negative.test.ts` proves detection of:

- Worker-only floor authorization;
- missing resource floor;
- registration-only takeover;
- revoked Worker reactivation through upsert;
- floor and Lease in different transactions;
- permit consumption without floor lock;
- missing row count;
- implicit global floor;
- cached egress floor;
- central authority fail-open.

## 8. Positive Static Tests

`tests/sql-positive.test.ts` checks:

- all six SQL files exist;
- no `fence_floor` authorization token exists;
- every annotated transaction passes the analyzer;
- the resource table and current-owner fields exist;
- the consolidated transaction artifact contains each complete source file;
- final egress uses a fresh resource-floor read.

## 9. What Static Review Proves

It proves the drafts contain the intended resource scope, conditions, row-count
markers, transaction grouping and negative-test sensitivity.

It does not prove PostgreSQL syntax acceptance, lock behavior, SQLSTATE,
multi-instance ordering or egress network isolation.
<!-- END_EXACT_SOURCE id=S008 -->

### S009. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX.md`
- Bytes: `3647`
- SHA-256: `633F8F15D83167C9D9D5D5B233177D7FFBFC47A3FAFDD3221866D7DB4420392A`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S009 sha256=633F8F15D83167C9D9D5D5B233177D7FFBFC47A3FAFDD3221866D7DB4420392A bytes=3647 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX

## 1. Evidence Classes

```text
SQL_STATIC_ANALYSIS
SQL_NEGATIVE_TESTS
OFFLINE_REFERENCE_MODEL
LOCAL_UNIT_TESTS

POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```

## 2. Core Fencing Matrix

| Requirement | Evidence | Result |
|---|---|---|
| one normalized Scope Key | scope tests, SQL schema | PASS |
| resource floor persists current owner | fencing-floor tests, SQL positive | PASS |
| token monotonic within scope | fencing-floor and race tests | PASS |
| Worker A 100 then B 101 | fencing-floor tests | PASS |
| A Registration remains ACTIVE | fencing-floor / race tests | PASS |
| A progress after B takeover denied | execution-boundary / race tests | PASS |
| A permit issuance denied | execution-boundary / race tests | PASS |
| A permit consumption denied | execution-boundary / race tests | PASS |
| A egress denied | execution-boundary / race tests | PASS |
| different scopes independent | scope / fencing-floor / race tests | PASS |
| takeover atomic floor + Lease + audit | SQL analyzer and model takeover | PASS |
| audit failure rolls back takeover | fencing-floor tests | PASS |
| row-count failure rolls back | fencing-floor / execution-boundary tests | PASS |
| COMMIT unknown recovery | fencing-floor and race tests | PASS |
| Emergency epoch mismatch denied | execution-boundary / race tests | PASS |
| Key revocation denied | execution-boundary / race tests | PASS |
| permit repeat denied | execution-boundary / race tests | PASS |
| central authority unavailable denied | fencing-floor / execution-boundary / race tests | PASS |
| final egress uses fresh central floor | execution-boundary tests / SQL positive | PASS |

## 3. SQL Negative Tests

`tests/sql-negative.test.ts` proves detection of:

```text
Worker-only fence authorization
missing resource floor
registration-only takeover
floor and Lease in different transactions
permit consumption without floor lock
missing row-count marker
implicit global floor
cached egress floor
authority fail-open
```

## 4. SQL Positive Tests

`tests/sql-positive.test.ts` verifies:

```text
all six SQL files exist
no Worker fence_floor authorization token exists
all transaction analyzers pass
resource floor and owner fields exist
scope_key appears in Lease and Send Authorization
final egress reads current floor
consolidated SQL artifact contains each full file
```

## 5. Race Scenarios

| Race | Outcome |
|---|---|
| A consumes permit, B takeover before write | egress denied by current floor |
| A writes before takeover | Provider cannot be recalled; unknown if no response |
| takeover vs Emergency | first committed control state governs pre-write stage |
| Key revocation vs permit | Key/revocation mismatch denies |
| Lease expiry vs takeover | expired Lease cannot advance/send |
| permit replay | denied |
| central authority loss | fail closed |
| COMMIT response lost | exact persisted recovery only |

## 6. Test Commands

```text
node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r3-fencing-remediation/vitest.config.ts
```

Result:

```text
7 test files / 49 tests PASS
```

Regression:

```text
R2-R3: 8 files / 74 tests PASS
R2:    10 files / 80 tests PASS
R1:    16 files / 91 tests PASS
R31-R36 relevant: 24 files / 179 tests PASS
PowerShell: 69/69 PASS
```

## 7. Verification Boundaries

```text
SQL_EXECUTED=NO
DATABASE_CONNECTED=NO
MULTI_INSTANCE_EXECUTED=NO
EGRESS_NETWORK_TESTED=NO
PROVIDER_TESTED=NO
```

Passing these tests proves only the declared offline model and static SQL
properties.
<!-- END_EXACT_SOURCE id=S009 -->

### S010. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL.md

- Category: `A_R3F_REPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL.md`
- Bytes: `4302`
- SHA-256: `BAFCAC5051A6C73197255849F25409F0AB2B40806F727FA71EC0709A82F1D097`
- Description: Complete R3 fencing report

<!-- BEGIN_EXACT_SOURCE id=S010 sha256=BAFCAC5051A6C73197255849F25409F0AB2B40806F727FA71EC0709A82F1D097 bytes=4302 fence=raw -->
# PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL

## 1. Scope

```text
MODEL=OFFLINE_ONLY
REAL_EGRESS_TEST=NOT_EXECUTED
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
```

This review covers resource-scoped fencing and its authorization boundaries.
It does not claim that adding a database table creates production fencing.

## 2. Fencing Scope

The unique scope is:

```text
providerKind=fetch
purpose=fetch_only
organizationId
targetDigest
```

These values are canonically encoded under domain `r3-fencing-resource-scope-v1`
and hashed into a `fence-scope-v1:sha256:<digest>` key.

Capability, Lease, Approval, Worker and registration IDs are not part of the
scope identity. They are current owners/claims checked against the persistent
scope floor.

## 3. Critical Threats

| Threat | Severity | Required control |
|---|---|---|
| Worker A continues after B takeover | CRITICAL | every Lease/progress/permit/egress check compares resource floor current token, Worker and Lease |
| Registration remains ACTIVE | CRITICAL | registration is liveness/diagnostic only; it is never sufficient authorization |
| SQL compares Worker-only floor | CRITICAL | all fencing authorization checks resource-scope floor |
| Old token presented | CRITICAL | exact current-token equality, not Worker birth data |
| Duplicate current owner | CRITICAL | resource floor row lock and conditional version update |
| First-floor creation race | HIGH | insert-on-conflict + lock/re-read before token allocation |
| Token allocated without floor/Lease | HIGH | one transaction and exact row counts |
| Floor points to Worker that never got Lease | HIGH | Worker, Lease, Capability and token updated together |
| Global token comparison across resources | HIGH | compare only within normalized scope key |
| Emergency epoch changed | CRITICAL | epoch equality at progress, permit and egress |
| Key revoked | HIGH | Key/revocation version equality at progress, permit and egress |
| Permit replay | CRITICAL | one-use `ISSUED -> CONSUMED` |
| Central authority unavailable | CRITICAL | fail closed for allocation, progress, permit and egress |
| Cached floor used at egress | CRITICAL | final read from trusted central authority |
| Provider ignores application fence | HIGH | trusted egress choke point remains mandatory |
| Direct Worker provider access | CRITICAL | network architecture must prevent bypass |
| COMMIT response lost | HIGH | recover by persisted scope/lease/token, never allocate blindly |

## 4. Race Results

### Worker A permit vs Worker B takeover

```text
B takeover commits first:
  A progress/issuance/consumption/egress -> stale

A permit consumption commits first, B takeover before egress:
  A permit is consumed
  final egress floor check rejects A
  no Provider write occurs

A write starts before takeover:
  request cannot be recalled
  response missing -> SEND_OUTCOME_UNKNOWN
```

### Emergency / Key Revocation

Emergency activation before permit consumption or egress denies the old
operation. Key revocation does the same. A Provider request already written
cannot be recalled.

### Central Authority Loss

If the trusted central resource floor cannot be read, no new progress, permit
or egress is authorized. Cached floor values are not sufficient.

## 5. Egress Boundary

The Egress component must:

- have exclusive Provider network access;
- read current resource floor immediately before writing;
- compare scope, token, Worker, Lease, Capability and permit;
- re-check Emergency epoch and Key versions;
- consume a one-use permit;
- fail closed on authority loss;
- not retry after an unknown write outcome.

The local database commit and the actual socket write remain non-atomic. This
window is residual and cannot be eliminated by SQL alone.

## 6. Confused Deputy and Cross-Scope

Every authorization object binds a normalized scope key. A valid token from
resource scope A does not authorize resource scope B. Organization and target
digest are part of scope derivation, preventing cross-tenant floor reuse.

## 7. Test Classification

```text
OFFLINE_REFERENCE_MODEL
LOCAL_UNIT_TESTS
SQL_STATIC_ANALYSIS
SQL_NEGATIVE_TESTS

POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_EGRESS_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```
<!-- END_EXACT_SOURCE id=S010 -->

### S011. preparation\production-trust\r3-fencing-remediation\sql\00-schema.sql

- Category: `B_R3F_SQL`
- Path: `preparation\production-trust\r3-fencing-remediation\sql\00-schema.sql`
- Bytes: `4974`
- SHA-256: `76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4`
- Description: Complete R4 fencing SQL draft

<!-- BEGIN_EXACT_SOURCE id=S011 sha256=76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4 bytes=4974 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R4 fencing layer. This draft assumes the R3 authorization, budget,
-- capability, key and emergency tables already exist. It does not modify the
-- frozen R3 schema.

CREATE TABLE trust_r4_resource_fencing (
  scope_key text PRIMARY KEY
    CHECK (scope_key ~ '^fence-scope-v1:sha256:[a-f0-9]{64}$'),
  current_fencing_token bigint NOT NULL DEFAULT 0
    CHECK (current_fencing_token >= 0),
  current_worker_id uuid,
  current_lease_id uuid,
  current_capability_id uuid,
  version bigint NOT NULL DEFAULT 1 CHECK (version >= 1),
  state text NOT NULL DEFAULT 'ACTIVE'
    CHECK (state IN ('ACTIVE', 'REVOKED')),
  updated_at_ms bigint NOT NULL,
  CHECK (
    (current_fencing_token = 0
      AND current_worker_id IS NULL
      AND current_lease_id IS NULL
      AND current_capability_id IS NULL)
    OR
    (current_fencing_token > 0
      AND current_worker_id IS NOT NULL
      AND current_lease_id IS NOT NULL
      AND current_capability_id IS NOT NULL)
  )
);

CREATE TABLE trust_r4_fencing_token_control (
  singleton_id smallint PRIMARY KEY CHECK (singleton_id = 1),
  next_token bigint NOT NULL CHECK (next_token >= 1),
  version bigint NOT NULL CHECK (version >= 1),
  updated_at_ms bigint NOT NULL
);

INSERT INTO trust_r4_fencing_token_control (
  singleton_id, next_token, version, updated_at_ms
) VALUES (1, 1, 1, 0);

CREATE TABLE trust_r4_worker_registration (
  worker_instance_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (state IN ('ACTIVE', 'DRAINING', 'REVOKED')),
  heartbeat_at_ms bigint NOT NULL,
  last_issued_token bigint NOT NULL DEFAULT 0 CHECK (last_issued_token >= 0),
  updated_at_ms bigint NOT NULL
);

CREATE TABLE trust_r4_execution_lease (
  lease_id uuid PRIMARY KEY,
  scope_key text NOT NULL REFERENCES trust_r4_resource_fencing (scope_key),
  capability_id uuid NOT NULL UNIQUE
    REFERENCES trust_r3_capability (capability_id),
  execution_authorization_id uuid NOT NULL
    REFERENCES trust_r3_execution_authorization (authorization_id),
  budget_reservation_id uuid NOT NULL
    REFERENCES trust_r3_budget_reservation (reservation_id),
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r4_worker_registration (worker_instance_id),
  fencing_token bigint NOT NULL CHECK (fencing_token > 0),
  state text NOT NULL CHECK (
    state IN (
      'ISSUED', 'KEY_READ', 'TRANSPORT_CREATED', 'SEND_AUTHORIZED',
      'SENT', 'RESPONSE_RECEIVED', 'COMPLETED', 'FAILED_BEFORE_SEND',
      'SEND_OUTCOME_UNKNOWN', 'FAILED_AFTER_SEND', 'EXPIRED', 'REVOKED',
      'EMERGENCY_BLOCKED'
    )
  ),
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  emergency_epoch bigint NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  UNIQUE (scope_key, fencing_token),
  CHECK (expires_at_ms > issued_at_ms),
  CHECK (expires_at_ms - issued_at_ms <= 60000)
);

ALTER TABLE trust_r4_resource_fencing
  ADD CONSTRAINT trust_r4_floor_worker_fk
  FOREIGN KEY (current_worker_id)
  REFERENCES trust_r4_worker_registration (worker_instance_id)
  DEFERRABLE INITIALLY DEFERRED;

ALTER TABLE trust_r4_resource_fencing
  ADD CONSTRAINT trust_r4_floor_lease_fk
  FOREIGN KEY (current_lease_id)
  REFERENCES trust_r4_execution_lease (lease_id)
  DEFERRABLE INITIALLY DEFERRED;

ALTER TABLE trust_r4_resource_fencing
  ADD CONSTRAINT trust_r4_floor_capability_fk
  FOREIGN KEY (current_capability_id)
  REFERENCES trust_r3_capability (capability_id)
  DEFERRABLE INITIALLY DEFERRED;

CREATE TABLE trust_r4_send_authorization (
  send_authorization_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (state IN ('ISSUED', 'CONSUMED', 'EXPIRED', 'REVOKED')),
  scope_key text NOT NULL REFERENCES trust_r4_resource_fencing (scope_key),
  lease_id uuid NOT NULL UNIQUE REFERENCES trust_r4_execution_lease (lease_id),
  capability_id uuid NOT NULL,
  worker_instance_id uuid NOT NULL,
  fencing_token bigint NOT NULL,
  budget_reservation_id uuid NOT NULL,
  emergency_epoch bigint NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  consumed_at_ms bigint,
  CHECK (expires_at_ms > issued_at_ms),
  CHECK (expires_at_ms - issued_at_ms <= 5000),
  CHECK (
    (state = 'ISSUED' AND consumed_at_ms IS NULL)
    OR (state = 'CONSUMED' AND consumed_at_ms IS NOT NULL)
    OR state IN ('EXPIRED', 'REVOKED')
  )
);

CREATE INDEX trust_r4_floor_worker_idx
  ON trust_r4_resource_fencing (current_worker_id, state);

CREATE INDEX trust_r4_floor_lease_idx
  ON trust_r4_resource_fencing (current_lease_id, state);

CREATE INDEX trust_r4_lease_worker_idx
  ON trust_r4_execution_lease (worker_instance_id, state, expires_at_ms);

CREATE INDEX trust_r4_send_state_idx
  ON trust_r4_send_authorization (state, expires_at_ms);
````
<!-- END_EXACT_SOURCE id=S011 -->

### S012. preparation\production-trust\r3-fencing-remediation\sql\10-worker-takeover.sql

- Category: `B_R3F_SQL`
- Path: `preparation\production-trust\r3-fencing-remediation\sql\10-worker-takeover.sql`
- Bytes: `6889`
- SHA-256: `000CC783457862E4CEFD5313E19EB3C055F02379FED642E982517361F42FB909`
- Description: Complete R4 fencing SQL draft

<!-- BEGIN_EXACT_SOURCE id=S012 sha256=000CC783457862E4CEFD5313E19EB3C055F02379FED642E982517361F42FB909 bytes=6889 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Atomic resource takeover + Lease issuance.
-- Linearization point: commit of resource-floor update and Lease insertion.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms, actor_id,
       organization_id, lead_id, target_digest, capability_id,
       budget_reservation_id, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r3_execution_authorization
WHERE authorization_id = $2
FOR UPDATE;

SELECT reservation_id, state, expires_at_ms, execution_authorization_id,
       capability_id, worker_instance_id, budget_version, send_started_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $3
FOR UPDATE;

SELECT capability_id, state, expires_at_ms, execution_authorization_id,
       consumption_id, worker_instance_id, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r3_capability
WHERE capability_id = $4
FOR UPDATE;

-- Secure first-use initialization. Concurrent creators block on the unique
-- scope key; after this statement and the following row lock, exactly one
-- authoritative floor is visible.
INSERT INTO trust_r4_resource_fencing (
  scope_key, current_fencing_token, current_worker_id, current_lease_id,
  current_capability_id, version, state, updated_at_ms
) VALUES (
  $5, 0, NULL, NULL, NULL, 1, 'ACTIVE', $6
)
ON CONFLICT (scope_key) DO NOTHING;

SELECT scope_key, current_fencing_token, current_worker_id, current_lease_id,
       current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $5
FOR UPDATE;

SELECT next_token, version
FROM trust_r4_fencing_token_control
WHERE singleton_id = 1
FOR UPDATE;

-- Worker registration is not an authorization source. last_issued_token is
-- diagnostic only; the resource floor remains authoritative.
INSERT INTO trust_r4_worker_registration (
  worker_instance_id, state, heartbeat_at_ms, last_issued_token, updated_at_ms
) VALUES (
  $7, 'ACTIVE', $6, 0, $6
)
ON CONFLICT (worker_instance_id) DO NOTHING;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration
SET heartbeat_at_ms = $6,
    updated_at_ms = $6
WHERE worker_instance_id = $7
  AND state = 'ACTIVE';

-- INSERT command tag must be one, and the conditional UPDATE must affect
-- exactly one row. A previously REVOKED Worker therefore rolls back instead
-- of being silently reactivated.

-- Allocate the next persistent token and bind it to this exact resource scope.
WITH allocated AS (
  -- ROW_COUNT_EXPECTATION: exactly 1
  UPDATE trust_r4_fencing_token_control
  SET next_token = next_token + 1,
      version = version + 1,
      updated_at_ms = $6
  WHERE singleton_id = 1
    AND next_token = $8
    AND version = $9
  RETURNING next_token - 1 AS fencing_token
)
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_resource_fencing AS floor
SET current_fencing_token = allocated.fencing_token,
    current_worker_id = $7,
    current_lease_id = $10,
    current_capability_id = $4,
    version = floor.version + 1,
    updated_at_ms = $6
FROM allocated
WHERE floor.scope_key = $5
  AND floor.state = 'ACTIVE'
  AND floor.version = $11
  AND floor.current_fencing_token < allocated.fencing_token
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $12
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key k
    WHERE k.key_id = $1
      AND k.state = 'ACTIVE'
      AND k.key_version = $13
      AND k.revocation_version = $14
      AND $6 >= k.valid_from_ms
      AND $6 < k.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization a
    WHERE a.authorization_id = $2
      AND a.state = 'ACTIVE'
      AND a.capability_id = $4
      AND a.budget_reservation_id = $3
      AND a.emergency_epoch = $12
      AND a.key_version = $13
      AND a.revocation_version = $14
      AND a.permission_version = $15
      AND a.policy_version = $16
      AND $6 < a.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $3
      AND b.state = 'RESERVED'
      AND b.execution_authorization_id = $2
      AND b.capability_id = $4
      AND b.worker_instance_id = $7
      AND b.send_started_at_ms IS NULL
      AND $6 < b.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability c
    WHERE c.capability_id = $4
      AND c.state = 'ISSUED'
      AND c.execution_authorization_id = $2
      AND c.worker_instance_id = $7
      AND c.budget_reservation_id = $3
      AND c.emergency_epoch = $12
      AND c.key_version = $13
      AND c.revocation_version = $14
      AND c.permission_version = $15
      AND c.policy_version = $16
      AND $6 < c.expires_at_ms
  )
RETURNING floor.current_fencing_token;

-- The driver must read exactly one returned token and bind it as $17 below.

WITH token AS (
  SELECT current_fencing_token
  FROM trust_r4_resource_fencing
  WHERE scope_key = $5
    AND current_worker_id = $7
    AND current_lease_id = $10
    AND current_capability_id = $4
)
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration AS worker
SET heartbeat_at_ms = $6,
    last_issued_token = token.current_fencing_token,
    updated_at_ms = $6
FROM token
WHERE worker.worker_instance_id = $7
  AND worker.state = 'ACTIVE';

-- INSERT command tag must be exactly one row.
INSERT INTO trust_r4_execution_lease (
  lease_id, scope_key, capability_id, execution_authorization_id,
  budget_reservation_id, worker_instance_id, fencing_token, state,
  issued_at_ms, expires_at_ms, emergency_epoch, key_version,
  revocation_version, permission_version, policy_version
) VALUES (
  $10, $5, $4, $2,
  $3, $7, $17, 'ISSUED',
  $6, $18, $12, $13,
  $14, $15, $16
);

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

-- INSERT command tag must be exactly one row.
INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $19, $20, $6, 'LEASE_ISSUED', 'ALLOW',
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

-- Any non-one command tag rolls back token allocation, floor update, Worker
-- registration mutation, Lease insertion and audit as one operation.
````
<!-- END_EXACT_SOURCE id=S012 -->

### S013. preparation\production-trust\r3-fencing-remediation\sql\20-lease-issuance.sql

- Category: `B_R3F_SQL`
- Path: `preparation\production-trust\r3-fencing-remediation\sql\20-lease-issuance.sql`
- Bytes: `2645`
- SHA-256: `101D3AACA2609E3A79FE1EC7AD7B0DBE376B9E2528B8CCB751056DEECAC79FC8`
- Description: Complete R4 fencing SQL draft

<!-- BEGIN_EXACT_SOURCE id=S013 sha256=101D3AACA2609E3A79FE1EC7AD7B0DBE376B9E2528B8CCB751056DEECAC79FC8 bytes=2645 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Lease Issuance recovery and verification.
--
-- The first issuance and Worker takeover are one atomic mutation in
-- 10-worker-takeover.sql. This transaction is used when the caller loses the
-- COMMIT acknowledgement or needs to verify an idempotent Lease request.
-- It never allocates another token and never inserts another Lease.

BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT reservation_id, state, execution_authorization_id, capability_id,
       worker_instance_id, expires_at_ms
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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       issued_at_ms, expires_at_ms, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r4_execution_lease
WHERE capability_id = $4
FOR UPDATE;

-- The driver must assert exactly one Lease row. The application validates:
--   lease.scope_key = floor.scope_key = $5
--   lease.fencing_token = floor.current_fencing_token = all supplied versions
--   lease.worker_instance_id = floor.current_worker_id = $6
--   lease.lease_id = floor.current_lease_id = $7
--   lease.capability_id = floor.current_capability_id = $4
--   Authorization, budget, Capability, Emergency and Key remain current
--   trusted now < Lease/resource/authorization/reservation expiry
--
-- If no Lease row exists after a COMMIT-unknown response, the caller may retry
-- 10-worker-takeover.sql. The unique capability_id Lease constraint is the
-- final duplicate-issuance arbiter.

COMMIT;
````
<!-- END_EXACT_SOURCE id=S013 -->

### S014. preparation\production-trust\r3-fencing-remediation\sql\30-worker-progress.sql

- Category: `B_R3F_SQL`
- Path: `preparation\production-trust\r3-fencing-remediation\sql\30-worker-progress.sql`
- Bytes: `9891`
- SHA-256: `5C9CC11B8763F7809D75F87C695E44B26A223132E5462071745A2A72F9534724`
- Description: Complete R4 fencing SQL draft

<!-- BEGIN_EXACT_SOURCE id=S014 sha256=5C9CC11B8763F7809D75F87C695E44B26A223132E5462071745A2A72F9534724 bytes=9891 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Worker Progress is two separate transactions. Worker registration metadata
-- is never sufficient; every update compares the authoritative resource floor.

-- Transaction 3A: ISSUED -> KEY_READ.
BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'KEY_READ'
WHERE lease.lease_id = $7
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND lease.state = 'ISSUED'
  AND lease.emergency_epoch = $9
  AND lease.key_version = $10
  AND lease.revocation_version = $11
  AND lease.permission_version = $12
  AND lease.policy_version = $13
  AND $14 < lease.expires_at_ms
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
      AND $14 - worker.heartbeat_at_ms <= 15000
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

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $15, $16, $14, 'WORKER_PROGRESS', 'ALLOW',
  $7, $17, $18
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $16,
    last_event_digest = $18
WHERE singleton_id = 1
  AND last_sequence = $16 - 1
  AND last_event_digest IS NOT DISTINCT FROM $17;

COMMIT;

-- Transaction 3B: KEY_READ -> TRANSPORT_CREATED.
BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'TRANSPORT_CREATED'
WHERE lease.lease_id = $7
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND lease.state = 'KEY_READ'
  AND lease.emergency_epoch = $9
  AND lease.key_version = $10
  AND lease.revocation_version = $11
  AND lease.permission_version = $12
  AND lease.policy_version = $13
  AND $14 < lease.expires_at_ms
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
      AND $14 - worker.heartbeat_at_ms <= 15000
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

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $15, $16, $14, 'WORKER_PROGRESS', 'ALLOW',
  $7, $17, $18
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $16,
    last_event_digest = $18
WHERE singleton_id = 1
  AND last_sequence = $16 - 1
  AND last_event_digest IS NOT DISTINCT FROM $17;

COMMIT;
````
<!-- END_EXACT_SOURCE id=S014 -->

### S015. preparation\production-trust\r3-fencing-remediation\sql\40-send-authorization-issuance.sql

- Category: `B_R3F_SQL`
- Path: `preparation\production-trust\r3-fencing-remediation\sql\40-send-authorization-issuance.sql`
- Bytes: `5964`
- SHA-256: `F1C8E92DD2CB3E649D491AF7B5748FF8157F32ED3AC1881AB3EB49B0E8FC7D94`
- Description: Complete R4 fencing SQL draft

<!-- BEGIN_EXACT_SOURCE id=S015 sha256=F1C8E92DD2CB3E649D491AF7B5748FF8157F32ED3AC1881AB3EB49B0E8FC7D94 bytes=5964 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- One short-lived Send Authorization for a TRANSPORT_CREATED Lease.

BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

-- A retry for the same Lease returns the existing permit. It does not create a
-- second permit or allocate another token.
SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version,
       issued_at_ms, expires_at_ms, consumed_at_ms
FROM trust_r4_send_authorization
WHERE lease_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'SEND_AUTHORIZED'
WHERE lease.lease_id = $7
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND lease.state = 'TRANSPORT_CREATED'
  AND lease.emergency_epoch = $9
  AND lease.key_version = $10
  AND lease.revocation_version = $11
  AND lease.permission_version = $12
  AND lease.policy_version = $13
  AND $14 < lease.expires_at_ms
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
      AND $14 - worker.heartbeat_at_ms <= 15000
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

-- INSERT command tag must be exactly one row.
INSERT INTO trust_r4_send_authorization (
  send_authorization_id, state, scope_key, lease_id, capability_id,
  worker_instance_id, fencing_token, budget_reservation_id,
  emergency_epoch, key_version, revocation_version,
  permission_version, policy_version, issued_at_ms, expires_at_ms,
  consumed_at_ms
) VALUES (
  $15, 'ISSUED', $5, $7, $4,
  $6, $8, $3,
  $9, $10, $11,
  $12, $13, $14, $16,
  NULL
);

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $17, $18, $14, 'SEND_AUTHORIZED', 'ALLOW',
  $15, $19, $20
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $18,
    last_event_digest = $20
WHERE singleton_id = 1
  AND last_sequence = $18 - 1
  AND last_event_digest IS NOT DISTINCT FROM $19;

COMMIT;

-- $16 must be less than Lease expiry, Resource/Authorization budget expiry and
-- no more than five seconds after $14.
````
<!-- END_EXACT_SOURCE id=S015 -->

### S016. preparation\production-trust\r3-fencing-remediation\sql\50-send-authorization-consume.sql

- Category: `B_R3F_SQL`
- Path: `preparation\production-trust\r3-fencing-remediation\sql\50-send-authorization-consume.sql`
- Bytes: `8641`
- SHA-256: `0ACA5410F758DD2B31A6C3681D7014A2A5BF1FEB509A2CA482423AF793E7A684`
- Description: Complete R4 fencing SQL draft

<!-- BEGIN_EXACT_SOURCE id=S016 sha256=0ACA5410F758DD2B31A6C3681D7014A2A5BF1FEB509A2CA482423AF793E7A684 bytes=8641 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Final Send Authorization consumption transaction.
-- The trusted Egress component performs the network write only after COMMIT.

BEGIN ISOLATION LEVEL READ COMMITTED;

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
      AND $14 - worker.heartbeat_at_ms <= 15000
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
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8;

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

-- COMMIT linearizes the local one-use permission. It does not prove Provider
-- receipt. The trusted Egress performs one write after this commit. Any crash,
-- lost response or uncertain external result becomes SEND_OUTCOME_UNKNOWN;
-- the permit must never be replayed and the budget must not be auto-released.

-- Final Egress pre-write check. This is a fresh central read performed after
-- the permit-consumption commit and immediately before the one socket write.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $5
FOR UPDATE;

SELECT permit.send_authorization_id, permit.state AS permit_state,
       permit.scope_key, permit.lease_id, permit.capability_id,
       permit.worker_instance_id, permit.fencing_token,
       permit.emergency_epoch, permit.key_version, permit.revocation_version,
       permit.permission_version, permit.policy_version,
       permit.consumed_at_ms, permit.expires_at_ms,
       lease.state AS lease_state,
       emergency.status AS emergency_status,
       emergency.epoch AS emergency_epoch_now,
       key.state AS key_state,
       key.key_version AS key_version_now,
       key.revocation_version AS revocation_version_now
FROM trust_r4_send_authorization permit
JOIN trust_r4_execution_lease lease ON lease.lease_id = permit.lease_id
JOIN trust_r3_emergency_control emergency ON emergency.singleton_id = 1
JOIN trust_r3_identity_key key ON key.key_id = $1
WHERE permit.send_authorization_id = $15
  AND permit.state = 'CONSUMED'
  AND permit.scope_key = $5
  AND permit.worker_instance_id = $6
  AND permit.lease_id = $7
  AND permit.capability_id = $4
  AND permit.fencing_token = $8
  AND lease.state = 'SENT'
  AND emergency.status = 'NORMAL'
  AND emergency.epoch = $9
  AND key.state = 'ACTIVE'
  AND key.key_version = $10
  AND key.revocation_version = $11
  AND $20 >= permit.consumed_at_ms
  AND $20 < permit.expires_at_ms
  AND $20 < lease.expires_at_ms
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

-- The Egress component must require exactly one returned row. If central
-- authority is unavailable or this query fails, it performs no network write.
-- A takeover committed after this check can still race with the socket write.

COMMIT;
````
<!-- END_EXACT_SOURCE id=S016 -->

### S017. preparation\production-trust\r3-fencing-remediation\contracts.ts

- Category: `C_R3F_MODEL_SUPPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\contracts.ts`
- Bytes: `5758`
- SHA-256: `B50E5388C90FC3E5C5DFE746A0D13FAB8E63CC4E35B4CEE44D672D31F733C0EE`
- Description: R4 fencing contract/support

<!-- BEGIN_EXACT_SOURCE id=S017 sha256=B50E5388C90FC3E5C5DFE746A0D13FAB8E63CC4E35B4CEE44D672D31F733C0EE bytes=5758 fence=fenced -->
````typescript
import { z } from "zod";

import {
  InstantSchema,
  UuidSchema,
} from "../contracts/common";
import {
  BudgetReservationSchema,
  CapabilityBindingSchema,
  ExecutionAuthorizationSchema,
  ExecutionLeaseStateSchema,
  SendAuthorizationStateSchema,
  type ExecutionLeaseState,
} from "../r2-r3-remediation/contracts";
import { FencingScopeKeySchema } from "./scope";

export const R4_CONTRACT_VERSION = "r2-r3-fencing-remediation-v1";

const IdentifierSchema = z.string().min(1).max(200).trim();
const SafeIntegerSchema = z.number().int().nonnegative().max(
  Number.MAX_SAFE_INTEGER,
);
const PositiveTokenSchema = SafeIntegerSchema.refine((value) => value > 0);

export const R4FailureCodeSchema = z.enum([
  "RESOURCE_SCOPE_MISMATCH",
  "RESOURCE_FLOOR_NOT_FOUND",
  "RESOURCE_FLOOR_CONFLICT",
  "FENCING_TOKEN_STALE",
  "FENCING_TOKEN_NOT_MONOTONIC",
  "WORKER_NOT_CURRENT",
  "LEASE_NOT_CURRENT",
  "WORKER_NOT_ACTIVE",
  "LEASE_STATE_INVALID",
  "LEASE_EXPIRED",
  "SEND_AUTHORIZATION_INVALID",
  "SEND_AUTHORIZATION_EXPIRED",
  "SEND_AUTHORIZATION_REPLAYED",
  "EMERGENCY_STOP_ACTIVE",
  "EMERGENCY_EPOCH_MISMATCH",
  "KEY_REVOKED",
  "KEY_VERSION_MISMATCH",
  "BUDGET_RESERVATION_CONFLICT",
  "BUDGET_RESERVATION_EXPIRED",
  "ROW_COUNT_CONFLICT",
  "AUTHORITY_UNAVAILABLE",
  "COMMIT_OUTCOME_UNKNOWN",
  "SEND_OUTCOME_UNKNOWN",
]);

export type R4FailureCode = z.infer<typeof R4FailureCodeSchema>;
export type R4Result<T> =
  | Readonly<{ ok: true; value: T }>
  | Readonly<{ ok: false; code: R4FailureCode }>;

export function ok<T>(value: T): R4Result<T> {
  return Object.freeze({ ok: true, value });
}

export function fail<T = never>(code: R4FailureCode): R4Result<T> {
  return Object.freeze({ ok: false, code });
}

export function requireExactlyOne(affectedRows: number): R4Result<true> {
  return affectedRows === 1 ? ok(true as const) : fail("ROW_COUNT_CONFLICT");
}

export const ResourceFencingFloorSchema = z.strictObject({
  schemaVersion: z.literal("r3-resource-fencing-floor-v1"),
  scopeKey: FencingScopeKeySchema,
  currentFencingToken: SafeIntegerSchema,
  currentWorkerId: UuidSchema.nullable(),
  currentLeaseId: UuidSchema.nullable(),
  currentCapabilityId: UuidSchema.nullable(),
  version: z.number().int().positive(),
  state: z.enum(["ACTIVE", "REVOKED"]),
  updatedAt: InstantSchema,
});

export const WorkerRegistrationSchema = z.strictObject({
  schemaVersion: z.literal("r3-fencing-worker-registration-v1"),
  workerInstanceId: UuidSchema,
  state: z.enum(["ACTIVE", "DRAINING", "REVOKED"]),
  heartbeatAt: InstantSchema,
  lastIssuedToken: SafeIntegerSchema,
  updatedAt: InstantSchema,
});

export const FencingAllocationSchema = z.strictObject({
  schemaVersion: z.literal("r3-fencing-allocation-v1"),
  scopeKey: FencingScopeKeySchema,
  fencingToken: PositiveTokenSchema,
  workerInstanceId: UuidSchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  floorVersion: z.number().int().positive(),
  allocatedAt: InstantSchema,
});

export const ExecutionLeaseSchema = z.strictObject({
  schemaVersion: z.literal("r3-fencing-execution-lease-v1"),
  leaseId: UuidSchema,
  scopeKey: FencingScopeKeySchema,
  capabilityId: UuidSchema,
  executionAuthorizationId: UuidSchema,
  budgetReservationId: UuidSchema,
  workerInstanceId: UuidSchema,
  fencingToken: PositiveTokenSchema,
  state: ExecutionLeaseStateSchema,
  issuedAt: InstantSchema,
  expiresAt: InstantSchema,
  emergencyEpoch: z.number().int().nonnegative(),
  keyVersion: z.number().int().positive(),
  revocationVersion: z.number().int().nonnegative(),
  permissionVersion: z.number().int().positive(),
  policyVersion: IdentifierSchema,
});

export const SendAuthorizationSchema = z.strictObject({
  schemaVersion: z.literal("r3-fencing-send-authorization-v1"),
  sendAuthorizationId: UuidSchema,
  state: SendAuthorizationStateSchema,
  scopeKey: FencingScopeKeySchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  workerInstanceId: UuidSchema,
  fencingToken: PositiveTokenSchema,
  budgetReservationId: UuidSchema,
  emergencyEpoch: z.number().int().nonnegative(),
  keyVersion: z.number().int().positive(),
  revocationVersion: z.number().int().nonnegative(),
  permissionVersion: z.number().int().positive(),
  policyVersion: IdentifierSchema,
  issuedAt: InstantSchema,
  expiresAt: InstantSchema,
  consumedAt: InstantSchema.nullable(),
});

export const ResourceFenceExpectationSchema = z.strictObject({
  scopeKey: FencingScopeKeySchema,
  fencingToken: PositiveTokenSchema,
  workerInstanceId: UuidSchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
});

export const EgressCheckInputSchema = z.strictObject({
  scopeKey: FencingScopeKeySchema,
  fencingToken: PositiveTokenSchema,
  workerInstanceId: UuidSchema,
  leaseId: UuidSchema,
  capabilityId: UuidSchema,
  sendAuthorizationId: UuidSchema,
  emergencyEpoch: z.number().int().nonnegative(),
  keyVersion: z.number().int().positive(),
  revocationVersion: z.number().int().nonnegative(),
  now: InstantSchema,
});

export type ResourceFencingFloor = z.infer<
  typeof ResourceFencingFloorSchema
>;
export type WorkerRegistration = z.infer<typeof WorkerRegistrationSchema>;
export type FencingAllocation = z.infer<typeof FencingAllocationSchema>;
export type ExecutionLease = z.infer<typeof ExecutionLeaseSchema>;
export type SendAuthorization = z.infer<typeof SendAuthorizationSchema>;
export type ResourceFenceExpectation = z.infer<
  typeof ResourceFenceExpectationSchema
>;
export type EgressCheckInput = z.infer<typeof EgressCheckInputSchema>;

export type R4ExecutionLeaseState = ExecutionLeaseState;
export {
  BudgetReservationSchema,
  CapabilityBindingSchema,
  ExecutionAuthorizationSchema,
  ExecutionLeaseStateSchema,
  SendAuthorizationStateSchema,
};
````
<!-- END_EXACT_SOURCE id=S017 -->

### S018. preparation\production-trust\r3-fencing-remediation\lock-order.ts

- Category: `C_R3F_MODEL_SUPPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\lock-order.ts`
- Bytes: `2228`
- SHA-256: `B203CC3BDA846BDD3BFA423D1C30659E5DE0E285792ACD1724122BD933207C64`
- Description: R4 fencing contract/support

<!-- BEGIN_EXACT_SOURCE id=S018 sha256=B203CC3BDA846BDD3BFA423D1C30659E5DE0E285792ACD1724122BD933207C64 bytes=2228 fence=fenced -->
````typescript
import { z } from "zod";

import {
  fail,
  ok,
  type R4Result,
} from "./contracts";

export const R4_LOCK_ORDER = Object.freeze([
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
  "AUDIT_SEQUENCE",
] as const);

export type R4LockDomain = typeof R4_LOCK_ORDER[number];

export function validateR4LockOrder(
  acquisitions: readonly unknown[],
): R4Result<readonly R4LockDomain[]> {
  const schema = z.array(z.strictObject({
    domain: z.enum(R4_LOCK_ORDER),
    acquiredAt: z.number().int().nonnegative(),
  }));
  const parsed = schema.safeParse(acquisitions);
  if (!parsed.success) return fail("ROW_COUNT_CONFLICT");
  let previous = -1;
  const domains: R4LockDomain[] = [];
  for (const item of parsed.data) {
    const index = R4_LOCK_ORDER.indexOf(item.domain);
    if (index < previous) return fail("ROW_COUNT_CONFLICT");
    previous = index;
    domains.push(item.domain);
  }
  return ok(Object.freeze(domains));
}

export class R4RetryableTransactionError extends Error {
  constructor(
    readonly code:
      | "DEADLOCK_DETECTED"
      | "SERIALIZATION_FAILURE"
      | "TRANSIENT_CONNECTION_FAILURE",
  ) {
    super(code);
    this.name = "R4RetryableTransactionError";
  }
}

export async function retryR4Transaction<T>(input: {
  maxAttempts: number;
  externalAttemptStarted: boolean;
  run: (attempt: number) => Promise<T>;
}): Promise<R4Result<T>> {
  if (input.externalAttemptStarted) return fail("SEND_OUTCOME_UNKNOWN");
  if (
    !Number.isInteger(input.maxAttempts)
    || input.maxAttempts < 1
    || input.maxAttempts > 3
  ) {
    return fail("COMMIT_OUTCOME_UNKNOWN");
  }
  for (let attempt = 1; attempt <= input.maxAttempts; attempt += 1) {
    try {
      return ok(await input.run(attempt));
    } catch (error) {
      if (
        !(error instanceof R4RetryableTransactionError)
        || attempt === input.maxAttempts
      ) {
        return fail("COMMIT_OUTCOME_UNKNOWN");
      }
    }
  }
  return fail("COMMIT_OUTCOME_UNKNOWN");
}
````
<!-- END_EXACT_SOURCE id=S018 -->

### S019. preparation\production-trust\r3-fencing-remediation\scope.ts

- Category: `C_R3F_MODEL_SUPPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\scope.ts`
- Bytes: `1743`
- SHA-256: `04B4E4FBBB246FC05EFC6B6894806C32B38F559674D87B0B7B0C6E5EADC31BEF`
- Description: R4 fencing contract/support

<!-- BEGIN_EXACT_SOURCE id=S019 sha256=04B4E4FBBB246FC05EFC6B6894806C32B38F559674D87B0B7B0C6E5EADC31BEF bytes=1743 fence=fenced -->
````typescript
import { createHash } from "node:crypto";

import { z } from "zod";

import {
  Sha256Schema,
  UuidSchema,
} from "../contracts/common";

export const FENCING_SCOPE_DOMAIN = "r3-fencing-resource-scope-v1";

export const FencingScopeKeySchema = z.string().regex(
  /^fence-scope-v1:sha256:[a-f0-9]{64}$/u,
);

export const FencingScopeInputSchema = z.strictObject({
  providerKind: z.literal("fetch"),
  purpose: z.literal("fetch_only"),
  organizationId: UuidSchema,
  targetDigest: Sha256Schema,
});

export type FencingScopeKey = z.infer<typeof FencingScopeKeySchema>;
export type FencingScopeInput = z.infer<typeof FencingScopeInputSchema>;

function canonical(value: unknown): string {
  if (Array.isArray(value)) return `[${value.map(canonical).join(",")}]`;
  if (value !== null && typeof value === "object") {
    return `{${Object.entries(value as Record<string, unknown>)
      .sort(([left], [right]) => left < right ? -1 : left > right ? 1 : 0)
      .map(([key, child]) => `${JSON.stringify(key)}:${canonical(child)}`)
      .join(",")}}`;
  }
  return JSON.stringify(value);
}

/**
 * The resource is organization-scoped Provider target identity:
 *   providerKind + purpose + organizationId + targetDigest.
 *
 * Capability, Lease and Approval IDs are deliberately excluded. A replacement
 * Worker/Lease for the same protected resource must advance the same floor.
 */
export function deriveFencingScopeKey(rawInput: unknown): FencingScopeKey {
  const input = FencingScopeInputSchema.parse(rawInput);
  const digest = createHash("sha256")
    .update(canonical({
      domain: FENCING_SCOPE_DOMAIN,
      ...input,
    }), "utf8")
    .digest("hex");
  return FencingScopeKeySchema.parse(`fence-scope-v1:sha256:${digest}`);
}
````
<!-- END_EXACT_SOURCE id=S019 -->

### S020. preparation\production-trust\r3-fencing-remediation\vitest.config.ts

- Category: `C_R3F_MODEL_SUPPORT`
- Path: `preparation\production-trust\r3-fencing-remediation\vitest.config.ts`
- Bytes: `223`
- SHA-256: `3498ED7EA917D283C253A19BE5C04FEA632664E3E1427B46FFFE1109A0F12FF0`
- Description: R4 fencing contract/support

<!-- BEGIN_EXACT_SOURCE id=S020 sha256=3498ED7EA917D283C253A19BE5C04FEA632664E3E1427B46FFFE1109A0F12FF0 bytes=223 fence=fenced -->
````typescript
import { defineConfig } from "vitest/config";

export default defineConfig({
  test: {
    environment: "node",
    include: [
      "preparation/production-trust/r3-fencing-remediation/tests/**/*.test.ts",
    ],
  },
});
````
<!-- END_EXACT_SOURCE id=S020 -->

### S021. preparation\production-trust\r3-fencing-remediation\models\execution-boundary.ts

- Category: `C_R3F_MODEL`
- Path: `preparation\production-trust\r3-fencing-remediation\models\execution-boundary.ts`
- Bytes: `10815`
- SHA-256: `0821E49639C34B4233FE99A691E10EEADB262AF966BE11E88E2C8F189623B7AE`
- Description: Complete offline fencing model

<!-- BEGIN_EXACT_SOURCE id=S021 sha256=0821E49639C34B4233FE99A691E10EEADB262AF966BE11E88E2C8F189623B7AE bytes=10815 fence=fenced -->
````typescript
import {
  SendAuthorizationSchema,
  fail,
  ok,
  requireExactlyOne,
  type ExecutionLease,
  type R4Result,
  type ResourceFenceExpectation,
  type SendAuthorization,
} from "../contracts";
import { OfflinePersistentFencingFloor } from "./fencing-floor";

export type BoundaryContext = Readonly<{
  now: number;
  emergencyStatus: "NORMAL" | "DRAINING" | "STOPPED" | "RECOVERY_PENDING";
  emergencyEpoch: number;
  keyState: "ACTIVE" | "REVOKED" | "EXPIRED" | "RETIRED";
  keyVersion: number;
  revocationVersion: number;
  budgetState: "RESERVED" | "COMMITTED" | "RELEASED_BEFORE_SEND" | "UNKNOWN";
  budgetExpiresAt: number;
}>;

type PermitRecord = Readonly<{
  permit: SendAuthorization;
  attemptStarted: boolean;
}>;

/**
 * OFFLINE_REFERENCE_MODEL.
 * Every authorization decision reads the current resource floor. Worker
 * Registration is checked for liveness only.
 */
export class OfflineExecutionBoundary {
  private readonly permits = new Map<string, PermitRecord>();
  private readonly permitByLease = new Map<string, string>();
  private failNextAudit = false;

  constructor(private readonly fencing: OfflinePersistentFencingFloor) {}

  setNextAuditFailure(): void {
    this.failNextAudit = true;
  }

  progressLease(input: {
    expectation: ResourceFenceExpectation;
    next: "KEY_READ" | "TRANSPORT_CREATED";
    context: BoundaryContext;
    rowCounts: Readonly<{ lease: number; audit: number }>;
  }): R4Result<ExecutionLease> {
    const rows = this.checkRows(input.rowCounts);
    if (!rows.ok) return rows;
    if (this.failNextAudit) {
      this.failNextAudit = false;
      return fail("ROW_COUNT_CONFLICT");
    }
    const current = this.fencing.validateCurrent({
      expectation: input.expectation,
      now: input.context.now,
    });
    if (!current.ok) return current;
    const allowedFrom = input.next === "KEY_READ"
      ? "ISSUED"
      : "KEY_READ";
    if (current.value.lease.state !== allowedFrom) {
      return fail("LEASE_STATE_INVALID");
    }
    const mutable = this.validateMutableContext(current.value.lease, input.context);
    if (!mutable.ok) return mutable;
    return this.fencing.transitionCurrentLease({
      expectation: input.expectation,
      next: input.next,
      rowCount: input.rowCounts.lease,
      now: input.context.now,
      emergencyStatus: input.context.emergencyStatus,
      emergencyEpoch: input.context.emergencyEpoch,
      keyState: input.context.keyState,
      keyVersion: input.context.keyVersion,
      revocationVersion: input.context.revocationVersion,
      budgetState: input.context.budgetState,
      budgetExpiresAt: input.context.budgetExpiresAt,
    });
  }

  issuePermit(input: {
    expectation: ResourceFenceExpectation;
    permitId: string;
    ttlMs: number;
    context: BoundaryContext;
    rowCounts: Readonly<{ lease: number; permit: number; audit: number }>;
  }): R4Result<SendAuthorization> {
    const rows = this.checkRows(input.rowCounts);
    if (!rows.ok) return rows;
    const existingId = this.permitByLease.get(input.expectation.leaseId);
    if (existingId) {
      const existing = this.permits.get(existingId);
      if (existing?.permit.state === "ISSUED") {
        const current = this.fencing.validateCurrent({
          expectation: input.expectation,
          now: input.context.now,
        });
        if (!current.ok) return current;
        const mutable = this.validateMutableContext(
          current.value.lease,
          input.context,
        );
        return mutable.ok ? ok(existing.permit) : mutable;
      }
      return fail("SEND_AUTHORIZATION_REPLAYED");
    }
    if (this.failNextAudit) {
      this.failNextAudit = false;
      return fail("ROW_COUNT_CONFLICT");
    }
    if (
      !Number.isSafeInteger(input.ttlMs)
      || input.ttlMs <= 0
      || input.ttlMs > 5_000
    ) {
      return fail("SEND_AUTHORIZATION_INVALID");
    }
    const current = this.fencing.validateCurrent({
      expectation: input.expectation,
      now: input.context.now,
    });
    if (!current.ok) return current;
    if (current.value.lease.state !== "TRANSPORT_CREATED") {
      return fail("LEASE_STATE_INVALID");
    }
    const mutable = this.validateMutableContext(current.value.lease, input.context);
    if (!mutable.ok) return mutable;
    const permit = SendAuthorizationSchema.parse({
      schemaVersion: "r3-fencing-send-authorization-v1",
      sendAuthorizationId: input.permitId,
      state: "ISSUED",
      scopeKey: current.value.lease.scopeKey,
      leaseId: current.value.lease.leaseId,
      capabilityId: current.value.lease.capabilityId,
      workerInstanceId: current.value.lease.workerInstanceId,
      fencingToken: current.value.lease.fencingToken,
      budgetReservationId: current.value.lease.budgetReservationId,
      emergencyEpoch: current.value.lease.emergencyEpoch,
      keyVersion: current.value.lease.keyVersion,
      revocationVersion: current.value.lease.revocationVersion,
      permissionVersion: current.value.lease.permissionVersion,
      policyVersion: current.value.lease.policyVersion,
      issuedAt: input.context.now,
      expiresAt: Math.min(
        current.value.lease.expiresAt,
        input.context.budgetExpiresAt,
        input.context.now + input.ttlMs,
      ),
      consumedAt: null,
    });
    const advanced = this.fencing.transitionCurrentLease({
      expectation: input.expectation,
      next: "SEND_AUTHORIZED",
      rowCount: input.rowCounts.lease,
      now: input.context.now,
      emergencyStatus: input.context.emergencyStatus,
      emergencyEpoch: input.context.emergencyEpoch,
      keyState: input.context.keyState,
      keyVersion: input.context.keyVersion,
      revocationVersion: input.context.revocationVersion,
      budgetState: input.context.budgetState,
      budgetExpiresAt: input.context.budgetExpiresAt,
    });
    if (!advanced.ok) return advanced;
    this.permits.set(permit.sendAuthorizationId, Object.freeze({
      permit,
      attemptStarted: false,
    }));
    this.permitByLease.set(permit.leaseId, permit.sendAuthorizationId);
    return ok(permit);
  }

  consumePermit(input: {
    permitId: string;
    expectation: ResourceFenceExpectation;
    context: BoundaryContext;
    rowCounts: Readonly<{
      permit: number;
      lease: number;
      budget: number;
      audit: number;
    }>;
  }): R4Result<Readonly<{
    permit: SendAuthorization;
    lease: ExecutionLease;
    externalOutcome: "PENDING";
  }>> {
    const rows = this.checkRows(input.rowCounts);
    if (!rows.ok) return rows;
    if (this.failNextAudit) {
      this.failNextAudit = false;
      return fail("ROW_COUNT_CONFLICT");
    }
    const record = this.permits.get(input.permitId);
    if (!record) return fail("SEND_AUTHORIZATION_INVALID");
    if (record.permit.state !== "ISSUED") {
      return fail("SEND_AUTHORIZATION_REPLAYED");
    }
    if (input.context.now >= record.permit.expiresAt) {
      return fail("SEND_AUTHORIZATION_EXPIRED");
    }
    const current = this.fencing.validateCurrent({
      expectation: input.expectation,
      now: input.context.now,
    });
    if (!current.ok) return current;
    if (current.value.lease.state !== "SEND_AUTHORIZED") {
      return fail("LEASE_STATE_INVALID");
    }
    const mutable = this.validateMutableContext(current.value.lease, input.context);
    if (!mutable.ok) return mutable;
    if (
      record.permit.scopeKey !== input.expectation.scopeKey
      || record.permit.leaseId !== input.expectation.leaseId
      || record.permit.capabilityId !== input.expectation.capabilityId
      || record.permit.workerInstanceId !== input.expectation.workerInstanceId
      || record.permit.fencingToken !== input.expectation.fencingToken
    ) {
      return fail("SEND_AUTHORIZATION_INVALID");
    }
    const consumed = SendAuthorizationSchema.parse({
      ...record.permit,
      state: "CONSUMED",
      consumedAt: input.context.now,
    });
    const lease = this.fencing.transitionCurrentLease({
      expectation: input.expectation,
      next: "SENT",
      rowCount: input.rowCounts.lease,
      now: input.context.now,
      emergencyStatus: input.context.emergencyStatus,
      emergencyEpoch: input.context.emergencyEpoch,
      keyState: input.context.keyState,
      keyVersion: input.context.keyVersion,
      revocationVersion: input.context.revocationVersion,
      budgetState: input.context.budgetState,
      budgetExpiresAt: input.context.budgetExpiresAt,
    });
    if (!lease.ok) return lease;
    this.permits.set(consumed.sendAuthorizationId, Object.freeze({
      permit: consumed,
      attemptStarted: true,
    }));
    return ok(Object.freeze({
      permit: consumed,
      lease: lease.value,
      externalOutcome: "PENDING" as const,
    }));
  }

  authorizeEgress(input: {
    permitId: string;
    expectation: ResourceFenceExpectation;
    context: BoundaryContext;
    rowCount: number;
  }): R4Result<Readonly<{ networkWriteAllowed: true }>> {
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    const record = this.permits.get(input.permitId);
    if (
      !record
      || record.permit.state !== "CONSUMED"
      || !record.attemptStarted
    ) {
      return fail("SEND_AUTHORIZATION_INVALID");
    }
    const current = this.fencing.validateCurrent({
      expectation: input.expectation,
      now: input.context.now,
    });
    if (!current.ok) return current;
    if (current.value.lease.state !== "SENT") {
      return fail("LEASE_STATE_INVALID");
    }
    const mutable = this.validateMutableContext(current.value.lease, input.context);
    if (!mutable.ok) return mutable;
    return ok(Object.freeze({ networkWriteAllowed: true as const }));
  }

  permit(permitId: string): SendAuthorization | null {
    return this.permits.get(permitId)?.permit ?? null;
  }

  private validateMutableContext(
    lease: ExecutionLease,
    context: BoundaryContext,
  ): R4Result<true> {
    if (
      context.emergencyStatus !== "NORMAL"
      || context.emergencyEpoch !== lease.emergencyEpoch
    ) {
      return fail("EMERGENCY_STOP_ACTIVE");
    }
    if (
      context.keyState !== "ACTIVE"
      || context.keyVersion !== lease.keyVersion
      || context.revocationVersion !== lease.revocationVersion
    ) {
      return fail("KEY_REVOKED");
    }
    if (
      context.budgetState !== "RESERVED"
      || context.now >= context.budgetExpiresAt
    ) {
      return fail("BUDGET_RESERVATION_CONFLICT");
    }
    return ok(true as const);
  }

  private checkRows(
    rowCounts: Readonly<Record<string, number>>,
  ): R4Result<true> {
    for (const value of Object.values(rowCounts)) {
      const checked = requireExactlyOne(value);
      if (!checked.ok) return checked;
    }
    return ok(true as const);
  }
}
````
<!-- END_EXACT_SOURCE id=S021 -->

### S022. preparation\production-trust\r3-fencing-remediation\models\fencing-floor.ts

- Category: `C_R3F_MODEL`
- Path: `preparation\production-trust\r3-fencing-remediation\models\fencing-floor.ts`
- Bytes: `13954`
- SHA-256: `83F085134850F4765ABAD9D5D2451B23684E60ABB3202A762B571D5BAA7A76DB`
- Description: Complete offline fencing model

<!-- BEGIN_EXACT_SOURCE id=S022 sha256=83F085134850F4765ABAD9D5D2451B23684E60ABB3202A762B571D5BAA7A76DB bytes=13954 fence=fenced -->
````typescript
import {
  ExecutionLeaseSchema,
  ResourceFencingFloorSchema,
  WorkerRegistrationSchema,
  fail,
  ok,
  requireExactlyOne,
  type ExecutionLease,
  type R4ExecutionLeaseState,
  type FencingAllocation,
  type R4Result,
  type ResourceFenceExpectation,
  type ResourceFencingFloor,
  type WorkerRegistration,
} from "../contracts";
import { FencingScopeKeySchema } from "../scope";

export class FencingCommitOutcomeUnknownError extends Error {
  constructor(readonly leaseId: string) {
    super("COMMIT_OUTCOME_UNKNOWN");
    this.name = "FencingCommitOutcomeUnknownError";
  }
}

type SharedState = {
  nextToken: number;
  authorityAvailable: boolean;
  floors: Map<string, ResourceFencingFloor>;
  workers: Map<string, WorkerRegistration>;
  leases: Map<string, ExecutionLease>;
  leaseByCapability: Map<string, string>;
  auditEvents: string[];
};

export type TakeoverInput = Readonly<{
  scopeKey: string;
  workerInstanceId: string;
  leaseId: string;
  capabilityId: string;
  executionAuthorizationId: string;
  budgetReservationId: string;
  now: number;
  expiresAt: number;
  emergencyEpoch: number;
  keyVersion: number;
  revocationVersion: number;
  permissionVersion: number;
  policyVersion: string;
  rowCounts: Readonly<{
    floor: number;
    worker: number;
    lease: number;
    audit: number;
  }>;
  failAudit?: boolean;
}>;

/**
 * OFFLINE_REFERENCE_MODEL.
 * The maps model persistent database rows. Token allocation, resource floor
 * update, Worker diagnostic metadata, Lease insertion and audit are one
 * synchronous linearization point.
 */
export class OfflinePersistentFencingFloor {
  private readonly shared: SharedState;

  constructor(input?: {
    initialToken?: number;
    shared?: OfflinePersistentFencingFloor;
  }) {
    this.shared = input?.shared?.shared ?? {
      nextToken: input?.initialToken ?? 1,
      authorityAvailable: true,
      floors: new Map(),
      workers: new Map(),
      leases: new Map(),
      leaseByCapability: new Map(),
      auditEvents: [],
    };
  }

  connect(): OfflinePersistentFencingFloor {
    return new OfflinePersistentFencingFloor({ shared: this });
  }

  setAuthorityAvailable(available: boolean): void {
    this.shared.authorityAvailable = available;
  }

  registerWorker(input: {
    workerInstanceId: string;
    now: number;
  }): R4Result<WorkerRegistration> {
    const existing = this.shared.workers.get(input.workerInstanceId);
    if (existing && existing.state !== "ACTIVE") {
      return fail("WORKER_NOT_ACTIVE");
    }
    const worker = WorkerRegistrationSchema.parse({
      schemaVersion: "r3-fencing-worker-registration-v1",
      workerInstanceId: input.workerInstanceId,
      state: "ACTIVE",
      heartbeatAt: input.now,
      lastIssuedToken: existing?.lastIssuedToken ?? 0,
      updatedAt: input.now,
    });
    this.shared.workers.set(worker.workerInstanceId, worker);
    return ok(worker);
  }

  setWorkerState(input: {
    workerInstanceId: string;
    state: "ACTIVE" | "DRAINING" | "REVOKED";
    now: number;
  }): R4Result<WorkerRegistration> {
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker) return fail("WORKER_NOT_ACTIVE");
    const updated = WorkerRegistrationSchema.parse({
      ...worker,
      state: input.state,
      updatedAt: input.now,
    });
    this.shared.workers.set(updated.workerInstanceId, updated);
    return ok(updated);
  }

  heartbeat(input: {
    workerInstanceId: string;
    now: number;
  }): R4Result<WorkerRegistration> {
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker || worker.state !== "ACTIVE") {
      return fail("WORKER_NOT_ACTIVE");
    }
    const updated = WorkerRegistrationSchema.parse({
      ...worker,
      heartbeatAt: input.now,
      updatedAt: input.now,
    });
    this.shared.workers.set(updated.workerInstanceId, updated);
    return ok(updated);
  }

  takeover(input: TakeoverInput): R4Result<ExecutionLease> {
    if (!this.shared.authorityAvailable) {
      return fail("AUTHORITY_UNAVAILABLE");
    }
    if (!FencingScopeKeySchema.safeParse(input.scopeKey).success) {
      return fail("RESOURCE_SCOPE_MISMATCH");
    }
    if (
      !Number.isSafeInteger(input.now)
      || !Number.isSafeInteger(input.expiresAt)
      || input.expiresAt <= input.now
    ) {
      return fail("LEASE_STATE_INVALID");
    }
    for (const rowCount of Object.values(input.rowCounts)) {
      const rows = requireExactlyOne(rowCount);
      if (!rows.ok) return rows;
    }
    if (input.failAudit) return fail("ROW_COUNT_CONFLICT");

    const idempotentLeaseId = this.shared.leaseByCapability.get(
      input.capabilityId,
    );
    if (idempotentLeaseId) {
      const existing = this.shared.leases.get(idempotentLeaseId);
      if (
        existing
        && existing.leaseId === input.leaseId
        && existing.scopeKey === input.scopeKey
        && existing.workerInstanceId === input.workerInstanceId
      ) {
        return ok(existing);
      }
      return fail("LEASE_NOT_CURRENT");
    }
    if (this.shared.leases.has(input.leaseId)) {
      return fail("LEASE_NOT_CURRENT");
    }

    const currentFloor = this.shared.floors.get(input.scopeKey);
    if (currentFloor && currentFloor.state !== "ACTIVE") {
      return fail("RESOURCE_FLOOR_CONFLICT");
    }
    const fencingToken = this.shared.nextToken;
    if (
      !Number.isSafeInteger(fencingToken)
      || currentFloor?.currentFencingToken !== undefined
        && fencingToken <= currentFloor.currentFencingToken
    ) {
      return fail("FENCING_TOKEN_NOT_MONOTONIC");
    }
    const existingWorker = this.shared.workers.get(input.workerInstanceId);
    if (
      existingWorker
      && (
        existingWorker.state !== "ACTIVE"
        || input.now < existingWorker.heartbeatAt
        || input.now - existingWorker.heartbeatAt > 15_000
      )
    ) {
      return fail("WORKER_NOT_ACTIVE");
    }

    const floor = ResourceFencingFloorSchema.parse({
      schemaVersion: "r3-resource-fencing-floor-v1",
      scopeKey: input.scopeKey,
      currentFencingToken: fencingToken,
      currentWorkerId: input.workerInstanceId,
      currentLeaseId: input.leaseId,
      currentCapabilityId: input.capabilityId,
      version: (currentFloor?.version ?? 1) + 1,
      state: "ACTIVE",
      updatedAt: input.now,
    });
    const worker = WorkerRegistrationSchema.parse({
      schemaVersion: "r3-fencing-worker-registration-v1",
      workerInstanceId: input.workerInstanceId,
      state: "ACTIVE",
      heartbeatAt: input.now,
      lastIssuedToken: fencingToken,
      updatedAt: input.now,
    });
    const lease = ExecutionLeaseSchema.parse({
      schemaVersion: "r3-fencing-execution-lease-v1",
      leaseId: input.leaseId,
      scopeKey: input.scopeKey,
      capabilityId: input.capabilityId,
      executionAuthorizationId: input.executionAuthorizationId,
      budgetReservationId: input.budgetReservationId,
      workerInstanceId: input.workerInstanceId,
      fencingToken,
      state: "ISSUED",
      issuedAt: input.now,
      expiresAt: input.expiresAt,
      emergencyEpoch: input.emergencyEpoch,
      keyVersion: input.keyVersion,
      revocationVersion: input.revocationVersion,
      permissionVersion: input.permissionVersion,
      policyVersion: input.policyVersion,
    });

    this.shared.nextToken += 1;
    this.shared.floors.set(input.scopeKey, floor);
    this.shared.workers.set(input.workerInstanceId, worker);
    this.shared.leases.set(input.leaseId, lease);
    this.shared.leaseByCapability.set(input.capabilityId, input.leaseId);
    this.shared.auditEvents.push(`LEASE_ISSUED:${input.leaseId}`);
    return ok(lease);
  }

  takeoverWithUnknownCommit(input: TakeoverInput): never {
    const result = this.takeover(input);
    if (!result.ok) throw new Error(result.code);
    throw new FencingCommitOutcomeUnknownError(input.leaseId);
  }

  recoverTakeover(input: {
    leaseId: string;
    expectation: ResourceFenceExpectation;
  }): R4Result<ExecutionLease> {
    const lease = this.shared.leases.get(input.leaseId);
    const floor = this.shared.floors.get(input.expectation.scopeKey);
    if (
      !lease
      || !floor
      || lease.scopeKey !== input.expectation.scopeKey
      || lease.workerInstanceId !== input.expectation.workerInstanceId
      || lease.capabilityId !== input.expectation.capabilityId
      || lease.fencingToken !== input.expectation.fencingToken
      || floor.currentLeaseId !== lease.leaseId
      || floor.currentFencingToken !== lease.fencingToken
    ) {
      return fail("COMMIT_OUTCOME_UNKNOWN");
    }
    return ok(lease);
  }

  validateCurrent(input: {
    expectation: ResourceFenceExpectation;
    now: number;
    requireWorkerHeartbeat?: boolean;
  }): R4Result<{
    floor: ResourceFencingFloor;
    worker: WorkerRegistration;
    lease: ExecutionLease;
  }> {
    if (!this.shared.authorityAvailable) {
      return fail("AUTHORITY_UNAVAILABLE");
    }
    const floor = this.shared.floors.get(input.expectation.scopeKey);
    const lease = this.shared.leases.get(input.expectation.leaseId);
    const worker = this.shared.workers.get(input.expectation.workerInstanceId);
    if (!floor || !lease || !worker) return fail("RESOURCE_FLOOR_NOT_FOUND");
    if (
      floor.scopeKey !== input.expectation.scopeKey
      || lease.scopeKey !== input.expectation.scopeKey
      || lease.capabilityId !== input.expectation.capabilityId
    ) {
      return fail("RESOURCE_SCOPE_MISMATCH");
    }
    if (
      floor.currentFencingToken !== input.expectation.fencingToken
      || lease.fencingToken !== input.expectation.fencingToken
    ) {
      return fail("FENCING_TOKEN_STALE");
    }
    if (
      floor.currentWorkerId !== input.expectation.workerInstanceId
      || lease.workerInstanceId !== input.expectation.workerInstanceId
    ) {
      return fail("WORKER_NOT_CURRENT");
    }
    if (
      floor.currentLeaseId !== input.expectation.leaseId
      || floor.currentCapabilityId !== input.expectation.capabilityId
    ) {
      return fail("LEASE_NOT_CURRENT");
    }
    if (input.now >= lease.expiresAt) return fail("LEASE_EXPIRED");
    if (
      worker.state !== "ACTIVE"
      || input.now < worker.heartbeatAt
      || input.requireWorkerHeartbeat !== false
        && input.now - worker.heartbeatAt > 15_000
    ) {
      return fail("WORKER_NOT_ACTIVE");
    }
    return ok(Object.freeze({ floor, worker, lease }));
  }

  transitionCurrentLease(
    input: {
      expectation: ResourceFenceExpectation;
      next: R4ExecutionLeaseState;
      rowCount: number;
      now: number;
      emergencyStatus: "NORMAL" | "DRAINING" | "STOPPED" | "RECOVERY_PENDING";
      emergencyEpoch: number;
      keyState: "ACTIVE" | "REVOKED" | "EXPIRED" | "RETIRED";
      keyVersion: number;
      revocationVersion: number;
      budgetState: "RESERVED" | "COMMITTED" | "RELEASED_BEFORE_SEND" | "UNKNOWN";
      budgetExpiresAt: number;
    },
  ): R4Result<ExecutionLease> {
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    const current = this.validateCurrent({
      expectation: input.expectation,
      now: input.now,
      requireWorkerHeartbeat: false,
    });
    if (!current.ok) return current;
    if (
      input.emergencyStatus !== "NORMAL"
      || input.emergencyEpoch !== current.value.lease.emergencyEpoch
    ) {
      return fail("EMERGENCY_STOP_ACTIVE");
    }
    if (
      input.keyState !== "ACTIVE"
      || input.keyVersion !== current.value.lease.keyVersion
      || input.revocationVersion !== current.value.lease.revocationVersion
    ) {
      return fail("KEY_REVOKED");
    }
    if (
      input.budgetState !== "RESERVED"
      || input.now >= input.budgetExpiresAt
    ) {
      return fail("BUDGET_RESERVATION_CONFLICT");
    }
    const transitions: Readonly<Record<string, readonly string[]>> = {
      ISSUED: ["KEY_READ"],
      KEY_READ: ["TRANSPORT_CREATED"],
      TRANSPORT_CREATED: ["SEND_AUTHORIZED"],
      SEND_AUTHORIZED: ["SENT"],
      SENT: ["RESPONSE_RECEIVED", "SEND_OUTCOME_UNKNOWN", "FAILED_AFTER_SEND"],
      RESPONSE_RECEIVED: ["COMPLETED"],
    };
    if (!(transitions[current.value.lease.state] ?? []).includes(input.next)) {
      return fail("LEASE_STATE_INVALID");
    }
    const updated = ExecutionLeaseSchema.parse({
      ...current.value.lease,
      state: input.next,
    });
    this.shared.leases.set(updated.leaseId, updated);
    return ok(updated);
  }

  getLease(leaseId: string): ExecutionLease | null {
    return this.shared.leases.get(leaseId) ?? null;
  }

  getWorker(workerInstanceId: string): WorkerRegistration | null {
    return this.shared.workers.get(workerInstanceId) ?? null;
  }

  getFloor(scopeKey: string): ResourceFencingFloor | null {
    return this.shared.floors.get(scopeKey) ?? null;
  }

  allocationFor(leaseId: string): FencingAllocation | null {
    const lease = this.shared.leases.get(leaseId);
    if (!lease) return null;
    const floor = this.shared.floors.get(lease.scopeKey);
    if (!floor) return null;
    return Object.freeze({
      schemaVersion: "r3-fencing-allocation-v1" as const,
      scopeKey: lease.scopeKey,
      fencingToken: lease.fencingToken,
      workerInstanceId: lease.workerInstanceId,
      leaseId: lease.leaseId,
      capabilityId: lease.capabilityId,
      floorVersion: floor.version,
      allocatedAt: lease.issuedAt,
    });
  }

  snapshot(): Readonly<{
    nextToken: number;
    authorityAvailable: boolean;
    floors: number;
    workers: number;
    leases: number;
    auditEvents: number;
  }> {
    return Object.freeze({
      nextToken: this.shared.nextToken,
      authorityAvailable: this.shared.authorityAvailable,
      floors: this.shared.floors.size,
      workers: this.shared.workers.size,
      leases: this.shared.leases.size,
      auditEvents: this.shared.auditEvents.length,
    });
  }
}
````
<!-- END_EXACT_SOURCE id=S022 -->

### S023. preparation\production-trust\r3-fencing-remediation\models\race-scenarios.ts

- Category: `C_R3F_MODEL`
- Path: `preparation\production-trust\r3-fencing-remediation\models\race-scenarios.ts`
- Bytes: `6481`
- SHA-256: `079FCF395897ED8D54B2C665A5B51AC0FBE4C6341EE9B7FE6E059B9940CF8839`
- Description: Complete offline fencing model

<!-- BEGIN_EXACT_SOURCE id=S023 sha256=079FCF395897ED8D54B2C665A5B51AC0FBE4C6341EE9B7FE6E059B9940CF8839 bytes=6481 fence=fenced -->
````typescript
import {
  ExecutionLeaseSchema,
  ResourceFencingFloorSchema,
  SendAuthorizationSchema,
  WorkerRegistrationSchema,
  fail,
  ok,
  type ExecutionLease,
  type R4Result,
  type SendAuthorization,
} from "../contracts";

export type FencingAttemptOperation =
  | "LEASE_PROGRESS"
  | "SEND_AUTHORIZATION_ISSUANCE"
  | "SEND_AUTHORIZATION_CONSUMPTION"
  | "EGRESS_WRITE";

export type FencingAttemptDecision =
  | "ALLOWED"
  | "AUTHORITY_UNAVAILABLE"
  | "RESOURCE_SCOPE_MISMATCH"
  | "FENCING_TOKEN_STALE"
  | "WORKER_NOT_CURRENT"
  | "LEASE_NOT_CURRENT"
  | "WORKER_NOT_ACTIVE"
  | "EMERGENCY_BLOCKED"
  | "KEY_BLOCKED"
  | "LEASE_EXPIRED";

export function evaluateResourceFencingAttempt(input: {
  operation: FencingAttemptOperation;
  scopeKey: string;
  floor: unknown;
  worker: unknown;
  lease: unknown;
  token: number;
  workerInstanceId: string;
  leaseId: string;
  now: number;
  authorityAvailable: boolean;
  emergencyStatus: "NORMAL" | "DRAINING" | "STOPPED" | "RECOVERY_PENDING";
  emergencyEpoch: number;
  keyActive: boolean;
  keyVersion: number;
  revocationVersion: number;
}): FencingAttemptDecision {
  if (!input.authorityAvailable) return "AUTHORITY_UNAVAILABLE";
  const floor = ResourceFencingFloorSchema.safeParse(input.floor);
  const worker = WorkerRegistrationSchema.safeParse(input.worker);
  const lease = ExecutionLeaseSchema.safeParse(input.lease);
  if (!floor.success || floor.data.state !== "ACTIVE") {
    return "RESOURCE_SCOPE_MISMATCH";
  }
  if (floor.data.scopeKey !== input.scopeKey) return "RESOURCE_SCOPE_MISMATCH";
  if (floor.data.currentFencingToken !== input.token) {
    return "FENCING_TOKEN_STALE";
  }
  if (floor.data.currentWorkerId !== input.workerInstanceId) {
    return "WORKER_NOT_CURRENT";
  }
  if (floor.data.currentLeaseId !== input.leaseId) return "LEASE_NOT_CURRENT";
  if (
    !worker.success
    || worker.data.workerInstanceId !== input.workerInstanceId
    || worker.data.state !== "ACTIVE"
    || input.now - worker.data.heartbeatAt > 15_000
  ) {
    return "WORKER_NOT_ACTIVE";
  }
  if (
    !lease.success
    || lease.data.scopeKey !== input.scopeKey
    || lease.data.workerInstanceId !== input.workerInstanceId
    || lease.data.fencingToken !== input.token
  ) {
    return "LEASE_NOT_CURRENT";
  }
  if (input.now >= lease.data.expiresAt) return "LEASE_EXPIRED";
  if (
    input.emergencyStatus !== "NORMAL"
    || input.emergencyEpoch !== lease.data.emergencyEpoch
  ) {
    return "EMERGENCY_BLOCKED";
  }
  if (
    !input.keyActive
    || input.keyVersion !== lease.data.keyVersion
    || input.revocationVersion !== lease.data.revocationVersion
  ) {
    return "KEY_BLOCKED";
  }
  return "ALLOWED";
}

export function consumePermitAgainstFloor(input: {
  permit: unknown;
  floor: unknown;
  now: number;
  authorityAvailable: boolean;
}): R4Result<{
  permit: SendAuthorization;
  writePermission: "GRANTED";
}> {
  if (!input.authorityAvailable) return fail("AUTHORITY_UNAVAILABLE");
  const permit = SendAuthorizationSchema.safeParse(input.permit);
  const floor = ResourceFencingFloorSchema.safeParse(input.floor);
  if (!permit.success || !floor.success) {
    return fail("SEND_AUTHORIZATION_INVALID");
  }
  if (permit.data.state !== "ISSUED") {
    return fail("SEND_AUTHORIZATION_REPLAYED");
  }
  if (input.now >= permit.data.expiresAt) {
    return fail("SEND_AUTHORIZATION_EXPIRED");
  }
  if (
    permit.data.scopeKey !== floor.data.scopeKey
    || permit.data.fencingToken !== floor.data.currentFencingToken
    || permit.data.workerInstanceId !== floor.data.currentWorkerId
    || permit.data.leaseId !== floor.data.currentLeaseId
    || permit.data.capabilityId !== floor.data.currentCapabilityId
  ) {
    return fail("FENCING_TOKEN_STALE");
  }
  return ok(Object.freeze({
    permit: SendAuthorizationSchema.parse({
      ...permit.data,
      state: "CONSUMED",
      consumedAt: input.now,
    }),
    writePermission: "GRANTED",
  }));
}

export type PermitRaceEvent =
  | Readonly<{ type: "TAKEOVER_COMMITTED" }>
  | Readonly<{ type: "EMERGENCY_COMMITTED" }>
  | Readonly<{ type: "KEY_REVOKED" }>
  | Readonly<{ type: "PERMIT_CONSUMED" }>
  | Readonly<{ type: "WRITE_STARTED" }>
  | Readonly<{ type: "RESPONSE_RECEIVED" }>
  | Readonly<{ type: "AUTHORITY_UNAVAILABLE" }>;

export type PermitRaceOutcome =
  | "PERMIT_DENIED_BEFORE_CONSUMPTION"
  | "CONSUMED_WRITE_BLOCKED"
  | "WRITE_STARTED_OUTCOME_UNKNOWN"
  | "WRITE_STARTED_RESPONSE_RECEIVED"
  | "AUTHORITY_UNAVAILABLE";

export function classifyPermitRace(
  events: readonly PermitRaceEvent[],
): PermitRaceOutcome {
  let invalidBeforeConsume = false;
  let invalidAfterConsume = false;
  let consumed = false;
  let authorityUnavailable = false;
  let writeStarted = false;
  let response = false;
  for (const event of events) {
    if (event.type === "AUTHORITY_UNAVAILABLE") {
      authorityUnavailable = true;
      if (!writeStarted) return "AUTHORITY_UNAVAILABLE";
    }
    if (
      event.type === "TAKEOVER_COMMITTED"
      || event.type === "EMERGENCY_COMMITTED"
      || event.type === "KEY_REVOKED"
    ) {
      if (consumed) invalidAfterConsume = true;
      else invalidBeforeConsume = true;
    }
    if (event.type === "PERMIT_CONSUMED") {
      if (invalidBeforeConsume || authorityUnavailable) continue;
      consumed = true;
    }
    if (event.type === "WRITE_STARTED") {
      if (consumed && !invalidAfterConsume && !authorityUnavailable) {
        writeStarted = true;
      }
    }
    if (event.type === "RESPONSE_RECEIVED" && writeStarted) response = true;
  }
  if (!consumed) return authorityUnavailable
    ? "AUTHORITY_UNAVAILABLE"
    : "PERMIT_DENIED_BEFORE_CONSUMPTION";
  if (!writeStarted) return "CONSUMED_WRITE_BLOCKED";
  return response
    ? "WRITE_STARTED_RESPONSE_RECEIVED"
    : "WRITE_STARTED_OUTCOME_UNKNOWN";
}

export function recoverTakeoverCommit(input: {
  persistedLease: unknown;
  expectedLeaseId: string;
  expectedWorkerInstanceId: string;
  expectedScopeKey: string;
  expectedFencingToken: number;
}): R4Result<ExecutionLease> {
  const lease = ExecutionLeaseSchema.safeParse(input.persistedLease);
  if (
    !lease.success
    || lease.data.leaseId !== input.expectedLeaseId
    || lease.data.workerInstanceId !== input.expectedWorkerInstanceId
    || lease.data.scopeKey !== input.expectedScopeKey
    || lease.data.fencingToken !== input.expectedFencingToken
  ) {
    return fail("COMMIT_OUTCOME_UNKNOWN");
  }
  return ok(lease.data);
}
````
<!-- END_EXACT_SOURCE id=S023 -->

### S024. preparation\production-trust\r3-fencing-remediation\models\sql-analyzer.ts

- Category: `C_R3F_MODEL`
- Path: `preparation\production-trust\r3-fencing-remediation\models\sql-analyzer.ts`
- Bytes: `7155`
- SHA-256: `98EB13EE3AA9F01FB72AFB9860A2AE2C15E143E0A627113EF882632258729FB5`
- Description: Complete offline fencing model

<!-- BEGIN_EXACT_SOURCE id=S024 sha256=98EB13EE3AA9F01FB72AFB9860A2AE2C15E143E0A627113EF882632258729FB5 bytes=7155 fence=fenced -->
````typescript
export type FencingSqlFinding = Readonly<{
  code: string;
  message: string;
  offset: number;
}>;

function stripCommentsPreservingOffsets(sql: string): string {
  return sql
    .replace(/\/\*[\s\S]*?\*\//gu, (comment) => " ".repeat(comment.length))
    .replace(/--[^\r\n]*/gu, (comment) => " ".repeat(comment.length));
}

function updateStatements(sql: string) {
  return [...sql.matchAll(
    /\bUPDATE\s+(trust_[a-z0-9_]+)\s+SET\s+([\s\S]*?);/giu,
  )].map((match) => {
    const body = match[2];
    const whereIndex = body.search(/\s+WHERE\s+/iu);
    return {
      table: match[1],
      setClause: whereIndex < 0 ? body : body.slice(0, whereIndex),
      whereClause: whereIndex < 0 ? "" : body.slice(whereIndex),
      offset: match.index ?? 0,
    };
  });
}

function transactionTexts(sql: string): string[] {
  return [...sql.matchAll(
    /\bBEGIN(?:\s+ISOLATION\s+LEVEL\s+[A-Z ]+)?\s*;[\s\S]*?\bCOMMIT\s*;/giu,
  )].map((match) => match[0]);
}

export function reviewResourceFencingSql(input: {
  name: string;
  text: string;
}): readonly FencingSqlFinding[] {
  const findings: FencingSqlFinding[] = [];
  const active = stripCommentsPreservingOffsets(input.text);
  const add = (code: string, message: string, offset = 0) => {
    findings.push(Object.freeze({ code, message, offset }));
  };

  const begins = (active.match(/\bBEGIN\b/giu) ?? []).length;
  const commits = (active.match(/\bCOMMIT\s*;/giu) ?? []).length;
  if (begins !== commits) add("TRANSACTION_BALANCE", "BEGIN/COMMIT mismatch");
  if (/\b(?:http|dblink|pg_net)\b/iu.test(active)) {
    add("EXTERNAL_SIDE_EFFECT", "forbidden network primitive");
  }
  if (input.name !== "00-schema.sql" && /\bfence_floor\b/iu.test(active)) {
    add(
      "WORKER_FLOOR_AUTHORITATIVE",
      "Worker registration floor must not authorize execution",
    );
  }

  for (const update of updateStatements(active)) {
    const prefix = input.text.slice(
      Math.max(0, update.offset - 220),
      update.offset,
    );
    if (!/--\s*ROW_COUNT_EXPECTATION:\s*exactly\s+1/iu.test(prefix)) {
      add(
        "ROW_COUNT_MARKER_MISSING",
        `${update.table} update lacks exactly-one marker`,
        update.offset,
      );
    }
    if (
      !/\bWHERE\b/iu.test(update.whereClause)
      || !/(scope_key|state|version|current_fencing_token|current_worker_id|current_lease_id|last_sequence|next_token)\s*=/iu
        .test(update.whereClause)
    ) {
      add(
        "MUTATION_GUARD_MISSING",
        `${update.table} update lacks binding/version guard`,
        update.offset,
      );
    }
  }

  if (input.name === "00-schema.sql") {
    for (const token of [
      "trust_r4_resource_fencing",
      "scope_key text PRIMARY KEY",
      "current_fencing_token",
      "current_worker_id",
      "current_lease_id",
      "current_capability_id",
      "trust_r4_fencing_token_control",
    ]) {
      if (!active.includes(token)) {
        add("RESOURCE_FLOOR_SCHEMA_MISSING", `missing ${token}`);
      }
    }
  }

  if (input.name === "10-worker-takeover.sql") {
    const transactions = transactionTexts(active);
    const takeover = transactions.find((tx) =>
      tx.includes("trust_r4_resource_fencing")
      && tx.includes("trust_r4_fencing_token_control")
      && tx.includes("trust_r4_execution_lease")
    );
    if (!takeover) {
      add(
        "TAKEOVER_ATOMICITY",
        "floor, token allocation and Lease must share one transaction",
      );
    }
    if (
      !/UPDATE\s+trust_r4_resource_fencing[\s\S]*current_fencing_token\s*=\s*(?:\$|allocated\.fencing_token)/iu
        .test(active)
      || !/current_worker_id\s*=\s*\$/iu.test(active)
      || !/current_lease_id\s*=\s*\$/iu.test(active)
      || !/current_capability_id\s*=\s*\$/iu.test(active)
      || !/version\s*=\s*version\s*\+\s*1/iu.test(active)
    ) {
      add(
        "TAKEOVER_FLOOR_UPDATE_INCOMPLETE",
        "takeover must persist token, Worker, Lease, Capability and version",
      );
    }
    if (
      !/INSERT\s+INTO\s+trust_r4_resource_fencing[\s\S]*ON\s+CONFLICT/iu
        .test(active)
    ) {
      add(
        "RESOURCE_INITIALIZATION_MISSING",
        "first resource floor requires conflict-safe initialization",
      );
    }
  }

  if ([
    "30-worker-progress.sql",
    "40-send-authorization-issuance.sql",
    "50-send-authorization-consume.sql",
  ].includes(input.name)) {
    if (
      !/FROM\s+trust_r4_resource_fencing[\s\S]*scope_key\s*=\s*\$[\s\S]*FOR\s+UPDATE/iu
        .test(active)
    ) {
      add(
        "RESOURCE_FLOOR_LOCK_MISSING",
        "authorization transaction must lock the resource floor by scope",
      );
    }
    if (
      !/current_fencing_token\s*=\s*\$/iu.test(active)
      || !/current_worker_id\s*=\s*\$/iu.test(active)
      || !/current_lease_id\s*=\s*\$/iu.test(active)
    ) {
      add(
        "RESOURCE_CURRENT_BINDING_MISSING",
        "must compare current token, Worker and Lease",
      );
    }
  }

  if (input.name === "30-worker-progress.sql") {
    if (!/scope_key\s*=\s*\$/iu.test(active)) {
      add("PROGRESS_SCOPE_MISSING", "progress must bind scope key");
    }
  }

  if (input.name === "40-send-authorization-issuance.sql") {
    if (
      !/state\s*=\s*'TRANSPORT_CREATED'/iu.test(active)
      || !/INSERT\s+INTO\s+trust_r4_send_authorization/iu.test(active)
      || !/scope_key/iu.test(active)
    ) {
      add(
        "SEND_AUTH_ISSUANCE_INCOMPLETE",
        "requires TRANSPORT_CREATED and scope-bound permit insert",
      );
    }
  }

  if (input.name === "50-send-authorization-consume.sql") {
    if (
      !/UPDATE\s+trust_r4_send_authorization[\s\S]*state\s*=\s*'CONSUMED'/iu
        .test(active)
      || !/state\s*=\s*'ISSUED'/iu.test(active)
      || !/UPDATE\s+trust_r4_execution_lease[\s\S]*state\s*=\s*'SENT'/iu
        .test(active)
    ) {
      add(
        "PERMIT_CONSUME_TRANSITION_MISSING",
        "permit ISSUED->CONSUMED and Lease SEND_AUTHORIZED->SENT required",
      );
    }
    if (!/trust_r[34]_audit_head[\s\S]*FOR\s+UPDATE/iu.test(active)) {
      add(
        "AUDIT_ATOMICITY_MISSING",
        "permit consumption must lock audit head in the same transaction",
      );
    }
  }

  return Object.freeze(findings);
}

export function reviewEgressPolicy(text: string): readonly FencingSqlFinding[] {
  const findings: FencingSqlFinding[] = [];
  const add = (code: string, message: string) => {
    findings.push(Object.freeze({ code, message, offset: 0 }));
  };
  if (
    !/current\s+resource\s+floor|currentFloor/iu.test(text)
    && !(
      /trust_r4_resource_fencing/iu.test(text)
      && /current_fencing_token/iu.test(text)
    )
  ) {
    add("EGRESS_FLOOR_MISSING", "egress must read current resource floor");
  }
  if (/cache|cached/iu.test(text) && !/must not|not.*cache|no cache/iu.test(text)) {
    add("EGRESS_CACHE_TRUSTED", "egress cannot authorize from cached floor");
  }
  if (
    /authority\s+unavailable|central\s+unavailable/iu.test(text)
    && !/fail\s+closed|reject|deny/iu.test(text)
  ) {
    add("EGRESS_FAIL_OPEN", "central authority failure must fail closed");
  }
  return Object.freeze(findings);
}
````
<!-- END_EXACT_SOURCE id=S024 -->

### S025. preparation\production-trust\r3-fencing-remediation\tests\execution-boundary.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\execution-boundary.test.ts`
- Bytes: `8680`
- SHA-256: `E8A2CE8FB05B7E7658348FA553FD0606F86D8ADF7D278B7D7158A9DED84D8A48`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S025 sha256=E8A2CE8FB05B7E7658348FA553FD0606F86D8ADF7D278B7D7158A9DED84D8A48 bytes=8680 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import { type ResourceFenceExpectation } from "../contracts";
import {
  OfflineExecutionBoundary,
  type BoundaryContext,
} from "../models/execution-boundary";
import {
  OfflinePersistentFencingFloor,
  type TakeoverInput,
} from "../models/fencing-floor";
import { deriveFencingScopeKey } from "../scope";

const NOW = Date.parse("2026-11-26T11:00:00Z");
const IDS = Object.freeze({
  workerA: "11111111-1111-4111-8111-111111111111",
  workerB: "22222222-2222-4222-8222-222222222222",
  org: "33333333-3333-4333-8333-333333333333",
  target: "44444444-4444-4444-8444-444444444444",
  leaseA: "55555555-5555-4555-8555-555555555555",
  leaseB: "66666666-6666-4666-8666-666666666666",
  capA: "77777777-7777-4777-8777-777777777777",
  capB: "88888888-8888-4888-8888-888888888888",
  authA: "99999999-9999-4999-8999-999999999999",
  authB: "aaaaaaaa-aaaa-4aaa-8aaa-aaaaaaaaaaaa",
  budgetA: "bbbbbbbb-bbbb-4bbb-8bbb-bbbbbbbbbbbb",
  budgetB: "cccccccc-cccc-4ccc-8ccc-cccccccccccc",
  permitA: "dddddddd-dddd-4ddd-8ddd-dddddddddddd",
});
const SCOPE = deriveFencingScopeKey({
  providerKind: "fetch",
  purpose: "fetch_only",
  organizationId: IDS.org,
  targetDigest: "sha256:" + "1".repeat(64),
});

function takeover(index: "A" | "B"): TakeoverInput {
  return {
    scopeKey: SCOPE,
    workerInstanceId: index === "A" ? IDS.workerA : IDS.workerB,
    leaseId: index === "A" ? IDS.leaseA : IDS.leaseB,
    capabilityId: index === "A" ? IDS.capA : IDS.capB,
    executionAuthorizationId: index === "A" ? IDS.authA : IDS.authB,
    budgetReservationId: index === "A" ? IDS.budgetA : IDS.budgetB,
    now: NOW,
    expiresAt: NOW + 30_000,
    emergencyEpoch: 3,
    keyVersion: 2,
    revocationVersion: 1,
    permissionVersion: 4,
    policyVersion: "r4-policy-v1",
    rowCounts: { floor: 1, worker: 1, lease: 1, audit: 1 },
  };
}

function expectation(index: "A" | "B", token: number): ResourceFenceExpectation {
  return {
    scopeKey: SCOPE,
    fencingToken: token,
    workerInstanceId: index === "A" ? IDS.workerA : IDS.workerB,
    leaseId: index === "A" ? IDS.leaseA : IDS.leaseB,
    capabilityId: index === "A" ? IDS.capA : IDS.capB,
  };
}

function context(overrides: Partial<BoundaryContext> = {}): BoundaryContext {
  return {
    now: NOW + 1,
    emergencyStatus: "NORMAL",
    emergencyEpoch: 3,
    keyState: "ACTIVE",
    keyVersion: 2,
    revocationVersion: 1,
    budgetState: "RESERVED",
    budgetExpiresAt: NOW + 20_000,
    ...overrides,
  };
}

function setup() {
  const fencing = new OfflinePersistentFencingFloor({ initialToken: 100 });
  fencing.registerWorker({
    workerInstanceId: IDS.workerA,
    now: NOW,
  });
  fencing.registerWorker({
    workerInstanceId: IDS.workerB,
    now: NOW,
  });
  const lease = fencing.takeover(takeover("A"));
  if (!lease.ok) throw new Error(lease.code);
  return {
    fencing,
    boundary: new OfflineExecutionBoundary(fencing),
    lease: lease.value,
  };
}

function toTransport(
  boundary: OfflineExecutionBoundary,
  ctx = context(),
) {
  expect(boundary.progressLease({
    expectation: expectation("A", 100),
    next: "KEY_READ",
    context: ctx,
    rowCounts: { lease: 1, audit: 1 },
  }).ok).toBe(true);
  expect(boundary.progressLease({
    expectation: expectation("A", 100),
    next: "TRANSPORT_CREATED",
    context: { ...ctx, now: ctx.now + 1 },
    rowCounts: { lease: 1, audit: 1 },
  }).ok).toBe(true);
}

describe("R3 execution boundary uses persistent resource floor", () => {
  it("allows the current Worker through progress, permit and egress", () => {
    const { boundary } = setup();
    toTransport(boundary);
    const permit = boundary.issuePermit({
      expectation: expectation("A", 100),
      permitId: IDS.permitA,
      ttlMs: 5_000,
      context: context({ now: NOW + 3 }),
      rowCounts: { lease: 1, permit: 1, audit: 1 },
    });
    if (!permit.ok) throw new Error(permit.code);
    const consumed = boundary.consumePermit({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 4 }),
      rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
    });
    expect(consumed.ok).toBe(true);
    expect(boundary.authorizeEgress({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 5 }),
      rowCount: 1,
    })).toEqual({ ok: true, value: { networkWriteAllowed: true } });
  });

  it("rejects stale Worker A after B takeover at every boundary", () => {
    const { fencing, boundary } = setup();
    toTransport(boundary);
    const permit = boundary.issuePermit({
      expectation: expectation("A", 100),
      permitId: IDS.permitA,
      ttlMs: 5_000,
      context: context({ now: NOW + 3 }),
      rowCounts: { lease: 1, permit: 1, audit: 1 },
    });
    if (!permit.ok) throw new Error(permit.code);
    const consumed = boundary.consumePermit({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 4 }),
      rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
    });
    expect(consumed.ok).toBe(true);
    const takeoverB = fencing.takeover(takeover("B"));
    expect(takeoverB.ok).toBe(true);
    expect(fencing.getWorker(IDS.workerA)?.state).toBe("ACTIVE");
    expect(boundary.authorizeEgress({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 5 }),
      rowCount: 1,
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
    expect(boundary.progressLease({
      expectation: expectation("A", 100),
      next: "KEY_READ",
      context: context({ now: NOW + 5 }),
      rowCounts: { lease: 1, audit: 1 },
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
  });

  it("fails closed for Emergency epoch, Key revocation and authority outage", () => {
    const emergency = setup();
    toTransport(emergency.boundary);
    expect(emergency.boundary.issuePermit({
      expectation: expectation("A", 100),
      permitId: IDS.permitA,
      ttlMs: 5_000,
      context: context({ now: NOW + 3, emergencyEpoch: 4 }),
      rowCounts: { lease: 1, permit: 1, audit: 1 },
    })).toEqual({ ok: false, code: "EMERGENCY_STOP_ACTIVE" });

    const key = setup();
    toTransport(key.boundary);
    expect(key.boundary.issuePermit({
      expectation: expectation("A", 100),
      permitId: IDS.permitA,
      ttlMs: 5_000,
      context: context({ now: NOW + 3, keyState: "REVOKED" }),
      rowCounts: { lease: 1, permit: 1, audit: 1 },
    })).toEqual({ ok: false, code: "KEY_REVOKED" });

    const unavailable = setup();
    unavailable.fencing.setAuthorityAvailable(false);
    expect(unavailable.boundary.progressLease({
      expectation: expectation("A", 100),
      next: "KEY_READ",
      context: context(),
      rowCounts: { lease: 1, audit: 1 },
    })).toEqual({ ok: false, code: "AUTHORITY_UNAVAILABLE" });
  });

  it("rejects replay and does not mutate on row-count or audit failure", () => {
    const { boundary } = setup();
    expect(boundary.progressLease({
      expectation: expectation("A", 100),
      next: "KEY_READ",
      context: context(),
      rowCounts: { lease: 0, audit: 1 },
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    boundary.setNextAuditFailure();
    expect(boundary.progressLease({
      expectation: expectation("A", 100),
      next: "KEY_READ",
      context: context(),
      rowCounts: { lease: 1, audit: 1 },
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    toTransport(boundary);
    const permit = boundary.issuePermit({
      expectation: expectation("A", 100),
      permitId: IDS.permitA,
      ttlMs: 5_000,
      context: context({ now: NOW + 3 }),
      rowCounts: { lease: 1, permit: 1, audit: 1 },
    });
    if (!permit.ok) throw new Error(permit.code);
    expect(boundary.consumePermit({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 4 }),
      rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
    }).ok).toBe(true);
    expect(boundary.consumePermit({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 5 }),
      rowCounts: { permit: 0, lease: 0, budget: 0, audit: 0 },
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(boundary.consumePermit({
      permitId: IDS.permitA,
      expectation: expectation("A", 100),
      context: context({ now: NOW + 5 }),
      rowCounts: { permit: 1, lease: 1, budget: 1, audit: 1 },
    })).toEqual({ ok: false, code: "SEND_AUTHORIZATION_REPLAYED" });
  });
});
````
<!-- END_EXACT_SOURCE id=S025 -->

### S026. preparation\production-trust\r3-fencing-remediation\tests\fencing-floor.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\fencing-floor.test.ts`
- Bytes: `7331`
- SHA-256: `5690EDDF00728F51F52EB55B9F73176909001B8A031E9DAFE28793D24E9A3A88`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S026 sha256=5690EDDF00728F51F52EB55B9F73176909001B8A031E9DAFE28793D24E9A3A88 bytes=7331 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import { type ResourceFenceExpectation } from "../contracts";
import {
  FencingCommitOutcomeUnknownError,
  OfflinePersistentFencingFloor,
  type TakeoverInput,
} from "../models/fencing-floor";
import { deriveFencingScopeKey } from "../scope";

const NOW = Date.parse("2026-11-26T10:00:00Z");
const IDS = Object.freeze({
  workerA: "11111111-1111-4111-8111-111111111111",
  workerB: "22222222-2222-4222-8222-222222222222",
  org: "33333333-3333-4333-8333-333333333333",
  targetA: "44444444-4444-4444-8444-444444444444",
  targetB: "55555555-5555-4555-8555-555555555555",
  leaseA: "66666666-6666-4666-8666-666666666666",
  leaseB: "77777777-7777-4777-8777-777777777777",
  capA: "88888888-8888-4888-8888-888888888888",
  capB: "99999999-9999-4999-8999-999999999999",
  authA: "aaaaaaaa-aaaa-4aaa-8aaa-aaaaaaaaaaaa",
  authB: "bbbbbbbb-bbbb-4bbb-8bbb-bbbbbbbbbbbb",
  budgetA: "cccccccc-cccc-4ccc-8ccc-cccccccccccc",
  budgetB: "dddddddd-dddd-4ddd-8ddd-dddddddddddd",
});
const DIGEST_A = "sha256:" + "1".repeat(64);
const DIGEST_B = "sha256:" + "2".repeat(64);

function scope(targetDigest = DIGEST_A) {
  return deriveFencingScopeKey({
    providerKind: "fetch",
    purpose: "fetch_only",
    organizationId: IDS.org,
    targetDigest,
  });
}

function takeoverInput(
  index: "A" | "B",
  scopeKey = scope(),
): TakeoverInput {
  return {
    scopeKey,
    workerInstanceId: index === "A" ? IDS.workerA : IDS.workerB,
    leaseId: index === "A" ? IDS.leaseA : IDS.leaseB,
    capabilityId: index === "A" ? IDS.capA : IDS.capB,
    executionAuthorizationId: index === "A" ? IDS.authA : IDS.authB,
    budgetReservationId: index === "A" ? IDS.budgetA : IDS.budgetB,
    now: NOW,
    expiresAt: NOW + 30_000,
    emergencyEpoch: 3,
    keyVersion: 2,
    revocationVersion: 1,
    permissionVersion: 4,
    policyVersion: "r4-policy-v1",
    rowCounts: { floor: 1, worker: 1, lease: 1, audit: 1 },
  };
}

function seeded() {
  const fencing = new OfflinePersistentFencingFloor({ initialToken: 100 });
  expect(fencing.registerWorker({
    workerInstanceId: IDS.workerA,
    now: NOW,
  }).ok).toBe(true);
  expect(fencing.registerWorker({
    workerInstanceId: IDS.workerB,
    now: NOW,
  }).ok).toBe(true);
  return fencing;
}

function expectation(
  index: "A" | "B",
  fencingToken: number,
  scopeKey = scope(),
): ResourceFenceExpectation {
  return {
    scopeKey,
    fencingToken,
    workerInstanceId: index === "A" ? IDS.workerA : IDS.workerB,
    leaseId: index === "A" ? IDS.leaseA : IDS.leaseB,
    capabilityId: index === "A" ? IDS.capA : IDS.capB,
  };
}

describe("R3 persistent resource fencing floor", () => {
  it("serializes Worker A token100 then Worker B takeover token101", () => {
    const fencing = seeded();
    const first = fencing.takeover(takeoverInput("A"));
    const second = fencing.takeover(takeoverInput("B"));
    expect(first.ok && second.ok).toBe(true);
    if (!first.ok || !second.ok) return;
    expect(first.value.fencingToken).toBe(100);
    expect(second.value.fencingToken).toBe(101);
    expect(fencing.getFloor(scope())).toMatchObject({
      currentFencingToken: 101,
      currentWorkerId: IDS.workerB,
      currentLeaseId: IDS.leaseB,
      currentCapabilityId: IDS.capB,
    });
    expect(fencing.getWorker(IDS.workerA)?.state).toBe("ACTIVE");
    expect(fencing.validateCurrent({
      expectation: expectation("A", 100),
      now: NOW + 1,
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
    expect(fencing.validateCurrent({
      expectation: expectation("B", 101),
      now: NOW + 1,
    }).ok).toBe(true);
  });

  it("keeps different resource scopes independent", () => {
    const fencing = seeded();
    const scopeA = scope(DIGEST_A);
    const scopeB = scope(DIGEST_B);
    expect(fencing.takeover(takeoverInput("A", scopeA)).ok).toBe(true);
    const second = fencing.takeover(takeoverInput("B", scopeB));
    expect(second.ok).toBe(true);
    expect(fencing.validateCurrent({
      expectation: expectation("A", 100, scopeA),
      now: NOW + 1,
    }).ok).toBe(true);
  });

  it("uses connected instances for one current floor and rejects stale active Worker", () => {
    const fencing = seeded();
    const other = fencing.connect();
    expect(fencing.takeover(takeoverInput("A")).ok).toBe(true);
    expect(other.takeover(takeoverInput("B")).ok).toBe(true);
    expect(other.snapshot().floors).toBe(1);
    expect(fencing.getWorker(IDS.workerA)?.state).toBe("ACTIVE");
    expect(fencing.validateCurrent({
      expectation: expectation("A", 100),
      now: NOW + 2,
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
  });

  it("recovers an unknown COMMIT without allocating twice", () => {
    const fencing = seeded();
    expect(() => fencing.takeoverWithUnknownCommit(takeoverInput("A")))
      .toThrow(FencingCommitOutcomeUnknownError);
    const recovered = fencing.recoverTakeover({
      leaseId: IDS.leaseA,
      expectation: expectation("A", 100),
    });
    expect(recovered).toMatchObject({
      ok: true,
      value: { leaseId: IDS.leaseA, fencingToken: 100 },
    });
    expect(fencing.snapshot().nextToken).toBe(101);
    expect(fencing.takeover(takeoverInput("A"))).toMatchObject({
      ok: true,
      value: { leaseId: IDS.leaseA, fencingToken: 100 },
    });
    expect(fencing.snapshot().nextToken).toBe(101);
  });

  it("rolls back all state on audit or row-count failure", () => {
    const fencing = seeded();
    expect(fencing.takeover({
      ...takeoverInput("A"),
      failAudit: true,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(fencing.getFloor(scope())).toBeNull();
    expect(fencing.getLease(IDS.leaseA)).toBeNull();
    expect(fencing.takeover({
      ...takeoverInput("A"),
      rowCounts: { floor: 0, worker: 1, lease: 1, audit: 1 },
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(fencing.snapshot()).toMatchObject({
      nextToken: 100,
      floors: 0,
      leases: 0,
    });
  });

  it("fails closed when central fencing authority is unavailable", () => {
    const fencing = seeded();
    fencing.setAuthorityAvailable(false);
    expect(fencing.takeover(takeoverInput("A"))).toEqual({
      ok: false,
      code: "AUTHORITY_UNAVAILABLE",
    });
  });

  it("rejects an expired Lease and a revoked Worker", () => {
    const fencing = seeded();
    expect(fencing.takeover(takeoverInput("A")).ok).toBe(true);
    expect(fencing.validateCurrent({
      expectation: expectation("A", 100),
      now: NOW + 30_000,
    })).toEqual({ ok: false, code: "LEASE_EXPIRED" });
    expect(fencing.setWorkerState({
      workerInstanceId: IDS.workerA,
      state: "REVOKED",
      now: NOW + 1,
    }).ok).toBe(true);
    expect(fencing.validateCurrent({
      expectation: expectation("A", 100),
      now: NOW + 1,
    })).toEqual({ ok: false, code: "WORKER_NOT_ACTIVE" });
  });

  it("does not silently reactivate a revoked Worker", () => {
    const fencing = seeded();
    expect(fencing.setWorkerState({
      workerInstanceId: IDS.workerA,
      state: "REVOKED",
      now: NOW + 1,
    }).ok).toBe(true);
    expect(fencing.registerWorker({
      workerInstanceId: IDS.workerA,
      now: NOW + 2,
    })).toEqual({ ok: false, code: "WORKER_NOT_ACTIVE" });
  });
});
````
<!-- END_EXACT_SOURCE id=S026 -->

### S027. preparation\production-trust\r3-fencing-remediation\tests\races.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\races.test.ts`
- Bytes: `9955`
- SHA-256: `94C7917C295334AB212344F7EF1A4AE64CBCBDEE36F40BC44701C8907D1F0DB1`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S027 sha256=94C7917C295334AB212344F7EF1A4AE64CBCBDEE36F40BC44701C8907D1F0DB1 bytes=9955 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import {
  ExecutionLeaseSchema,
  ResourceFencingFloorSchema,
  SendAuthorizationSchema,
  WorkerRegistrationSchema,
} from "../contracts";
import {
  classifyPermitRace,
  consumePermitAgainstFloor,
  evaluateResourceFencingAttempt,
  recoverTakeoverCommit,
} from "../models/race-scenarios";
import { deriveFencingScopeKey } from "../scope";

const NOW = Date.parse("2026-11-26T10:00:00Z");
const IDs = Object.freeze({
  org: "11111111-1111-4111-8111-111111111111",
  workerA: "22222222-2222-4222-8222-222222222222",
  workerB: "33333333-3333-4333-8333-333333333333",
  leaseA: "44444444-4444-4444-8444-444444444444",
  leaseB: "55555555-5555-4555-8555-555555555555",
  capabilityA: "66666666-6666-4666-8666-666666666666",
  capabilityB: "77777777-7777-4777-8777-777777777777",
  authorizationA: "88888888-8888-4888-8888-888888888888",
  authorizationB: "99999999-9999-4999-8999-999999999999",
  reservationA: "aaaaaaaa-aaaa-4aaa-8aaa-aaaaaaaaaaaa",
  reservationB: "bbbbbbbb-bbbb-4bbb-8bbb-bbbbbbbbbbbb",
  permit: "cccccccc-cccc-4ccc-8ccc-cccccccccccc",
});
const target = "sha256:" + "1".repeat(64);
const scope = deriveFencingScopeKey({
  providerKind: "fetch",
  purpose: "fetch_only",
  organizationId: IDs.org,
  targetDigest: target,
});

function floor(
  token: number,
  worker: string,
  lease: string,
  capability: string,
  scopeKey = scope,
) {
  return ResourceFencingFloorSchema.parse({
    schemaVersion: "r3-resource-fencing-floor-v1",
    scopeKey,
    currentFencingToken: token,
    currentWorkerId: worker,
    currentLeaseId: lease,
    currentCapabilityId: capability,
    version: token,
    state: "ACTIVE",
    updatedAt: NOW,
  });
}

function worker(id: string, heartbeatAt = NOW) {
  return WorkerRegistrationSchema.parse({
    schemaVersion: "r3-fencing-worker-registration-v1",
    workerInstanceId: id,
    state: "ACTIVE",
    heartbeatAt,
    lastIssuedToken: id === IDs.workerA ? 100 : 101,
    updatedAt: NOW,
  });
}

function lease(input: {
  id: string;
  worker: string;
  capability: string;
  authorization: string;
  reservation: string;
  token: number;
  expiresAt?: number;
}) {
  return ExecutionLeaseSchema.parse({
    schemaVersion: "r3-fencing-execution-lease-v1",
    leaseId: input.id,
    scopeKey: scope,
    capabilityId: input.capability,
    executionAuthorizationId: input.authorization,
    budgetReservationId: input.reservation,
    workerInstanceId: input.worker,
    fencingToken: input.token,
    state: "SEND_AUTHORIZED",
    issuedAt: NOW,
    expiresAt: input.expiresAt ?? NOW + 30_000,
    emergencyEpoch: 4,
    keyVersion: 3,
    revocationVersion: 2,
    permissionVersion: 5,
    policyVersion: "policy-v1",
  });
}

function attempt(input?: {
  floorToken?: number;
  floorWorker?: string;
  floorLease?: string;
  floorCapability?: string;
  workerId?: string;
  leaseId?: string;
  token?: number;
  now?: number;
  emergencyStatus?: "NORMAL" | "DRAINING" | "STOPPED" | "RECOVERY_PENDING";
  emergencyEpoch?: number;
  keyActive?: boolean;
  keyVersion?: number;
  revocationVersion?: number;
  authorityAvailable?: boolean;
  scopeKey?: string;
}) {
  const leaseId = input?.leaseId ?? IDs.leaseA;
  const workerId = input?.workerId ?? IDs.workerA;
  const token = input?.token ?? 100;
  const capability = input?.floorCapability ?? IDs.capabilityA;
  return evaluateResourceFencingAttempt({
    operation: "SEND_AUTHORIZATION_CONSUMPTION",
    scopeKey: input?.scopeKey ?? scope,
    floor: floor(
      input?.floorToken ?? token,
      input?.floorWorker ?? workerId,
      input?.floorLease ?? leaseId,
      capability,
      input?.scopeKey ?? scope,
    ),
    worker: worker(workerId, input?.now ?? NOW + 1),
    lease: ExecutionLeaseSchema.parse({
      ...lease({
        id: leaseId,
        worker: workerId,
        capability,
        authorization: workerId === IDs.workerA
          ? IDs.authorizationA
          : IDs.authorizationB,
        reservation: workerId === IDs.workerA
          ? IDs.reservationA
          : IDs.reservationB,
        token,
      }),
      scopeKey: input?.scopeKey ?? scope,
    }),
    token,
    workerInstanceId: workerId,
    leaseId,
    now: input?.now ?? NOW + 1,
    authorityAvailable: input?.authorityAvailable ?? true,
    emergencyStatus: input?.emergencyStatus ?? "NORMAL",
    emergencyEpoch: input?.emergencyEpoch ?? 4,
    keyActive: input?.keyActive ?? true,
    keyVersion: input?.keyVersion ?? 3,
    revocationVersion: input?.revocationVersion ?? 2,
  });
}

describe("Resource Floor takeover races", () => {
  it("rejects all stale Worker A operations after B takes token 101", () => {
    const takeoverFloor = floor(101, IDs.workerB, IDs.leaseB, IDs.capabilityB);
    for (const operation of [
      "LEASE_PROGRESS",
      "SEND_AUTHORIZATION_ISSUANCE",
      "SEND_AUTHORIZATION_CONSUMPTION",
      "EGRESS_WRITE",
    ] as const) {
      expect(evaluateResourceFencingAttempt({
        operation,
        scopeKey: scope,
        floor: takeoverFloor,
        worker: worker(IDs.workerA),
        lease: lease({
          id: IDs.leaseA,
          worker: IDs.workerA,
          capability: IDs.capabilityA,
          authorization: IDs.authorizationA,
          reservation: IDs.reservationA,
          token: 100,
        }),
        token: 100,
        workerInstanceId: IDs.workerA,
        leaseId: IDs.leaseA,
        now: NOW + 1,
        authorityAvailable: true,
        emergencyStatus: "NORMAL",
        emergencyEpoch: 4,
        keyActive: true,
        keyVersion: 3,
        revocationVersion: 2,
      })).toBe("FENCING_TOKEN_STALE");
    }
  });

  it("does not infer authority from an ACTIVE old Worker registration", () => {
    expect(attempt({
      floorToken: 101,
      floorWorker: IDs.workerB,
      floorLease: IDs.leaseB,
      floorCapability: IDs.capabilityB,
      workerId: IDs.workerA,
      leaseId: IDs.leaseA,
      token: 100,
    })).toBe("FENCING_TOKEN_STALE");
  });

  it("keeps independent Resource Scope floors isolated", () => {
    const otherScope = deriveFencingScopeKey({
      providerKind: "fetch",
      purpose: "fetch_only",
      organizationId: IDs.org,
      targetDigest: "sha256:" + "2".repeat(64),
    });
    expect(attempt({
      scopeKey: otherScope,
      floorToken: 100,
      floorWorker: IDs.workerA,
      floorLease: IDs.leaseA,
      token: 100,
    })).toBe("ALLOWED");
    expect(scope).not.toBe(otherScope);
  });

  it("rejects an expired Lease before any further progress", () => {
    expect(attempt({ now: NOW + 30_001 })).toBe("LEASE_EXPIRED");
  });

  it("fails closed for authority loss, Emergency and Key revocation", () => {
    expect(attempt({ authorityAvailable: false })).toBe("AUTHORITY_UNAVAILABLE");
    expect(attempt({ emergencyStatus: "DRAINING" })).toBe("EMERGENCY_BLOCKED");
    expect(attempt({ emergencyEpoch: 5 })).toBe("EMERGENCY_BLOCKED");
    expect(attempt({ keyActive: false })).toBe("KEY_BLOCKED");
    expect(attempt({ revocationVersion: 3 })).toBe("KEY_BLOCKED");
  });
});

describe("Permit consumption races", () => {
  const permit = SendAuthorizationSchema.parse({
    schemaVersion: "r3-fencing-send-authorization-v1",
    sendAuthorizationId: IDs.permit,
    state: "ISSUED",
    scopeKey: scope,
    leaseId: IDs.leaseA,
    capabilityId: IDs.capabilityA,
    workerInstanceId: IDs.workerA,
    fencingToken: 100,
    budgetReservationId: IDs.reservationA,
    emergencyEpoch: 4,
    keyVersion: 3,
    revocationVersion: 2,
    permissionVersion: 5,
    policyVersion: "policy-v1",
    issuedAt: NOW,
    expiresAt: NOW + 5_000,
    consumedAt: null,
  });

  it("denies Worker A when Worker B has already advanced the same floor", () => {
    expect(consumePermitAgainstFloor({
      permit,
      floor: floor(101, IDs.workerB, IDs.leaseB, IDs.capabilityB),
      now: NOW + 1,
      authorityAvailable: true,
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
  });

  it("rejects a replay of a consumed permit", () => {
    expect(consumePermitAgainstFloor({
      permit: { ...permit, state: "CONSUMED", consumedAt: NOW + 1 },
      floor: floor(100, IDs.workerA, IDs.leaseA, IDs.capabilityA),
      now: NOW + 2,
      authorityAvailable: true,
    })).toEqual({ ok: false, code: "SEND_AUTHORIZATION_REPLAYED" });
  });

  it("blocks write after permit commit but before write when takeover wins", () => {
    expect(classifyPermitRace([
      { type: "PERMIT_CONSUMED" },
      { type: "TAKEOVER_COMMITTED" },
    ])).toBe("CONSUMED_WRITE_BLOCKED");
  });

  it("records unknown after an actual write and no response", () => {
    expect(classifyPermitRace([
      { type: "PERMIT_CONSUMED" },
      { type: "WRITE_STARTED" },
      { type: "TAKEOVER_COMMITTED" },
    ])).toBe("WRITE_STARTED_OUTCOME_UNKNOWN");
  });

  it("does not retry after authority loss around the write", () => {
    expect(classifyPermitRace([
      { type: "PERMIT_CONSUMED" },
      { type: "AUTHORITY_UNAVAILABLE" },
    ])).toBe("AUTHORITY_UNAVAILABLE");
  });
});

describe("Takeover COMMIT ambiguity recovery", () => {
  it("returns only the exact persisted takeover Lease", () => {
    const persisted = lease({
      id: IDs.leaseB,
      worker: IDs.workerB,
      capability: IDs.capabilityB,
      authorization: IDs.authorizationB,
      reservation: IDs.reservationB,
      token: 101,
    });
    expect(recoverTakeoverCommit({
      persistedLease: persisted,
      expectedLeaseId: IDs.leaseB,
      expectedWorkerInstanceId: IDs.workerB,
      expectedScopeKey: scope,
      expectedFencingToken: 101,
    })).toMatchObject({ ok: true });
    expect(recoverTakeoverCommit({
      persistedLease: persisted,
      expectedLeaseId: IDs.leaseA,
      expectedWorkerInstanceId: IDs.workerA,
      expectedScopeKey: scope,
      expectedFencingToken: 100,
    })).toEqual({ ok: false, code: "COMMIT_OUTCOME_UNKNOWN" });
  });
});
````
<!-- END_EXACT_SOURCE id=S027 -->

### S028. preparation\production-trust\r3-fencing-remediation\tests\scope-lock-order.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\scope-lock-order.test.ts`
- Bytes: `3687`
- SHA-256: `D99EF9FDF09E102F4B4E7F37D73DB9DDD4EA20E384F1E4DBB370AE5301167C2B`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S028 sha256=D99EF9FDF09E102F4B4E7F37D73DB9DDD4EA20E384F1E4DBB370AE5301167C2B bytes=3687 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import {
  R4_CONTRACT_VERSION,
  ResourceFencingFloorSchema,
  requireExactlyOne,
} from "../contracts";
import {
  R4_LOCK_ORDER,
  validateR4LockOrder,
} from "../lock-order";
import {
  FENCING_SCOPE_DOMAIN,
  deriveFencingScopeKey,
} from "../scope";

const TARGET_A = "sha256:" + "1".repeat(64);
const TARGET_B = "sha256:" + "2".repeat(64);
const ORG_A = "11111111-1111-4111-8111-111111111111";
const ORG_B = "22222222-2222-4222-8222-222222222222";

describe("R3 fencing Scope Key contract", () => {
  it("derives one deterministic scope from provider target identity", () => {
    const input = {
      providerKind: "fetch" as const,
      purpose: "fetch_only" as const,
      organizationId: ORG_A,
      targetDigest: TARGET_A,
    };
    const key = deriveFencingScopeKey(input);
    expect(key).toBe(deriveFencingScopeKey({
      targetDigest: input.targetDigest,
      organizationId: input.organizationId,
      purpose: input.purpose,
      providerKind: input.providerKind,
    }));
    expect(key).toMatch(/^fence-scope-v1:sha256:[a-f0-9]{64}$/u);
    expect(FENCING_SCOPE_DOMAIN).toBe("r3-fencing-resource-scope-v1");
  });

  it("separates different targets and organizations", () => {
    const base = {
      providerKind: "fetch" as const,
      purpose: "fetch_only" as const,
      organizationId: ORG_A,
      targetDigest: TARGET_A,
    };
    expect(deriveFencingScopeKey(base))
      .not.toBe(deriveFencingScopeKey({ ...base, targetDigest: TARGET_B }));
    expect(deriveFencingScopeKey(base))
      .not.toBe(deriveFencingScopeKey({ ...base, organizationId: ORG_B }));
  });

  it("fixed contract version and resource floor shape", () => {
    expect(R4_CONTRACT_VERSION).toBe("r2-r3-fencing-remediation-v1");
    expect(ResourceFencingFloorSchema.safeParse({
      schemaVersion: "r3-resource-fencing-floor-v1",
      scopeKey: deriveFencingScopeKey({
        providerKind: "fetch",
        purpose: "fetch_only",
        organizationId: ORG_A,
        targetDigest: TARGET_A,
      }),
      currentFencingToken: 100,
      currentWorkerId: ORG_A,
      currentLeaseId: null,
      currentCapabilityId: null,
      version: 1,
      state: "ACTIVE",
      updatedAt: 1,
    }).success).toBe(true);
  });
});

describe("R4 fencing lock order and row count", () => {
  it("places resource floor before token allocator and lease", () => {
    expect(R4_LOCK_ORDER.indexOf("RESOURCE_FENCING_FLOOR"))
      .toBeLessThan(R4_LOCK_ORDER.indexOf("FENCING_TOKEN_CONTROL"));
    expect(R4_LOCK_ORDER.indexOf("FENCING_TOKEN_CONTROL"))
      .toBeLessThan(R4_LOCK_ORDER.indexOf("WORKER_REGISTRATION"));
    expect(R4_LOCK_ORDER.indexOf("WORKER_REGISTRATION"))
      .toBeLessThan(R4_LOCK_ORDER.indexOf("EXECUTION_LEASE"));
    expect(R4_LOCK_ORDER.indexOf("SEND_AUTHORIZATION"))
      .toBeLessThan(R4_LOCK_ORDER.indexOf("AUDIT_SEQUENCE"));
  });

  it("accepts canonical lock order and rejects crossing", () => {
    expect(validateR4LockOrder(
      R4_LOCK_ORDER.map((domain, index) => ({
        domain,
        acquiredAt: index,
      })),
    ).ok).toBe(true);
    expect(validateR4LockOrder([
      { domain: "AUDIT_SEQUENCE", acquiredAt: 1 },
      { domain: "RESOURCE_FENCING_FLOOR", acquiredAt: 2 },
    ])).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
  });

  it("requires exactly one affected update row", () => {
    expect(requireExactlyOne(1)).toEqual({ ok: true, value: true });
    expect(requireExactlyOne(0)).toEqual({
      ok: false,
      code: "ROW_COUNT_CONFLICT",
    });
    expect(requireExactlyOne(2)).toEqual({
      ok: false,
      code: "ROW_COUNT_CONFLICT",
    });
  });
});
````
<!-- END_EXACT_SOURCE id=S028 -->

### S029. preparation\production-trust\r3-fencing-remediation\tests\scope-lock.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\scope-lock.test.ts`
- Bytes: `4417`
- SHA-256: `45E38B57F90919DA480E8348D8CD14B8036E2A96CD84392BDF79EE5E3AD5EB98`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S029 sha256=45E38B57F90919DA480E8348D8CD14B8036E2A96CD84392BDF79EE5E3AD5EB98 bytes=4417 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import {
  R4_CONTRACT_VERSION,
  ResourceFencingFloorSchema,
  requireExactlyOne,
} from "../contracts";
import {
  R4_LOCK_ORDER,
  R4RetryableTransactionError,
  retryR4Transaction,
  validateR4LockOrder,
} from "../lock-order";
import {
  deriveFencingScopeKey,
  FencingScopeKeySchema,
} from "../scope";

const DIGEST_A = "sha256:" + "1".repeat(64);
const DIGEST_B = "sha256:" + "2".repeat(64);
const ORG_A = "11111111-1111-4111-8111-111111111111";
const ORG_B = "22222222-2222-4222-8222-222222222222";

describe("R4 normalized fencing scope", () => {
  it("derives one stable key from resource identity", () => {
    const input = {
      providerKind: "fetch" as const,
      purpose: "fetch_only" as const,
      organizationId: ORG_A,
      targetDigest: DIGEST_A,
    };
    const first = deriveFencingScopeKey(input);
    const second = deriveFencingScopeKey({
      targetDigest: input.targetDigest,
      organizationId: input.organizationId,
      purpose: input.purpose,
      providerKind: input.providerKind,
    });
    expect(first).toBe(second);
    expect(FencingScopeKeySchema.safeParse(first).success).toBe(true);
    expect(first).toMatch(/^fence-scope-v1:sha256:[a-f0-9]{64}$/u);
  });

  it("separates organizations and target digests", () => {
    const base = {
      providerKind: "fetch" as const,
      purpose: "fetch_only" as const,
      organizationId: ORG_A,
      targetDigest: DIGEST_A,
    };
    expect(deriveFencingScopeKey(base)).not.toBe(
      deriveFencingScopeKey({ ...base, organizationId: ORG_B }),
    );
    expect(deriveFencingScopeKey(base)).not.toBe(
      deriveFencingScopeKey({ ...base, targetDigest: DIGEST_B }),
    );
  });

  it("rejects client-only or unknown scope fields", () => {
    expect(() => deriveFencingScopeKey({
      providerKind: "fetch",
      purpose: "fetch_only",
      organizationId: ORG_A,
      targetDigest: DIGEST_A,
      actorId: "33333333-3333-4333-8333-333333333333",
    })).toThrow();
  });

  it("validates the complete persistent floor shape", () => {
    expect(ResourceFencingFloorSchema.safeParse({
      schemaVersion: "r3-resource-fencing-floor-v1",
      scopeKey: deriveFencingScopeKey({
        providerKind: "fetch",
        purpose: "fetch_only",
        organizationId: ORG_A,
        targetDigest: DIGEST_A,
      }),
      currentFencingToken: 101,
      currentWorkerId: "44444444-4444-4444-8444-444444444444",
      currentLeaseId: "55555555-5555-4555-8555-555555555555",
      currentCapabilityId: "66666666-6666-4666-8666-666666666666",
      version: 3,
      state: "ACTIVE",
      updatedAt: 1_000,
    }).success).toBe(true);
  });
});

describe("R4 lock order and transaction retry", () => {
  it("keeps resource floor before token control and Lease", () => {
    expect(R4_CONTRACT_VERSION).toBe("r2-r3-fencing-remediation-v1");
    expect(R4_LOCK_ORDER.indexOf("RESOURCE_FENCING_FLOOR")).toBeLessThan(
      R4_LOCK_ORDER.indexOf("FENCING_TOKEN_CONTROL"),
    );
    expect(R4_LOCK_ORDER.indexOf("FENCING_TOKEN_CONTROL")).toBeLessThan(
      R4_LOCK_ORDER.indexOf("EXECUTION_LEASE"),
    );
    expect(validateR4LockOrder(
      R4_LOCK_ORDER.map((domain, index) => ({
        domain,
        acquiredAt: index,
      })),
    ).ok).toBe(true);
  });

  it("rejects crossing locks and retry after network attempt", async () => {
    expect(validateR4LockOrder([
      { domain: "SEND_AUTHORIZATION", acquiredAt: 1 },
      { domain: "RESOURCE_FENCING_FLOOR", acquiredAt: 2 },
    ])).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    await expect(retryR4Transaction({
      maxAttempts: 2,
      externalAttemptStarted: true,
      run: async () => "not-run",
    })).resolves.toEqual({ ok: false, code: "SEND_OUTCOME_UNKNOWN" });
  });

  it("retries only bounded transactional failures", async () => {
    let attempts = 0;
    await expect(retryR4Transaction({
      maxAttempts: 2,
      externalAttemptStarted: false,
      run: async () => {
        attempts += 1;
        if (attempts === 1) {
          throw new R4RetryableTransactionError("DEADLOCK_DETECTED");
        }
        return true;
      },
    })).resolves.toEqual({ ok: true, value: true });
    expect(requireExactlyOne(1)).toEqual({ ok: true, value: true });
    expect(requireExactlyOne(0)).toEqual({
      ok: false,
      code: "ROW_COUNT_CONFLICT",
    });
  });
});
````
<!-- END_EXACT_SOURCE id=S029 -->

### S030. preparation\production-trust\r3-fencing-remediation\tests\sql-negative.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\sql-negative.test.ts`
- Bytes: `4328`
- SHA-256: `A9185EAC405B111E9323239200C0DA3C4ECAFB297220F71A4E4DBA81D27162A2`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S030 sha256=A9185EAC405B111E9323239200C0DA3C4ECAFB297220F71A4E4DBA81D27162A2 bytes=4328 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import {
  reviewEgressPolicy,
  reviewResourceFencingSql,
} from "../models/sql-analyzer";

function codes(name: string, text: string): string[] {
  return reviewResourceFencingSql({ name, text })
    .map((finding) => finding.code);
}

describe("R3 fencing SQL negative analysis", () => {
  it("detects Worker-only fence authorization", () => {
    const result = codes("30-worker-progress.sql", `
      BEGIN;
      UPDATE trust_r4_execution_lease
      SET state = 'KEY_READ'
      WHERE lease_id = $1
        AND state = 'ISSUED'
        AND EXISTS (
          SELECT 1 FROM trust_r4_worker_registration w
          WHERE w.worker_instance_id = $2 AND w.fence_floor = $3
        );
      COMMIT;
    `);
    expect(result).toContain("WORKER_FLOOR_AUTHORITATIVE");
    expect(result).toContain("RESOURCE_FLOOR_LOCK_MISSING");
  });

  it("detects registration-only takeover without resource floor", () => {
    const result = codes("10-worker-takeover.sql", `
      BEGIN;
      UPDATE trust_r4_worker_registration SET last_issued_token = $1
      WHERE worker_instance_id = $2 AND state = 'ACTIVE';
      UPDATE trust_r4_execution_lease SET state = 'ISSUED'
      WHERE lease_id = $3 AND state = 'PENDING';
      COMMIT;
    `);
    expect(result).toContain("TAKEOVER_ATOMICITY");
    expect(result).toContain("TAKEOVER_FLOOR_UPDATE_INCOMPLETE");
    expect(result).toContain("RESOURCE_INITIALIZATION_MISSING");
  });

  it("detects floor and Lease in different transactions", () => {
    const result = codes("10-worker-takeover.sql", `
      BEGIN;
      INSERT INTO trust_r4_resource_fencing (scope_key) VALUES ($1)
      ON CONFLICT DO NOTHING;
      UPDATE trust_r4_resource_fencing
      SET current_fencing_token = $2, current_worker_id = $3,
          current_lease_id = $4, current_capability_id = $5,
          version = version + 1
      WHERE scope_key = $1 AND version = $6;
      COMMIT;
      BEGIN;
      INSERT INTO trust_r4_execution_lease (lease_id) VALUES ($4);
      COMMIT;
    `);
    expect(result).toContain("TAKEOVER_ATOMICITY");
  });

  it("detects permit consumption without resource floor lock", () => {
    const result = codes("50-send-authorization-consume.sql", `
      BEGIN;
      SELECT * FROM trust_r4_send_authorization
      WHERE send_authorization_id = $1 FOR UPDATE;
      UPDATE trust_r4_send_authorization SET state = 'CONSUMED'
      WHERE send_authorization_id = $1 AND state = 'ISSUED';
      UPDATE trust_r4_execution_lease SET state = 'SENT'
      WHERE lease_id = $2 AND state = 'SEND_AUTHORIZED';
      SELECT * FROM trust_r4_audit_head FOR UPDATE;
      COMMIT;
    `);
    expect(result).toContain("RESOURCE_FLOOR_LOCK_MISSING");
    expect(result).toContain("RESOURCE_CURRENT_BINDING_MISSING");
  });

  it("detects missing row-count markers", () => {
    const result = codes("30-worker-progress.sql", `
      BEGIN;
      SELECT * FROM trust_r4_resource_fencing
      WHERE scope_key = $1
        AND current_fencing_token = $2
        AND current_worker_id = $3
        AND current_lease_id = $4
      FOR UPDATE;
      UPDATE trust_r4_execution_lease SET state = 'KEY_READ'
      WHERE lease_id = $4 AND state = 'ISSUED' AND scope_key = $1;
      COMMIT;
    `);
    expect(result).toContain("ROW_COUNT_MARKER_MISSING");
  });

  it("does not accept an implicit global resource floor", () => {
    const result = codes("50-send-authorization-consume.sql", `
      BEGIN;
      UPDATE trust_r4_send_authorization SET state = 'CONSUMED'
      WHERE send_authorization_id = $1 AND state = 'ISSUED';
      COMMIT;
    `);
    expect(result).toContain("RESOURCE_FLOOR_LOCK_MISSING");
  });
});

describe("R3 egress policy negative analysis", () => {
  it("detects cached floor and authority fail-open", () => {
    const result = reviewEgressPolicy(`
      use cached floor;
      if authority unavailable then continue;
    `).map((finding) => finding.code);
    expect(result).toContain("EGRESS_CACHE_TRUSTED");
    expect(result).toContain("EGRESS_FAIL_OPEN");
  });

  it("accepts current floor and fail-closed language", () => {
    expect(reviewEgressPolicy(`
      read current resource floor;
      must not use cached floor;
      if authority unavailable, reject and fail closed;
    `)).toEqual([]);
  });
});
````
<!-- END_EXACT_SOURCE id=S030 -->

### S031. preparation\production-trust\r3-fencing-remediation\tests\sql-positive.test.ts

- Category: `D_R3F_TEST`
- Path: `preparation\production-trust\r3-fencing-remediation\tests\sql-positive.test.ts`
- Bytes: `2404`
- SHA-256: `5F82F0DD4A89BCC65672F7CDA7EFA0D0FF1BCCCE95FABAE22DBBEBE24BAB279C`
- Description: Complete fencing test

<!-- BEGIN_EXACT_SOURCE id=S031 sha256=5F82F0DD4A89BCC65672F7CDA7EFA0D0FF1BCCCE95FABAE22DBBEBE24BAB279C bytes=2404 fence=fenced -->
````typescript
import { readFileSync, readdirSync } from "node:fs";
import { join } from "node:path";
import { fileURLToPath } from "node:url";

import { describe, expect, it } from "vitest";

import {
  reviewEgressPolicy,
  reviewResourceFencingSql,
} from "../models/sql-analyzer";

const sqlRoot = fileURLToPath(new URL("../sql/", import.meta.url));
const remediationRoot = fileURLToPath(new URL("../", import.meta.url));

function read(name: string): string {
  return readFileSync(join(sqlRoot, name), "utf8");
}

const FILES = [
  "00-schema.sql",
  "10-worker-takeover.sql",
  "20-lease-issuance.sql",
  "30-worker-progress.sql",
  "40-send-authorization-issuance.sql",
  "50-send-authorization-consume.sql",
] as const;

describe("R3 fencing positive SQL analysis", () => {
  it("contains every required SQL draft and no Worker-floor authority", () => {
    expect(readdirSync(sqlRoot).filter((name) => name.endsWith(".sql")).sort())
      .toEqual([...FILES].sort());
    for (const name of FILES) {
      const source = read(name);
      expect(source, name).not.toMatch(/\bfence_floor\b/iu);
      expect(reviewResourceFencingSql({ name, text: source }), name)
        .toEqual([]);
    }
  });

  it("binds every regulated table to scope key", () => {
    const schema = read("00-schema.sql");
    for (const table of [
      "trust_r4_resource_fencing",
      "trust_r4_execution_lease",
      "trust_r4_send_authorization",
    ]) {
      expect(schema).toContain(table);
    }
    for (const name of FILES.slice(1)) {
      expect(read(name), name).toMatch(/scope_key/iu);
    }
  });

  it("keeps final egress fresh-read and fail-closed", () => {
    expect(reviewEgressPolicy(read("50-send-authorization-consume.sql")))
      .toEqual([]);
  });

  it("contains complete transaction files in the consolidated SQL artifact", () => {
    const consolidated = readFileSync(
      join(
        remediationRoot,
        "PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql",
      ),
      "utf8",
    );
    for (const name of FILES.slice(1)) {
      expect(consolidated).toContain(read(name));
    }
  });

  it("keeps the required root schema artifact byte-identical to its source", () => {
    const rootSchema = readFileSync(
      join(
        remediationRoot,
        "PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql",
      ),
      "utf8",
    );
    expect(rootSchema).toBe(read("00-schema.sql"));
  });
});
````
<!-- END_EXACT_SOURCE id=S031 -->

### S032. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql

- Category: `E_R3F_ARTIFACT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql`
- Bytes: `4974`
- SHA-256: `76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4`
- Description: Required consolidated artifact

<!-- BEGIN_EXACT_SOURCE id=S032 sha256=76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4 bytes=4974 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- R4 fencing layer. This draft assumes the R3 authorization, budget,
-- capability, key and emergency tables already exist. It does not modify the
-- frozen R3 schema.

CREATE TABLE trust_r4_resource_fencing (
  scope_key text PRIMARY KEY
    CHECK (scope_key ~ '^fence-scope-v1:sha256:[a-f0-9]{64}$'),
  current_fencing_token bigint NOT NULL DEFAULT 0
    CHECK (current_fencing_token >= 0),
  current_worker_id uuid,
  current_lease_id uuid,
  current_capability_id uuid,
  version bigint NOT NULL DEFAULT 1 CHECK (version >= 1),
  state text NOT NULL DEFAULT 'ACTIVE'
    CHECK (state IN ('ACTIVE', 'REVOKED')),
  updated_at_ms bigint NOT NULL,
  CHECK (
    (current_fencing_token = 0
      AND current_worker_id IS NULL
      AND current_lease_id IS NULL
      AND current_capability_id IS NULL)
    OR
    (current_fencing_token > 0
      AND current_worker_id IS NOT NULL
      AND current_lease_id IS NOT NULL
      AND current_capability_id IS NOT NULL)
  )
);

CREATE TABLE trust_r4_fencing_token_control (
  singleton_id smallint PRIMARY KEY CHECK (singleton_id = 1),
  next_token bigint NOT NULL CHECK (next_token >= 1),
  version bigint NOT NULL CHECK (version >= 1),
  updated_at_ms bigint NOT NULL
);

INSERT INTO trust_r4_fencing_token_control (
  singleton_id, next_token, version, updated_at_ms
) VALUES (1, 1, 1, 0);

CREATE TABLE trust_r4_worker_registration (
  worker_instance_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (state IN ('ACTIVE', 'DRAINING', 'REVOKED')),
  heartbeat_at_ms bigint NOT NULL,
  last_issued_token bigint NOT NULL DEFAULT 0 CHECK (last_issued_token >= 0),
  updated_at_ms bigint NOT NULL
);

CREATE TABLE trust_r4_execution_lease (
  lease_id uuid PRIMARY KEY,
  scope_key text NOT NULL REFERENCES trust_r4_resource_fencing (scope_key),
  capability_id uuid NOT NULL UNIQUE
    REFERENCES trust_r3_capability (capability_id),
  execution_authorization_id uuid NOT NULL
    REFERENCES trust_r3_execution_authorization (authorization_id),
  budget_reservation_id uuid NOT NULL
    REFERENCES trust_r3_budget_reservation (reservation_id),
  worker_instance_id uuid NOT NULL
    REFERENCES trust_r4_worker_registration (worker_instance_id),
  fencing_token bigint NOT NULL CHECK (fencing_token > 0),
  state text NOT NULL CHECK (
    state IN (
      'ISSUED', 'KEY_READ', 'TRANSPORT_CREATED', 'SEND_AUTHORIZED',
      'SENT', 'RESPONSE_RECEIVED', 'COMPLETED', 'FAILED_BEFORE_SEND',
      'SEND_OUTCOME_UNKNOWN', 'FAILED_AFTER_SEND', 'EXPIRED', 'REVOKED',
      'EMERGENCY_BLOCKED'
    )
  ),
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  emergency_epoch bigint NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  UNIQUE (scope_key, fencing_token),
  CHECK (expires_at_ms > issued_at_ms),
  CHECK (expires_at_ms - issued_at_ms <= 60000)
);

ALTER TABLE trust_r4_resource_fencing
  ADD CONSTRAINT trust_r4_floor_worker_fk
  FOREIGN KEY (current_worker_id)
  REFERENCES trust_r4_worker_registration (worker_instance_id)
  DEFERRABLE INITIALLY DEFERRED;

ALTER TABLE trust_r4_resource_fencing
  ADD CONSTRAINT trust_r4_floor_lease_fk
  FOREIGN KEY (current_lease_id)
  REFERENCES trust_r4_execution_lease (lease_id)
  DEFERRABLE INITIALLY DEFERRED;

ALTER TABLE trust_r4_resource_fencing
  ADD CONSTRAINT trust_r4_floor_capability_fk
  FOREIGN KEY (current_capability_id)
  REFERENCES trust_r3_capability (capability_id)
  DEFERRABLE INITIALLY DEFERRED;

CREATE TABLE trust_r4_send_authorization (
  send_authorization_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (state IN ('ISSUED', 'CONSUMED', 'EXPIRED', 'REVOKED')),
  scope_key text NOT NULL REFERENCES trust_r4_resource_fencing (scope_key),
  lease_id uuid NOT NULL UNIQUE REFERENCES trust_r4_execution_lease (lease_id),
  capability_id uuid NOT NULL,
  worker_instance_id uuid NOT NULL,
  fencing_token bigint NOT NULL,
  budget_reservation_id uuid NOT NULL,
  emergency_epoch bigint NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  consumed_at_ms bigint,
  CHECK (expires_at_ms > issued_at_ms),
  CHECK (expires_at_ms - issued_at_ms <= 5000),
  CHECK (
    (state = 'ISSUED' AND consumed_at_ms IS NULL)
    OR (state = 'CONSUMED' AND consumed_at_ms IS NOT NULL)
    OR state IN ('EXPIRED', 'REVOKED')
  )
);

CREATE INDEX trust_r4_floor_worker_idx
  ON trust_r4_resource_fencing (current_worker_id, state);

CREATE INDEX trust_r4_floor_lease_idx
  ON trust_r4_resource_fencing (current_lease_id, state);

CREATE INDEX trust_r4_lease_worker_idx
  ON trust_r4_execution_lease (worker_instance_id, state, expires_at_ms);

CREATE INDEX trust_r4_send_state_idx
  ON trust_r4_send_authorization (state, expires_at_ms);
````
<!-- END_EXACT_SOURCE id=S032 -->

### S033. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql

- Category: `E_R3F_ARTIFACT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql`
- Bytes: `35018`
- SHA-256: `512E790234B41699AF72DCDE172F4CF247911DE02E9C04915D985ED5C739D8B1`
- Description: Required consolidated artifact

<!-- BEGIN_EXACT_SOURCE id=S033 sha256=512E790234B41699AF72DCDE172F4CF247911DE02E9C04915D985ED5C739D8B1 bytes=35018 fence=fenced -->
````sql
-- PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Consolidated view of the complete R4 fencing transaction drafts.
-- Canonical lock order:
-- EMERGENCY_CONTROL -> KEY_REGISTRY -> APPROVAL -> APPROVAL_CONSUMPTION
-- -> EXECUTION_AUTHORIZATION -> BUDGET_CONTROL -> BUDGET_RESERVATION
-- -> CAPABILITY -> RESOURCE_FENCING_FLOOR -> FENCING_TOKEN_CONTROL
-- -> WORKER_REGISTRATION -> EXECUTION_LEASE -> SEND_AUTHORIZATION
-- -> AUDIT_SEQUENCE

-- ===== BEGIN 10-worker-takeover.sql =====
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Atomic resource takeover + Lease issuance.
-- Linearization point: commit of resource-floor update and Lease insertion.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms, actor_id,
       organization_id, lead_id, target_digest, capability_id,
       budget_reservation_id, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r3_execution_authorization
WHERE authorization_id = $2
FOR UPDATE;

SELECT reservation_id, state, expires_at_ms, execution_authorization_id,
       capability_id, worker_instance_id, budget_version, send_started_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $3
FOR UPDATE;

SELECT capability_id, state, expires_at_ms, execution_authorization_id,
       consumption_id, worker_instance_id, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r3_capability
WHERE capability_id = $4
FOR UPDATE;

-- Secure first-use initialization. Concurrent creators block on the unique
-- scope key; after this statement and the following row lock, exactly one
-- authoritative floor is visible.
INSERT INTO trust_r4_resource_fencing (
  scope_key, current_fencing_token, current_worker_id, current_lease_id,
  current_capability_id, version, state, updated_at_ms
) VALUES (
  $5, 0, NULL, NULL, NULL, 1, 'ACTIVE', $6
)
ON CONFLICT (scope_key) DO NOTHING;

SELECT scope_key, current_fencing_token, current_worker_id, current_lease_id,
       current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $5
FOR UPDATE;

SELECT next_token, version
FROM trust_r4_fencing_token_control
WHERE singleton_id = 1
FOR UPDATE;

-- Worker registration is not an authorization source. last_issued_token is
-- diagnostic only; the resource floor remains authoritative.
INSERT INTO trust_r4_worker_registration (
  worker_instance_id, state, heartbeat_at_ms, last_issued_token, updated_at_ms
) VALUES (
  $7, 'ACTIVE', $6, 0, $6
)
ON CONFLICT (worker_instance_id) DO NOTHING;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration
SET heartbeat_at_ms = $6,
    updated_at_ms = $6
WHERE worker_instance_id = $7
  AND state = 'ACTIVE';

-- INSERT command tag must be one, and the conditional UPDATE must affect
-- exactly one row. A previously REVOKED Worker therefore rolls back instead
-- of being silently reactivated.

-- Allocate the next persistent token and bind it to this exact resource scope.
WITH allocated AS (
  -- ROW_COUNT_EXPECTATION: exactly 1
  UPDATE trust_r4_fencing_token_control
  SET next_token = next_token + 1,
      version = version + 1,
      updated_at_ms = $6
  WHERE singleton_id = 1
    AND next_token = $8
    AND version = $9
  RETURNING next_token - 1 AS fencing_token
)
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_resource_fencing AS floor
SET current_fencing_token = allocated.fencing_token,
    current_worker_id = $7,
    current_lease_id = $10,
    current_capability_id = $4,
    version = floor.version + 1,
    updated_at_ms = $6
FROM allocated
WHERE floor.scope_key = $5
  AND floor.state = 'ACTIVE'
  AND floor.version = $11
  AND floor.current_fencing_token < allocated.fencing_token
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $12
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key k
    WHERE k.key_id = $1
      AND k.state = 'ACTIVE'
      AND k.key_version = $13
      AND k.revocation_version = $14
      AND $6 >= k.valid_from_ms
      AND $6 < k.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization a
    WHERE a.authorization_id = $2
      AND a.state = 'ACTIVE'
      AND a.capability_id = $4
      AND a.budget_reservation_id = $3
      AND a.emergency_epoch = $12
      AND a.key_version = $13
      AND a.revocation_version = $14
      AND a.permission_version = $15
      AND a.policy_version = $16
      AND $6 < a.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $3
      AND b.state = 'RESERVED'
      AND b.execution_authorization_id = $2
      AND b.capability_id = $4
      AND b.worker_instance_id = $7
      AND b.send_started_at_ms IS NULL
      AND $6 < b.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability c
    WHERE c.capability_id = $4
      AND c.state = 'ISSUED'
      AND c.execution_authorization_id = $2
      AND c.worker_instance_id = $7
      AND c.budget_reservation_id = $3
      AND c.emergency_epoch = $12
      AND c.key_version = $13
      AND c.revocation_version = $14
      AND c.permission_version = $15
      AND c.policy_version = $16
      AND $6 < c.expires_at_ms
  )
RETURNING floor.current_fencing_token;

-- The driver must read exactly one returned token and bind it as $17 below.

WITH token AS (
  SELECT current_fencing_token
  FROM trust_r4_resource_fencing
  WHERE scope_key = $5
    AND current_worker_id = $7
    AND current_lease_id = $10
    AND current_capability_id = $4
)
-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_worker_registration AS worker
SET heartbeat_at_ms = $6,
    last_issued_token = token.current_fencing_token,
    updated_at_ms = $6
FROM token
WHERE worker.worker_instance_id = $7
  AND worker.state = 'ACTIVE';

-- INSERT command tag must be exactly one row.
INSERT INTO trust_r4_execution_lease (
  lease_id, scope_key, capability_id, execution_authorization_id,
  budget_reservation_id, worker_instance_id, fencing_token, state,
  issued_at_ms, expires_at_ms, emergency_epoch, key_version,
  revocation_version, permission_version, policy_version
) VALUES (
  $10, $5, $4, $2,
  $3, $7, $17, 'ISSUED',
  $6, $18, $12, $13,
  $14, $15, $16
);

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

-- INSERT command tag must be exactly one row.
INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $19, $20, $6, 'LEASE_ISSUED', 'ALLOW',
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

-- Any non-one command tag rolls back token allocation, floor update, Worker
-- registration mutation, Lease insertion and audit as one operation.
-- ===== END 10-worker-takeover.sql =====

-- ===== BEGIN 20-lease-issuance.sql =====
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Lease Issuance recovery and verification.
--
-- The first issuance and Worker takeover are one atomic mutation in
-- 10-worker-takeover.sql. This transaction is used when the caller loses the
-- COMMIT acknowledgement or needs to verify an idempotent Lease request.
-- It never allocates another token and never inserts another Lease.

BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT reservation_id, state, execution_authorization_id, capability_id,
       worker_instance_id, expires_at_ms
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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       issued_at_ms, expires_at_ms, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r4_execution_lease
WHERE capability_id = $4
FOR UPDATE;

-- The driver must assert exactly one Lease row. The application validates:
--   lease.scope_key = floor.scope_key = $5
--   lease.fencing_token = floor.current_fencing_token = all supplied versions
--   lease.worker_instance_id = floor.current_worker_id = $6
--   lease.lease_id = floor.current_lease_id = $7
--   lease.capability_id = floor.current_capability_id = $4
--   Authorization, budget, Capability, Emergency and Key remain current
--   trusted now < Lease/resource/authorization/reservation expiry
--
-- If no Lease row exists after a COMMIT-unknown response, the caller may retry
-- 10-worker-takeover.sql. The unique capability_id Lease constraint is the
-- final duplicate-issuance arbiter.

COMMIT;
-- ===== END 20-lease-issuance.sql =====

-- ===== BEGIN 30-worker-progress.sql =====
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Worker Progress is two separate transactions. Worker registration metadata
-- is never sufficient; every update compares the authoritative resource floor.

-- Transaction 3A: ISSUED -> KEY_READ.
BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'KEY_READ'
WHERE lease.lease_id = $7
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND lease.state = 'ISSUED'
  AND lease.emergency_epoch = $9
  AND lease.key_version = $10
  AND lease.revocation_version = $11
  AND lease.permission_version = $12
  AND lease.policy_version = $13
  AND $14 < lease.expires_at_ms
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
      AND $14 - worker.heartbeat_at_ms <= 15000
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

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $15, $16, $14, 'WORKER_PROGRESS', 'ALLOW',
  $7, $17, $18
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $16,
    last_event_digest = $18
WHERE singleton_id = 1
  AND last_sequence = $16 - 1
  AND last_event_digest IS NOT DISTINCT FROM $17;

COMMIT;

-- Transaction 3B: KEY_READ -> TRANSPORT_CREATED.
BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'TRANSPORT_CREATED'
WHERE lease.lease_id = $7
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND lease.state = 'KEY_READ'
  AND lease.emergency_epoch = $9
  AND lease.key_version = $10
  AND lease.revocation_version = $11
  AND lease.permission_version = $12
  AND lease.policy_version = $13
  AND $14 < lease.expires_at_ms
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
      AND $14 - worker.heartbeat_at_ms <= 15000
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

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $15, $16, $14, 'WORKER_PROGRESS', 'ALLOW',
  $7, $17, $18
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $16,
    last_event_digest = $18
WHERE singleton_id = 1
  AND last_sequence = $16 - 1
  AND last_event_digest IS NOT DISTINCT FROM $17;

COMMIT;
-- ===== END 30-worker-progress.sql =====

-- ===== BEGIN 40-send-authorization-issuance.sql =====
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- One short-lived Send Authorization for a TRANSPORT_CREATED Lease.

BEGIN ISOLATION LEVEL READ COMMITTED;

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

SELECT lease_id, scope_key, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token, state,
       expires_at_ms, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r4_execution_lease
WHERE lease_id = $7
FOR UPDATE;

-- A retry for the same Lease returns the existing permit. It does not create a
-- second permit or allocate another token.
SELECT send_authorization_id, state, scope_key, lease_id, capability_id,
       worker_instance_id, fencing_token, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version,
       issued_at_ms, expires_at_ms, consumed_at_ms
FROM trust_r4_send_authorization
WHERE lease_id = $7
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r4_execution_lease AS lease
SET state = 'SEND_AUTHORIZED'
WHERE lease.lease_id = $7
  AND lease.scope_key = $5
  AND lease.capability_id = $4
  AND lease.execution_authorization_id = $2
  AND lease.budget_reservation_id = $3
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8
  AND lease.state = 'TRANSPORT_CREATED'
  AND lease.emergency_epoch = $9
  AND lease.key_version = $10
  AND lease.revocation_version = $11
  AND lease.permission_version = $12
  AND lease.policy_version = $13
  AND $14 < lease.expires_at_ms
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
      AND $14 - worker.heartbeat_at_ms <= 15000
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

-- INSERT command tag must be exactly one row.
INSERT INTO trust_r4_send_authorization (
  send_authorization_id, state, scope_key, lease_id, capability_id,
  worker_instance_id, fencing_token, budget_reservation_id,
  emergency_epoch, key_version, revocation_version,
  permission_version, policy_version, issued_at_ms, expires_at_ms,
  consumed_at_ms
) VALUES (
  $15, 'ISSUED', $5, $7, $4,
  $6, $8, $3,
  $9, $10, $11,
  $12, $13, $14, $16,
  NULL
);

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $17, $18, $14, 'SEND_AUTHORIZED', 'ALLOW',
  $15, $19, $20
);

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $18,
    last_event_digest = $20
WHERE singleton_id = 1
  AND last_sequence = $18 - 1
  AND last_event_digest IS NOT DISTINCT FROM $19;

COMMIT;

-- $16 must be less than Lease expiry, Resource/Authorization budget expiry and
-- no more than five seconds after $14.
-- ===== END 40-send-authorization-issuance.sql =====

-- ===== BEGIN 50-send-authorization-consume.sql =====
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Final Send Authorization consumption transaction.
-- The trusted Egress component performs the network write only after COMMIT.

BEGIN ISOLATION LEVEL READ COMMITTED;

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
      AND $14 - worker.heartbeat_at_ms <= 15000
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
  AND lease.worker_instance_id = $6
  AND lease.fencing_token = $8;

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

-- COMMIT linearizes the local one-use permission. It does not prove Provider
-- receipt. The trusted Egress performs one write after this commit. Any crash,
-- lost response or uncertain external result becomes SEND_OUTCOME_UNKNOWN;
-- the permit must never be replayed and the budget must not be auto-released.

-- Final Egress pre-write check. This is a fresh central read performed after
-- the permit-consumption commit and immediately before the one socket write.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT scope_key, current_fencing_token, current_worker_id,
       current_lease_id, current_capability_id, version, state
FROM trust_r4_resource_fencing
WHERE scope_key = $5
FOR UPDATE;

SELECT permit.send_authorization_id, permit.state AS permit_state,
       permit.scope_key, permit.lease_id, permit.capability_id,
       permit.worker_instance_id, permit.fencing_token,
       permit.emergency_epoch, permit.key_version, permit.revocation_version,
       permit.permission_version, permit.policy_version,
       permit.consumed_at_ms, permit.expires_at_ms,
       lease.state AS lease_state,
       emergency.status AS emergency_status,
       emergency.epoch AS emergency_epoch_now,
       key.state AS key_state,
       key.key_version AS key_version_now,
       key.revocation_version AS revocation_version_now
FROM trust_r4_send_authorization permit
JOIN trust_r4_execution_lease lease ON lease.lease_id = permit.lease_id
JOIN trust_r3_emergency_control emergency ON emergency.singleton_id = 1
JOIN trust_r3_identity_key key ON key.key_id = $1
WHERE permit.send_authorization_id = $15
  AND permit.state = 'CONSUMED'
  AND permit.scope_key = $5
  AND permit.worker_instance_id = $6
  AND permit.lease_id = $7
  AND permit.capability_id = $4
  AND permit.fencing_token = $8
  AND lease.state = 'SENT'
  AND emergency.status = 'NORMAL'
  AND emergency.epoch = $9
  AND key.state = 'ACTIVE'
  AND key.key_version = $10
  AND key.revocation_version = $11
  AND $20 >= permit.consumed_at_ms
  AND $20 < permit.expires_at_ms
  AND $20 < lease.expires_at_ms
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

-- The Egress component must require exactly one returned row. If central
-- authority is unavailable or this query fails, it performs no network write.
-- A takeover committed after this check can still race with the socket write.

COMMIT;
-- ===== END 50-send-authorization-consume.sql =====

````
<!-- END_EXACT_SOURCE id=S033 -->

### S034. preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SHA256SUMS.txt

- Category: `E_R3F_ARTIFACT`
- Path: `preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SHA256SUMS.txt`
- Bytes: `5233`
- SHA-256: `581C7B8D543ACB813039F019CE9CEECB3E65E0EFA740E2D5978C771A60076D80`
- Description: Required consolidated artifact

<!-- BEGIN_EXACT_SOURCE id=S034 sha256=581C7B8D543ACB813039F019CE9CEECB3E65E0EFA740E2D5978C771A60076D80 bytes=5233 fence=fenced -->
````text
# PHASE_R3_FENCING_REMEDIATION_SHA256SUMS
# STATUS=R3_FENCING_REMEDIATION_PASS
# ENTRIES=34
# MANIFEST_SELF_HASH=EXCLUDED_BY_DEFINITION

18F7A37FC271C2AEAFFAF1F71419BAF9474A00E8987EF26EE63C956D8E1BBA12  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE.md
C013857E3F4A8C38E49ACCCF2B3FC6AC19DA7002B72D0F6D45D606966E39B050  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_BASELINE_SHA256SUMS.txt
F43185B267AB79ED23C9D29DD57EB69FF31517F1DFE043E2614F4F6946834650  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CONTRACT.md
8E455E4299C7687D634EC3AEE4ACC2C80D9252AAB5E9D6EB9C1C0DDB2AFAA016  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_CROSS_REVIEW.md
45DC3E67B086C92AF9ADF8C44AE8ECD17C7E9E7595401A1C6213B589C16A8E94  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_DIFF.md
8A2D510E772B1CE0B2EC724FBB902F11D9C19230EBBA46480DA10C49898FBED4  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_FINAL_REPORT.md
D5D1B28AAC2727F1841AB0A0940EFA623A48730319A6EDFFE82833286F78F18F  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_MODEL.md
3A1F3BFD5BB6B4BFE28F7D9FE71D719B2BF8799CE8E1193CE37AA4EFC88A455D  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_RISK_REGISTER.md
76C6D0E62BE3801D9A0725114F8B1EA7BD9DAE477B820A49A5417C7525C789A4  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SCHEMA.sql
E6CED6736E59AA4AE2CBDE965380CD4BF76765A67393BF32344FDF6E70D73986  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_SQL_REVIEW.md
633F8F15D83167C9D9D5D5B233177D7FFBFC47A3FAFDD3221866D7DB4420392A  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TEST_MATRIX.md
BAFCAC5051A6C73197255849F25409F0AB2B40806F727FA71EC0709A82F1D097  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_THREAT_MODEL.md
512E790234B41699AF72DCDE172F4CF247911DE02E9C04915D985ED5C739D8B1  preparation\production-trust\r3-fencing-remediation\PHASE_R3_FENCING_REMEDIATION_TRANSACTIONS.sql
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
````
<!-- END_EXACT_SOURCE id=S034 -->

### S035. preparation/production-trust/r2-r3-remediation/contracts.ts

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/contracts.ts`
- Bytes: `12209`
- SHA-256: `905F300FFDBD9C31545F775F126ADB2AC6186EC997D4E4A3A0642F53735D8B5D`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S035 sha256=905F300FFDBD9C31545F775F126ADB2AC6186EC997D4E4A3A0642F53735D8B5D bytes=12209 fence=fenced -->
````typescript
import { z } from "zod";

import {
  InstantSchema,
  Sha256Schema,
  UuidSchema,
} from "../contracts/common";

export const R3_CONTRACT_VERSION = "p1-p8-r2-r3-security-v1";

const IdentifierSchema = z.string().min(1).max(200).trim();
const VersionSchema = z.number().int().positive();
const EpochSchema = z.number().int().nonnegative();
const SafeIntegerSchema = z.number().int().nonnegative().max(
  Number.MAX_SAFE_INTEGER,
);
const HashSchema = Sha256Schema;
const TimeSchema = InstantSchema;
const IdSchema = UuidSchema;

export const R3FailureCodeSchema = z.enum([
  "APPROVAL_STATE_INVALID",
  "APPROVAL_EXPIRED",
  "APPROVAL_ALREADY_CONSUMED",
  "REQUEST_BINDING_MISMATCH",
  "CONSUMPTION_COMMIT_UNKNOWN",
  "CONSUMPTION_UNIQUE_CONFLICT",
  "CONSUMPTION_AUDIT_FAILED",
  "KEY_REVOKED",
  "KEY_VERSION_MISMATCH",
  "EMERGENCY_STOP_ACTIVE",
  "EMERGENCY_EPOCH_MISMATCH",
  "BUDGET_EXCEEDED",
  "BUDGET_VERSION_MISMATCH",
  "BUDGET_RESERVATION_CONFLICT",
  "BUDGET_RESERVATION_EXPIRED",
  "BUDGET_RELEASE_FORBIDDEN",
  "BUDGET_UNKNOWN_OUTCOME",
  "FENCING_ALLOCATION_FAILED",
  "FENCING_TOKEN_STALE",
  "WORKER_NOT_ACTIVE",
  "LEASE_STATE_INVALID",
  "LEASE_EXPIRED",
  "LEASE_REVOKED",
  "LEASE_BINDING_MISMATCH",
  "SEND_AUTHORIZATION_DENIED",
  "SEND_AUTHORIZATION_REPLAYED",
  "SEND_AUTHORIZATION_EXPIRED",
  "SEND_AUTHORIZATION_CONTEXT_MISMATCH",
  "SEND_OUTCOME_UNKNOWN",
  "ROW_COUNT_CONFLICT",
  "AUDIT_CHAIN_CONFLICT",
  "AUDIT_EVENT_DUPLICATE",
  "TRANSACTION_RETRY_EXHAUSTED",
]);

export type R3FailureCode = z.infer<typeof R3FailureCodeSchema>;

export type R3Result<T> =
  | Readonly<{ ok: true; value: T }>
  | Readonly<{ ok: false; code: R3FailureCode }>;

export function ok<T>(value: T): R3Result<T> {
  return Object.freeze({ ok: true, value });
}

export function fail<T = never>(code: R3FailureCode): R3Result<T> {
  return Object.freeze({ ok: false, code });
}

export function requireExactlyOne(
  affectedRows: number,
): R3Result<1> {
  return affectedRows === 1 ? ok(1 as const) : fail("ROW_COUNT_CONFLICT");
}

export const EmergencyStateSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-emergency-state-v1"),
  status: z.enum(["NORMAL", "DRAINING", "STOPPED", "RECOVERY_PENDING"]),
  epoch: EpochSchema,
  version: VersionSchema,
  reasonCode: IdentifierSchema.nullable(),
  recoveryRequestedByActorId: IdSchema.nullable(),
  recoveryApprovedByActorId: IdSchema.nullable(),
});

export const KeyStateSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-key-state-v1"),
  keyId: IdentifierSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  state: z.enum([
    "REGISTERED",
    "ACTIVE",
    "RETIRING",
    "RETIRED",
    "REVOKED",
    "EXPIRED",
    "RECOVERY_REQUIRED",
  ]),
  validFrom: TimeSchema,
  expiresAt: TimeSchema,
});

export const ApprovalBindingSchema = z.strictObject({
  approvalId: IdSchema,
  approvalVersion: VersionSchema,
  actorId: IdSchema,
  organizationId: IdSchema,
  leadId: IdSchema,
  signedApprovalDigest: HashSchema,
  identityDigest: HashSchema,
  evidenceDigest: HashSchema,
  snapshotDigest: HashSchema,
  dossierDigest: HashSchema,
  targetDigest: HashSchema,
  nonceDigest: HashSchema,
  keyId: IdentifierSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  emergencyEpoch: EpochSchema,
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
});

export const ApprovalConsumptionRequestSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-approval-consumption-request-v1"),
  requestId: IdSchema,
  binding: ApprovalBindingSchema,
  consumedAt: TimeSchema,
});

export const ApprovalConsumptionStatusSchema = z.enum([
  "CONSUMED",
  "ALREADY_CONSUMED_SAME_REQUEST",
  "ALREADY_CONSUMED_OTHER_REQUEST",
  "REQUEST_BINDING_MISMATCH",
  "COMMIT_UNKNOWN",
  "REJECTED",
]);

export const ApprovalConsumptionRecordSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-approval-consumption-record-v1"),
  status: ApprovalConsumptionStatusSchema,
  approvalId: IdSchema,
  approvalVersion: VersionSchema,
  consumptionId: IdSchema,
  requestId: IdSchema,
  actorId: IdSchema,
  organizationId: IdSchema,
  leadId: IdSchema,
  signedApprovalDigest: HashSchema,
  identityDigest: HashSchema,
  evidenceDigest: HashSchema,
  snapshotDigest: HashSchema,
  dossierDigest: HashSchema,
  targetDigest: HashSchema,
  nonceDigest: HashSchema,
  keyId: IdentifierSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  emergencyEpoch: EpochSchema,
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
  consumedAt: TimeSchema,
  auditEventId: IdSchema,
});

export const BudgetControlSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-budget-control-v1"),
  singletonId: z.literal(1),
  maxTotalRequests: z.number().int().positive(),
  reservedRequests: z.number().int().nonnegative(),
  consumedRequests: z.number().int().nonnegative(),
  maxUsdMicros: SafeIntegerSchema,
  reservedUsdMicros: SafeIntegerSchema,
  consumedUsdMicros: SafeIntegerSchema,
  budgetVersion: VersionSchema,
  updatedAt: TimeSchema,
}).superRefine((value, context) => {
  if (value.reservedRequests + value.consumedRequests > value.maxTotalRequests) {
    context.addIssue({
      code: "custom",
      path: ["maxTotalRequests"],
      message: "REQUEST_COUNTER_EXCEEDS_LIMIT",
    });
  }
  if (value.reservedUsdMicros + value.consumedUsdMicros > value.maxUsdMicros) {
    context.addIssue({
      code: "custom",
      path: ["maxUsdMicros"],
      message: "USD_COUNTER_EXCEEDS_LIMIT",
    });
  }
});

export const BudgetReservationStateSchema = z.enum([
  "RESERVED",
  "COMMITTED",
  "RELEASED_BEFORE_SEND",
  "UNKNOWN",
  "SETTLED",
]);

export const BudgetReservationSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-budget-reservation-v1"),
  reservationId: IdSchema,
  executionAuthorizationId: IdSchema,
  consumptionId: IdSchema,
  capabilityId: IdSchema,
  workerInstanceId: IdSchema,
  state: BudgetReservationStateSchema,
  requestCount: z.literal(1),
  reservedUsdMicros: SafeIntegerSchema,
  actualUsdMicros: SafeIntegerSchema.nullable(),
  budgetVersion: VersionSchema,
  sendStartedAt: TimeSchema.nullable(),
  createdAt: TimeSchema,
  expiresAt: TimeSchema,
  settledAt: TimeSchema.nullable(),
});

export const ExecutionAuthorizationSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-execution-authorization-v1"),
  authorizationId: IdSchema,
  consumptionId: IdSchema,
  approvalId: IdSchema,
  actorId: IdSchema,
  organizationId: IdSchema,
  leadId: IdSchema,
  signedApprovalDigest: HashSchema,
  identityDigest: HashSchema,
  evidenceDigest: HashSchema,
  snapshotDigest: HashSchema,
  dossierDigest: HashSchema,
  targetDigest: HashSchema,
  providerKind: z.literal("fetch"),
  purpose: z.literal("fetch_only"),
  budgetReservationId: IdSchema,
  capabilityId: IdSchema,
  keyId: IdentifierSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  emergencyEpoch: EpochSchema,
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
  issuedAt: TimeSchema,
  expiresAt: TimeSchema,
  state: z.enum(["ACTIVE", "EXHAUSTED", "REVOKED", "EXPIRED"]),
});

export const CapabilityBindingSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-capability-binding-v1"),
  capabilityId: IdSchema,
  executionAuthorizationId: IdSchema,
  consumptionId: IdSchema,
  approvalId: IdSchema,
  workerInstanceId: IdSchema,
  budgetReservationId: IdSchema,
  signedApprovalDigest: HashSchema,
  identityDigest: HashSchema,
  evidenceDigest: HashSchema,
  snapshotDigest: HashSchema,
  dossierDigest: HashSchema,
  targetDigest: HashSchema,
  keyId: IdentifierSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  emergencyEpoch: EpochSchema,
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
  expiresAt: TimeSchema,
});

export const WorkerRegistrationSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-worker-registration-v1"),
  workerInstanceId: IdSchema,
  state: z.enum(["ACTIVE", "DRAINING", "REVOKED"]),
  heartbeatAt: TimeSchema,
  fenceFloor: SafeIntegerSchema,
});

export const FencingAllocationSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-fencing-allocation-v1"),
  fencingToken: SafeIntegerSchema.refine((value) => value > 0),
  workerInstanceId: IdSchema,
  leaseId: IdSchema,
  allocatedAt: TimeSchema,
  allocatorName: z.literal("trust_r3_fencing_control"),
  allocationMode: z.literal("row_locked_monotonic_counter"),
});

export const ExecutionLeaseStateSchema = z.enum([
  "ISSUED",
  "KEY_READ",
  "TRANSPORT_CREATED",
  "SEND_AUTHORIZED",
  "SENT",
  "RESPONSE_RECEIVED",
  "COMPLETED",
  "FAILED_BEFORE_SEND",
  "SEND_OUTCOME_UNKNOWN",
  "FAILED_AFTER_SEND",
  "EXPIRED",
  "REVOKED",
  "EMERGENCY_BLOCKED",
]);

export const ExecutionLeaseSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-execution-lease-v1"),
  leaseId: IdSchema,
  capabilityId: IdSchema,
  executionAuthorizationId: IdSchema,
  budgetReservationId: IdSchema,
  workerInstanceId: IdSchema,
  fencingToken: SafeIntegerSchema.refine((value) => value > 0),
  state: ExecutionLeaseStateSchema,
  issuedAt: TimeSchema,
  expiresAt: TimeSchema,
  emergencyEpoch: EpochSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
});

export const SendAuthorizationStateSchema = z.enum([
  "ISSUED",
  "CONSUMED",
  "EXPIRED",
  "REVOKED",
]);

export const SendAuthorizationSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-send-authorization-v1"),
  sendAuthorizationId: IdSchema,
  state: SendAuthorizationStateSchema,
  leaseId: IdSchema,
  capabilityId: IdSchema,
  workerInstanceId: IdSchema,
  fencingToken: SafeIntegerSchema.refine((value) => value > 0),
  budgetReservationId: IdSchema,
  emergencyEpoch: EpochSchema,
  keyVersion: VersionSchema,
  revocationVersion: EpochSchema,
  permissionVersion: VersionSchema,
  policyVersion: IdentifierSchema,
  issuedAt: TimeSchema,
  expiresAt: TimeSchema,
  consumedAt: TimeSchema.nullable(),
});

export const AuditEventSchema = z.strictObject({
  schemaVersion: z.literal("r2-r3-audit-event-v1"),
  eventId: IdSchema,
  sequence: z.number().int().positive(),
  occurredAt: TimeSchema,
  eventType: z.enum([
    "APPROVAL_CONSUMED",
    "BUDGET_RESERVED",
    "BUDGET_SEND_STARTED",
    "BUDGET_COMMITTED",
    "BUDGET_RELEASED",
    "BUDGET_SETTLED",
    "LEASE_ISSUED",
    "WORKER_PROGRESS",
    "SEND_AUTHORIZED",
    "SEND_AUTHORIZATION_CONSUMED",
    "REQUEST_SENT",
    "SEND_OUTCOME_UNKNOWN",
    "RESPONSE_RECEIVED",
    "EMERGENCY_ACTIVATED",
    "EMERGENCY_RECOVERY_REQUESTED",
    "EMERGENCY_RECOVERY_APPROVED",
    "KEY_REVOKED",
  ]),
  outcome: z.enum(["ALLOW", "BLOCK", "FAILED", "UNKNOWN"]),
  subjectId: IdSchema,
  previousEventDigest: HashSchema.nullable(),
});

export const StoredAuditEventSchema = z.strictObject({
  event: AuditEventSchema,
  eventDigest: HashSchema,
});

export type EmergencyState = z.infer<typeof EmergencyStateSchema>;
export type KeyState = z.infer<typeof KeyStateSchema>;
export type ApprovalBinding = z.infer<typeof ApprovalBindingSchema>;
export type ApprovalConsumptionRequest = z.infer<
  typeof ApprovalConsumptionRequestSchema
>;
export type ApprovalConsumptionRecord = z.infer<
  typeof ApprovalConsumptionRecordSchema
>;
export type BudgetControl = z.infer<typeof BudgetControlSchema>;
export type BudgetReservation = z.infer<typeof BudgetReservationSchema>;
export type ExecutionAuthorization = z.infer<
  typeof ExecutionAuthorizationSchema
>;
export type CapabilityBinding = z.infer<typeof CapabilityBindingSchema>;
export type WorkerRegistration = z.infer<typeof WorkerRegistrationSchema>;
export type FencingAllocation = z.infer<typeof FencingAllocationSchema>;
export type ExecutionLeaseState = z.infer<
  typeof ExecutionLeaseStateSchema
>;
export type ExecutionLease = z.infer<typeof ExecutionLeaseSchema>;
export type SendAuthorization = z.infer<typeof SendAuthorizationSchema>;
export type AuditEvent = z.infer<typeof AuditEventSchema>;
export type StoredAuditEvent = z.infer<typeof StoredAuditEventSchema>;
````
<!-- END_EXACT_SOURCE id=S035 -->

### S036. preparation/production-trust/r2-r3-remediation/lock-order.ts

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/lock-order.ts`
- Bytes: `2260`
- SHA-256: `BFBE3374B1BCB5521D52FC9191CD42CBAD77AC43A67FD9AF84202001CD5344EA`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S036 sha256=BFBE3374B1BCB5521D52FC9191CD42CBAD77AC43A67FD9AF84202001CD5344EA bytes=2260 fence=fenced -->
````typescript
import { z } from "zod";

import {
  fail,
  ok,
  type R3Result,
} from "./contracts";

export const R3_LOCK_ORDER = Object.freeze([
  "EMERGENCY_CONTROL",
  "KEY_REGISTRY",
  "APPROVAL",
  "APPROVAL_CONSUMPTION",
  "EXECUTION_AUTHORIZATION",
  "BUDGET_CONTROL",
  "BUDGET_RESERVATION",
  "CAPABILITY",
  "FENCING_SEQUENCE",
  "WORKER_REGISTRATION",
  "EXECUTION_LEASE",
  "SEND_AUTHORIZATION",
  "AUDIT_SEQUENCE",
] as const);

export type R3LockDomain = typeof R3_LOCK_ORDER[number];

const LockAcquisitionSchema = z.strictObject({
  domain: z.enum(R3_LOCK_ORDER),
  acquiredAt: z.number().int().nonnegative(),
});

export function validateR3LockOrder(
  acquisitions: readonly unknown[],
): R3Result<readonly R3LockDomain[]> {
  const parsed = z.array(LockAcquisitionSchema).safeParse(acquisitions);
  if (!parsed.success) return fail("ROW_COUNT_CONFLICT");
  let previous = -1;
  const domains: R3LockDomain[] = [];
  for (const acquisition of parsed.data) {
    const current = R3_LOCK_ORDER.indexOf(acquisition.domain);
    if (current < previous) return fail("ROW_COUNT_CONFLICT");
    previous = current;
    domains.push(acquisition.domain);
  }
  return ok(Object.freeze(domains));
}

export class R3RetryableTransactionError extends Error {
  constructor(
    readonly code:
      | "DEADLOCK_DETECTED"
      | "SERIALIZATION_FAILURE"
      | "TRANSIENT_CONNECTION_FAILURE",
  ) {
    super(code);
    this.name = "R3RetryableTransactionError";
  }
}

export async function retryR3Transaction<T>(input: {
  maxAttempts: number;
  externalAttemptStarted: boolean;
  run: (attempt: number) => Promise<T>;
}): Promise<R3Result<T>> {
  if (input.externalAttemptStarted) return fail("SEND_OUTCOME_UNKNOWN");
  if (
    !Number.isInteger(input.maxAttempts)
    || input.maxAttempts < 1
    || input.maxAttempts > 3
  ) {
    return fail("TRANSACTION_RETRY_EXHAUSTED");
  }
  for (let attempt = 1; attempt <= input.maxAttempts; attempt += 1) {
    try {
      return ok(await input.run(attempt));
    } catch (error) {
      if (
        !(error instanceof R3RetryableTransactionError)
        || attempt === input.maxAttempts
      ) {
        return fail("TRANSACTION_RETRY_EXHAUSTED");
      }
    }
  }
  return fail("TRANSACTION_RETRY_EXHAUSTED");
}
````
<!-- END_EXACT_SOURCE id=S036 -->

### S037. preparation/production-trust/r2-r3-remediation/models/fencing-registry.ts

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/models/fencing-registry.ts`
- Bytes: `5510`
- SHA-256: `58CF8B73866D8107FD01835617E3D554016060DD92FF8E20B12FF21685178D55`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S037 sha256=58CF8B73866D8107FD01835617E3D554016060DD92FF8E20B12FF21685178D55 bytes=5510 fence=fenced -->
````typescript
import {
  FencingAllocationSchema,
  WorkerRegistrationSchema,
  fail,
  ok,
  type FencingAllocation,
  type R3Result,
  type WorkerRegistration,
} from "../contracts";

type SharedState = {
  nextToken: number;
  controlVersion: number;
  authorityAvailable: boolean;
  workers: Map<string, WorkerRegistration>;
  resourceFloors: Map<string, number>;
  allocations: Map<string, FencingAllocation>;
};

/**
 * OFFLINE_REFERENCE_MODEL.
 * Models a persistent singleton row lock behind a serialized method. It does
 * not claim PostgreSQL behavior.
 */
export class OfflineFencingRegistry {
  private readonly shared: SharedState;

  constructor(shared?: OfflineFencingRegistry) {
    this.shared = shared?.shared ?? {
      nextToken: 1,
      controlVersion: 1,
      authorityAvailable: true,
      workers: new Map(),
      resourceFloors: new Map(),
      allocations: new Map(),
    };
  }

  connect(): OfflineFencingRegistry {
    return new OfflineFencingRegistry(this);
  }

  setAuthorityAvailable(available: boolean): void {
    this.shared.authorityAvailable = available;
  }

  registerWorker(input: {
    workerInstanceId: string;
    heartbeatAt: number;
  }): R3Result<WorkerRegistration> {
    const existing = this.shared.workers.get(input.workerInstanceId);
    const worker = WorkerRegistrationSchema.parse({
      schemaVersion: "r2-r3-worker-registration-v1",
      workerInstanceId: input.workerInstanceId,
      state: "ACTIVE",
      heartbeatAt: input.heartbeatAt,
      fenceFloor: existing?.fenceFloor ?? 0,
    });
    this.shared.workers.set(input.workerInstanceId, worker);
    return ok(worker);
  }

  heartbeat(input: {
    workerInstanceId: string;
    now: number;
  }): R3Result<WorkerRegistration> {
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker || worker.state !== "ACTIVE") {
      return fail("WORKER_NOT_ACTIVE");
    }
    const updated = WorkerRegistrationSchema.parse({
      ...worker,
      heartbeatAt: input.now,
    });
    this.shared.workers.set(input.workerInstanceId, updated);
    return ok(updated);
  }

  revokeWorker(input: {
    workerInstanceId: string;
  }): R3Result<WorkerRegistration> {
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker) return fail("WORKER_NOT_ACTIVE");
    const updated = WorkerRegistrationSchema.parse({
      ...worker,
      state: "REVOKED",
    });
    this.shared.workers.set(input.workerInstanceId, updated);
    return ok(updated);
  }

  allocate(input: {
    leaseId: string;
    resourceId: string;
    workerInstanceId: string;
    now: number;
    expectedControlVersion: number;
  }): R3Result<FencingAllocation> {
    if (
      !this.shared.authorityAvailable
      || !Number.isSafeInteger(input.now)
      || input.now < 0
    ) {
      return fail("FENCING_ALLOCATION_FAILED");
    }
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker || worker.state !== "ACTIVE") {
      return fail("WORKER_NOT_ACTIVE");
    }
    if (input.expectedControlVersion !== this.shared.controlVersion) {
      return fail("FENCING_ALLOCATION_FAILED");
    }
    if (this.shared.allocations.has(input.leaseId)) {
      return fail("FENCING_ALLOCATION_FAILED");
    }
    const fencingToken = this.shared.nextToken;
    if (!Number.isSafeInteger(fencingToken) || fencingToken <= 0) {
      return fail("FENCING_ALLOCATION_FAILED");
    }
    const allocation = FencingAllocationSchema.parse({
      schemaVersion: "r2-r3-fencing-allocation-v1",
      fencingToken,
      workerInstanceId: input.workerInstanceId,
      leaseId: input.leaseId,
      allocatedAt: input.now,
      allocatorName: "trust_r3_fencing_control",
      allocationMode: "row_locked_monotonic_counter",
    });
    this.shared.nextToken += 1;
    this.shared.controlVersion += 1;
    this.shared.resourceFloors.set(input.resourceId, fencingToken);
    this.shared.allocations.set(input.leaseId, allocation);
    this.shared.workers.set(input.workerInstanceId, WorkerRegistrationSchema.parse({
      ...worker,
      fenceFloor: Math.max(worker.fenceFloor, fencingToken),
    }));
    return ok(allocation);
  }

  authorizeResourceWrite(input: {
    resourceId: string;
    allocation: unknown;
    workerInstanceId: string;
    now: number;
  }): R3Result<true> {
    if (!this.shared.authorityAvailable) {
      return fail("FENCING_ALLOCATION_FAILED");
    }
    const parsed = FencingAllocationSchema.safeParse(input.allocation);
    if (!parsed.success) return fail("FENCING_TOKEN_STALE");
    const currentFloor = this.shared.resourceFloors.get(input.resourceId);
    if (
      parsed.data.fencingToken !== currentFloor
      || parsed.data.workerInstanceId !== input.workerInstanceId
    ) {
      return fail("FENCING_TOKEN_STALE");
    }
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker || worker.state !== "ACTIVE" || input.now - worker.heartbeatAt > 15_000) {
      return fail("WORKER_NOT_ACTIVE");
    }
    return ok(true as const);
  }

  snapshot(): Readonly<{
    nextToken: number;
    controlVersion: number;
    authorityAvailable: boolean;
    resourceFloors: Readonly<Record<string, number>>;
  }> {
    return Object.freeze({
      nextToken: this.shared.nextToken,
      controlVersion: this.shared.controlVersion,
      authorityAvailable: this.shared.authorityAvailable,
      resourceFloors: Object.freeze(
        Object.fromEntries(this.shared.resourceFloors),
      ),
    });
  }
}
````
<!-- END_EXACT_SOURCE id=S037 -->

### S038. preparation/production-trust/r2-r3-remediation/models/execution-lease.ts

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/models/execution-lease.ts`
- Bytes: `28892`
- SHA-256: `BA86F24E1FDC9E2862A83E6ECEAA02B54F237AFEE34542EB6BA23FCBC5802AB1`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S038 sha256=BA86F24E1FDC9E2862A83E6ECEAA02B54F237AFEE34542EB6BA23FCBC5802AB1 bytes=28892 fence=fenced -->
````typescript
import { randomUUID } from "node:crypto";

import {
  BudgetReservationSchema,
  CapabilityBindingSchema,
  EmergencyStateSchema,
  ExecutionAuthorizationSchema,
  ExecutionLeaseSchema,
  FencingAllocationSchema,
  KeyStateSchema,
  SendAuthorizationSchema,
  WorkerRegistrationSchema,
  fail,
  ok,
  requireExactlyOne,
  type BudgetReservation,
  type CapabilityBinding,
  type EmergencyState,
  type ExecutionAuthorization,
  type ExecutionLease,
  type ExecutionLeaseState,
  type FencingAllocation,
  type KeyState,
  type R3Result,
  type SendAuthorization,
  type WorkerRegistration,
} from "../contracts";

export type FencingAllocator = Readonly<{
  allocate(input: {
    workerInstanceId: string;
    leaseId: string;
    resourceId: string;
    now: number;
    expectedControlVersion: number;
  }): R3Result<FencingAllocation>;
}>;

type CapabilityState = "ISSUED" | "RESERVED" | "REVOKED" | "EXPIRED";

type SharedState = {
  globalFenceCeiling: number;
  emergency: EmergencyState;
  keys: Map<string, KeyState>;
  capabilities: Map<string, CapabilityBinding>;
  capabilityStates: Map<string, CapabilityState>;
  authorizations: Map<string, ExecutionAuthorization>;
  reservations: Map<string, BudgetReservation>;
  workers: Map<string, WorkerRegistration>;
  leases: Map<string, ExecutionLease>;
  leaseByCapability: Map<string, string>;
  sendAuthorizations: Map<string, SendAuthorization>;
  sendAuthorizationByLease: Map<string, string>;
};

const INITIAL_EMERGENCY: EmergencyState = {
  schemaVersion: "r2-r3-emergency-state-v1",
  status: "NORMAL",
  epoch: 3,
  version: 1,
  reasonCode: null,
  recoveryRequestedByActorId: null,
  recoveryApprovedByActorId: null,
};

const ALLOWED_PROGRESS: Readonly<
  Record<"KEY_READ" | "TRANSPORT_CREATED", ExecutionLeaseState>
> = Object.freeze({
  KEY_READ: "ISSUED",
  TRANSPORT_CREATED: "KEY_READ",
});

/**
 * OFFLINE_REFERENCE_MODEL.
 *
 * The model separates Lease Issuance, Worker Progress, Send Authorization
 * Issuance and Send Authorization Consumption. It is a synchronous shared
 * object model, not PostgreSQL and not a cross-process coordinator.
 */
export class OfflineExecutionLeaseModel {
  private readonly shared: SharedState;

  constructor(shared?: OfflineExecutionLeaseModel) {
    this.shared = shared?.shared ?? {
      globalFenceCeiling: 0,
      emergency: INITIAL_EMERGENCY,
      keys: new Map(),
      capabilities: new Map(),
      capabilityStates: new Map(),
      authorizations: new Map(),
      reservations: new Map(),
      workers: new Map(),
      leases: new Map(),
      leaseByCapability: new Map(),
      sendAuthorizations: new Map(),
      sendAuthorizationByLease: new Map(),
    };
  }

  connect(): OfflineExecutionLeaseModel {
    return new OfflineExecutionLeaseModel(this);
  }

  seedEmergency(raw: unknown): R3Result<EmergencyState> {
    const parsed = EmergencyStateSchema.safeParse(raw);
    if (!parsed.success) return fail("EMERGENCY_EPOCH_MISMATCH");
    this.shared.emergency = Object.freeze(parsed.data);
    return ok(this.shared.emergency);
  }

  seedKey(raw: unknown): R3Result<KeyState> {
    const parsed = KeyStateSchema.safeParse(raw);
    if (!parsed.success) return fail("KEY_VERSION_MISMATCH");
    this.shared.keys.set(parsed.data.keyId, Object.freeze(parsed.data));
    return ok(parsed.data);
  }

  seedCapability(
    raw: unknown,
    state: CapabilityState = "ISSUED",
  ): R3Result<CapabilityBinding> {
    const parsed = CapabilityBindingSchema.safeParse(raw);
    if (!parsed.success) return fail("LEASE_BINDING_MISMATCH");
    if (this.shared.capabilities.has(parsed.data.capabilityId)) {
      return fail("LEASE_BINDING_MISMATCH");
    }
    this.shared.capabilities.set(
      parsed.data.capabilityId,
      Object.freeze(parsed.data),
    );
    this.shared.capabilityStates.set(parsed.data.capabilityId, state);
    return ok(parsed.data);
  }

  seedAuthorization(raw: unknown): R3Result<ExecutionAuthorization> {
    const parsed = ExecutionAuthorizationSchema.safeParse(raw);
    if (!parsed.success || this.shared.authorizations.has(
      parsed.data.authorizationId,
    )) {
      return fail("LEASE_BINDING_MISMATCH");
    }
    this.shared.authorizations.set(
      parsed.data.authorizationId,
      Object.freeze(parsed.data),
    );
    return ok(parsed.data);
  }

  seedReservation(raw: unknown): R3Result<BudgetReservation> {
    const parsed = BudgetReservationSchema.safeParse(raw);
    if (!parsed.success || this.shared.reservations.has(
      parsed.data.reservationId,
    )) {
      return fail("BUDGET_RESERVATION_CONFLICT");
    }
    this.shared.reservations.set(
      parsed.data.reservationId,
      Object.freeze(parsed.data),
    );
    return ok(parsed.data);
  }

  registerWorker(input: {
    workerInstanceId: string;
    resourceId: string;
    expectedFencingControlVersion: number;
    now: number;
  }): R3Result<WorkerRegistration> {
    const existing = this.shared.workers.get(input.workerInstanceId);
    if (existing?.state === "ACTIVE") {
      return ok(existing);
    }
    const parsed = WorkerRegistrationSchema.safeParse({
      schemaVersion: "r2-r3-worker-registration-v1",
      workerInstanceId: input.workerInstanceId,
      state: "ACTIVE",
      heartbeatAt: input.now,
      fenceFloor: existing?.fenceFloor ?? 0,
    });
    if (!parsed.success) return fail("WORKER_NOT_ACTIVE");
    this.shared.workers.set(
      parsed.data.workerInstanceId,
      Object.freeze(parsed.data),
    );
    return ok(parsed.data);
  }

  heartbeat(workerInstanceId: string, now: number): R3Result<true> {
    const worker = this.shared.workers.get(workerInstanceId);
    if (!worker || worker.state !== "ACTIVE") {
      return fail("WORKER_NOT_ACTIVE");
    }
    this.shared.workers.set(workerInstanceId, Object.freeze({
      ...worker,
      heartbeatAt: now,
    }));
    return ok(true);
  }

  retireWorker(workerInstanceId: string): R3Result<WorkerRegistration> {
    const worker = this.shared.workers.get(workerInstanceId);
    if (!worker) return fail("WORKER_NOT_ACTIVE");
    const retired = Object.freeze({ ...worker, state: "REVOKED" as const });
    this.shared.workers.set(workerInstanceId, retired);
    this.revokePreSendForWorker(workerInstanceId);
    return ok(retired);
  }

  issueLease(input: {
    allocation: FencingAllocator;
    capability: unknown;
    authorization: unknown;
    reservation: unknown;
    key: unknown;
    workerInstanceId: string;
    resourceId: string;
    expectedFencingControlVersion: number;
    now: number;
    ttlMs: number;
  }): R3Result<ExecutionLease> {
    const capability = CapabilityBindingSchema.safeParse(input.capability);
    const authorization = ExecutionAuthorizationSchema.safeParse(
      input.authorization,
    );
    const reservation = BudgetReservationSchema.safeParse(input.reservation);
    const key = KeyStateSchema.safeParse(input.key);
    if (
      !capability.success
      || !authorization.success
      || !reservation.success
      || !key.success
    ) {
      return fail("LEASE_BINDING_MISMATCH");
    }
    const binding = this.validateBinding({
      capability: capability.data,
      authorization: authorization.data,
      reservation: reservation.data,
      key: key.data,
      workerInstanceId: input.workerInstanceId,
      now: input.now,
    });
    if (!binding.ok) return binding;

    const existingLeaseId = this.shared.leaseByCapability.get(
      capability.data.capabilityId,
    );
    if (existingLeaseId) {
      const existing = this.shared.leases.get(existingLeaseId);
      if (
        existing
        && existing.workerInstanceId === input.workerInstanceId
        && existing.state === "ISSUED"
      ) {
        return ok(existing);
      }
      return fail("LEASE_STATE_INVALID");
    }
    if (
      this.shared.capabilityStates.get(capability.data.capabilityId)
      !== "ISSUED"
    ) {
      return fail("LEASE_STATE_INVALID");
    }
    if (
      !Number.isSafeInteger(input.ttlMs)
      || input.ttlMs <= 0
      || input.ttlMs > 60_000
    ) {
      return fail("LEASE_STATE_INVALID");
    }

    const leaseId = randomUUID();
    const allocation = input.allocation.allocate({
      workerInstanceId: input.workerInstanceId,
      leaseId,
      resourceId: input.resourceId,
      now: input.now,
      expectedControlVersion: input.expectedFencingControlVersion,
    });
    if (!allocation.ok) return allocation;
    const parsedAllocation = FencingAllocationSchema.safeParse(
      allocation.value,
    );
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (
      !parsedAllocation.success
      || !worker
      || worker.state !== "ACTIVE"
      || parsedAllocation.data.leaseId !== leaseId
      || parsedAllocation.data.workerInstanceId !== input.workerInstanceId
      || parsedAllocation.data.fencingToken <= worker.fenceFloor
      || parsedAllocation.data.fencingToken <= this.shared.globalFenceCeiling
    ) {
      return fail("FENCING_ALLOCATION_FAILED");
    }

    const lease = ExecutionLeaseSchema.parse({
      schemaVersion: "r2-r3-execution-lease-v1",
      leaseId,
      capabilityId: capability.data.capabilityId,
      executionAuthorizationId: authorization.data.authorizationId,
      budgetReservationId: reservation.data.reservationId,
      workerInstanceId: input.workerInstanceId,
      fencingToken: parsedAllocation.data.fencingToken,
      state: "ISSUED",
      issuedAt: input.now,
      expiresAt: input.now + input.ttlMs,
      emergencyEpoch: capability.data.emergencyEpoch,
      keyVersion: capability.data.keyVersion,
      revocationVersion: capability.data.revocationVersion,
      permissionVersion: capability.data.permissionVersion,
      policyVersion: capability.data.policyVersion,
    });

    this.shared.globalFenceCeiling = lease.fencingToken;
    this.shared.capabilityStates.set(capability.data.capabilityId, "RESERVED");
    this.shared.workers.set(worker.workerInstanceId, Object.freeze({
      ...worker,
      fenceFloor: lease.fencingToken,
      heartbeatAt: input.now,
    }));
    this.shared.leases.set(lease.leaseId, Object.freeze(lease));
    this.shared.leaseByCapability.set(lease.capabilityId, lease.leaseId);
    return ok(lease);
  }

  progressLease(input: {
    leaseId: string;
    next: "KEY_READ" | "TRANSPORT_CREATED";
    workerInstanceId: string;
    fencingToken: number;
    key: unknown;
    reservation: unknown;
    now: number;
    rowCount: number;
  }): R3Result<ExecutionLease> {
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    const lease = this.shared.leases.get(input.leaseId);
    if (!lease) return fail("LEASE_STATE_INVALID");
    if (
      lease.state === input.next
      && lease.workerInstanceId === input.workerInstanceId
      && lease.fencingToken === input.fencingToken
    ) {
      const context = this.validateLeaseContext(lease, input);
      return context.ok ? ok(lease) : context;
    }
    if (ALLOWED_PROGRESS[input.next] !== lease.state) {
      return fail("LEASE_STATE_INVALID");
    }
    const context = this.validateLeaseContext(lease, input);
    if (!context.ok) return context;
    const updated = Object.freeze({ ...lease, state: input.next });
    this.shared.leases.set(lease.leaseId, updated);
    return ok(updated);
  }

  issueSendAuthorization(input: {
    leaseId: string;
    workerInstanceId: string;
    fencingToken: number;
    key: unknown;
    reservation: unknown;
    now: number;
    ttlMs: number;
  }): R3Result<SendAuthorization> {
    const lease = this.shared.leases.get(input.leaseId);
    if (!lease) return fail("LEASE_STATE_INVALID");
    const existingId = this.shared.sendAuthorizationByLease.get(
      input.leaseId,
    );
    if (existingId) {
      const existing = this.shared.sendAuthorizations.get(existingId);
      if (
        existing
        && existing.state === "ISSUED"
        && existing.workerInstanceId === input.workerInstanceId
        && existing.fencingToken === input.fencingToken
        && input.now < existing.expiresAt
      ) {
        return ok(existing);
      }
      return fail("SEND_AUTHORIZATION_REPLAYED");
    }
    if (lease.state !== "TRANSPORT_CREATED") {
      return fail("LEASE_STATE_INVALID");
    }
    const context = this.validateLeaseContext(lease, input);
    if (!context.ok) return context;
    if (
      !Number.isSafeInteger(input.ttlMs)
      || input.ttlMs <= 0
      || input.ttlMs > 5_000
    ) {
      return fail("SEND_AUTHORIZATION_DENIED");
    }
    const authorization = SendAuthorizationSchema.parse({
      schemaVersion: "r2-r3-send-authorization-v1",
      sendAuthorizationId: randomUUID(),
      state: "ISSUED",
      leaseId: lease.leaseId,
      capabilityId: lease.capabilityId,
      workerInstanceId: lease.workerInstanceId,
      fencingToken: lease.fencingToken,
      budgetReservationId: lease.budgetReservationId,
      emergencyEpoch: lease.emergencyEpoch,
      keyVersion: lease.keyVersion,
      revocationVersion: lease.revocationVersion,
      permissionVersion: lease.permissionVersion,
      policyVersion: lease.policyVersion,
      issuedAt: input.now,
      expiresAt: Math.min(lease.expiresAt, input.now + input.ttlMs),
      consumedAt: null,
    });
    const updatedLease = Object.freeze({
      ...lease,
      state: "SEND_AUTHORIZED" as const,
    });
    this.shared.leases.set(lease.leaseId, updatedLease);
    this.shared.sendAuthorizations.set(
      authorization.sendAuthorizationId,
      Object.freeze(authorization),
    );
    this.shared.sendAuthorizationByLease.set(
      lease.leaseId,
      authorization.sendAuthorizationId,
    );
    return ok(authorization);
  }

  consumeSendAuthorization(input: {
    sendAuthorizationId: string;
    workerInstanceId: string;
    fencingToken: number;
    key: unknown;
    reservation: unknown;
    now: number;
    rowCountSend: number;
    rowCountLease: number;
    rowCountBudget: number;
  }): R3Result<Readonly<{
    sendAuthorization: SendAuthorization;
    lease: ExecutionLease;
    reservation: BudgetReservation;
    externalOutcome: "PENDING";
  }>> {
    for (const rowCount of [
      input.rowCountSend,
      input.rowCountLease,
      input.rowCountBudget,
    ]) {
      const rows = requireExactlyOne(rowCount);
      if (!rows.ok) return rows;
    }
    const authorization = this.shared.sendAuthorizations.get(
      input.sendAuthorizationId,
    );
    if (!authorization) return fail("SEND_AUTHORIZATION_DENIED");
    if (authorization.state !== "ISSUED") {
      return fail("SEND_AUTHORIZATION_REPLAYED");
    }
    if (
      authorization.workerInstanceId !== input.workerInstanceId
      || authorization.fencingToken !== input.fencingToken
    ) {
      return fail("SEND_AUTHORIZATION_CONTEXT_MISMATCH");
    }
    if (input.now >= authorization.expiresAt) {
      return fail("SEND_AUTHORIZATION_EXPIRED");
    }
    const lease = this.shared.leases.get(authorization.leaseId);
    if (
      !lease
      || lease.state !== "SEND_AUTHORIZED"
      || lease.workerInstanceId !== authorization.workerInstanceId
      || lease.fencingToken !== authorization.fencingToken
    ) {
      return fail("LEASE_STATE_INVALID");
    }
    const context = this.validateLeaseContext(lease, input);
    if (!context.ok) return context;
    const reservation = this.shared.reservations.get(
      authorization.budgetReservationId,
    );
    if (
      !reservation
      || reservation.state !== "RESERVED"
      || reservation.sendStartedAt !== null
    ) {
      return fail("BUDGET_RELEASE_FORBIDDEN");
    }
    const consumedAuthorization = Object.freeze({
      ...authorization,
      state: "CONSUMED" as const,
      consumedAt: input.now,
    });
    const sentLease = Object.freeze({ ...lease, state: "SENT" as const });
    const startedReservation = Object.freeze({
      ...reservation,
      sendStartedAt: input.now,
    });
    this.shared.sendAuthorizations.set(
      consumedAuthorization.sendAuthorizationId,
      consumedAuthorization,
    );
    this.shared.leases.set(sentLease.leaseId, sentLease);
    this.shared.reservations.set(
      startedReservation.reservationId,
      startedReservation,
    );
    return ok(Object.freeze({
      sendAuthorization: consumedAuthorization,
      lease: sentLease,
      reservation: startedReservation,
      externalOutcome: "PENDING" as const,
    }));
  }

  recordNetworkResult(input: {
    leaseId: string;
    result: "RESPONSE_RECEIVED" | "SEND_OUTCOME_UNKNOWN" | "FAILED_AFTER_SEND";
  }): R3Result<ExecutionLease> {
    const lease = this.shared.leases.get(input.leaseId);
    if (!lease || lease.state !== "SENT") {
      return fail("LEASE_STATE_INVALID");
    }
    if (input.result === "RESPONSE_RECEIVED") {
      const received = Object.freeze({
        ...lease,
        state: "RESPONSE_RECEIVED" as const,
      });
      const completed = Object.freeze({
        ...received,
        state: "COMPLETED" as const,
      });
      this.shared.leases.set(lease.leaseId, completed);
      return ok(completed);
    }
    const terminal = Object.freeze({ ...lease, state: input.result });
    this.shared.leases.set(lease.leaseId, terminal);
    return input.result === "SEND_OUTCOME_UNKNOWN"
      ? ok(terminal)
      : ok(terminal);
  }

  failBeforeSend(input: {
    leaseId: string;
    rowCount: number;
  }): R3Result<ExecutionLease> {
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    const lease = this.shared.leases.get(input.leaseId);
    if (
      !lease
      || ![
        "ISSUED",
        "KEY_READ",
        "TRANSPORT_CREATED",
        "SEND_AUTHORIZED",
      ].includes(lease.state)
    ) {
      return fail("LEASE_STATE_INVALID");
    }
    const failed = Object.freeze({
      ...lease,
      state: "FAILED_BEFORE_SEND" as const,
    });
    this.shared.leases.set(lease.leaseId, failed);
    return ok(failed);
  }

  expireLease(input: {
    leaseId: string;
    now: number;
    rowCount: number;
  }): R3Result<ExecutionLease> {
    const rows = requireExactlyOne(input.rowCount);
    if (!rows.ok) return rows;
    const lease = this.shared.leases.get(input.leaseId);
    if (
      !lease
      || input.now < lease.expiresAt
      || [
        "COMPLETED",
        "SEND_OUTCOME_UNKNOWN",
        "FAILED_AFTER_SEND",
        "EXPIRED",
        "REVOKED",
        "EMERGENCY_BLOCKED",
      ].includes(lease.state)
    ) {
      return fail("LEASE_STATE_INVALID");
    }
    const expired = Object.freeze({ ...lease, state: "EXPIRED" as const });
    this.shared.leases.set(lease.leaseId, expired);
    return ok(expired);
  }

  activateEmergency(reasonCode: string): R3Result<EmergencyState> {
    if (this.shared.emergency.status !== "NORMAL") {
      return fail("EMERGENCY_STOP_ACTIVE");
    }
    const emergency = EmergencyStateSchema.parse({
      ...this.shared.emergency,
      status: "DRAINING",
      epoch: this.shared.emergency.epoch + 1,
      version: this.shared.emergency.version + 1,
      reasonCode,
      recoveryRequestedByActorId: null,
      recoveryApprovedByActorId: null,
    });
    this.shared.emergency = Object.freeze(emergency);
    for (const [leaseId, lease] of this.shared.leases) {
      if (
        lease.state !== "SENT"
        && lease.state !== "RESPONSE_RECEIVED"
        && lease.state !== "COMPLETED"
        && lease.state !== "SEND_OUTCOME_UNKNOWN"
        && lease.state !== "FAILED_AFTER_SEND"
        && lease.state !== "FAILED_BEFORE_SEND"
        && lease.state !== "EXPIRED"
        && lease.state !== "REVOKED"
        && lease.state !== "EMERGENCY_BLOCKED"
      ) {
        this.shared.leases.set(
          leaseId,
          Object.freeze({ ...lease, state: "EMERGENCY_BLOCKED" }),
        );
      }
    }
    for (const [authorizationId, authorization] of this.shared.sendAuthorizations) {
      if (authorization.state === "ISSUED") {
        this.shared.sendAuthorizations.set(
          authorizationId,
          Object.freeze({ ...authorization, state: "REVOKED" }),
        );
      }
    }
    return ok(this.shared.emergency);
  }

  revokeKey(input: {
    keyId: string;
    expectedKeyVersion: number;
  }): R3Result<KeyState> {
    const key = this.shared.keys.get(input.keyId);
    if (key?.state === "REVOKED") return fail("KEY_REVOKED");
    if (!key || key.keyVersion !== input.expectedKeyVersion) {
      return fail("KEY_VERSION_MISMATCH");
    }
    const revoked = Object.freeze({
      ...key,
      keyVersion: key.keyVersion + 1,
      revocationVersion: key.revocationVersion + 1,
      state: "REVOKED" as const,
    });
    this.shared.keys.set(key.keyId, revoked);
    return ok(revoked);
  }

  revokeAuthorization(
    authorizationId: string,
  ): R3Result<ExecutionAuthorization> {
    const authorization = this.shared.authorizations.get(authorizationId);
    if (!authorization || authorization.state !== "ACTIVE") {
      return fail("LEASE_BINDING_MISMATCH");
    }
    const revoked = Object.freeze({
      ...authorization,
      state: "REVOKED" as const,
    });
    this.shared.authorizations.set(authorizationId, revoked);
    return ok(revoked);
  }

  getLease(leaseId: string): ExecutionLease | null {
    return this.shared.leases.get(leaseId) ?? null;
  }

  getSendAuthorization(id: string): SendAuthorization | null {
    return this.shared.sendAuthorizations.get(id) ?? null;
  }

  getReservation(id: string): BudgetReservation | null {
    return this.shared.reservations.get(id) ?? null;
  }

  snapshot(): Readonly<{
    emergency: EmergencyState;
    globalFenceCeiling: number;
    leaseCount: number;
    sendAuthorizationCount: number;
  }> {
    return Object.freeze({
      emergency: this.shared.emergency,
      globalFenceCeiling: this.shared.globalFenceCeiling,
      leaseCount: this.shared.leases.size,
      sendAuthorizationCount: this.shared.sendAuthorizations.size,
    });
  }

  private validateBinding(input: {
    capability: CapabilityBinding;
    authorization: ExecutionAuthorization;
    reservation: BudgetReservation;
    key: KeyState;
    workerInstanceId: string;
    now: number;
  }): R3Result<true> {
    if (
      input.capability.executionAuthorizationId
        !== input.authorization.authorizationId
      || input.capability.consumptionId
        !== input.authorization.consumptionId
      || input.capability.approvalId !== input.authorization.approvalId
      || input.capability.capabilityId !== input.authorization.capabilityId
      || input.capability.workerInstanceId !== input.workerInstanceId
      || input.capability.budgetReservationId
        !== input.reservation.reservationId
      || input.authorization.budgetReservationId
        !== input.reservation.reservationId
      || input.reservation.capabilityId !== input.capability.capabilityId
      || input.reservation.executionAuthorizationId
        !== input.authorization.authorizationId
      || input.reservation.workerInstanceId !== input.workerInstanceId
      || input.capability.signedApprovalDigest
        !== input.authorization.signedApprovalDigest
      || input.capability.identityDigest !== input.authorization.identityDigest
      || input.capability.evidenceDigest !== input.authorization.evidenceDigest
      || input.capability.snapshotDigest !== input.authorization.snapshotDigest
      || input.capability.dossierDigest !== input.authorization.dossierDigest
      || input.capability.targetDigest !== input.authorization.targetDigest
      || input.capability.keyId !== input.authorization.keyId
      || input.capability.keyVersion !== input.authorization.keyVersion
      || input.capability.revocationVersion
        !== input.authorization.revocationVersion
      || input.capability.emergencyEpoch
        !== input.authorization.emergencyEpoch
      || input.capability.permissionVersion
        !== input.authorization.permissionVersion
      || input.capability.policyVersion !== input.authorization.policyVersion
      || input.reservation.state !== "RESERVED"
      || input.reservation.sendStartedAt !== null
      || input.now >= input.reservation.expiresAt
      || input.now >= input.capability.expiresAt
      || input.now >= input.authorization.expiresAt
      || input.authorization.state !== "ACTIVE"
    ) {
      return fail("LEASE_BINDING_MISMATCH");
    }
    if (
      this.shared.emergency.status !== "NORMAL"
      || this.shared.emergency.epoch !== input.capability.emergencyEpoch
    ) {
      return fail("EMERGENCY_STOP_ACTIVE");
    }
    if (
      input.key.state !== "ACTIVE"
      || input.key.keyId !== input.capability.keyId
      || input.key.keyVersion !== input.capability.keyVersion
      || input.key.revocationVersion !== input.capability.revocationVersion
      || input.now < input.key.validFrom
      || input.now >= input.key.expiresAt
    ) {
      return fail("KEY_REVOKED");
    }
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (!worker || worker.state !== "ACTIVE") {
      return fail("WORKER_NOT_ACTIVE");
    }
    if (
      input.now < worker.heartbeatAt
      || input.now - worker.heartbeatAt > 15_000
    ) {
      return fail("WORKER_NOT_ACTIVE");
    }
    return ok(true);
  }

  private validateLeaseContext(
    lease: ExecutionLease,
    input: {
      workerInstanceId: string;
      fencingToken: number;
      key: unknown;
      reservation: unknown;
      now: number;
    },
  ): R3Result<true> {
    if (
      lease.workerInstanceId !== input.workerInstanceId
      || lease.fencingToken !== input.fencingToken
    ) {
      return fail("SEND_AUTHORIZATION_CONTEXT_MISMATCH");
    }
    const worker = this.shared.workers.get(input.workerInstanceId);
    if (
      !worker
      || worker.state !== "ACTIVE"
      || worker.fenceFloor !== lease.fencingToken
      || input.now < worker.heartbeatAt
      || input.now - worker.heartbeatAt > 15_000
    ) {
      return fail(worker && worker.fenceFloor > lease.fencingToken
        ? "FENCING_TOKEN_STALE"
        : "WORKER_NOT_ACTIVE");
    }
    if (input.now >= lease.expiresAt) return fail("LEASE_EXPIRED");
    if (
      this.shared.emergency.status !== "NORMAL"
      || this.shared.emergency.epoch !== lease.emergencyEpoch
    ) {
      return fail("EMERGENCY_STOP_ACTIVE");
    }
    const capability = this.shared.capabilities.get(lease.capabilityId);
    const authorization = this.shared.authorizations.get(
      lease.executionAuthorizationId,
    );
    if (
      !capability
      || this.shared.capabilityStates.get(lease.capabilityId) !== "RESERVED"
      || capability.executionAuthorizationId
        !== lease.executionAuthorizationId
      || capability.budgetReservationId !== lease.budgetReservationId
    ) {
      return fail("LEASE_BINDING_MISMATCH");
    }
    if (
      !authorization
      || authorization.state !== "ACTIVE"
      || input.now >= authorization.expiresAt
      || authorization.capabilityId !== lease.capabilityId
      || authorization.budgetReservationId !== lease.budgetReservationId
    ) {
      return fail("LEASE_STATE_INVALID");
    }
    const key = KeyStateSchema.safeParse(input.key);
    const reservation = BudgetReservationSchema.safeParse(input.reservation);
    if (!key.success || !reservation.success) {
      return fail("LEASE_BINDING_MISMATCH");
    }
    if (
      key.data.state !== "ACTIVE"
      || key.data.keyVersion !== lease.keyVersion
      || key.data.revocationVersion !== lease.revocationVersion
      || input.now < key.data.validFrom
      || input.now >= key.data.expiresAt
    ) {
      return fail("KEY_REVOKED");
    }
    if (
      reservation.data.state !== "RESERVED"
      || reservation.data.reservationId !== lease.budgetReservationId
      || reservation.data.sendStartedAt !== null
      || input.now >= reservation.data.expiresAt
    ) {
      return fail("BUDGET_RELEASE_FORBIDDEN");
    }
    return ok(true);
  }

  private revokePreSendForWorker(workerInstanceId: string): void {
    for (const [leaseId, lease] of this.shared.leases) {
      if (
        lease.workerInstanceId === workerInstanceId
        && lease.state !== "SENT"
        && lease.state !== "RESPONSE_RECEIVED"
        && lease.state !== "COMPLETED"
        && lease.state !== "SEND_OUTCOME_UNKNOWN"
        && lease.state !== "FAILED_AFTER_SEND"
      ) {
        this.shared.leases.set(
          leaseId,
          Object.freeze({ ...lease, state: "REVOKED" }),
        );
      }
    }
    for (const [id, authorization] of this.shared.sendAuthorizations) {
      if (
        authorization.workerInstanceId === workerInstanceId
        && authorization.state === "ISSUED"
      ) {
        this.shared.sendAuthorizations.set(
          id,
          Object.freeze({ ...authorization, state: "REVOKED" }),
        );
      }
    }
  }
}
````
<!-- END_EXACT_SOURCE id=S038 -->

### S039. preparation/production-trust/r2-r3-remediation/sql/00-schema.sql

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/sql/00-schema.sql`
- Bytes: `12896`
- SHA-256: `7EFB81B768F0B037D3DFA7218F4C1D2F3EB476F3E847A19FFA8CDFD0C22BBD69`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S039 sha256=7EFB81B768F0B037D3DFA7218F4C1D2F3EB476F3E847A19FFA8CDFD0C22BBD69 bytes=12896 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- This is a design draft, not a migration and must never be executed by the
-- offline R2-R3 remediation tests.

CREATE TABLE trust_r3_emergency_control (
  singleton_id smallint PRIMARY KEY CHECK (singleton_id = 1),
  status text NOT NULL CHECK (
    status IN ('NORMAL', 'DRAINING', 'STOPPED', 'RECOVERY_PENDING')
  ),
  epoch bigint NOT NULL CHECK (epoch >= 0),
  version bigint NOT NULL CHECK (version >= 1),
  reason_code text,
  recovery_requested_by_actor_id uuid,
  recovery_approved_by_actor_id uuid,
  updated_at_ms bigint NOT NULL,
  CHECK (
    recovery_requested_by_actor_id IS NULL
    OR recovery_approved_by_actor_id IS NULL
    OR recovery_requested_by_actor_id <> recovery_approved_by_actor_id
  )
);

INSERT INTO trust_r3_emergency_control (
  singleton_id, status, epoch, version, updated_at_ms
) VALUES (1, 'NORMAL', 1, 1, 0);

CREATE TABLE trust_r3_identity_key (
  key_id text PRIMARY KEY,
  key_version bigint NOT NULL CHECK (key_version >= 1),
  revocation_version bigint NOT NULL CHECK (revocation_version >= 0),
  state text NOT NULL CHECK (
    state IN (
      'REGISTERED', 'ACTIVE', 'RETIRING', 'RETIRED',
      'REVOKED', 'EXPIRED', 'RECOVERY_REQUIRED'
    )
  ),
  valid_from_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  updated_at_ms bigint NOT NULL,
  CHECK (expires_at_ms > valid_from_ms)
);

CREATE TABLE trust_r3_approval (
  approval_id uuid PRIMARY KEY,
  approval_version bigint NOT NULL CHECK (approval_version >= 1),
  state text NOT NULL CHECK (
    state IN ('PENDING', 'APPROVED', 'CONSUMED', 'REVOKED', 'EXPIRED', 'REJECTED')
  ),
  actor_id uuid NOT NULL,
  organization_id uuid NOT NULL,
  lead_id uuid NOT NULL,
  signed_approval_digest varchar(71) NOT NULL
    CHECK (signed_approval_digest ~ '^sha256:[a-f0-9]{64}$'),
  identity_digest varchar(71) NOT NULL,
  evidence_digest varchar(71) NOT NULL,
  snapshot_digest varchar(71) NOT NULL,
  dossier_digest varchar(71) NOT NULL,
  target_digest varchar(71) NOT NULL,
  nonce_digest varchar(71) NOT NULL UNIQUE,
  key_id text NOT NULL REFERENCES trust_r3_identity_key (key_id),
  key_version bigint NOT NULL CHECK (key_version >= 1),
  revocation_version bigint NOT NULL CHECK (revocation_version >= 0),
  emergency_epoch bigint NOT NULL CHECK (emergency_epoch >= 0),
  permission_version bigint NOT NULL CHECK (permission_version >= 1),
  policy_version text NOT NULL,
  expires_at_ms bigint NOT NULL,
  consumed_request_id uuid,
  consumption_id uuid,
  updated_at_ms bigint NOT NULL,
  CHECK (
    state <> 'CONSUMED'
    OR (consumed_request_id IS NOT NULL AND consumption_id IS NOT NULL)
  )
);

CREATE TABLE trust_r3_approval_consumption (
  consumption_id uuid PRIMARY KEY,
  request_id uuid NOT NULL UNIQUE,
  approval_id uuid NOT NULL UNIQUE REFERENCES trust_r3_approval (approval_id),
  approval_version bigint NOT NULL CHECK (approval_version >= 2),
  actor_id uuid NOT NULL,
  organization_id uuid NOT NULL,
  lead_id uuid NOT NULL,
  signed_approval_digest varchar(71) NOT NULL,
  identity_digest varchar(71) NOT NULL,
  evidence_digest varchar(71) NOT NULL,
  snapshot_digest varchar(71) NOT NULL,
  dossier_digest varchar(71) NOT NULL,
  target_digest varchar(71) NOT NULL,
  nonce_digest varchar(71) NOT NULL,
  key_id text NOT NULL REFERENCES trust_r3_identity_key (key_id),
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  emergency_epoch bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  consumed_at_ms bigint NOT NULL,
  audit_event_id uuid NOT NULL
);

CREATE TABLE trust_r3_execution_authorization (
  authorization_id uuid PRIMARY KEY,
  consumption_id uuid NOT NULL UNIQUE
    REFERENCES trust_r3_approval_consumption (consumption_id),
  approval_id uuid NOT NULL REFERENCES trust_r3_approval (approval_id),
  actor_id uuid NOT NULL,
  organization_id uuid NOT NULL,
  lead_id uuid NOT NULL,
  signed_approval_digest varchar(71) NOT NULL,
  identity_digest varchar(71) NOT NULL,
  evidence_digest varchar(71) NOT NULL,
  snapshot_digest varchar(71) NOT NULL,
  dossier_digest varchar(71) NOT NULL,
  target_digest varchar(71) NOT NULL,
  provider_kind text NOT NULL CHECK (provider_kind = 'fetch'),
  purpose text NOT NULL CHECK (purpose = 'fetch_only'),
  budget_reservation_id uuid NOT NULL UNIQUE,
  capability_id uuid NOT NULL UNIQUE,
  key_id text NOT NULL REFERENCES trust_r3_identity_key (key_id),
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  emergency_epoch bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  state text NOT NULL CHECK (
    state IN ('ACTIVE', 'EXHAUSTED', 'REVOKED', 'EXPIRED')
  ),
  CHECK (expires_at_ms > issued_at_ms)
);

CREATE TABLE trust_r3_capability (
  capability_id uuid PRIMARY KEY,
  execution_authorization_id uuid NOT NULL UNIQUE
    REFERENCES trust_r3_execution_authorization (authorization_id),
  consumption_id uuid NOT NULL REFERENCES trust_r3_approval_consumption (consumption_id),
  approval_id uuid NOT NULL,
  worker_instance_id uuid NOT NULL,
  budget_reservation_id uuid NOT NULL UNIQUE,
  signed_approval_digest varchar(71) NOT NULL,
  identity_digest varchar(71) NOT NULL,
  evidence_digest varchar(71) NOT NULL,
  snapshot_digest varchar(71) NOT NULL,
  dossier_digest varchar(71) NOT NULL,
  target_digest varchar(71) NOT NULL,
  key_id text NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  emergency_epoch bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  state text NOT NULL CHECK (
    state IN (
      'ISSUED', 'RESERVED', 'EXECUTING', 'COMPLETED',
      'FAILED_BEFORE_SEND', 'REVOKED', 'EXPIRED'
    )
  ),
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  CHECK (expires_at_ms > issued_at_ms)
);

CREATE TABLE trust_r3_budget_control (
  singleton_id smallint PRIMARY KEY CHECK (singleton_id = 1),
  max_total_requests integer NOT NULL CHECK (max_total_requests > 0),
  reserved_requests integer NOT NULL DEFAULT 0 CHECK (reserved_requests >= 0),
  consumed_requests integer NOT NULL DEFAULT 0 CHECK (consumed_requests >= 0),
  max_usd_micros bigint NOT NULL CHECK (max_usd_micros > 0),
  reserved_usd_micros bigint NOT NULL DEFAULT 0 CHECK (reserved_usd_micros >= 0),
  consumed_usd_micros bigint NOT NULL DEFAULT 0 CHECK (consumed_usd_micros >= 0),
  budget_version bigint NOT NULL CHECK (budget_version >= 1),
  updated_at_ms bigint NOT NULL,
  CHECK (reserved_requests + consumed_requests <= max_total_requests),
  CHECK (reserved_usd_micros + consumed_usd_micros <= max_usd_micros)
);

INSERT INTO trust_r3_budget_control (
  singleton_id, max_total_requests, reserved_requests, consumed_requests,
  max_usd_micros, reserved_usd_micros, consumed_usd_micros,
  budget_version, updated_at_ms
) VALUES (1, 1, 0, 0, 750, 0, 0, 1, 0);

CREATE TABLE trust_r3_budget_reservation (
  reservation_id uuid PRIMARY KEY,
  execution_authorization_id uuid NOT NULL UNIQUE
    REFERENCES trust_r3_execution_authorization (authorization_id),
  consumption_id uuid NOT NULL UNIQUE
    REFERENCES trust_r3_approval_consumption (consumption_id),
  capability_id uuid NOT NULL UNIQUE,
  worker_instance_id uuid NOT NULL,
  state text NOT NULL CHECK (
    state IN ('RESERVED', 'COMMITTED', 'RELEASED_BEFORE_SEND', 'UNKNOWN', 'SETTLED')
  ),
  request_count integer NOT NULL DEFAULT 1 CHECK (request_count = 1),
  reserved_usd_micros bigint NOT NULL CHECK (reserved_usd_micros > 0),
  actual_usd_micros bigint CHECK (actual_usd_micros >= 0),
  budget_version bigint NOT NULL CHECK (budget_version >= 1),
  send_started_at_ms bigint,
  created_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  settled_at_ms bigint,
  CHECK (created_at_ms < expires_at_ms),
  CHECK (
    state <> 'RELEASED_BEFORE_SEND'
    OR (send_started_at_ms IS NULL AND actual_usd_micros = 0)
  ),
  CHECK (
    state NOT IN ('UNKNOWN', 'SETTLED')
    OR send_started_at_ms IS NOT NULL
  )
);

ALTER TABLE trust_r3_execution_authorization
  ADD CONSTRAINT trust_r3_authorization_budget_fk
  FOREIGN KEY (budget_reservation_id)
  REFERENCES trust_r3_budget_reservation (reservation_id)
  DEFERRABLE INITIALLY DEFERRED;

ALTER TABLE trust_r3_capability
  ADD CONSTRAINT trust_r3_capability_budget_fk
  FOREIGN KEY (budget_reservation_id)
  REFERENCES trust_r3_budget_reservation (reservation_id)
  DEFERRABLE INITIALLY DEFERRED;

ALTER TABLE trust_r3_budget_reservation
  ADD CONSTRAINT trust_r3_reservation_capability_fk
  FOREIGN KEY (capability_id)
  REFERENCES trust_r3_capability (capability_id)
  DEFERRABLE INITIALLY DEFERRED;

CREATE TABLE trust_r3_worker_registration (
  worker_instance_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (state IN ('ACTIVE', 'DRAINING', 'REVOKED')),
  heartbeat_at_ms bigint NOT NULL,
  fence_floor bigint NOT NULL DEFAULT 0 CHECK (fence_floor >= 0),
  updated_at_ms bigint NOT NULL
);

CREATE TABLE trust_r3_fencing_control (
  singleton_id smallint PRIMARY KEY CHECK (singleton_id = 1),
  next_token bigint NOT NULL CHECK (next_token >= 1),
  version bigint NOT NULL CHECK (version >= 1),
  updated_at_ms bigint NOT NULL
);

INSERT INTO trust_r3_fencing_control (
  singleton_id, next_token, version, updated_at_ms
) VALUES (1, 1, 1, 0);

CREATE TABLE trust_r3_execution_lease (
  lease_id uuid PRIMARY KEY,
  capability_id uuid NOT NULL UNIQUE REFERENCES trust_r3_capability (capability_id),
  execution_authorization_id uuid NOT NULL
    REFERENCES trust_r3_execution_authorization (authorization_id),
  budget_reservation_id uuid NOT NULL
    REFERENCES trust_r3_budget_reservation (reservation_id),
  worker_instance_id uuid NOT NULL REFERENCES trust_r3_worker_registration (worker_instance_id),
  fencing_token bigint NOT NULL UNIQUE CHECK (fencing_token >= 1),
  state text NOT NULL CHECK (
    state IN (
      'ISSUED', 'KEY_READ', 'TRANSPORT_CREATED', 'SEND_AUTHORIZED',
      'SENT', 'RESPONSE_RECEIVED', 'COMPLETED', 'FAILED_BEFORE_SEND',
      'SEND_OUTCOME_UNKNOWN', 'FAILED_AFTER_SEND', 'EXPIRED', 'REVOKED',
      'EMERGENCY_BLOCKED'
    )
  ),
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  emergency_epoch bigint NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  row_version bigint NOT NULL DEFAULT 1 CHECK (row_version >= 1),
  CHECK (expires_at_ms > issued_at_ms),
  CHECK (expires_at_ms - issued_at_ms <= 60000)
);

CREATE TABLE trust_r3_send_authorization (
  send_authorization_id uuid PRIMARY KEY,
  state text NOT NULL CHECK (state IN ('ISSUED', 'CONSUMED', 'EXPIRED', 'REVOKED')),
  lease_id uuid NOT NULL UNIQUE REFERENCES trust_r3_execution_lease (lease_id),
  capability_id uuid NOT NULL,
  worker_instance_id uuid NOT NULL,
  fencing_token bigint NOT NULL,
  budget_reservation_id uuid NOT NULL,
  emergency_epoch bigint NOT NULL,
  key_version bigint NOT NULL,
  revocation_version bigint NOT NULL,
  permission_version bigint NOT NULL,
  policy_version text NOT NULL,
  issued_at_ms bigint NOT NULL,
  expires_at_ms bigint NOT NULL,
  consumed_at_ms bigint,
  CHECK (expires_at_ms > issued_at_ms),
  CHECK (expires_at_ms - issued_at_ms <= 5000),
  CHECK (
    (state = 'ISSUED' AND consumed_at_ms IS NULL)
    OR (state = 'CONSUMED' AND consumed_at_ms IS NOT NULL)
    OR state IN ('EXPIRED', 'REVOKED')
  )
);

CREATE TABLE trust_r3_audit_head (
  singleton_id smallint PRIMARY KEY CHECK (singleton_id = 1),
  last_sequence bigint NOT NULL CHECK (last_sequence >= 0),
  last_event_digest varchar(71),
  CHECK (
    (last_sequence = 0 AND last_event_digest IS NULL)
    OR (last_sequence > 0 AND last_event_digest IS NOT NULL)
  )
);

INSERT INTO trust_r3_audit_head (
  singleton_id, last_sequence, last_event_digest
) VALUES (1, 0, NULL);

CREATE TABLE trust_r3_audit_event (
  event_id uuid PRIMARY KEY,
  sequence bigint NOT NULL UNIQUE CHECK (sequence >= 1),
  occurred_at_ms bigint NOT NULL,
  event_type text NOT NULL CHECK (
    event_type IN (
      'APPROVAL_CONSUMED', 'BUDGET_RESERVED', 'BUDGET_SEND_STARTED',
      'BUDGET_COMMITTED', 'BUDGET_RELEASED',
      'BUDGET_SETTLED', 'LEASE_ISSUED', 'WORKER_PROGRESS',
      'SEND_AUTHORIZED', 'SEND_AUTHORIZATION_CONSUMED',
      'REQUEST_SENT', 'SEND_OUTCOME_UNKNOWN', 'RESPONSE_RECEIVED',
      'EMERGENCY_ACTIVATED', 'EMERGENCY_RECOVERY_REQUESTED',
      'EMERGENCY_RECOVERY_APPROVED', 'KEY_REVOKED'
    )
  ),
  outcome text NOT NULL CHECK (outcome IN ('ALLOW', 'BLOCK', 'FAILED', 'UNKNOWN')),
  subject_id uuid NOT NULL,
  previous_event_digest varchar(71),
  event_digest varchar(71) NOT NULL UNIQUE,
  CHECK (
    (sequence = 1 AND previous_event_digest IS NULL)
    OR (sequence > 1 AND previous_event_digest IS NOT NULL)
  )
);
````
<!-- END_EXACT_SOURCE id=S039 -->

### S040. preparation/production-trust/r2-r3-remediation/sql/10-lease-issuance.sql

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/sql/10-lease-issuance.sql`
- Bytes: `5124`
- SHA-256: `2DB415FE7D2CD867AA48648941CA2869CB48AD1F04386250E8786A3A11DF0116`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S040 sha256=2DB415FE7D2CD867AA48648941CA2869CB48AD1F04386250E8786A3A11DF0116 bytes=5124 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Stage 1: Execution Lease Issuance.
-- Every UPDATE is expected to affect exactly one row. Application code MUST
-- check the driver row count and ROLLBACK on any other result.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms, capability_id,
       budget_reservation_id, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r3_execution_authorization
WHERE authorization_id = $2
FOR UPDATE;

SELECT reservation_id, state, expires_at_ms, execution_authorization_id,
       consumption_id, capability_id, worker_instance_id, budget_version
FROM trust_r3_budget_reservation
WHERE reservation_id = $3
FOR UPDATE;

SELECT capability_id, state, expires_at_ms, execution_authorization_id,
       consumption_id, emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r3_capability
WHERE capability_id = $4
FOR UPDATE;

-- Persistent row-locked monotonic fence allocation. This is part of the
-- transaction and therefore rolls back with Lease issuance.
SELECT next_token, version
FROM trust_r3_fencing_control
WHERE singleton_id = 1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_fencing_control
SET next_token = next_token + 1,
    version = version + 1,
    updated_at_ms = $9
WHERE singleton_id = 1
  AND next_token = $8
  AND version = $16
RETURNING next_token - 1 AS allocated_fencing_token;
-- EXPECTED_ROW_COUNT=1

SELECT state, fence_floor
FROM trust_r3_worker_registration
WHERE worker_instance_id = $5
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_capability
SET state = 'RESERVED'
WHERE capability_id = $4
  AND state = 'ISSUED'
  AND execution_authorization_id = $2
  AND consumption_id = $6
  AND emergency_epoch = $11
  AND key_version = $12
  AND revocation_version = $13
  AND permission_version = $14
  AND policy_version = $15
  AND $9 < expires_at_ms
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $11
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key k
    WHERE k.key_id = $1
      AND k.state = 'ACTIVE'
      AND k.key_version = $12
      AND k.revocation_version = $13
      AND $9 >= k.valid_from_ms
      AND $9 < k.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_execution_authorization a
    WHERE a.authorization_id = $2
      AND a.state = 'ACTIVE'
      AND a.capability_id = $4
      AND a.budget_reservation_id = $3
      AND a.emergency_epoch = $11
      AND a.key_version = $12
      AND a.revocation_version = $13
      AND a.permission_version = $14
      AND a.policy_version = $15
      AND $9 < a.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $3
      AND b.state = 'RESERVED'
      AND b.execution_authorization_id = $2
      AND b.capability_id = $4
      AND b.worker_instance_id = $5
      AND b.send_started_at_ms IS NULL
      AND $9 < b.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_worker_registration w
    WHERE w.worker_instance_id = $5
      AND w.state = 'ACTIVE'
      AND $9 - w.heartbeat_at_ms <= 15000
  );
-- EXPECTED_ROW_COUNT=1

INSERT INTO trust_r3_execution_lease (
  lease_id, capability_id, execution_authorization_id,
  budget_reservation_id, worker_instance_id, fencing_token, state,
  issued_at_ms, expires_at_ms, emergency_epoch, key_version,
  revocation_version, permission_version, policy_version
) VALUES (
  $7, $4, $2,
  $3, $5, $17, 'ISSUED',
  $9, $10, $11, $12,
  $13, $14, $15
);
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_worker_registration
SET fence_floor = $17,
    heartbeat_at_ms = $9
WHERE worker_instance_id = $5
  AND state = 'ACTIVE'
  AND fence_floor < $17;
-- EXPECTED_ROW_COUNT=1

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES (
  $18, $19, $9, 'LEASE_ISSUED', 'ALLOW',
  $7, $20, $21
);
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $19,
    last_event_digest = $21
WHERE singleton_id = 1
  AND last_sequence = $19 - 1;
-- EXPECTED_ROW_COUNT=1

COMMIT;

-- Application preconditions checked after locks:
--   Emergency status NORMAL and epoch = $11
--   Key ACTIVE, versions match, trusted now in key validity
--   Authorization ACTIVE, unexpired and bound to reservation/capability
--   Reservation RESERVED and unexpired
--   Capability ISSUED and all immutable bindings match
--   Worker ACTIVE and heartbeat fresh
--   allocated fencing token > worker.fence_floor
````
<!-- END_EXACT_SOURCE id=S040 -->

### S041. preparation/production-trust/r2-r3-remediation/sql/20-worker-progress.sql

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/sql/20-worker-progress.sql`
- Bytes: `5958`
- SHA-256: `C56E0437EE45860A26D1FA25981187C441C922FB830C8288BDBB952594C3E1CD`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S041 sha256=C56E0437EE45860A26D1FA25981187C441C922FB830C8288BDBB952594C3E1CD bytes=5958 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Stage 2: Worker Progress. This file intentionally contains two separate
-- transactions. A Worker cannot jump ISSUED -> TRANSPORT_CREATED.

-- Transaction 2A: record successful Key Read.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT lease_id, state, worker_instance_id, fencing_token,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms,
       capability_id, execution_authorization_id, budget_reservation_id
FROM trust_r3_execution_lease
WHERE lease_id = $2
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_execution_lease
SET state = 'KEY_READ'
WHERE lease_id = $2
  AND state = 'ISSUED'
  AND worker_instance_id = $3
  AND fencing_token = $4
  AND emergency_epoch = $5
  AND key_version = $6
  AND revocation_version = $7
  AND permission_version = $8
  AND policy_version = $9
  AND capability_id = $15
  AND execution_authorization_id = $16
  AND budget_reservation_id = $17
  AND $10 < expires_at_ms
  AND EXISTS (
    SELECT 1
    FROM trust_r3_worker_registration w
    WHERE w.worker_instance_id = $3
      AND w.state = 'ACTIVE'
      AND w.fence_floor = $4
      AND $10 - w.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $5
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_identity_key k
    WHERE k.key_id = $1
      AND k.state = 'ACTIVE'
      AND k.key_version = $6
      AND k.revocation_version = $7
      AND $10 >= k.valid_from_ms
      AND $10 < k.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability c
    WHERE c.capability_id = $15
      AND c.state = 'RESERVED'
      AND c.execution_authorization_id = $16
      AND c.budget_reservation_id = $17
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization a
    WHERE a.authorization_id = $16
      AND a.state = 'ACTIVE'
      AND a.capability_id = $15
      AND a.budget_reservation_id = $17
      AND $10 < a.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $17
      AND b.state = 'RESERVED'
      AND b.send_started_at_ms IS NULL
      AND $10 < b.expires_at_ms
  );
-- EXPECTED_ROW_COUNT=1

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES ($11, $12, $10, 'WORKER_PROGRESS', 'ALLOW', $2, $13, $14);
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $12, last_event_digest = $14
WHERE singleton_id = 1 AND last_sequence = $12 - 1;
-- EXPECTED_ROW_COUNT=1

COMMIT;

-- Transaction 2B: record successful Transport creation.
BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT lease_id, state, worker_instance_id, fencing_token,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, expires_at_ms,
       capability_id, execution_authorization_id, budget_reservation_id
FROM trust_r3_execution_lease
WHERE lease_id = $2
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_execution_lease
SET state = 'TRANSPORT_CREATED'
WHERE lease_id = $2
  AND state = 'KEY_READ'
  AND worker_instance_id = $3
  AND fencing_token = $4
  AND emergency_epoch = $5
  AND key_version = $6
  AND revocation_version = $7
  AND permission_version = $8
  AND policy_version = $9
  AND capability_id = $15
  AND execution_authorization_id = $16
  AND budget_reservation_id = $17
  AND $10 < expires_at_ms
  AND EXISTS (
    SELECT 1 FROM trust_r3_worker_registration w
    WHERE w.worker_instance_id = $3
      AND w.state = 'ACTIVE'
      AND w.fence_floor = $4
      AND $10 - w.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $5
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key k
    WHERE k.key_id = $1
      AND k.state = 'ACTIVE'
      AND k.key_version = $6
      AND k.revocation_version = $7
      AND $10 >= k.valid_from_ms
      AND $10 < k.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_capability c
    WHERE c.capability_id = $15
      AND c.state = 'RESERVED'
      AND c.execution_authorization_id = $16
      AND c.budget_reservation_id = $17
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_execution_authorization a
    WHERE a.authorization_id = $16
      AND a.state = 'ACTIVE'
      AND a.capability_id = $15
      AND a.budget_reservation_id = $17
      AND $10 < a.expires_at_ms
  )
  AND EXISTS (
    SELECT 1
    FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $17
      AND b.state = 'RESERVED'
      AND b.send_started_at_ms IS NULL
      AND $10 < b.expires_at_ms
  );
-- EXPECTED_ROW_COUNT=1

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES ($11, $12, $10, 'WORKER_PROGRESS', 'ALLOW', $2, $13, $14);
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $12, last_event_digest = $14
WHERE singleton_id = 1 AND last_sequence = $12 - 1;
-- EXPECTED_ROW_COUNT=1

COMMIT;
````
<!-- END_EXACT_SOURCE id=S041 -->

### S042. preparation/production-trust/r2-r3-remediation/sql/30-send-authorization-issuance.sql

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/sql/30-send-authorization-issuance.sql`
- Bytes: `3518`
- SHA-256: `8178ABC188D29E8D766AF5DF4A7E537F015A444877CF88483C3777EDD76102BD`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S042 sha256=8178ABC188D29E8D766AF5DF4A7E537F015A444877CF88483C3777EDD76102BD bytes=3518 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Stage 3: Send Authorization Issuance. The Lease must already be
-- TRANSPORT_CREATED. This transaction does not perform a network write.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT authorization_id, state, expires_at_ms,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version
FROM trust_r3_execution_authorization
WHERE authorization_id = $2
FOR UPDATE;

SELECT reservation_id, state, expires_at_ms, send_started_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $3
FOR UPDATE;

SELECT capability_id, state
FROM trust_r3_capability
WHERE capability_id = $4
FOR UPDATE;

SELECT state, fence_floor, heartbeat_at_ms
FROM trust_r3_worker_registration
WHERE worker_instance_id = $5
FOR UPDATE;

SELECT lease_id, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token,
       state, expires_at_ms, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r3_execution_lease
WHERE lease_id = $6
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_execution_lease
SET state = 'SEND_AUTHORIZED'
WHERE lease_id = $6
  AND state = 'TRANSPORT_CREATED'
  AND capability_id = $4
  AND execution_authorization_id = $2
  AND budget_reservation_id = $3
  AND worker_instance_id = $5
  AND fencing_token = $7
  AND emergency_epoch = $8
  AND key_version = $9
  AND revocation_version = $10
  AND permission_version = $11
  AND policy_version = $12
  AND $13 < expires_at_ms
  AND EXISTS (
    SELECT 1 FROM trust_r3_worker_registration w
    WHERE w.worker_instance_id = $5
      AND w.state = 'ACTIVE'
      AND w.fence_floor = $7
      AND $13 - w.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $8
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $3
      AND b.state = 'RESERVED'
      AND b.send_started_at_ms IS NULL
      AND $13 < b.expires_at_ms
  );
-- EXPECTED_ROW_COUNT=1

INSERT INTO trust_r3_send_authorization (
  send_authorization_id, state, lease_id, capability_id,
  worker_instance_id, fencing_token, budget_reservation_id,
  emergency_epoch, key_version, revocation_version,
  permission_version, policy_version, issued_at_ms, expires_at_ms,
  consumed_at_ms
) VALUES (
  $14, 'ISSUED', $6, $4,
  $5, $7, $3,
  $8, $9, $10,
  $11, $12, $13, $15,
  NULL
);
-- EXPECTED_ROW_COUNT=1

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES ($16, $17, $13, 'SEND_AUTHORIZED', 'ALLOW', $6, $18, $19);
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $17, last_event_digest = $19
WHERE singleton_id = 1 AND last_sequence = $17 - 1;
-- EXPECTED_ROW_COUNT=1

COMMIT;

-- $15 MUST be <= min($13 + 5000, lease.expires_at_ms, reservation.expires_at_ms).
-- Unique lease_id on trust_r3_send_authorization makes issuance one-use.
````
<!-- END_EXACT_SOURCE id=S042 -->

### S043. preparation/production-trust/r2-r3-remediation/sql/40-send-authorization-consume.sql

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/sql/40-send-authorization-consume.sql`
- Bytes: `4389`
- SHA-256: `93EB68288F6B2E319C37BFEE8E6CE754D7DB8690D167B43B471C128E7235240B`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S043 sha256=93EB68288F6B2E319C37BFEE8E6CE754D7DB8690D167B43B471C128E7235240B bytes=4389 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Stage 4: Send Authorization Consumption and network-write boundary.
-- This transaction grants the final local write permission. It does not prove
-- that the external Provider received the request.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT status, epoch, version
FROM trust_r3_emergency_control
WHERE singleton_id = 1
FOR UPDATE;

SELECT key_version, revocation_version, state, valid_from_ms, expires_at_ms
FROM trust_r3_identity_key
WHERE key_id = $1
FOR UPDATE;

SELECT reservation_id, state, expires_at_ms, send_started_at_ms
FROM trust_r3_budget_reservation
WHERE reservation_id = $2
FOR UPDATE;

SELECT lease_id, capability_id, execution_authorization_id,
       budget_reservation_id, worker_instance_id, fencing_token,
       state, expires_at_ms, emergency_epoch, key_version,
       revocation_version, permission_version, policy_version
FROM trust_r3_execution_lease
WHERE lease_id = $3
FOR UPDATE;

SELECT send_authorization_id, state, lease_id, capability_id,
       worker_instance_id, fencing_token, budget_reservation_id,
       emergency_epoch, key_version, revocation_version,
       permission_version, policy_version, issued_at_ms, expires_at_ms,
       consumed_at_ms
FROM trust_r3_send_authorization
WHERE send_authorization_id = $4
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_send_authorization
SET state = 'CONSUMED',
    consumed_at_ms = $5
WHERE send_authorization_id = $4
  AND state = 'ISSUED'
  AND lease_id = $3
  AND capability_id = $6
  AND worker_instance_id = $7
  AND fencing_token = $8
  AND budget_reservation_id = $2
  AND emergency_epoch = $9
  AND key_version = $10
  AND revocation_version = $11
  AND permission_version = $12
  AND policy_version = $13
  AND $5 >= issued_at_ms
  AND $5 < expires_at_ms
  AND $5 < $14
  AND EXISTS (
    SELECT 1 FROM trust_r3_execution_lease l
    WHERE l.lease_id = $3
      AND l.state = 'SEND_AUTHORIZED'
      AND l.worker_instance_id = $7
      AND l.fencing_token = $8
      AND l.emergency_epoch = $9
      AND l.key_version = $10
      AND l.revocation_version = $11
      AND l.permission_version = $12
      AND l.policy_version = $13
      AND $5 < l.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_worker_registration w
    WHERE w.worker_instance_id = $7
      AND w.state = 'ACTIVE'
      AND w.fence_floor = $8
      AND $5 - w.heartbeat_at_ms <= 15000
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_emergency_control e
    WHERE e.singleton_id = 1
      AND e.status = 'NORMAL'
      AND e.epoch = $9
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_identity_key k
    WHERE k.key_id = $1
      AND k.state = 'ACTIVE'
      AND k.key_version = $10
      AND k.revocation_version = $11
      AND $5 >= k.valid_from_ms
      AND $5 < k.expires_at_ms
  )
  AND EXISTS (
    SELECT 1 FROM trust_r3_budget_reservation b
    WHERE b.reservation_id = $2
      AND b.state = 'RESERVED'
      AND b.send_started_at_ms IS NULL
      AND $5 < b.expires_at_ms
  );
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_execution_lease
SET state = 'SENT'
WHERE lease_id = $3
  AND state = 'SEND_AUTHORIZED'
  AND worker_instance_id = $7
  AND fencing_token = $8;
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_budget_reservation
SET send_started_at_ms = $5
WHERE reservation_id = $2
  AND state = 'RESERVED'
  AND send_started_at_ms IS NULL
  AND $5 < expires_at_ms;
-- EXPECTED_ROW_COUNT=1

SELECT last_sequence, last_event_digest
FROM trust_r3_audit_head
WHERE singleton_id = 1
FOR UPDATE;

INSERT INTO trust_r3_audit_event (
  event_id, sequence, occurred_at_ms, event_type, outcome,
  subject_id, previous_event_digest, event_digest
) VALUES ($15, $16, $5, 'SEND_AUTHORIZATION_CONSUMED', 'ALLOW', $4, $17, $18);
-- EXPECTED_ROW_COUNT=1

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_audit_head
SET last_sequence = $16, last_event_digest = $18
WHERE singleton_id = 1 AND last_sequence = $16 - 1;
-- EXPECTED_ROW_COUNT=1

COMMIT;

-- After COMMIT, the trusted network component may perform exactly one write.
-- The database state SENT means "write permission committed", not "Provider
-- received". Any crash or missing response after this point becomes
-- SEND_OUTCOME_UNKNOWN. Automatic replay of the same Send Authorization is
-- forbidden.
````
<!-- END_EXACT_SOURCE id=S043 -->

### S044. preparation/production-trust/r2-r3-remediation/sql/70-fencing-registry.sql

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/sql/70-fencing-registry.sql`
- Bytes: `1060`
- SHA-256: `C089AADA9F5D583EA78CFC218F935B8E268CA66F81C74AE60F207C58B99F00EB`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S044 sha256=C089AADA9F5D583EA78CFC218F935B8E268CA66F81C74AE60F207C58B99F00EB bytes=1060 fence=fenced -->
````sql
-- OFFLINE_REFERENCE_MODEL / STATIC_SQL_REVIEW_ONLY / NOT_EXECUTED
-- Persistent row-locked monotonic fencing allocation.

BEGIN ISOLATION LEVEL READ COMMITTED;

SELECT next_token, version
FROM trust_r3_fencing_control
WHERE singleton_id = 1
FOR UPDATE;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_fencing_control
SET next_token = next_token + 1,
    version = version + 1,
    updated_at_ms = $1
WHERE singleton_id = 1
  AND next_token = $2
  AND version = $3
RETURNING next_token - 1 AS allocated_fencing_token;

-- ROW_COUNT_EXPECTATION: exactly 1
UPDATE trust_r3_worker_registration
SET fence_floor = GREATEST(fence_floor, $4),
    updated_at_ms = $1
WHERE worker_instance_id = $5
  AND state = 'ACTIVE'
  AND fence_floor < $4;

COMMIT;

-- The allocator and Worker fence-floor update commit atomically. A Lease must
-- persist the returned token before any Send Authorization can be issued.
-- PostgreSQL transaction rollback also rolls back the counter increment, unlike
-- a standalone sequence. Gaps are acceptable but never a token decrease.
````
<!-- END_EXACT_SOURCE id=S044 -->

### S045. preparation/production-trust/r2-r3-remediation/tests/execution-lease.test.ts

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/tests/execution-lease.test.ts`
- Bytes: `21893`
- SHA-256: `80FE63A0E5FB5CC764C418696AD4161E402558F495C2D28F4DDCFF4C9375F6FB`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S045 sha256=80FE63A0E5FB5CC764C418696AD4161E402558F495C2D28F4DDCFF4C9375F6FB bytes=21893 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import {
  BudgetReservationSchema,
  CapabilityBindingSchema,
  ExecutionAuthorizationSchema,
  FencingAllocationSchema,
  KeyStateSchema,
  requireExactlyOne,
  type R3Result,
} from "../contracts";
import {
  OfflineExecutionLeaseModel,
  type FencingAllocator,
} from "../models/execution-lease";

const NOW = Date.parse("2026-11-26T08:00:00Z");

const ids = {
  workerA: "aaaaaaaa-aaaa-4aaa-8aaa-aaaaaaaaaaaa",
  workerB: "bbbbbbbb-bbbb-4bbb-8bbb-bbbbbbbbbbbb",
  approval: "11111111-1111-4111-8111-111111111111",
  consumption: "22222222-2222-4222-8222-222222222222",
  authorization: "33333333-3333-4333-8333-333333333333",
  reservation: "44444444-4444-4444-8444-444444444444",
  capability: "55555555-5555-4555-8555-555555555555",
  actor: "66666666-6666-4666-8666-666666666666",
  organization: "77777777-7777-4777-8777-777777777777",
  lead: "88888888-8888-4888-8888-888888888888",
} as const;

const digests = {
  signed: "sha256:" + "1".repeat(64),
  identity: "sha256:" + "2".repeat(64),
  evidence: "sha256:" + "3".repeat(64),
  snapshot: "sha256:" + "4".repeat(64),
  dossier: "sha256:" + "5".repeat(64),
  target: "sha256:" + "6".repeat(64),
} as const;

function makeAllocator(start = 0): FencingAllocator & { calls: number } {
  let token = start;
  const allocator = {
    calls: 0,
    allocate(input: {
      workerInstanceId: string;
      leaseId: string;
      resourceId: string;
      now: number;
      expectedControlVersion: number;
    }): R3Result<ReturnType<typeof FencingAllocationSchema.parse>> {
      token += 1;
      allocator.calls += 1;
      return {
        ok: true,
        value: FencingAllocationSchema.parse({
          schemaVersion: "r2-r3-fencing-allocation-v1",
          fencingToken: token,
          workerInstanceId: input.workerInstanceId,
          leaseId: input.leaseId,
          allocatedAt: input.now,
          allocatorName: "trust_r3_fencing_control",
          allocationMode: "row_locked_monotonic_counter",
        }),
      };
    },
  };
  return allocator;
}

function fixture(index = 1) {
  const capabilityId = index === 1
    ? ids.capability
    : "99999999-9999-4999-8999-999999999999";
  const authorizationId = index === 1
    ? ids.authorization
    : "12121212-1212-4212-8212-121212121212";
  const reservationId = index === 1
    ? ids.reservation
    : "13131313-1313-4313-8313-131313131313";
  const consumptionId = index === 1
    ? ids.consumption
    : "14141414-1414-4414-8414-141414141414";
  const key = KeyStateSchema.parse({
    schemaVersion: "r2-r3-key-state-v1",
    keyId: "r3-approval-key",
    keyVersion: 2,
    revocationVersion: 1,
    state: "ACTIVE",
    validFrom: NOW - 60_000,
    expiresAt: NOW + 3_600_000,
  });
  const capability = CapabilityBindingSchema.parse({
    schemaVersion: "r2-r3-capability-binding-v1",
    capabilityId,
    executionAuthorizationId: authorizationId,
    consumptionId,
    approvalId: ids.approval,
    workerInstanceId: ids.workerA,
    budgetReservationId: reservationId,
    signedApprovalDigest: digests.signed,
    identityDigest: digests.identity,
    evidenceDigest: digests.evidence,
    snapshotDigest: digests.snapshot,
    dossierDigest: digests.dossier,
    targetDigest: digests.target,
    keyId: key.keyId,
    keyVersion: key.keyVersion,
    revocationVersion: key.revocationVersion,
    emergencyEpoch: 3,
    permissionVersion: 4,
    policyVersion: "r2-r3-policy-v1",
    expiresAt: NOW + 120_000,
  });
  const authorization = ExecutionAuthorizationSchema.parse({
    schemaVersion: "r2-r3-execution-authorization-v1",
    authorizationId,
    consumptionId,
    approvalId: ids.approval,
    actorId: ids.actor,
    organizationId: ids.organization,
    leadId: ids.lead,
    signedApprovalDigest: digests.signed,
    identityDigest: digests.identity,
    evidenceDigest: digests.evidence,
    snapshotDigest: digests.snapshot,
    dossierDigest: digests.dossier,
    targetDigest: digests.target,
    providerKind: "fetch",
    purpose: "fetch_only",
    budgetReservationId: reservationId,
    capabilityId,
    keyId: key.keyId,
    keyVersion: key.keyVersion,
    revocationVersion: key.revocationVersion,
    emergencyEpoch: 3,
    permissionVersion: 4,
    policyVersion: "r2-r3-policy-v1",
    issuedAt: NOW - 1_000,
    expiresAt: NOW + 120_000,
    state: "ACTIVE",
  });
  const reservation = BudgetReservationSchema.parse({
    schemaVersion: "r2-r3-budget-reservation-v1",
    reservationId,
    executionAuthorizationId: authorizationId,
    consumptionId,
    capabilityId,
    workerInstanceId: ids.workerA,
    state: "RESERVED",
    requestCount: 1,
    reservedUsdMicros: 750,
    actualUsdMicros: null,
    budgetVersion: 1,
    sendStartedAt: null,
    createdAt: NOW - 1_000,
    expiresAt: NOW + 120_000,
    settledAt: null,
  });
  return { key, capability, authorization, reservation };
}

function seed(
  model: OfflineExecutionLeaseModel,
  data = fixture(),
) {
  expect(model.registerWorker({
    workerInstanceId: ids.workerA,
    resourceId: data.capability.capabilityId,
    expectedFencingControlVersion: 1,
    now: NOW,
  }).ok).toBe(true);
  expect(model.seedKey(data.key).ok).toBe(true);
  expect(model.seedCapability(data.capability).ok).toBe(true);
  expect(model.seedAuthorization(data.authorization).ok).toBe(true);
  expect(model.seedReservation(data.reservation).ok).toBe(true);
  return data;
}

function issue(
  model: OfflineExecutionLeaseModel,
  allocator: FencingAllocator,
  data = fixture(),
) {
  const lease = model.issueLease({
    allocation: allocator,
    capability: data.capability,
    authorization: data.authorization,
    reservation: data.reservation,
    key: data.key,
    workerInstanceId: ids.workerA,
    resourceId: data.capability.capabilityId,
    expectedFencingControlVersion: 1,
    now: NOW,
    ttlMs: 30_000,
  });
  if (!lease.ok) throw new Error(lease.code);
  return lease.value;
}

function toTransportCreated(
  model: OfflineExecutionLeaseModel,
  lease: ReturnType<typeof issue>,
  data = fixture(),
) {
  expect(model.progressLease({
    leaseId: lease.leaseId,
    next: "KEY_READ",
    workerInstanceId: ids.workerA,
    fencingToken: lease.fencingToken,
    key: data.key,
    reservation: data.reservation,
    now: NOW + 1,
      rowCount: 1,
  }).ok).toBe(true);
  expect(model.progressLease({
    leaseId: lease.leaseId,
    next: "TRANSPORT_CREATED",
    workerInstanceId: ids.workerA,
    fencingToken: lease.fencingToken,
    key: data.key,
    reservation: data.reservation,
    now: NOW + 2,
      rowCount: 1,
  }).ok).toBe(true);
}

describe("R3 Execution Lease and Send Authorization", () => {
  it("issues exactly one persistent-fence lease per capability", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const first = issue(model, allocator, data);
    const second = model.issueLease({
      allocation: allocator,
      capability: data.capability,
      authorization: data.authorization,
      reservation: data.reservation,
      key: data.key,
      workerInstanceId: ids.workerA,
      resourceId: data.capability.capabilityId,
      expectedFencingControlVersion: 1,
      now: NOW,
      ttlMs: 30_000,
    });
    expect(second).toMatchObject({
      ok: true,
      value: { leaseId: first.leaseId, state: "ISSUED" },
    });
    expect(allocator.calls).toBe(1);
    expect(model.snapshot().globalFenceCeiling).toBe(first.fencingToken);
  });

  it("enforces exact staged progress and idempotent replay", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "TRANSPORT_CREATED",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 1,
      rowCount: 1,
    })).toEqual({ ok: false, code: "LEASE_STATE_INVALID" });
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "KEY_READ",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 1,
      rowCount: 1,
    }).ok).toBe(true);
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "KEY_READ",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 2,
      rowCount: 1,
    }).ok).toBe(true);
  });

  it("requires exact row counts at progress boundaries", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "KEY_READ",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 1,
      rowCount: 0,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(model.getLease(lease.leaseId)?.state).toBe("ISSUED");
    expect(requireExactlyOne(1)).toEqual({ ok: true, value: 1 });
  });

  it("issues only after TRANSPORT_CREATED and returns the same permit idempotently", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    expect(model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 1,
      ttlMs: 5_000,
    })).toEqual({ ok: false, code: "LEASE_STATE_INVALID" });
    toTransportCreated(model, lease, data);
    const permit = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    expect(permit.ok).toBe(true);
    if (!permit.ok) return;
    const replay = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 4,
      ttlMs: 5_000,
    });
    expect(replay).toMatchObject({
      ok: true,
      value: { sendAuthorizationId: permit.value.sendAuthorizationId },
    });
  });

  it("atomically consumes one send permit and never equates commit with Provider receipt", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    toTransportCreated(model, lease, data);
    const permit = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    if (!permit.ok) throw new Error(permit.code);
    const consumed = model.consumeSendAuthorization({
      sendAuthorizationId: permit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 4,
      rowCountBudget: 1,
      rowCountSend: 1,
      rowCountLease: 1,
    });
    expect(consumed).toMatchObject({
      ok: true,
      value: {
        sendAuthorization: { state: "CONSUMED" },
        lease: { state: "SENT" },
        externalOutcome: "PENDING",
      },
    });
    expect(model.getReservation(ids.reservation)?.sendStartedAt).toBe(NOW + 4);
    expect(model.consumeSendAuthorization({
      sendAuthorizationId: permit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: model.getReservation(ids.reservation),
      now: NOW + 5,
      rowCountSend: 1,
      rowCountLease: 1,
      rowCountBudget: 1,
    })).toEqual({ ok: false, code: "SEND_AUTHORIZATION_REPLAYED" });
  });

  it("rolls back when either send-boundary update does not affect one row", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    toTransportCreated(model, lease, data);
    const permit = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    if (!permit.ok) throw new Error(permit.code);
    expect(model.consumeSendAuthorization({
      sendAuthorizationId: permit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 4,
      rowCountBudget: 1,
      rowCountSend: 1,
      rowCountLease: 0,
    })).toEqual({ ok: false, code: "ROW_COUNT_CONFLICT" });
    expect(model.getSendAuthorization(permit.value.sendAuthorizationId)?.state)
      .toBe("ISSUED");
    expect(model.getLease(lease.leaseId)?.state).toBe("SEND_AUTHORIZED");
    expect(model.getReservation(ids.reservation)?.sendStartedAt).toBeNull();
  });

  it("rejects stale workers after a higher fence is allocated", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const firstData = seed(model);
    const firstLease = issue(model, allocator, firstData);
    toTransportCreated(model, firstLease, firstData);
    const firstPermit = model.issueSendAuthorization({
      leaseId: firstLease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: firstLease.fencingToken,
      key: firstData.key,
      reservation: firstData.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    if (!firstPermit.ok) throw new Error(firstPermit.code);

    const secondData = fixture(2);
    expect(model.seedCapability(secondData.capability).ok).toBe(true);
    expect(model.seedAuthorization(secondData.authorization).ok).toBe(true);
    expect(model.seedReservation(secondData.reservation).ok).toBe(true);
    const secondLease = issue(model, allocator, secondData);
    expect(secondLease.fencingToken).toBeGreaterThan(firstLease.fencingToken);
    expect(model.consumeSendAuthorization({
      sendAuthorizationId: firstPermit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: firstLease.fencingToken,
      key: firstData.key,
      reservation: firstData.reservation,
      now: NOW + 4,
      rowCountSend: 1,
      rowCountLease: 1,
      rowCountBudget: 1,
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
  });

  it("blocks send consumption after Key revocation", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    toTransportCreated(model, lease, data);
    const permit = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    if (!permit.ok) throw new Error(permit.code);
    expect(model.revokeKey({
      keyId: data.key.keyId,
      expectedKeyVersion: data.key.keyVersion,
    }).ok).toBe(true);
    const revoked = model.revokeKey({
      keyId: data.key.keyId,
      expectedKeyVersion: data.key.keyVersion + 1,
    });
    expect(revoked.ok).toBe(false);
    expect(model.consumeSendAuthorization({
      sendAuthorizationId: permit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: {
        ...data.key,
        state: "REVOKED",
        keyVersion: data.key.keyVersion + 1,
        revocationVersion: data.key.revocationVersion + 1,
      },
      reservation: data.reservation,
      now: NOW + 4,
      rowCountSend: 1,
      rowCountLease: 1,
      rowCountBudget: 1,
    })).toEqual({ ok: false, code: "KEY_REVOKED" });
  });

  it("blocks Worker progress after Authorization revocation", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    expect(model.revokeAuthorization(ids.authorization).ok).toBe(true);
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "KEY_READ",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 1,
      rowCount: 1,
    })).toEqual({ ok: false, code: "LEASE_STATE_INVALID" });
  });

  it("revokes pre-send authority on Emergency and leaves SENT outcomes uncertain", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    toTransportCreated(model, lease, data);
    const permit = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    if (!permit.ok) throw new Error(permit.code);
    expect(model.activateEmergency("SYNTHETIC_INCIDENT").ok).toBe(true);
    expect(model.getLease(lease.leaseId)?.state).toBe("EMERGENCY_BLOCKED");
    expect(model.getSendAuthorization(permit.value.sendAuthorizationId)?.state)
      .toBe("REVOKED");
  });

  it("records SEND_OUTCOME_UNKNOWN without automatic retry", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    toTransportCreated(model, lease, data);
    const permit = model.issueSendAuthorization({
      leaseId: lease.leaseId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 3,
      ttlMs: 5_000,
    });
    if (!permit.ok) throw new Error(permit.code);
    expect(model.consumeSendAuthorization({
      sendAuthorizationId: permit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 4,
      rowCountSend: 1,
      rowCountLease: 1,
      rowCountBudget: 1,
    }).ok).toBe(true);
    expect(model.recordNetworkResult({
      leaseId: lease.leaseId,
      result: "SEND_OUTCOME_UNKNOWN",
    })).toMatchObject({
      ok: true,
      value: { state: "SEND_OUTCOME_UNKNOWN" },
    });
    expect(model.consumeSendAuthorization({
      sendAuthorizationId: permit.value.sendAuthorizationId,
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: model.getReservation(ids.reservation),
      now: NOW + 5,
      rowCountSend: 1,
      rowCountLease: 1,
      rowCountBudget: 1,
    })).toEqual({ ok: false, code: "SEND_AUTHORIZATION_REPLAYED" });
  });

  it("rejects expired, partitioned or retired Worker contexts", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "KEY_READ",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 15_001,
      rowCount: 1,
    })).toEqual({ ok: false, code: "WORKER_NOT_ACTIVE" });
    expect(model.heartbeat(ids.workerA, NOW + 15_001).ok).toBe(true);
    expect(model.retireWorker(ids.workerA).ok).toBe(true);
    expect(model.getLease(lease.leaseId)?.state).toBe("REVOKED");
  });

  it("closes failure and expiry terminals without reactivation", () => {
    const model = new OfflineExecutionLeaseModel();
    const allocator = makeAllocator();
    const data = seed(model);
    const lease = issue(model, allocator, data);
    expect(model.failBeforeSend({
      leaseId: lease.leaseId,
      rowCount: 1,
    })).toMatchObject({
      ok: true,
      value: { state: "FAILED_BEFORE_SEND" },
    });
    expect(model.progressLease({
      leaseId: lease.leaseId,
      next: "KEY_READ",
      workerInstanceId: ids.workerA,
      fencingToken: lease.fencingToken,
      key: data.key,
      reservation: data.reservation,
      now: NOW + 1,
      rowCount: 1,
    })).toEqual({ ok: false, code: "LEASE_STATE_INVALID" });

    const secondData = fixture(2);
    expect(model.seedCapability(secondData.capability).ok).toBe(true);
    expect(model.seedAuthorization(secondData.authorization).ok).toBe(true);
    expect(model.seedReservation(secondData.reservation).ok).toBe(true);
    const secondLease = issue(model, allocator, secondData);
    expect(model.expireLease({
      leaseId: secondLease.leaseId,
      now: NOW,
      rowCount: 1,
    })).toEqual({ ok: false, code: "LEASE_STATE_INVALID" });
    expect(model.expireLease({
      leaseId: secondLease.leaseId,
      now: secondLease.expiresAt,
      rowCount: 1,
    })).toMatchObject({
      ok: true,
      value: { state: "EXPIRED" },
    });
  });
});
````
<!-- END_EXACT_SOURCE id=S045 -->

### S046. preparation/production-trust/r2-r3-remediation/tests/fencing-audit-emergency.test.ts

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/tests/fencing-audit-emergency.test.ts`
- Bytes: `8185`
- SHA-256: `02ED83707FDA735091910825FA0AABA5BA6B69DD6EDFE7472CFDBE181C1059BD`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S046 sha256=02ED83707FDA735091910825FA0AABA5BA6B69DD6EDFE7472CFDBE181C1059BD bytes=8185 fence=fenced -->
````typescript
import { describe, expect, it } from "vitest";

import { OfflineR3AuditLedger, verifyR3AuditChain } from "../models/audit-ledger";
import { OfflineEmergencyControl } from "../models/emergency-control";
import { OfflineFencingRegistry } from "../models/fencing-registry";

const IDS = Object.freeze({
  workerA: "11111111-1111-4111-8111-111111111111",
  workerB: "22222222-2222-4222-8222-222222222222",
  leaseA: "33333333-3333-4333-8333-333333333333",
  leaseB: "44444444-4444-4444-8444-444444444444",
  resourceA: "55555555-5555-4555-8555-555555555555",
  resourceB: "66666666-6666-4666-8666-666666666666",
  subjectA: "77777777-7777-4777-8777-777777777777",
});

const NOW = Date.parse("2026-11-26T08:00:00Z");

describe("R3 persistent fencing reference model", () => {
  it("allocates monotonic tokens and rejects an old Worker token", () => {
    const fencing = new OfflineFencingRegistry();
    fencing.registerWorker({
      workerInstanceId: IDS.workerA,
      heartbeatAt: NOW,
    });
    fencing.registerWorker({
      workerInstanceId: IDS.workerB,
      heartbeatAt: NOW,
    });
    const old = fencing.allocate({
      leaseId: IDS.leaseA,
      resourceId: IDS.resourceA,
      workerInstanceId: IDS.workerA,
      now: NOW,
      expectedControlVersion: 1,
    });
    expect(old.ok).toBe(true);
    if (!old.ok) return;
    expect(fencing.revokeWorker({ workerInstanceId: IDS.workerA }).ok)
      .toBe(true);
    const takeover = fencing.allocate({
      leaseId: IDS.leaseB,
      resourceId: IDS.resourceA,
      workerInstanceId: IDS.workerB,
      now: NOW + 1,
      expectedControlVersion: 2,
    });
    expect(takeover.ok).toBe(true);
    if (!takeover.ok) return;
    expect(takeover.value.fencingToken).toBe(old.value.fencingToken + 1);
    expect(fencing.authorizeResourceWrite({
      resourceId: IDS.resourceA,
      allocation: old.value,
      workerInstanceId: IDS.workerA,
      now: NOW + 2,
    })).toEqual({ ok: false, code: "FENCING_TOKEN_STALE" });
    expect(fencing.authorizeResourceWrite({
      resourceId: IDS.resourceA,
      allocation: takeover.value,
      workerInstanceId: IDS.workerB,
      now: NOW + 2,
    })).toEqual({ ok: true, value: true });
  });

  it("scopes fencing per resource and fails closed without central authority", () => {
    const fencing = new OfflineFencingRegistry();
    fencing.registerWorker({
      workerInstanceId: IDS.workerA,
      heartbeatAt: NOW,
    });
    const first = fencing.allocate({
      leaseId: IDS.leaseA,
      resourceId: IDS.resourceA,
      workerInstanceId: IDS.workerA,
      now: NOW,
      expectedControlVersion: 1,
    });
    const second = fencing.allocate({
      leaseId: IDS.leaseB,
      resourceId: IDS.resourceB,
      workerInstanceId: IDS.workerA,
      now: NOW,
      expectedControlVersion: 2,
    });
    expect(first.ok && second.ok).toBe(true);
    if (!first.ok || !second.ok) return;
    expect(fencing.authorizeResourceWrite({
      resourceId: IDS.resourceA,
      allocation: first.value,
      workerInstanceId: IDS.workerA,
      now: NOW + 1,
    }).ok).toBe(true);
    fencing.setAuthorityAvailable(false);
    expect(fencing.authorizeResourceWrite({
      resourceId: IDS.resourceA,
      allocation: first.value,
      workerInstanceId: IDS.workerA,
      now: NOW + 2,
    })).toEqual({
      ok: false,
      code: "FENCING_ALLOCATION_FAILED",
    });
  });

  it("rejects stale heartbeats and stale control versions", () => {
    const fencing = new OfflineFencingRegistry();
    fencing.registerWorker({
      workerInstanceId: IDS.workerA,
      heartbeatAt: NOW,
    });
    expect(fencing.allocate({
      leaseId: IDS.leaseA,
      resourceId: IDS.resourceA,
      workerInstanceId: IDS.workerA,
      now: NOW,
      expectedControlVersion: 2,
    })).toEqual({
      ok: false,
      code: "FENCING_ALLOCATION_FAILED",
    });
    const allocated = fencing.allocate({
      leaseId: IDS.leaseA,
      resourceId: IDS.resourceA,
      workerInstanceId: IDS.workerA,
      now: NOW,
      expectedControlVersion: 1,
    });
    expect(allocated.ok).toBe(true);
    if (!allocated.ok) return;
    expect(fencing.authorizeResourceWrite({
      resourceId: IDS.resourceA,
      allocation: allocated.value,
      workerInstanceId: IDS.workerA,
      now: NOW + 15_001,
    })).toEqual({ ok: false, code: "WORKER_NOT_ACTIVE" });
  });
});

describe("R3 audit chain", () => {
  function event(index: number) {
    return {
      eventId: `${String(index).padStart(8, "0")}-0000-4000-8000-000000000000`,
      occurredAt: NOW + index,
      eventType: "WORKER_PROGRESS" as const,
      outcome: "ALLOW" as const,
      subjectId: IDS.subjectA,
    };
  }

  it("serializes concurrent appends into one contiguous chain", async () => {
    const ledger = new OfflineR3AuditLedger();
    await Promise.all(
      Array.from({ length: 20 }, async (_, index) => {
        expect(ledger.append(event(index + 1)).ok).toBe(true);
      }),
    );
    const snapshot = ledger.snapshot();
    expect(snapshot).toHaveLength(20);
    expect(snapshot.map((item) => item.event.sequence))
      .toEqual(Array.from({ length: 20 }, (_, index) => index + 1));
    expect(verifyR3AuditChain(snapshot)).toBe(true);
  });

  it("rejects duplicate IDs and detects digest or predecessor changes", () => {
    const ledger = new OfflineR3AuditLedger();
    const first = ledger.append(event(1));
    const second = ledger.append(event(2));
    expect(first.ok && second.ok).toBe(true);
    if (!first.ok || !second.ok) return;
    expect(ledger.append(event(1))).toEqual({
      ok: false,
      code: "AUDIT_EVENT_DUPLICATE",
    });
    expect(verifyR3AuditChain([
      first.value,
      { ...second.value, eventDigest: "sha256:" + "0".repeat(64) },
    ])).toBe(false);
    expect(verifyR3AuditChain([
      first.value,
      {
        ...second.value,
        event: {
          ...second.value.event,
          previousEventDigest: "sha256:" + "1".repeat(64),
        },
      },
    ])).toBe(false);
  });

  it("rejects two independently created sequence-one roots", () => {
    const firstLedger = new OfflineR3AuditLedger();
    const secondLedger = new OfflineR3AuditLedger();
    const first = firstLedger.append(event(1));
    const second = secondLedger.append(event(2));
    expect(first.ok && second.ok).toBe(true);
    if (!first.ok || !second.ok) return;
    expect(verifyR3AuditChain([first.value, second.value])).toBe(false);
  });
});

describe("R3 Emergency control", () => {
  it("increments epoch on activation and blocks old-epoch work", () => {
    const emergency = new OfflineEmergencyControl();
    const original = emergency.snapshot();
    const activated = emergency.activate({
      expectedVersion: original.version,
      reasonCode: "SYNTHETIC_INCIDENT",
    });
    expect(activated).toMatchObject({
      ok: true,
      value: { status: "DRAINING", epoch: original.epoch + 1 },
    });
    expect(emergency.mayStartNewWork(original.epoch)).toEqual({
      ok: false,
      code: "EMERGENCY_STOP_ACTIVE",
    });
  });

  it("requires stop, recovery request and a distinct second approver", () => {
    const emergency = new OfflineEmergencyControl();
    const activated = emergency.activate({
      expectedVersion: 1,
      reasonCode: "SYNTHETIC_INCIDENT",
    });
    if (!activated.ok) throw new Error(activated.code);
    const stopped = emergency.stop({
      expectedVersion: activated.value.version,
    });
    if (!stopped.ok) throw new Error(stopped.code);
    const requested = emergency.requestRecovery({
      expectedVersion: stopped.value.version,
      actorId: IDS.workerA,
    });
    if (!requested.ok) throw new Error(requested.code);
    expect(emergency.approveRecovery({
      expectedVersion: requested.value.version,
      approverActorId: IDS.workerA,
    })).toEqual({ ok: false, code: "EMERGENCY_STOP_ACTIVE" });
    const recovered = emergency.approveRecovery({
      expectedVersion: requested.value.version,
      approverActorId: IDS.workerB,
    });
    expect(recovered).toMatchObject({
      ok: true,
      value: { status: "NORMAL", epoch: requested.value.epoch + 1 },
    });
  });
});
````
<!-- END_EXACT_SOURCE id=S046 -->

### S047. preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FENCING_MODEL.md

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FENCING_MODEL.md`
- Bytes: `2589`
- SHA-256: `48D0E33681FEEBCD11BD674B4BF744461DED4DB8DB43F15D638FEC968827121A`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S047 sha256=48D0E33681FEEBCD11BD674B4BF744461DED4DB8DB43F15D638FEC968827121A bytes=2589 fence=raw -->
# PHASE_R2_R3_REMEDIATION_FENCING_MODEL

## 1. Allocation

Persistent control object:

```text
trust_r3_fencing_control(
  singleton_id,
  next_token,
  version,
  updated_at_ms
)
```

Allocation uses:

```text
SELECT ... FOR UPDATE
UPDATE next_token = next_token + 1
RETURNING next_token - 1
```

The allocation and Lease insertion commit in one transaction. Rollback also
rolls back allocation. No process-local counter or standalone sequence is used.

## 2. Why Not a Sequence

A PostgreSQL sequence can allocate increasing numbers without respecting the
commit order of Lease transactions. R3 requires a fencing value whose durable
visibility and Lease ownership follow one row-locked transaction.

## 3. Worker Takeover

```text
old Worker holds fence N
new Worker obtains fence N+1 for the same resource
Worker registration fence floor advances
old Worker with token N is rejected
```

The offline model and SQL drafts bind Worker, Capability, Lease, Budget,
Emergency epoch, Key version and permit ID.

## 4. Resource Scope

Fencing is scoped to a protected resource/Capability. A token allocated for a
different resource does not invalidate unrelated work merely because its
numeric value is higher.

Within one resource, only the current floor token can authorize an egress
operation.

## 5. No Central Authority

```text
central fencing authority unavailable
  -> no new allocation
  -> no new send authorization
```

A divided Worker cannot rely on cached local control state.

## 6. Egress Enforcement

The Provider does not validate application fencing. The trusted egress
component must be the only network path and must compare the permit and fence
with current central state immediately before the one write.

If any Worker can bypass the egress component and call the network directly,
fencing is not enforceable at the final boundary. That remains a deployment
blocker.

## 7. Recovery

| Situation | Result |
|---|---|
| Worker pauses, heartbeat stale | new progress/send denied |
| Lease expires | no further progress or send |
| new Worker takes over | higher fence; old Worker rejected |
| old Worker resumes | stale token rejected |
| Emergency epoch changes | old permit rejected |
| Key revoked | old permit rejected |
| central authority unavailable | fail closed |
| already sent | cannot be recalled; record unknown outcome |

## 8. Validation

Offline tests cover monotonic allocation, resource scope, Worker takeover,
stale heartbeat, stale control version and unavailable central authority.
Real multi-instance fencing is `MULTI_INSTANCE_TEST=NOT_EXECUTED`.
<!-- END_EXACT_SOURCE id=S047 -->

### S048. preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_THREAT_MODEL.md

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_THREAT_MODEL.md`
- Bytes: `3925`
- SHA-256: `6945F66EC216A932698DB0707745A73DE8D29034C0A781ECB7A5910D32B213A5`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S048 sha256=6945F66EC216A932698DB0707745A73DE8D29034C0A781ECB7A5910D32B213A5 bytes=3925 fence=raw -->
# PHASE_R2_R3_REMEDIATION_THREAT_MODEL

## 1. Method

STRIDE plus distributed authorization, replay, fencing and failure-boundary
analysis.

## 2. STRIDE

| Threat | Severity | Current offline control | Residual |
|---|---|---|---|
| Spoofed Worker/Actor | CRITICAL | trusted binding supplied by higher control plane; Worker ID and heartbeat bound | production session/actor service absent |
| Tampered Approval binding | CRITICAL | nonce, identity/evidence/snapshot/dossier/target digests and versions bound | production signature/read path not connected |
| Replayed Approval | HIGH | lock-first requestId and Approval uniqueness | PostgreSQL behavior not executed |
| Replayed Send Authorization | CRITICAL | `ISSUED -> CONSUMED`, unique Lease, one-use permit | trusted egress component not deployed |
| Budget double spend | HIGH | row-locked cumulative counters and budget version | PostgreSQL concurrency not executed |
| Stale Worker continues | CRITICAL | persistent fence floor, Worker state/heartbeat, higher token | direct Provider egress bypass would defeat it |
| Emergency bypass | CRITICAL | epoch checked at Consumption, Lease, Send and final permit | final write already started cannot be recalled |
| Key remains usable after revocation | HIGH | Key version/revocation version checked at each stage | revocation propagation not verified |
| Audit omission or fork | HIGH | audit head row locked last, single sequence, event/head updates required | cross-process behavior not executed |
| Sensitive logging | CRITICAL | audit excludes keys/cookies/raw content | future implementation must enforce |
| Partial-failure ambiguity | HIGH | database `SENT` distinct from Provider receipt; `SEND_OUTCOME_UNKNOWN` terminal | external exactly-once impossible |
| Request/response loss | HIGH | no automatic retry of consumed permit | operator process not deployed |

## 3. Confused Deputy

All downstream stages compare Worker, Capability, Authorization, Budget,
Approval digests, Key/revocation version, Emergency epoch, permission version
and policy version. A caller cannot substitute one context for another without
the conditional update returning zero rows or the model returning a context
mismatch.

## 4. Fencing Boundary

The database fence prevents an old Worker from obtaining new central send
permission after takeover. It does not cause an external Provider to reject a
request.

The final security boundary is:

```text
trusted egress component verifies current permit/fence/epoch/key
  -> performs exactly one network write
```

Any direct Worker network route outside this component is a critical deployment
blocker.

## 5. TOCTOU

| Interval | Control | Remaining risk |
|---|---|---|
| requestId read vs locks | lookups only after locks | none in modeled path |
| budget check vs reservation | same locked transaction | DB execution unverified |
| permit commit vs network write | final permit one-use and short TTL | stop can occur after commit |
| last check vs write | trusted egress short critical section | finite local race remains |
| response loss | unknown terminal state | Provider may have executed |

## 6. Audit Threat

Concurrent writers must not compute `previousEventDigest` independently. The
head row is locked and advanced conditionally; event IDs, sequences and digests
are unique. A failure rolls back the local security operation.

## 7. Emergency Threat

Emergency activation increments epoch before granting new permissions. Old
Capabilities, Leases and permits fail. The database cannot reverse a Provider
request already sent.

## 8. Remaining Production Blockers

- real PostgreSQL row-lock and isolation tests;
- real multi-instance fence test;
- trusted egress deployment and network isolation;
- production Actor/session;
- production Key registry and secret management;
- production trusted clock and Snapshot allowlist;
- operational unknown-outcome reconciliation.
<!-- END_EXACT_SOURCE id=S048 -->

### S049. preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_RISK_REGISTER.md

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_RISK_REGISTER.md`
- Bytes: `1907`
- SHA-256: `04357AA0F8D0F7262954900E9350A03E0C916CD3FFD66D9F88A16C9BB69EEA5D`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S049 sha256=04357AA0F8D0F7262954900E9350A03E0C916CD3FFD66D9F88A16C9BB69EEA5D bytes=1907 fence=raw -->
# PHASE_R2_R3_REMEDIATION_RISK_REGISTER

## 1. Open Findings

| ID | Severity | Finding | Status |
|---|---|---|---|
| R3-R1 | HIGH | no real PostgreSQL execution | blocked by authorization; test plan only |
| R3-R2 | HIGH | no real multi-instance/central coordinator test | `MULTI_INSTANCE_TEST=NOT_EXECUTED` |
| R3-R3 | CRITICAL if deployed without egress isolation | Worker could bypass trusted egress | production blocker |
| R3-R4 | HIGH | finite interval after permit commit before network write | residual; short TTL/unknown handling |
| R3-R5 | HIGH | no production trusted clock/Actor/key registry | production blocker |
| R3-R6 | HIGH | actual Provider cost/billing absent | conservative synthetic limit only |
| R3-R7 | MEDIUM | SQL driver command tag semantics not exercised | future integration test |
| R3-R8 | MEDIUM | offline concurrency is single-process | explicitly not production evidence |

## 2. Closed Offline Findings

| Defect | Resolution |
|---|---|
| Lease insert/update contradiction | four separate transactions and exact predecessor states |
| missing row-count checks | mandatory markers plus model `requireExactlyOne()` |
| budget lacked cumulative counters | persistent request/USD counters in one locked transaction |
| requestId pre-lock race | lock-first and post-lock request re-read |
| unique conflict had no recovery | rollback + winner read + complete binding validation |
| process-local fence | persistent row-locked allocator |
| send permit replay | one-use explicit state transition |
| unknown outcome auto-release | forbidden; explicit reconciled settlement only |
| audit separate from action | audit append included in security transactions |

## 3. Production Classification

```text
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

The R3 design can pass offline review while production remains blocked.
<!-- END_EXACT_SOURCE id=S049 -->

### S050. preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FINAL_REPORT.md

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_FINAL_REPORT.md`
- Bytes: `7736`
- SHA-256: `9917648CA16E3A88DCC7E2ACA0D5877DC370A530D2484BA24849D59265739DA9`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S050 sha256=9917648CA16E3A88DCC7E2ACA0D5877DC370A530D2484BA24849D59265739DA9 bytes=7736 fence=raw -->
# PHASE_R2_R3_REMEDIATION_FINAL_REPORT

## 1. Final Status

```text
R2_R3_REMEDIATION_PASS
R2_R3_OFFLINE_ACCEPTANCE=PASS
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

This PASS covers the authorized offline design, reference models, SQL drafts
and tests. It does not approve production deployment.

## 2. Required Acceptance Criteria

```text
LEASE_SEND_SQL_STATE_MACHINE=PASS
SQL_ROW_COUNT_ENFORCEMENT=PASS
GLOBAL_BUDGET_ATOMIC_RESERVATION=PASS
APPROVAL_SAME_REQUEST_ID_IDEMPOTENCY=PASS
APPROVAL_DIFFERENT_REQUEST_CONFLICT=PASS
COMMIT_AMBIGUITY_RECOVERY=PASS
PERSISTENT_FENCING=PASS
EMERGENCY_SEND_AUTHORIZATION_SEMANTICS=PASS
AUDIT_CHAIN_CONCURRENCY=PASS
SQL_MODEL_CONTRACT_CONSISTENCY=PASS

SQL_STATIC_ANALYSIS=PASS
SQL_NEGATIVE_TESTS=PASS
OFFLINE_MODEL_TESTS=PASS
LOCAL_UNIT_TESTS=PASS
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```

## 3. Defects Closed

### Execution Lease / Send Authorization

The contradictory R2 transaction is replaced by four stages:

```text
Lease Issuance
Worker Progress
Send Authorization Issuance
Send Authorization Consumption
```

The Lease can no longer skip states, and permit issuance cannot precede
`TRANSPORT_CREATED`. Every security update requires exactly one affected row.

### Global Budget

R3 uses persistent cumulative counters:

```text
reserved_requests
consumed_requests
reserved_usd_micros
consumed_usd_micros
budget_version
```

Reservation, release, known commit, unknown settlement and explicit
reconciliation are separate tested transitions. Floating-point money is absent.

### Approval Idempotency

The transaction locks Emergency, Key and Approval before re-reading
`request_id`. Same-request exact replay returns the persisted IDs; changed
binding fails; another request for a consumed Approval fails; unique losers
recover only by reading and validating the winner.

### Persistent Fencing

`trust_r3_fencing_control` is a singleton row-locked allocator. Token
allocation and Lease issuance commit together. A higher Worker/resource fence
rejects old Worker permits and progress.

## 4. Associated Repairs

- Approval binding includes `nonceDigest` in model and SQL.
- Emergency state persists requested and approving Actors.
- Emergency activation and recovery have explicit audited SQL transitions.
- Key revocation includes same-transaction audit.
- Budget release/settlement includes actual audit append in every transaction.
- `SEND_OUTCOME_UNKNOWN` is terminal, charged, and never automatically retried.
- Audit append locks one singleton head and advances sequence/digest once.
- Static analysis includes negative fixtures, not only success string checks.

## 5. Files Created

Core reports:

```text
PHASE_R2_R3_REMEDIATION_BASELINE.md
PHASE_R2_R3_REMEDIATION_BASELINE_SHA256SUMS.txt
PHASE_R2_R3_REMEDIATION_ARCHITECTURE.md
PHASE_R2_R3_REMEDIATION_CONTRACTS.md
PHASE_R2_R3_REMEDIATION_TRANSACTION_MODEL.md
PHASE_R2_R3_REMEDIATION_EXECUTION_GATE.md
PHASE_R2_R3_REMEDIATION_BUDGET_MODEL.md
PHASE_R2_R3_REMEDIATION_IDEMPOTENCY_MODEL.md
PHASE_R2_R3_REMEDIATION_FENCING_MODEL.md
PHASE_R2_R3_REMEDIATION_AUDIT_EMERGENCY_MODEL.md
PHASE_R2_R3_REMEDIATION_SQL_REVIEW.md
PHASE_R2_R3_REMEDIATION_TEST_MATRIX.md
PHASE_R2_R3_REMEDIATION_POSTGRESQL_TEST_PLAN.md
PHASE_R2_R3_REMEDIATION_THREAT_MODEL.md
PHASE_R2_R3_REMEDIATION_RISK_REGISTER.md
PHASE_R2_R3_REMEDIATION_IMPLEMENTATION_PLAN.md
PHASE_R2_R3_REMEDIATION_DEFECT_DIFF.md
PHASE_R2_R3_REMEDIATION_CROSS_REVIEW.md
PHASE_R2_R3_REMEDIATION_FINAL_REPORT.md
```

Models and tests:

```text
contracts.ts
lock-order.ts
vitest.config.ts
models/approval-consumption.ts
models/audit-ledger.ts
models/budget-ledger.ts
models/consumption-recovery.ts
models/emergency-control.ts
models/execution-lease.ts
models/fencing-registry.ts
models/sql-analyzer.ts
tests/approval-consumption.test.ts
tests/budget-ledger.test.ts
tests/contracts-lock-order.test.ts
tests/execution-lease.test.ts
tests/fencing-audit-emergency.test.ts
tests/integration-flow.test.ts
tests/sql-model-consistency.test.ts
tests/sql-review.test.ts
```

SQL drafts:

```text
sql/00-schema.sql
sql/10-lease-issuance.sql
sql/20-worker-progress.sql
sql/30-send-authorization-issuance.sql
sql/40-send-authorization-consume.sql
sql/50-budget-reservation.sql
sql/55-budget-release-settlement.sql
sql/60-approval-consumption.sql
sql/70-fencing-registry.sql
sql/80-audit-append.sql
sql/90-emergency-key-control.sql
```

## 6. Files Modified

No existing R1/R2 source, test, SQL, report, Manifest, production code or frozen
security asset was modified. All implementation changes are new R3 files under
`preparation/production-trust/r2-r3-remediation/`.

## 7. Files Outside Scope

```text
FILES_OUTSIDE_SCOPE=0
MAIN_WORKSPACE_ACCESS=0
SRC_SCRIPTS_MODIFIED=0
R31_R36_MODIFIED=0
IDENTITY_CORE_MODIFIED=0
A3_D1_D2_MODIFIED=0
```

## 8. Test Results

```text
R2-R3 Vitest:                 8 files / 74 tests PASS
R2 regression:               10 files / 80 tests PASS
R1 regression:               16 files / 91 tests PASS
R31-R36 relevant regression: 24 files / 179 tests PASS
PowerShell Launcher:         40/40 PASS
PowerShell Key Session:      25/25 PASS
Fetch enforcement:            4/4 PASS
PowerShell total:            69/69 PASS
PowerShell 5.1 Parser:       PASS / 6 scripts
TypeScript strict:           PASS
ESLint:                      PASS
Next.js production build:    PASS
```

Test commands:

```text
node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2-r3-remediation/vitest.config.ts
node node_modules/vitest/vitest.mjs run --config preparation/production-trust/r2/vitest.config.ts
node node_modules/vitest/vitest.mjs run --config preparation/production-trust/vitest.config.ts
powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-only-launcher.ps1
powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-key-session.ps1
powershell.exe -NoProfile -ExecutionPolicy Bypass -File scripts/windows/test-fetch-only-production-enforcement.ps1
npx tsc --noEmit --pretty false
npx eslint preparation/production-trust/r2-r3-remediation
pnpm build
```

## 9. Test Evidence Classification

| Class | Status |
|---|---|
| Static SQL Analysis | PASS |
| Offline Reference Model | PASS |
| Local Unit Test | PASS |
| PostgreSQL Integration Test | NOT_EXECUTED |
| Multi-instance Test | NOT_EXECUTED |
| Real Provider Test | NOT_EXECUTED |

The in-memory synchronous and Promise interleaving tests are not PostgreSQL
concurrency evidence.

## 10. Safety Boundaries

```text
REAL_KEY_ACCESSED=NO
REAL_API_CALLED=NO
NETWORK_ACCESSED=NO
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
```

The production Fetch entry hash remains:

```text
1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309
```

and still reports zero Key reads, Transport creations and network calls.

## 11. Cross-Review

Internal cross-review is recorded in:

```text
PHASE_R2_R3_REMEDIATION_CROSS_REVIEW.md
```

Nine integration findings were closed. No unresolved P0 offline defect remains.
The work was performed with same-host Codex subagents and the coordinating
agent; it is not an independent third-party audit.

## 12. Residual Risks

The largest remaining risks are:

- no real PostgreSQL integration execution;
- no real multi-instance/egress enforcement test;
- finite final-check-to-network-write interval;
- production trust services not connected;
- no external independent audit;
- no real Provider/billing validation.

## 13. Stop State

```text
STOP_AFTER_R2_R3_OFFLINE_ACCEPTANCE
R3_IMPLEMENTATION_AUTHORIZED=NO
REAL_FETCH_AUTHORIZED=NO
```
<!-- END_EXACT_SOURCE id=S050 -->

### S051. preparation/production-trust/PHASE_R2_R3_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md

- Category: `F_R2_R3_COMPARATIVE`
- Path: `preparation/production-trust/PHASE_R2_R3_FULL_SECURITY_REVIEW_BUNDLE_REPORT.md`
- Bytes: `4240`
- SHA-256: `7F9D6B4908850BA2597BB7939F3A4B8D45A5B8BB8EFA9CFF5ACBA0CFC4AAAC8C`
- Description: Original R2-R3 comparison material

<!-- BEGIN_EXACT_SOURCE id=S051 sha256=7F9D6B4908850BA2597BB7939F3A4B8D45A5B8BB8EFA9CFF5ACBA0CFC4AAAC8C bytes=4240 fence=raw -->
# PHASE_R2_R3_FULL_SECURITY_REVIEW_BUNDLE_REPORT

## 1. Bundle Status

```text
BUNDLE_STATUS=PASS
R2_R3_REMEDIATION_PASS
PRODUCTION_IMPLEMENTATION=NOT_STARTED
PRODUCTION_ENFORCEMENT=BLOCKED
REAL_FETCH_AUTHORIZED=NO
```

The Bundle is complete for the declared offline scope. It is not proof of
production deployment, real PostgreSQL concurrency or Provider behavior.

## 2. Bundle Identity

```text
BUNDLE_BYTES=474813
BUNDLE_SHA256=0D19F9B25F2D3E9444AE78A1C641828E43708378FF911F1759BEDA47638CAF0F
SOURCE_FILES_INCLUDED=64
SOURCE_HASH_MISMATCHES=0
BODY_EXACT_EQUALITY_ERRORS=0
```

Bundle path:

```text
preparation/production-trust/PHASE_R2_R3_FULL_SECURITY_REVIEW_BUNDLE.md
```

## 3. Included Evidence

```text
R3 core reports
all 11 R3 SQL drafts
all R3 reference models and contracts
all 8 R3 test files
relevant original R2 comparison files
R2 baseline and final Manifests
R31-R36 frozen Manifest
R36 frozen acceptance report
production Fetch entry hard-block source
historical Vitest recovery source report
R3 remediation Manifest
```

## 4. Defect Review

```text
LEASE_SEND_SQL_STATE_MACHINE=PASS_OFFLINE
SQL_ROW_COUNT_ENFORCEMENT=PASS_OFFLINE
GLOBAL_BUDGET_ATOMIC_RESERVATION=PASS_OFFLINE
APPROVAL_SAME_REQUEST_IDEMPOTENCY=PASS_OFFLINE
APPROVAL_DIFFERENT_REQUEST_CONFLICT=PASS_OFFLINE
COMMIT_AMBIGUITY_RECOVERY=PASS_OFFLINE
PERSISTENT_FENCING=PASS_OFFLINE
EMERGENCY_SEND_AUTHORIZATION_SEMANTICS=PASS_OFFLINE
AUDIT_CHAIN_CONCURRENCY=PASS_OFFLINE
SQL_MODEL_CONTRACT_CONSISTENCY=PASS_OFFLINE
```

## 5. Test Results

```text
R2-R3 Vitest:                  8 files / 74 tests PASS
R2 regression:                10 files / 80 tests PASS
R1 regression:                16 files / 91 tests PASS
R31-R36 relevant regression:  24 files / 179 tests PASS
PowerShell total:             69/69 PASS
PowerShell 5.1 Parser:        PASS / 6 scripts
TypeScript strict:            PASS
ESLint:                       PASS
Next.js production build:     PASS
```

Evidence classification:

```text
POSTGRESQL_INTEGRATION=NOT_EXECUTED
MULTI_INSTANCE_TEST=NOT_EXECUTED
REAL_PROVIDER_TEST=NOT_EXECUTED
```

In-memory synchronous/Promise tests are not described as real PostgreSQL or
multi-instance evidence.

## 6. Freeze Status

The source catalog in the Bundle records each path, byte count and SHA-256.
After Bundle generation, all 64 source bodies were re-read and compared
byte-for-byte with the embedded bodies.

The immutable R2 baseline was checked before remediation:

```text
R2_BASELINE_ENTRIES=34
R2_BASELINE_MISMATCHES=0
```

The R31-R36 frozen Manifest was checked:

```text
R31_R36_ENTRIES=68
R31_R36_MISMATCHES=0
```

The remediation Manifest is separate:

```text
preparation/production-trust/r2-r3-remediation/PHASE_R2_R3_REMEDIATION_SHA256SUMS.txt
ENTRIES=49
SHA256=E392CB5985C3EC2C2671278BCF7DBFEA37B3B29208B20A92171DBB8E1FC5176A
```

## 7. Vitest Historical Recovery Incident

The prior R2 review phase's mis-ordered `--json` argument overwrote:

```text
src/server/public-enterprise-search/diagnostics/fetch-diagnostic-budget.test.ts
```

Historical expected hash:

```text
A36EAAB0CDBD630C4CE21B1059D0E1330DD3BB0E957B2ECAC8FECEFEFAC5C58C
```

Restored hash:

```text
A36EAAB0CDBD630C4CE21B1059D0E1330DD3BB0E957B2ECAC8FECEFEFAC5C58C
```

The live pre-overwrite bytes and exact discovery/stop timestamps were not
recorded. Source-map provenance is only partially verifiable. The Bundle
contains the exact historical command, cache path, cache hash, cache
timestamps, restoration method and residual forensic limitations.

## 8. Safety Accounting

```text
MAIN_WORKSPACE_MODIFIED=NO
SRC_SCRIPTS_MODIFIED=NO
R31_R36_MODIFIED=NO
IDENTITY_CORE_MODIFIED=NO
A3_D1_D2_MODIFIED=NO
REAL_KEY_ACCESSED=NO
REAL_API_CALLED=NO
NETWORK_ACCESSED=NO
DATABASE_CONNECTED=NO
SQL_EXECUTED=NO
DOCKER_ACCESSED=NO
GITHUB_ACCESSED=NO
DEPENDENCIES_INSTALLED=NO
```

## 9. Residual Risk

The Bundle remains limited by:

- `REQUIRES_POSTGRESQL_INTEGRATION`;
- `REQUIRES_REAL_MULTI_INSTANCE_TEST`;
- `REQUIRES_EXTERNAL_PROVIDER_TEST`;
- the unavoidable final local-authorization-to-network-write interval;
- absence of third-party independent audit.

The sole production Fetch entry remains hard-blocked with zero Key reads,
Transport creations and network calls.
<!-- END_EXACT_SOURCE id=S051 -->

### S052. PHASE_R31_R36_SHA256SUMS.txt

- Category: `G_FREEZE_EVIDENCE`
- Path: `PHASE_R31_R36_SHA256SUMS.txt`
- Bytes: `9031`
- SHA-256: `D0191FBB856E284AE40614A16F9B92B69B45D1D59DB4E2FAD4D52DDB1DC4778C`
- Description: Immutable freeze evidence

<!-- BEGIN_EXACT_SOURCE id=S052 sha256=D0191FBB856E284AE40614A16F9B92B69B45D1D59DB4E2FAD4D52DDB1DC4778C bytes=9031 fence=fenced -->
````text
00BC115CD44BA1A31B4F5AE22570846914953DEF334C33BEE0218A21B000A6C9  src/server/public-enterprise-search/diagnostics/fetch-diagnostic-cli.test.ts
03EA89B6A64D734156474D90B610DA77C07C0899CE0E33864CD749B3A4F57204  src/server/public-enterprise-search/identity/identity-gate.ts
0839837FBB07C599D4D66912086B3CF38D00E71DCBC01B53EB7A25DFED6370F7  src/server/public-enterprise-search/provider/provider-factory-protection.test.ts
0A30A46A8BB1DCA887168BB9D6109A3CF96E6D01B21124824B63001F7C2EFA5A  PHASE_R34_BLOCKER_REPORT.md
11B6F83DF6D4F681356CF976515C7E94B7648B6B109DE074A614709DB0D7779D  src/server/public-enterprise-search/provider/aux-http-transports.test.ts
1583366A2A7C5FF6C84CDD0A41E5152001E2268E6B797B480586BD376A099BD1  src/server/public-enterprise-search/provider/deepseek-fetch-loopback.test.ts
17EE55FF45DF41EAC0C942CC34A657B09998E193E482A409C6EC1D6E4FE5E145  archive/r31-r36-original-baseline/src__server__public-enterprise-search__provider__deepseek-http-transport.test.ts.txt
1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309  src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts
1D3F57F3E024DB071D383A08491A5FE72D006209CC41F30ECD0E7E4FE2CC9339  snapshot-archive/real-provider-trial/20261126-identity-correction-01/lead.json
1D3F57F3E024DB071D383A08491A5FE72D006209CC41F30ECD0E7E4FE2CC9339  test-results/real-provider-trial/20261126-identity-correction-01/lead.json
209CA4DDA0803D76B79B79B51A613C41069A569FE7EEF7ADB1AFFB4FCC94BD95  PHASE_R36_FINAL_SECURITY_ACCEPTANCE_REPORT.md
24122EF46B62C16130F695607C77EB7C6083C07208EB9AE2317FF73AB64CD2DB  scripts/run-real-provider-trial.ts
246E1CBCCB3B37FCCC4CDD28DF981C5AF3AD87438C8882FBAFE2D78C6E43CA26  src/server/public-enterprise-search/provider/provider-execution-authorization.ts
25DA4DDB40B5A26C2C47940B2136723BD2A555FC599BB345BBEC1C4150E07494  PHASE_R35_BYPASS_COVERAGE_REPORT.md
25DCFE0C567FF8245A9CA2148228FF96F4C671B6D7668B3D27CA42317C608127  scripts/windows/test-fetch-key-session.ps1
26F108A11F0C8204E8A131DDB949B2D513397BBF530D49E5B449F1F74C1B360B  src/server/public-enterprise-search/identity/identity-gate.test.ts
30A6B4A42FAD52699BB2BB5FD3A5C84C36D6BC706C2F10AB39AB56DCB8501239  archive/r31-r36-original-baseline/src__server__public-enterprise-search__provider__deepseek-model-http-transport.ts.txt
327BFF2CCD84F1EF7F50CA15D70CC49916187E0B53AA560BF9E9DBA5383875D9  src/server/public-enterprise-search/local-live/live-config.test.ts
3DBF3819C8113A90AD7A49292993C65F0F726E0DFDD29387A467F4E93E27A418  archive/r31-r36-original-baseline/src__server__public-enterprise-search__provider__deepseek-fetch-loopback.test.ts.txt
3EAB2CC03BB377AC987333B359C751B4FDE1EEF7050DBF5D271A66AE317CFF53  src/server/public-enterprise-search/local-live/live-config.ts
44FC2153675107E0E61DBA8E88E955281B913D3341718C224110AB5B2F6C7F4D  package.json
46DAA52C5F8E4BF68BC8F7A6A3B49A85F4115386559075C6CF530BEBBE30ACDF  src/server/public-enterprise-search/provider/deepseek-http-transport.ts
489ACE6B24DB59F4E8C083BE5C3A0F5E937EA23DE1ADC2D7289B0480504BE24D  PHASE_R27_R30_SHA256SUMS.txt
4F519236B7E9BFECC4706D789E5A8300FFED1BD733F972343FE33B88EB542077  src/server/public-enterprise-search/identity/identity-contract.ts
53A24FB36B2EEB39D1E2DBAEC2AC37E283AD3B7F6B6787BA4D39274AB7855F70  src/server/public-enterprise-search/diagnostics/fetch-diagnostic.ts
54E0BC7368530C99BB0644D7907350D9702DFCA3425BC8BF97249C58144F9CAF  PHASE_R31_R36_RESIDUAL_RISK_REGISTER.md
5C863CD05586CB4FFBE73DC038B82BD477C7410EF126F4B8AC5002176ED10BD5  src/server/public-enterprise-search/trial/run-real-provider-trial.zero-network.test.ts
5D7BD4DC6CE69722BA6195E4EAE21445AD8B784F53B54397C0C121C17E700604  src/server/public-enterprise-search/provider/deepseek-http-transport.test.ts
5E8D22A7EBB2370DF7AD20B063DCAD29A27C532DF261D58ED35E05ABB4E2493A  archive/r31-r36-original-baseline/src__server__public-enterprise-search__trial__run-real-provider-trial.ts.txt
61466EA1CB4B57FF5086B42F3D9CB865D0F33B10AD3387573DA88F2146D77B6C  archive/r31-r36-original-baseline/scripts__run-real-provider-trial.ts.txt
648340B2B4D0AC7A9DBE74665F566B22815F0B99082D76FB0AC4EA6874B160E6  src/server/public-enterprise-search/identity/runtime/production-fetch-entry.test.ts
6912ABF5078DF7F927F863716603B474A1C0BF8DC82545701C440B08EFA865BB  PHASE_R31_BYPASS_INVENTORY.md
6FAC8A84F5738DFA4037066A5745131F135F293DBE6949BDDB97DE6188640B2A  archive/r31-r36-original-baseline/src__server__public-enterprise-search__diagnostics__fetch-diagnostic.ts.txt
7AF5A007D9FCABB33A60762D1787AFDAB851A3241EB0ADE5E7005E01804663C7  src/server/public-enterprise-search/provider/deepseek-fetch-http-transport.ts
7D159F0B2E047F2B67D3E9B5EA82F12D8B4344740C358BB5466FCE3A25F5F74A  src/server/public-enterprise-search/trial/run-real-provider-trial.ts
802A3981C35E8DDEDBBDA80D02825454C9FA23DD862881C5EA7C119D9AF1E450  archive/r31-r36-original-baseline/src__server__public-enterprise-search__provider__deepseek-http-transport.ts.txt
8A43200C66FBA4B6A0244C1EAEB9EB0DA0BEA5F44FF04491E298EF52A6F8CD4C  PHASE_R35_FULL_SECURITY_TEST_MATRIX.md
8A86D252CC0DED62523515C03A43AA81BD3C0C0C798752F5E901DAA1D0E02556  src/server/public-enterprise-search/identity/runtime/fetch-entry-guard.ts
8BE8EC0F82220F93D16D6784A37E39400239F632852CBC5E3D812374EA6B068F  snapshot-archive/real-provider-trial/20261125-preflight-02/lead.json
8BE8EC0F82220F93D16D6784A37E39400239F632852CBC5E3D812374EA6B068F  test-results/real-provider-trial/20261125-preflight-02/lead.json
8DE91FA65ECB77A204BAB03DAB6B834BCE3085DC2E56EEEE5EA9C46FA9E4D83D  PHASE_R33_UNIQUE_FETCH_ENTRY_DESIGN.md
8E6E79E2134F1EC5A70C94D4C95EBC207AB80B946D64717787A5084D0F4F5808  scripts/windows/fetch-only-launcher-child-fixture.ps1
926DFD4A33A662BAAB424E7C9FBBFD5FB16B74BE2E6119AD9F6A0D5144B719B4  pnpm-lock.yaml
944623E5B1A6F658288C9E3B53040BE0A0DE34BDAD1771D905876081D421C51D  evidence/r31-r36/PHASE_R36_AUDIT_END_SHA256SUMS.txt
944623E5B1A6F658288C9E3B53040BE0A0DE34BDAD1771D905876081D421C51D  evidence/r31-r36/PHASE_R36_AUDIT_START_SHA256SUMS.txt
9739843EC193472305210FF4951E6810037DD6D59A26046BE6995774C8681477  archive/r31-r36-original-baseline/src__server__public-enterprise-search__provider__deepseek-fetch-http-transport.ts.txt
97F5EC2ED12E86F99BDF74DE1E7887C6BCFF30B073ACDE269B1FB48FA0F09071  PHASE_FETCH_ONLY_R1_R4_SHA256SUMS.txt
A1F2CC6D82717EFD7B8BE48E0F6848C2745988B9AB2B8B76C5128BCA24C57094  src/server/public-enterprise-search/identity/runtime/fetch-entry-guard.test.ts
A2CC118A59084DB09E4C26B1E9B1CCC0CB9651842F03034148848DCFDC76370D  archive/r31-r36-original-baseline/src__server__public-enterprise-search__provider__aux-http-transports.test.ts.txt
A312E4F316DB76F6094D5D8866D5A66499E27B9972EBB42314F6868CB0CBE53F  PHASE_R33_UNIQUE_FETCH_ENTRY_IMPLEMENTATION_REPORT.md
A5FB583C337C611723B027B9A518F1E63B86DB391422FD44E0974966D52A623C  src/server/public-enterprise-search/diagnostics/fetch-diagnostic.test.ts
A664EC54E6148D4CC122743B9DF80B18EDA6CDFB54DBD7B1EC94455F0E95811E  archive/r31-r36-original-baseline/src__server__public-enterprise-search__diagnostics__fetch-diagnostic.test.ts.txt
AC6ADD268F37A74442504A297D872DBAEF33B39A17A0809CC153572A285A018F  PHASE_R34_PRODUCTION_TRUST_CAPABILITY_MATRIX.md
B29B060480E74716205AC6BD99DC38503449295C4E5CD3185A6C68BAA3345ADD  PHASE_R32_BYPASS_REGRESSION_REPORT.md
BAF3957D2EDB2946DDAD3709D00E2F7D68C3B0D5B10BC18312BE1D040D4ED382  src/server/public-enterprise-search/trial/run-real-provider-trial-cli.test.ts
BB0E2150D8BBF7707D97858D4C6C6891BB54F8A0C253AD391DA8413C6D116783  PHASE_R31_FILE_SCOPE_AND_BASELINE.md
BC17C580AA96A4D3E96CCA357DBA0FD80E5DFB890D82A9D9B5F0CF6584DB215F  scripts/windows/fetch-key-session.ps1
BC3E7AB65DB50D592ACEE2DADA3D2664AA8A3B4C313AB6DB26839BEC721E662D  PHASE_R32_BYPASS_REMEDIATION_REPORT.md
BD5DFC790E60C2EE3F3FCB07ABFFBE002222AAA40DA435695A1984794DCB15FB  src/server/public-enterprise-search/trial/run-real-provider-trial.test.ts
BDB4873AC0B2EF015486DEF90383EB64920E3A6039CBF3C170F81AB991072FC1  PHASE_R31_R36_MASTER_FINAL_REPORT.md
BE49C66CE5FAA64A4315B277698D2818A3E862BBEDD757A4127E88F313650170  PHASE_R31_FULL_PROVIDER_CALLGRAPH_REPORT.md
C602B5788E3C6207C8E2C20DCA02BB05E49807E6ACA0B4568C3EBE560DA6194D  src/server/public-enterprise-search/provider/deepseek-model-http-transport.ts
CD2E0AD6744753DCB6771BA84EB0862D3D66C892F53AA95E5C7F5548FC6CB85D  archive/r31-r36-original-baseline/src__server__public-enterprise-search__trial__run-real-provider-trial.test.ts.txt
D2B1CF4B288BFECAA05A87E5356060F475DB2316B5C7F98E74F5B62FF202CD8B  scripts/windows/test-fetch-only-launcher.ps1
D5F0C17718C3FEEB0F671EDAB9A6816F10FC08531FCE0E90E0B1ED0FA076EE04  PHASE_R34_DEPLOYMENT_REQUIREMENTS.md
D7CDE30D887378FDBC4CF96D4A37F815FE4C3CE1AF4BF16486EBA4AD1E4A82AF  PHASE_R35_SECURITY_TEST_REPORT.md
FA9CC4BCCD73937F75FACC75DECDA21D1373DBB83FAD81EC6891FC1F0A6DCAB8  PHASE_R33_ENTRY_ENFORCEMENT_TEST_REPORT.md
FAE52C794CED2B0A0CAE98821E85B531314CAA7E0CED777B6CBE4D608DD19679  src/server/public-enterprise-search/provider/provider-execution-authorization.test.ts
````
<!-- END_EXACT_SOURCE id=S052 -->

### S053. src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts

- Category: `G_FREEZE_EVIDENCE`
- Path: `src/server/public-enterprise-search/identity/runtime/production-fetch-entry.ts`
- Bytes: `933`
- SHA-256: `1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309`
- Description: Immutable freeze evidence

<!-- BEGIN_EXACT_SOURCE id=S053 sha256=1B2A7104D65C921D95A919CD1EC4FA11B29E6375224553396A096A674943D309 bytes=933 fence=fenced -->
````typescript
import "server-only";

/**
 * The sole future production Fetch entry.
 *
 * R31-R36 deliberately provides no dependency injection, environment switch,
 * or fallback composition. Production Actor, approval storage, trusted clock,
 * key registry, and snapshot allowlist are not connected, so this entry is a
 * stable fail-closed choke point rather than an authorizing implementation.
 */
export type ProductionFetchEntryResult = Readonly<{
  status: "BLOCKED";
  code: "PRODUCTION_FETCH_TRUST_UNAVAILABLE";
  productionTrustConnected: false;
  keyReads: 0;
  transportCreations: 0;
  networkCalls: 0;
}>;

export async function runProductionFetchEntry(
  input: unknown,
): Promise<ProductionFetchEntryResult> {
  void input;
  return Object.freeze({
    status: "BLOCKED",
    code: "PRODUCTION_FETCH_TRUST_UNAVAILABLE",
    productionTrustConnected: false,
    keyReads: 0,
    transportCreations: 0,
    networkCalls: 0,
  });
}
````
<!-- END_EXACT_SOURCE id=S053 -->

