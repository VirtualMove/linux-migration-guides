# Verify a Linux rebuild and read the result in context

Compare the rebuilt target with the attestation created for the migration. Keep application acceptance and cutover approval alongside the technical report.

**Watch:** [What signed migration evidence proves](https://www.youtube.com/watch?v=0uwder9Jthg).

## 1. Match the evidence to the workload

Keep the source identification, target release, client version, migration attestation, and operator's execution record together. Confirm that the target being examined belongs to this migration.

## 2. Verify the target

For an already mounted target filesystem:

```bash
vrtmv verify --attestation out/vrtmv-attestation.json --root /mnt/rebuild
```

To write JSON and request signing with an authenticated account:

```bash
vrtmv verify --attestation out/vrtmv-attestation.json \
  --root /mnt/rebuild --sign --json --out out/verification.json
```

Use the [current command reference](https://docs.vrtmv.com/commands/verify.html) for target-type options. Inspect the report to confirm whether signing succeeded.

## 3. Read more than the headline verdict

Check the measured classes, gaps, source coverage, and `unverified` categories. Decide what additional evidence your application needs. A container demonstration does not establish VM boot behavior, and matching package/configuration checks do not establish database upgrade success or response equivalence.

The [recent recorded demo](https://www.youtube.com/watch?v=LNM01hmRdZs&t=135s) explicitly discusses those boundaries. Use it to practice reading the findings, rather than treating it as a production acceptance result.

## 4. Understand the signature

A valid signature authenticates the signed evidence and protects its integrity. It does not extend measurement coverage or turn a partial result into a complete one.

## 5. Complete acceptance

Use the [acceptance checklist](../checklists/migration-acceptance.md) to record application tests, data checks, ownership, and rollback readiness. Review gaps with the responsible engineer before approving cutover.

## References

- [verify command](https://docs.vrtmv.com/commands/verify.html)
- [Parity attestation documentation](https://docs.vrtmv.com/concepts/attestation.html)

Documentation check: November 9, 2026. Example commands have not been executed for this guide.
