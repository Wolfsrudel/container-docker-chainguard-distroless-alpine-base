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
| `latest` | `sha256:05e7f3837c461c4db91fec1c8312151bec0e74c06e161be1ef3f9d5bdfadb830`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:05e7f3837c461c4db91fec1c8312151bec0e74c06e161be1ef3f9d5bdfadb830) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221119` | `sha256:b45e881509e4fe79101a62692735840ffad724b9f999cd1d587f386c446bb7e6`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:b45e881509e4fe79101a62692735840ffad724b9f999cd1d587f386c446bb7e6) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration` `migration-20221122` | `sha256:612917f345997a51f8e2534ebb7cb9f4149d29d5164d1f8e223c7de0abd44e7c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:612917f345997a51f8e2534ebb7cb9f4149d29d5164d1f8e223c7de0abd44e7c) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221120` | `sha256:d0bf89ec9e1e7986e76115d112234e05170253276d22169ae802a18de9029401`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d0bf89ec9e1e7986e76115d112234e05170253276d22169ae802a18de9029401) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221121` | `sha256:466083e3e0fbd5808ce39af0989d6cf06cc010433c5fe15f9210c96ab409afe6`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:466083e3e0fbd5808ce39af0989d6cf06cc010433c5fe15f9210c96ab409afe6) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


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
        "docker-manifest-digest": "sha256:05e7f3837c461c4db91fec1c8312151bec0e74c06e161be1ef3f9d5bdfadb830"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "1c59b430ecf16a131fd226c09ae96d27b878de3f",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEYCIQCBdveyRS8jAHaNO3+lJ4Y/V/m7X3Z1Gs7DyCLbdo1CnwIhAL5w3/s4Se+S96nvnTX0DgoDohSOy99U58MD3fqi8p0X",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI0Y2VmMDI3NTY0M2Q2NjIyZTFlNjA1YmFjYmQ2YTY2NTdlYTM0NGI2YmE0NGQwOWJhZGEyZDgzZjhiNThkYTA2In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FWUNJUURNNWx1WG5NMmU0a3NwdlVMV3J3VWpWZXJKTkwvZHBMYURrMUVQN3V6eklBSWhBTXhaSUkxWDQxYy94MEJlN3BLbkI4SlFOU1doMXlGcHB2NmpYbFFDZk9aNiIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBha05EUVhwNVowRjNTVUpCWjBsVlFqWnpLM0o1VWpFMWFESnVaM3BDYm01SFIwMXJTR0ZDV0hkTmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hsTlJFRjNUMVJKZVZkb1kwNU5ha2w0VFZSSmVVMUVRWGhQVkVsNVYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZKYzBkaFYyOVdXbk40TjA0elMwTmlhWGQwTkZWd1JrNVJlbEkxY1RSTGRUTlZlbVVLWmpCMGVFczRNR2hsYXpkNWRWSldOQ3RLUW1Sek1tRTBjM0pOVTFSTlFrdFFTamt6UVdFMVdFVkJUVzlCZGtZM1JHRlBRMEZzYzNkblowcFlUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZuTkVKbUNubE9VMnRFTTFkWFJWQlBhR1pLUm5sV1N6UjJkM2xqZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyZDRXWHBWTlZscVVYcE5SMVpxV21wRk1sbFVSWHBOVjFwclRXcEpNbGw2UVRWWlYxVTFDazV0VVhsT01razBUbnBvYTFwVVRtMU5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWwzV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUk1UWtoelFXVlJRak5CVGpBNUNrMUhja2Q0ZUVWNVdYaHJaVWhLYkc1T2QwdHBVMncyTkROcWVYUXZOR1ZMWTI5QmRrdGxOazlCUVVGQ2FFcDVjUzlRTkVGQlFWRkVRVVZuZDFKblNXZ0tRVTFNZEhkVlpGQXdUalI0U2l0dmNHdDZWMHRGWlhGVVF6RkhhMGxoUkVSYVlUWktUVXBhTWt0SU5qQkJhVVZCZVZwVFkybDJOaXRyZFM5aFoyVnNVd292VWtoWFprMVplVkZTWkhnMVRteHhWRFZuVG5wU1dVaE1kakIzUTJkWlNVdHZXa2w2YWpCRlFYZE5SR0ZCUVhkYVVVbDRRVWxxZDJoUGMwTnpNMjVyQ21kWFVVWTFjamhqSzBkaGVGaEpiak5sVlZGWE1sWnRORGxEYjJGT2VIaEdNa1pwU0dOMVkyTllOM0ZDVm5CaFFrcEtNRzQ1UVVsM1RVWjVOMkowYVRFS1JGQkpTV1Z0UVcxcGFrNVhlWGhDU1hOM05YTjRObXRqWkhvelZEVm9TRWxRYjNOd2JGcEVNR00zVnpFclFUUlZhemR1V2taTlJEY0tMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1669075783,
          "logIndex": 7575575,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "1c59b430ecf16a131fd226c09ae96d27b878de3f",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3519163991",
      "sha": "1c59b430ecf16a131fd226c09ae96d27b878de3f"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

