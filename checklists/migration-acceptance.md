# Linux migration acceptance checklist

Use this working checklist with your own change process. A checked box should point to evidence and an owner.

## Before the rebuild

- [ ] Record the workload owner and business function.
- [ ] Record the exact source and target releases and platform requirements.
- [ ] Confirm backup/restore and the rollback decision point.
- [ ] Inventory application components, dependencies, data, and network requirements.
- [ ] Review preflight findings and assign unresolved work.
- [ ] Agree application acceptance tests before making changes.

## During the rebuild

- [ ] Preserve the reviewed plan and migration attestation.
- [ ] Record the client version and relevant execution details.
- [ ] Record manual changes, warnings, and failed steps.
- [ ] Confirm data migration steps through the application's approved procedure.

## Before cutover approval

- [ ] Verify the intended target against the matching attestation.
- [ ] Read missing items, coverage limits, caveats, and unverified categories.
- [ ] Check signature status when signed evidence is required.
- [ ] Test application behavior, connectivity, access, and scheduled work.
- [ ] Complete application-specific data and performance checks.
- [ ] Obtain the workload owner's acceptance and record the decision.
- [ ] Confirm rollback readiness and the cutover owner.

## After cutover

- [ ] Retain the migration evidence and change record.
- [ ] Confirm monitoring, backup, and operational ownership.
- [ ] Review issues observed after the move and document their resolution.

[Verification guide](../guides/verify-a-linux-rebuild.md) · [Start with one workload](https://try.vrtmv.co/?utm_source=github&utm_medium=referral&utm_campaign=linux_migration_guides&utm_content=checklist)
