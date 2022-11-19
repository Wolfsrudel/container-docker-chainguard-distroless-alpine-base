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
| `latest` | `sha256:169c4f1b9f18ca64e96695ed35d85ae3599a69edc1dff2c6bb8c84ae03f737ff`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:169c4f1b9f18ca64e96695ed35d85ae3599a69edc1dff2c6bb8c84ae03f737ff) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration` `migration-20221119` | `sha256:50e3e8b3df6fa5cb3cd9b471f770ac189ff0933f163b3def27f5adcbea7041b4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:50e3e8b3df6fa5cb3cd9b471f770ac189ff0933f163b3def27f5adcbea7041b4) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


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
        "docker-manifest-digest": "sha256:169c4f1b9f18ca64e96695ed35d85ae3599a69edc1dff2c6bb8c84ae03f737ff"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "578fb0b43411c56c890ee6b94c14b6483e07e365",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQDvPlpQXHr9Xi8xkMmwyWqnzjNb+jcOsPlB/GX/1jlrIgIgOxwR7NfSu4MMgSx7l94fnS1NX1SlNakgE/gbHYt2zzs=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiIwMTA2NjRlMmIzOTJhZTdlMzhkMzkxNDQyZjFmMDhiODdlOTJlM2E1Y2YzMWUyYThiYzBmOWMzZTc3NDYzMTI2In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FWUNJUUQ5aENmYUVzV2FDM011WDRQSm5rSGpRNlcyTGN2WjdSc3Y2VENUc2FiL3ZRSWhBT2dia1FQbWpXemlPWFg2LzFoUmkvaDc5dzZSUEVHSEZZZUhFYjhqSlY4ciIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBha05EUVhwMVowRjNTVUpCWjBsVldETjVPV053YmtSVVVuUjRPVUUzUkVSaVpFVTRTRVJEWTAwNGQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVUlRWTlJFVjNUVlJKZUZkb1kwNU5ha2w0VFZSRk5VMUVSWGhOVkVsNFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVYyWTFScFprbGFXbFV3VVVNeE4zWmxhR2Q1ZUZSSFJWQnpXa0ZDTlZONlptczBlbmdLYkZoVWJGSlNlbFZrVEdGVFZucEdWREpSYW10dVdEVk9lbms1WVRWNFkwZDZRME5FVDJwUVprZEVPVEkxVFVKWGNVdFBRMEZzYjNkblowcFhUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlUxVGtSR0NrSnVZbVYxWlZSaWJWbzVhaloxVVdacFVHZEhiRlYzZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyY3hUbnBvYlZscVFtbE9SRTB3VFZSR2FrNVVXbXBQUkd0M1dsZFZNbGxxYXpCWmVrVXdDbGxxV1RCUFJFNXNUVVJrYkUxNldURk5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWxuV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUk0UWtodlFXVkJRakpCVGpBNUNrMUhja2Q0ZUVWNVdYaHJaVWhLYkc1T2QwdHBVMncyTkROcWVYUXZOR1ZMWTI5QmRrdGxOazlCUVVGQ2FFa3hibVkzZDBGQlFWRkVRVVZqZDFKUlNXY0tZelV6YnpkNFRGZHZNamR3ZGxaNU5ISTJOU3RVWTB0a2EybGFRMkUwV2tVemRtZFVXSE5TYW0wemMwTkpVVVIzU1hCUVJDOXFNRzVrVG5FeVowbzBPQXBVVmtOVVdsWTVOR3BOSzIxM05IZHNOVVZLYmpaSU5uUjFWRUZMUW1kbmNXaHJhazlRVVZGRVFYZE9jRUZFUW0xQmFrVkJNMnA0T1VJMmJVNU5hbUZhQ2pnMVZYa3JkMVZpTHk5RlVrdFlkek5EUTNwaU16Uk1kMnRQYjNsRVNqaDVUR2xxVTB4aU0wZzJlR1IxUkRnM05FRk9TbVpCYWtWQk5XSXJVWGREYVVvS1lVOVJWWFpoWml0VVZrNTFSRmt5WTJaRWFuaFFiakJJYzNFNGRYWjNaR3RKWVRGbmRpczVXVFZqTjFCeFYzYzNTVlJvU2tGblZEY0tMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1668819701,
          "logIndex": 7383253,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "578fb0b43411c56c890ee6b94c14b6483e07e365",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3501350876",
      "sha": "578fb0b43411c56c890ee6b94c14b6483e07e365"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

