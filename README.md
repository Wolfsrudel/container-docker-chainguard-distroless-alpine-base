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
| `latest` | `sha256:0e6927b7ea112b6eab42a225ade42bf39e346abdd408386e51be7544be3cc76f`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:0e6927b7ea112b6eab42a225ade42bf39e346abdd408386e51be7544be3cc76f) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


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
        "docker-manifest-digest": "sha256:0e6927b7ea112b6eab42a225ade42bf39e346abdd408386e51be7544be3cc76f"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "a3e2bbf1493d0f445c96be5640787e0e0ee56882",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEYCIQCahZIFj+KeMXycPaIDgxIaYorNAebrLbnXa8zr7+JbgQIhANW13jtzrqmnlxmwjoGpYM3Fqd1u4pApH/SyviFOipxD",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI3NDNhMjViOTQ5OGEyNDE0Mjk5NjAyNDg4MGRjNGMzMDM4MWM4ZTkyZWNkNWU5MTgxYTkyNWQ1YzUxNWQ1NmJkIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJQ1dIRmw1SVBGd3dpeXRyQ0hPcFlrTEF2MlVCLzVqRk00VEZkZ3p2aGFrR0FpRUFucWs0SysxWjlCdDBPUUpkZWhTb056NjN4S3Z5TmZ6aVAvZ3hLZTFoelI0PSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBWRU5EUVhwMVowRjNTVUpCWjBsVlpYVTNUbGxvWjFCT2EySlVMekJpU0drMVMyWlFTMUJDYTJsSmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVUVhsTlJFVjRUWHBGTTFkb1kwNU5ha2w0VFZSQmVVMUVSWGxOZWtVelYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZEUmsxelZ6VjFUSFJNZUc1V2R6TTNVMU5LVEVkc2FtdDZXRlJrYjA5T2VuZE1XakVLWlhoeGQxYzVhRGhCVEd0b05VeHdXamhMTmxwalJWVnNZamxaU0RGdVZpODRXV2t6UzFSVGNYQmhWRWhaZFdsdE4wdFBRMEZzYjNkblowcFhUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlV2TUhKNkNrWjZWaXRUWTFJMllYRTJkbVY0ZWpKNVlqaG5aRGh6ZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyaG9UVEpWZVZsdFNtMU5WRkUxVFRKUmQxcHFVVEJPVjAwMVRtMUtiRTVVV1RCTlJHTTBDazR5VlhkYVZFSnNXbFJWTWs5RVozbE5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWxuV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUk0UWtodlFXVkJRakpCVGpBNUNrMUhja2Q0ZUVWNVdYaHJaVWhLYkc1T2QwdHBVMncyTkROcWVYUXZOR1ZMWTI5QmRrdGxOazlCUVVGQ2FFUlliVlZEUlVGQlFWRkVRVVZqZDFKUlNXY0tXRmhMZWpaWFFWQnJUM2N4TWpZMVUwdFlXbkYxYkZWV1VUaERiMFV6VlVKV1FWUTFhbWdyYUdSMU9FTkpVVU5XWW1KU2JFZHlTVkZ0UjFwUVYySTBUd281Y3pWbWFVeEpNbkIxYUd4VFFYWTFkV2RQY3pCemJURmxWRUZMUW1kbmNXaHJhazlRVVZGRVFYZE9iMEZFUW14QmFrVkJhV1pWV0Vsc2RuQmtjVE4wQ2pGTmJuSm5RVzQ1VWxWeFNFWXJjMFZqVWtjeVoxSmllWFZNTjFRMlpEUndaRmc1Wmt0T2R6SlViRU15UTBWUVdUaHFiVTFCYWtJNWVYcElTMHBxTlhZS1JuZFRWV0ZvV2xsRVdXbHFLMlpTUTI5ME1FTlphWGhxUzBjMGEyaEtiRmcyWmtkamFXeEplakl5VlUwclJtWnRZMWh1VUZGSGJ6MEtMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1667351637,
          "logIndex": 6324446,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "a3e2bbf1493d0f445c96be5640787e0e0ee56882",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3374103531",
      "sha": "a3e2bbf1493d0f445c96be5640787e0e0ee56882"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

