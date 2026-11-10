# Inspect an old Linux VM before planning its migration

Use this guide when you have an unfamiliar Linux disk image and need an initial inventory.

**Watch:** [Inspect old Linux VM images: 46-image test](https://www.youtube.com/watch?v=3FcGkMOA2S4).

## Prepare

Use a Linux host with the current Virtual Move client. Follow the [installation instructions](https://docs.vrtmv.com/guide/installation.html) for image-mount tooling and permissions. Work from an authorized copy or snapshot and record the source image and client version used.

## 1. Identify the image format

```bash
vrtmv --version
vrtmv assess centos7.vmdk
```

`assess` identifies the disk format from its leading bytes. It does not mount the image and needs no account or root access. Recognizing a format is an initial check; it does not establish that the complete workload can be migrated.

## 2. Read the operating system and package inventory

```bash
vrtmv inventory --image centos7.vmdk
```

Image inventory requires the mounting tools and access described in the installation guide. The source is attached read-only. Check the detected distribution, release, installed packages, and any extraction errors before proceeding.

Optional translation-name resolution uses the authenticated API:

```bash
vrtmv inventory --image centos7.vmdk --resolve
```

## 3. Record what still needs investigation

Build a short workload record: application owner, business function, data locations, dependencies, network requirements, and intended target. A package list alone is not an application acceptance test.

If format recognition succeeds but inventory fails, capture the error and check the source layout, required host tools, and documented source limitations. Preserve the original image while diagnosing the issue.

Next: [Run preflight for a CentOS 7 to Rocky Linux 9 plan](centos7-to-rocky9-preflight.md).

## References

- [assess command](https://docs.vrtmv.com/commands/assess.html)
- [inventory command](https://docs.vrtmv.com/commands/inventory.html)
- [Source types](https://docs.vrtmv.com/guide/sources.html)

Documentation check: November 9, 2026. These examples are a guide, not a recorded test of your image.
