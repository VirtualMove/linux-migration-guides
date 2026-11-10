# Linux Migration Guides by Virtual Move

Practical guides for inspecting legacy Linux workloads, finding migration blockers, and checking what changed after a rebuild.

Moving a workload starts with understanding what it depends on. These guides pair written steps with Virtual Move's engineering demonstrations so you can inspect the process and its limits.

## Start with your question

| Your question | Start here | Watch |
| --- | --- | --- |
| What is inside this old Linux VM? | [Inspect the source](guides/inspect-a-linux-vm.md) | [46-image engineering test](https://www.youtube.com/watch?v=3FcGkMOA2S4) |
| What needs attention before I rebuild it? | [Run and review preflight](guides/centos7-to-rocky9-preflight.md) | [Preflight walkthrough](https://www.youtube.com/watch?v=oVE4_qoBr1E&t=110s) |
| How do I check the rebuilt target? | [Read the verification evidence](guides/verify-a-linux-rebuild.md) | [Parity evidence explained](https://www.youtube.com/watch?v=0uwder9Jthg) |
| What should my team record? | [Migration acceptance checklist](checklists/migration-acceptance.md) | [Recent CentOS-to-Rocky demonstration](https://www.youtube.com/watch?v=LNM01hmRdZs) |

## See the workflow

The [CentOS 7 to Rocky Linux 9 demonstration](https://www.youtube.com/watch?v=LNM01hmRdZs) follows source inspection, a generated plan, operator-controlled application, and target verification.

That recording uses a Rocky Linux 9 **Podman container target**. It demonstrates a workload rebuild and checks within the report's scope. It does not show a target VM boot or production cutover. Its displayed report is unsigned and includes coverage limits and unverified categories.

For account setup and the wider process, watch the [full workflow walkthrough](https://www.youtube.com/watch?v=oVE4_qoBr1E). Find the complete [engineering video index](videos/README.md).

## Where Virtual Move fits

Virtual Move provides workload analysis, rebuild planning, and scoped parity verification. Your engineering team or chosen migration operator reviews and executes the migration and owns application acceptance and cutover decisions.

Read a verification result together with its coverage, caveats, missing items, and unverified categories. A signature protects the authenticity and integrity of signed evidence; it does not establish facts outside the checks performed.

## Try your own workload

[Start with 10 free migrations](https://try.vrtmv.co/?utm_source=github&utm_medium=referral&utm_campaign=linux_migration_guides&utm_content=readme). Start with one representative workload and inspect the findings before planning a fleet rollout.

Useful references: [Quickstart](https://docs.vrtmv.com/guide/quickstart.html) · [Supported paths](https://vrtmv.com/supported) · [Documentation](https://docs.vrtmv.com/) · [Contact the team](mailto:sales@vrtmv.co).

## Using these guides

The command examples use illustrative local paths. Replace them with your own paths and check your installed client's help. The linked product documentation is the authoritative command reference. Guides were checked against published documentation on November 9, 2026; the command examples have not been executed against your environment.

The guides and video links are available to read without a trial account. Using the commercial Virtual Move service is subject to its account requirements and terms.

[Suggest a correction](CONTRIBUTING.md).
