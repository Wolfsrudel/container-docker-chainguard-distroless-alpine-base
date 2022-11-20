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
| `latest` | `sha256:bc01031422d4ba8b94fc8ac660c01c8170c27e55c67ec26460806192a017a949`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:bc01031422d4ba8b94fc8ac660c01c8170c27e55c67ec26460806192a017a949) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221119` | `sha256:b45e881509e4fe79101a62692735840ffad724b9f999cd1d587f386c446bb7e6`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:b45e881509e4fe79101a62692735840ffad724b9f999cd1d587f386c446bb7e6) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration` `migration-20221120` | `sha256:d0bf89ec9e1e7986e76115d112234e05170253276d22169ae802a18de9029401`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d0bf89ec9e1e7986e76115d112234e05170253276d22169ae802a18de9029401) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


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
        "docker-manifest-digest": "sha256:bc01031422d4ba8b94fc8ac660c01c8170c27e55c67ec26460806192a017a949"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "eb775835dd8a86949da00efa62d8b6aed1a910cb",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIAQboDIDqD9Q6X/W19IVXxZcuNJa27EnOg9tz47WEGhJAiEAyUELXMjFrl1C2U3Rzd+b+4UCKegqnvGZ5aCqnv+aBbI=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI0OTEwZTg4YWZkMmZkZWI4N2JmYmM5ZDFiMGZlNzE4MmY3YzY5ZGViZTY2NmI1NTAyYjhjNDA1NGE0Zjc2MGM0In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUUR6ZTZMMEdtYTNpaGs0MjgyY0svcEFTZ0ZpOTRtcndPYW5US0lwQmhBMWF3SWdSOVc2YXl4c0l6aGdCdndXTisrY3pNb01jME93alVqMFBHYktaeHZUZEU4PSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBha05EUVhwNVowRjNTVUpCWjBsVlZFNVpZa2cwYW1wb1dTOVphWE42T1VoMlJWWXpiMDQxVDFSQmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hkTlJFVjNUa1JSZUZkb1kwNU5ha2w0VFZSSmQwMUVSWGhPUkZGNFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZ1TVVoR1lXZEdaakZTUzBKNE9IWmtUbFpRYjFNelNERm5lV2h3UkUxamNHWXlSbThLTURKblowRjFRMWR2UTNSVlFuQlZjbUpXU1dreFMyWldjbVpOVFhCVlRGWnFjMnczWkUxbFVITkVjSFZNVmxZdk16WlBRMEZzYzNkblowcFlUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZ5VjFKR0NuRkhUMUoxUVhrdlduUnJWRU5IY1ZZMk5pOTRkemRKZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyaHNXV3BqTTA1VVozcE9WMUpyVDBkRk5FNXFhekJQVjFKb1RVUkNiRnB0UlRKTmJWRTBDbGxxV21oYVYxRjRXVlJyZUUxSFRtbE5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWwzV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUk1UWtoelFXVlJRak5CVGpBNUNrMUhja2Q0ZUVWNVdYaHJaVWhLYkc1T2QwdHBVMncyTkROcWVYUXZOR1ZMWTI5QmRrdGxOazlCUVVGQ2FFcExVVFpxUlVGQlFWRkVRVVZuZDFKblNXZ0tRVXg1YkZNdlNuZ3lNRk5qWlZGbFEzUnFRMFZDUVZFNGFpOXhjR3RETjNGelMydE1ObWwwZDB0MlFUZEJhVVZCTW1KSk1VMVlOMVY0WjA1UWNUQTRjQXBYYTNGQmIyTkJia0oyYVVSck9GQklXbEZNVlhGbWVIZ3dNelIzUTJkWlNVdHZXa2w2YWpCRlFYZE5SR0ZCUVhkYVVVbDNRMFpJZEhGR0wwZzRkelk1Q21sUllWQkNVWFpXV0dsUVZUZGxkbE5DUTNaQlRWUlJTaTlNYXpjd1VHWTJkMkY2VjBsa1JtSkNkRXR4TW1nNGNWZDBWRTlCYWtWQk4yeG1XRk12YUUwS2MxZG9aa2xPV0ZnNGRHVnpaRkYzUTI5RFMxTlpNMFUwUzJKbWJrVlNjMXBLU2pGcEwxbHhOV1l5ZUdOcmIwMWpVVXhaTVhKcldsVUtMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1668906300,
          "logIndex": 7448745,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "eb775835dd8a86949da00efa62d8b6aed1a910cb",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3505878172",
      "sha": "eb775835dd8a86949da00efa62d8b6aed1a910cb"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

