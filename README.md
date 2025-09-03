BioinfoUgrp DebianMed Images
============================

GitHub actions workflow to create Debian Med images for OISTs bioinformatics user group.

See also <https://github.com/oist/BioinfoUgrp/blob/master/DebianMedModules.md> and
[oist/BioinfoUgrp_UnixGoodies_Images](https://github.com/oist/BioinfoUgrp_UnixGoodies_Images).

## How to get the image:

```
ml singularity
singularity pull docker://ghcr.io/oist/bioinfougrp_debianmed_images:latest
```

## For admins, how to tag the image

Make sure you have a [token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) with at least read permissions for packages.

Example with `13.0-1`.

```
podman login ghcr.io
podman pull  ghcr.io/oist/bioinfougrp_debianmed_images:latest
podman tag   ghcr.io/oist/bioinfougrp_debianmed_images:latest ghcr.io/oist/bioinfougrp_debianmed_images:13.0-1
podman push  ghcr.io/oist/bioinfougrp_debianmed_images:13.0-1
```
