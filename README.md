# alpine-base

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/alpine-base/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/alpine-base/actions/workflows/release.yaml)

Alpine base image built with [apko](https://github.com/chainguard-dev/apko). Uses packages from the [Alpine distribution](https://www.alpinelinux.org/).

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/alpine-base:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `latest` | `sha256:c4b45060649d5b23d2c6578a0b63cb215c830472e310f565cde1f73ef3cb61b7`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:c4b45060649d5b23d2c6578a0b63cb215c830472e310f565cde1f73ef3cb61b7) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


## Usage

```
docker run cgr.dev/chainguard/alpine-base echo "hello"
```

See the [examples/](./examples/) directory for how
to use this as a base image.


## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/alpine-base:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/alpine-base:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/alpine-base"
      },
      "image": {
        "docker-manifest-digest": "sha256:c4b45060649d5b23d2c6578a0b63cb215c830472e310f565cde1f73ef3cb61b7"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "03778148bb0a1ef2e21e4bd21a661c854d464de4",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCICCw2KiHWKKcZhZflpyJtec0RkFfgkQ6xBasuLZHYnczAiBLn5DipYhLa3ayocMIQtmGIwBwz0rzSmE4n6BrgUcAAg==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI0NDA2ZDgyN2Y2NGY4MjcyNGIxZDI2ODVlMTZmMzU3ZDljMDgzMTU2ZjIwMzUyN2U5MzFjZmE1NGRlNDY1YWU5In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUURoQ244VFNkRXZNaTZ4NDdvT04vTVJISnA0NWkxMHJKOW51V3paUGtJbmx3SWdTeTZSc296eDVZczlMM3AycDNzenFIN053WkFhNVJpWTVBMVJvY0NXRG9zPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBSRU5EUVhweFowRjNTVUpCWjBsVlZtZHFUa1ZTVmxoeGNIRjZWMnRKUjFWeFUzUjZVMjVUVm1kWmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVUlRSTlJFVjNUa1JKZVZkb1kwNU5ha2w0VFZSRk5FMUVSWGhPUkVsNVYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZGSzBoeFdYUkNhRk5DUW1GalIwZDVaMGN4Y2k4d1RsTTVkVVJ0WjNkR1pXZFVPV2dLZDFaNFowNHhkbTl3ZERKcGFVMUtNVVJXTlVFcmVFSXlLek5EVVhOb1YxUjJLMmhsYURWck1YaDJkSHBKUWk5b2FtRlBRMEZzYTNkblowcFdUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZXWm5sR0NuSlRRbEJ2YVdodk9VSTJVRTV2Y1RkcmREaHBOVGd3ZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyZDNUWHBqTTA5RVJUQlBSMHBwVFVkRmVGcFhXWGxhVkVsNFdsUlNhVnBFU1hoWlZGa3lDazFYVFRST1ZGSnJUa1JaTUZwSFZUQk5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWxSV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUkzUWtoclFXUjNRakZCVGpBNUNrMUhja2Q0ZUVWNVdYaHJaVWhLYkc1T2QwdHBVMncyTkROcWVYUXZOR1ZMWTI5QmRrdGxOazlCUVVGQ2FFbG9SRFpOYjBGQlFWRkVRVVZaZDFKQlNXY0tVMGxXY1VjMVdHWlVMMVZrUlV4WlNFVkVhV1J4UkV0cFZ6aDFNRFYyU0hoelVWaG5OVVV4TTBoMmIwTkpSWGxXWVVoSVYzcDNWVUpaZGpsSmVqSnBaUXBaTmxKVlEweE9iVEZrWVZkVVdtdG1aRFpaVkZKMFlXOU5RVzlIUTBOeFIxTk5ORGxDUVUxRVFUSm5RVTFIVlVOTlEySlphV0pyWm1aSmRHcDVPVEoxQ25KTEwzQTBWWEJVTTJaUVRUSXpWbGRSUTFsNGRXUkJRV3dyVDBsVFZGZGpVamhaVUZOQmFsWkpWM1EzUWpkYVVsTm5TWGhCUzFSWksxSlVXVkJ5Y0ZJS04zQTVhWGQwTldGeVMyTndXVFpoTmpGSVJraFlTakZWVm5GYWQwNXdabGxFVG5OWU5qTnJkbHBtWm1WdE1HZDNOV3RTYld0M1BUMEtMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1668733483,
          "logIndex": 7310377,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "03778148bb0a1ef2e21e4bd21a661c854d464de4",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3493304069",
      "sha": "03778148bb0a1ef2e21e4bd21a661c854d464de4"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

