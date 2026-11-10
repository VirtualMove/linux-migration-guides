# CentOS 7 to Rocky Linux 9: inspect the plan before applying it

Use preflight to identify items requiring an engineering decision before a rebuild.

**Watch:** [Preflight in the full walkthrough, starting at 1:50](https://www.youtube.com/watch?v=oVE4_qoBr1E&t=110s).

## Before you start

Install the client, configure your account through the [authentication guide](https://docs.vrtmv.com/guide/authentication.html), and confirm your exact source and target releases against [supported paths](https://vrtmv.com/supported). A listed source and a listed target do not imply that every combination is supported.

Use your own authorized source image. The path below is illustrative.

## 1. Request a feasibility assessment

```bash
vrtmv migrate --image centos7.vmdk --target rocky9 --preflight
```

The documented preflight reports mapping counts and blocking manual steps. It writes no migration output files and consumes no usage credit.

## 2. Review the decisions

| Finding | Engineering follow-up |
| --- | --- |
| Unresolved or untranslated packages | Identify the application dependency and agree a replacement or manual step. |
| Configuration caveats | Check the relevant setting and target behavior. |
| Blocking manual steps | Assign an owner and define evidence that the step is complete. |
| Unsupported or unknown conditions | Investigate the condition before treating it as satisfied. |

Keep the findings with your workload record. Treat unresolved items as work to investigate; do not silently omit them from acceptance criteria.

## 3. Generate the plan when ready

```bash
vrtmv migrate --image centos7.vmdk --target rocky9 -o out/
```

The default output includes an Ansible role and a migration attestation. This is a full run, subject to your plan's usage terms. Inspect the generated files before using them on a target. Signing availability must be checked in the actual output; generating a report does not by itself mean it was signed.

Your operator reviews and applies the approved plan, handles manual migration work, and decides when the application is ready for acceptance testing.

## Related demonstration

The [recent rebuild demonstration](https://www.youtube.com/watch?v=LNM01hmRdZs) uses a Podman target. It is useful for following the plan and verification, but does not demonstrate a bootable target VM or production cutover.

Next: [Verify the rebuilt target](verify-a-linux-rebuild.md).

## References

- [Current quickstart](https://docs.vrtmv.com/guide/quickstart.html)
- [migrate command and output](https://docs.vrtmv.com/commands/migrate.html)

Documentation check: November 9, 2026. Commands have not been executed as part of preparing this guide.
